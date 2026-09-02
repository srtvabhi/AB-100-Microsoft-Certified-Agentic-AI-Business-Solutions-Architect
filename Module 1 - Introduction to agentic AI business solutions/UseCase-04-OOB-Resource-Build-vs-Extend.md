# Use Case 4 --- Decide Whether to Reuse, Extend, or Build

## Unit mapping

**Unit:** Identify Out-of-the-Box (OOB) Microsoft AI Agent Resources

## Source concept alignment

The unit describes OOB resources such as prebuilt agents, templates,
tools, and scenario libraries and positions them as accelerators that
can reduce development time and support enterprise adoption.

## Scenario

Contoso wants an Employee Service Agent. The delivery team proposes
building a custom solution from scratch. The architect must determine
whether OOB resources can accelerate the project.

## Learner task 1 --- Classify the need

For each requirement, decide:

-   Reuse as-is.
-   Configure.
-   Extend.
-   Build custom.
-   Defer.

Example requirements:

1.  Answer employee policy questions.
2.  Use Contoso-specific HR documents.
3.  Submit an IT equipment request.
4.  Apply a custom manager approval rule.
5.  Produce a unique predictive model.
6.  Escalate to a human.

## Learner task 2 --- Evaluate OOB resources

Use these evaluation criteria:

  Criterion        Question
  ---------------- -----------------------------------------------------
  Functional fit   Does the resource cover most of the process?
  Time to value    Does it reduce build effort?
  Customization    Can Contoso-specific behavior be added?
  Integration      Can it connect to required systems?
  Governance       Can controls and approvals be enforced?
  Security         Can enterprise identity/access requirements be met?
  Operations       Can it be monitored and supported?
  Scalability      Can it grow with adoption?

## Learner task 3 --- Make the decision

Recommended training decision:

> **Extend/configure an OOB agent pattern rather than build the complete
> employee experience from scratch.**

Reasoning:

-   The use case is a common enterprise knowledge/workflow scenario.
-   The module explicitly emphasizes prebuilt agents/templates and
    Copilot Studio.
-   Custom logic should be reserved for Contoso-specific integrations,
    policies, and controls.

## Learner task 4 --- Identify customization boundaries

### Configure

-   Agent name and role.
-   Instructions.
-   Knowledge.
-   Topics/behavior.
-   Channels where supported.

### Extend

-   IT service request action.
-   Approval workflow.
-   Enterprise API.
-   Custom business rules.

### Keep deterministic

-   Authorization.
-   Approval.
-   Transaction validation.
-   System-of-record updates.

## Deliverable

A **Build vs Reuse vs Extend Decision Record**.

## Debate

Team A argues for full custom development.\
Team B argues for OOB-only with no extensions.

Learners must propose a balanced architecture.

## Debrief

OOB resources are accelerators, not a substitute for architecture.
Enterprise-specific data, integration, governance, and operational
decisions still need deliberate design.
