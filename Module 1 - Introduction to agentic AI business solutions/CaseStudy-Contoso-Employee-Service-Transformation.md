# Case Study --- Contoso Employee Service Transformation

## Scope

**Entire AB-100 Module 1: Introduction to Agentic AI Business Solution
Architecture**

## Purpose

This case study provides one continuous scenario that can be revealed
progressively across the units. It is designed to make each unit feel
like another architecture decision in the same transformation rather
than an unrelated example.

> **Synthetic training scenario:** All Contoso operational details below
> are created for the lab and are not assertions from the AB-100 source
> deck.

## Company situation

Contoso has a large employee population. HR and IT service teams receive
frequent repetitive requests about:

-   leave,
-   benefits,
-   onboarding,
-   travel,
-   employee policy,
-   laptop/equipment support.

Employees often search across multiple sources before finding an answer.
Service teams spend significant time answering routine questions.

Leadership wants to evaluate **agentic AI**.

## Executive request

> Design an Employee Service Agent that improves self-service, uses
> approved enterprise knowledge, integrates safely with business
> workflows, and can scale while maintaining responsible AI, security,
> compliance, and human oversight.

# Stage 1 --- Introduction

## Business question

Should Contoso use AI here at all?

## Learner output

**Agent Opportunity Canvas**

### Business outcome

Improve employee self-service while reducing repetitive support work.

### Candidate KPIs

-   containment,
-   time to answer,
-   escalation,
-   satisfaction,
-   grounded-answer quality.

### Initial scope

Knowledge-based employee service.

### Initial risk

Incorrect or unsupported policy guidance.

# Stage 2 --- Role of the Architect

## Business question

What architecture decisions must exist before implementation?

## Learner output

**AI Architect Decision Canvas**

Cover:

-   vision/roadmap,
-   data,
-   integration,
-   security/ethics,
-   performance monitoring.

## Architecture principle

Start small, establish governance, and expand only after measurable
evidence.

# Stage 3 --- Microsoft AI Technologies

## Business question

Which Microsoft capabilities satisfy the requirements?

## Learner output

**Requirement-to-Technology Matrix**

Avoid using technology without a requirement.

Logical view:

``` text
Employee
   |
   v
Agent experience
   |
   +--> Approved knowledge
   |
   +--> AI reasoning
   |
   +--> Controlled actions
             |
             v
       Enterprise workflow
```

# Stage 4 --- OOB Agent Resources

## Business question

Should Contoso build everything from scratch?

## Learner output

**Build / Reuse / Extend Decision**

Recommended training decision:

-   reuse/configure OOB agent capabilities,
-   extend with Contoso-specific knowledge and workflows,
-   custom-build only where justified.

# Stage 5 --- OOB Microsoft AI Agents

## Business question

Can we create a useful first release?

## Practical

Run **Demo 1 --- Employee Policy Agent**.

## Release 1 behavior

The agent can:

-   answer approved policy questions,
-   summarize onboarding guidance,
-   ask clarification,
-   decline unsupported/out-of-scope requests,
-   escalate to HR.

## Evaluation

Use supported, ambiguous, missing-knowledge, out-of-scope, and
adversarial prompts.

# Stage 6 --- Agentic evolution

## New leadership request

> Employees like the policy agent. Can it complete routine requests too?

## Architecture response

Yes, but actions must be deliberately classified and governed.

## Practical

Run **Demo 2 --- Agentic IT Equipment Workflow**.

## Example request

> My laptop has crashed four times today and I have a customer
> presentation tomorrow. Can you get me a replacement?

## Desired agent behavior

1.  Understand the goal.
2.  Retrieve relevant equipment policy.
3.  Collect missing information.
4.  Determine the approved process.
5.  Explain the intended action.
6.  Obtain confirmation.
7.  Invoke a controlled workflow.
8.  Return request status.
9.  Escalate exceptions.

# Final target architecture

``` text
+----------------------+
|      Employees       |
+----------+-----------+
           |
           v
+----------------------+
| Employee Service     |
| Agent                |
+----+-----------+-----+
     |           |
     |           +-------------------+
     v                               v
+------------+                 +------------+
| Approved   |                 | Guardrails |
| Knowledge  |                 | & Policy   |
+------------+                 +------------+
     \                               /
      \                             /
       +------------+--------------+
                    |
                    v
             +-------------+
             | Reasoning / |
             | Orchestration|
             +------+------+
                    |
                    v
             +-------------+
             | Controlled  |
             | Actions     |
             +------+------+
                    |
          +---------+----------+
          |                    |
          v                    v
+----------------+     +----------------+
| IT/HR Workflow |     | Human Approval |
+-------+--------+     +-------+--------+
        |                      |
        +----------+-----------+
                   |
                   v
          +------------------+
          | Audit / KPIs /   |
          | Monitoring       |
          +------------------+
```

# Architecture review checklist

## Business alignment

-   Is the outcome measurable?
-   Is the agent solving a real process problem?

## Data

-   Are knowledge sources authoritative?
-   Is ownership defined?
-   Is sensitive data controlled?

## Integration

-   Are read and write actions clearly separated?
-   Are system-of-record updates deterministic?

## Security

-   Is identity enforced?
-   Is least privilege applied?
-   Can prompts bypass authorization? They must not.

## Responsible AI

-   Fairness.
-   Reliability and safety.
-   Privacy and security.
-   Inclusiveness.
-   Transparency.
-   Accountability.

## Operations

-   Who owns the agent?
-   Who handles escalations?
-   What happens when an action fails?
-   How are changes tested?

## Monitoring

-   Business KPIs.
-   Quality KPIs.
-   Operational KPIs.
-   Risk KPIs.

# Final learner challenge

Present a five-minute architecture recommendation to a fictional
steering committee.

The presentation must answer:

1.  What business problem are we solving?
2.  Why use an agent?
3.  What is the Release 1 scope?
4.  Which Microsoft capability categories are used?
5.  What is reused versus extended?
6.  What can the agent do?
7.  What can it not do?
8.  Where is human approval required?
9.  How will success be measured?
10. What must be true before enterprise rollout?

# Suggested assessment rubric

  Area                            Weight
  ----------------------------- --------
  Business alignment                 15%
  Architecture quality               20%
  Technology fit                     15%
  Data/knowledge design              10%
  Security and Responsible AI        20%
  Agentic action controls            10%
  Monitoring and scale               10%

## Expected capstone message

A successful Agentic AI Business Solution Architect does not simply
select an AI tool. The architect connects measurable business outcomes
to data, AI capabilities, integration, responsible AI, security,
scalable design, controlled actions, and continuous monitoring.
