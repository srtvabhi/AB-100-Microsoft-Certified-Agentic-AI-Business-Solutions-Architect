# Use Case 5 --- Customize an OOB Employee Service Agent

## Unit mapping

**Unit:** Identify Out-of-the-Box (OOB) Microsoft AI Agents

## Source concept alignment

The unit focuses on OOB agents, pre-built agents/templates, real-world
business scenarios, Copilot Studio, templates, scenario libraries,
faster deployment, scalability, and responsible AI.

## Scenario

Contoso has chosen an OOB/configuration-first approach. The team must
tailor the agent to the Employee Service scenario.

## Relationship to hands-on demo

This use case leads directly into **Demo 1 --- Build a Grounded Employee
Policy Agent**.

## Learner task 1 --- Define the agent contract

### Agent role

Employee self-service assistant for approved HR and onboarding
information.

### Agent users

Contoso employees.

### Agent may

-   answer approved policy questions,
-   summarize onboarding steps,
-   ask clarifying questions,
-   route unsupported cases to HR.

### Agent may not

-   invent policy,
-   expose another employee's data,
-   bypass authorization,
-   make financial commitments,
-   provide unrelated professional advice.

## Learner task 2 --- Design knowledge

Create a knowledge inventory:

  Source                      Owner       Sensitivity   Update cadence      Authoritative?
  --------------------------- ----------- ------------- ------------------- ----------------
  Leave policy                HR          Internal      As policy changes   Yes
  Benefits FAQ                HR          Internal      Periodic            Yes
  Onboarding checklist        HR/IT       Internal      Periodic            Yes
  Employee discussion forum   Employees   Variable      Continuous          No

Discuss why not every available source should automatically become
grounding knowledge.

## Learner task 3 --- Design conversation behavior

### Supported request

> What is the parental leave policy?

### Ambiguous request

> Can I carry leave?

### Missing knowledge

> What will the policy be in 2027?

### Out of scope

> Which stock should I buy with my bonus?

### Escalation

> My manager says the policy does not apply to me. What should I do?

For each, define the desired agent behavior before testing.

## Learner task 4 --- Responsible AI review

Evaluate:

-   fairness,
-   reliability/safety,
-   privacy/security,
-   inclusiveness,
-   transparency,
-   accountability.

## Learner task 5 --- Test plan

Create at least:

-   3 happy-path tests,
-   2 ambiguous tests,
-   2 missing-knowledge tests,
-   2 out-of-scope tests,
-   2 adversarial/control-bypass tests.

## Deliverable

An **Agent Definition + Knowledge + Test Plan**.

## Completion activity

Run `Demo-01-Employee-Policy-Agent.md`.

## Debrief

A prebuilt agent becomes an enterprise solution only after it is aligned
to business scope, authoritative knowledge, controls, test criteria, and
operating ownership.
