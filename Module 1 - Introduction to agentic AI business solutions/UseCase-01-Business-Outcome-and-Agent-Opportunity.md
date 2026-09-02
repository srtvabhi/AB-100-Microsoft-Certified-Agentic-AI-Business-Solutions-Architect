# Use Case 1 --- Identify the Business Outcome and Agent Opportunity

## Unit mapping

**Unit:** Introduction

## Source concept alignment

The module introduction frames AI transformation as a strategic shift
affecting business processes, people, and culture. It emphasizes
measurable business outcomes, responsible AI, modular design,
collaboration, and monitoring/optimization.

## Scenario

Contoso HR receives repetitive employee questions across leave,
benefits, onboarding, travel, and policy. Leadership asks whether an AI
agent could improve employee self-service.

## Learner role

You are the Agentic AI Business Solution Architect.

## Business challenge

Do **not** start by choosing a tool. First determine whether the problem
is worth solving and what successful transformation would mean.

## Learner task 1 --- Write the outcome statement

Complete:

> We will use an Employee Service Agent to \_\_\_\_\_\_\_\_\_\_ for
> \_\_\_\_\_\_\_\_\_\_ so that \_\_\_\_\_\_\_\_\_\_, measured by
> \_\_\_\_\_\_\_\_\_\_.

Example:

> We will use an Employee Service Agent to improve access to approved
> employee information for Contoso employees so that routine support
> demand and time-to-answer decrease, measured by containment rate,
> resolution time, and satisfaction.

## Learner task 2 --- Identify stakeholders

  Stakeholder           Need                           Concern
  --------------------- ------------------------------ ----------------------------
  Employees             Fast, accurate answers         Privacy and clarity
  HR                    Lower repetitive workload      Incorrect policy responses
  IT                    Secure, supportable solution   Integration and operations
  Security              Controlled access              Data leakage
  Legal/Compliance      Policy-aligned behavior        Accountability
  Business leadership   Measurable value               Adoption and ROI

## Learner task 3 --- Define KPIs

Choose 3--5:

-   Self-service containment rate.
-   Average time to useful answer.
-   HR ticket reduction.
-   Escalation rate.
-   Employee satisfaction.
-   Grounded-answer quality.
-   Incorrect-policy response rate.

## Learner task 4 --- Define scope

### In scope

-   Approved HR policy questions.
-   Onboarding guidance.
-   Benefits FAQ.
-   Routing to HR.

### Out of scope

-   Personal legal advice.
-   Medical diagnosis.
-   Investment advice.
-   Unapproved policy interpretation.
-   Autonomous changes to employee records in the first release.

## Learner task 5 --- Agent suitability test

Rate each from 1--5:

-   Is the process language-heavy?
-   Is information distributed across approved sources?
-   Is the task repetitive?
-   Is there a measurable business outcome?
-   Can risky actions be bounded?
-   Is human escalation available?

## Architecture decision

**Proceed as a bounded employee self-service agent**, beginning with
knowledge-grounded use cases before transactional automation.

## Deliverable

One-page **Agent Opportunity Canvas** containing:

1.  Business problem.
2.  Users.
3.  Desired outcome.
4.  KPIs.
5.  In/out scope.
6.  Key risks.
7.  Candidate agent capability.

## Debrief

The architect's first output is not a bot. It is a clear link between
business outcomes, process change, technology, governance, and
measurement.
