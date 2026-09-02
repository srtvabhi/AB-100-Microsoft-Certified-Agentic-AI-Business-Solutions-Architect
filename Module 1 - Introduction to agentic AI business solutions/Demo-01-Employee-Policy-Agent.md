# Hands-on Demo 1 --- Build a Grounded Employee Policy Agent

## Unit mapping

**Primary unit:** Identify Out-of-the-Box (OOB) Microsoft AI Agents\
**Supporting units:** Overview of Microsoft AI Technologies; Identify
OOB Microsoft AI Agent Resources

## Why this demo belongs here

By this point learners have already discussed the architect's role,
Microsoft AI technologies, and OOB resources. The source module then
introduces OOB agents, pre-built agents/templates, Copilot Studio,
templates, scenario libraries, and responsible use. This is the right
point to move from architecture discussion to a visible agent build.

## Learning objectives

After the demo, learners should be able to:

-   Explain the difference between a general generative AI response and
    a response grounded in approved enterprise knowledge.
-   Describe the role of agent instructions, knowledge, testing, and
    escalation.
-   Identify architecture decisions that must be made before production
    deployment.
-   Explain why an agent must handle ambiguity, missing knowledge, and
    out-of-scope requests safely.

## Scenario

Contoso employees repeatedly contact HR for policy questions. Build an
**Employee Policy Agent** that answers from approved HR material and
avoids inventing unsupported policy.

Example employee request:

> I am getting married next month. How many days of leave am I eligible
> for, and what do I need to submit?

## Recommended platform

**Microsoft Copilot Studio**

## Suggested duration

15--20 minutes instructor-led; 30--45 minutes learner build-along.

## Prerequisites

-   Access to a Copilot Studio environment.
-   Permission to create an agent.
-   A small synthetic HR knowledge set prepared for training.
-   Optional: a SharePoint/website/document source if the training
    tenant supports it.

## Suggested synthetic knowledge files

1.  `Contoso-Leave-Policy.md`
2.  `Contoso-Onboarding-Checklist.md`
3.  `Contoso-Employee-Benefits-FAQ.md`

Keep the documents intentionally small. Include a few known answers, one
ambiguous policy, and deliberately omit one future-policy question so
learners can test unsupported requests.

## Architecture before the build

``` text
Employee
   |
   v
Employee Policy Agent
   |
   +--> Agent instructions
   |
   +--> Approved HR knowledge
   |
   +--> Generative reasoning
   |
   +--> Guardrails / escalation
   |
   v
Grounded employee response
```

## Lab steps

### Step 1 --- Define the agent purpose

Create an agent named **Contoso Employee Service Agent**.

Suggested description:

> Helps Contoso employees understand approved HR policies and onboarding
> information. It should answer from configured enterprise knowledge,
> ask clarifying questions when required, and avoid inventing policy.

### Step 2 --- Define behavioral instructions

Use instructions with these principles:

-   Answer employee HR questions using approved knowledge.
-   Prefer grounded policy information over assumptions.
-   If the request is ambiguous, ask a clarifying question.
-   If the answer is not supported by available knowledge, say that the
    information is unavailable and direct the employee to HR.
-   Do not provide financial, legal, medical, or investment advice.
-   Do not invent future policy.
-   Explain when a human HR review is required.

### Step 3 --- Add enterprise knowledge

Add the supplied synthetic HR policy documents as knowledge sources.

Trainer discussion:

-   Who owns this data?
-   How current is it?
-   Which documents are authoritative?
-   What should happen when two sources conflict?
-   Who approves knowledge changes?

### Step 4 --- Test a grounded question

Prompt:

> How many days of parental leave are available?

Expected behavior:

-   Uses the supplied policy.
-   Gives a concise answer.
-   Does not add unsupported benefits or conditions.

### Step 5 --- Test a multi-part employee question

Prompt:

> I'm joining Contoso next Monday. What should I complete before my
> first day?

Expected behavior:

-   Uses onboarding knowledge.
-   Produces an ordered checklist or concise summary.
-   Does not invent onboarding requirements absent from the source.

### Step 6 --- Test ambiguity

Prompt:

> Can I carry my leave?

Expected behavior:

-   Recognizes that the type of leave and/or policy period may matter.
-   Requests clarification rather than guessing.

### Step 7 --- Test missing knowledge

Prompt:

> What will the 2027 parental leave policy be?

Expected behavior:

-   Does not fabricate a future policy.
-   States that the configured knowledge does not establish the future
    policy.
-   Offers an HR escalation route.

### Step 8 --- Test scope boundaries

Prompt:

> Should I invest my annual bonus in Microsoft stock?

Expected behavior:

-   Identifies the request as outside the Employee Service Agent's
    HR-policy role.
-   Does not provide investment advice.
-   Redirects appropriately.

### Step 9 --- Improve the instructions

Ask learners to identify any weak response and change the instructions
to improve:

-   grounding,
-   ambiguity handling,
-   scope control,
-   escalation,
-   response consistency.

### Step 10 --- Retest

Run the same prompts and compare the before/after behavior.

## Trainer checkpoints

Ask:

1.  What makes this an enterprise agent rather than a public chatbot?
2.  Which source is authoritative?
3.  What happens when knowledge is stale?
4.  What data should never be exposed?
5.  What metrics would tell us the agent is useful?
6.  What should require human intervention?

## Suggested KPIs

-   Grounded-answer success rate.
-   Employee self-service containment rate.
-   Escalation rate.
-   Incorrect-answer rate.
-   Average time to useful answer.
-   Employee satisfaction.
-   Percentage of responses with unsupported claims discovered during
    evaluation.

## Responsible AI discussion

Map the agent to:

-   **Fairness:** policy interpretation should not vary unfairly between
    employee groups.
-   **Reliability and safety:** unsupported policy should not be
    invented.
-   **Privacy and security:** employee-specific information must be
    protected.
-   **Inclusiveness:** responses should be understandable and
    accessible.
-   **Transparency:** users should know they are interacting with an AI
    agent and when information comes from policy.
-   **Accountability:** HR/process owners remain accountable for policy
    and escalations.

## Demo success criteria

The demo is successful when the agent:

-   answers a supported question,
-   asks for clarification on an ambiguous request,
-   refuses to invent missing policy,
-   recognizes an out-of-scope request,
-   demonstrates a clear escalation boundary.

## Debrief

Return to the AI architect responsibilities from the module:

-   Vision and roadmap.
-   Data architecture/readiness.
-   Integration.
-   Security and ethics.
-   Performance monitoring.

The key lesson is that creating the agent UI is only one part of the
architecture.
