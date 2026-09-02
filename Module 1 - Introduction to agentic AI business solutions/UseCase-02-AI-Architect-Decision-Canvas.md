# Use Case 2 --- AI Architect Decision Canvas

## Unit mapping

**Unit:** Role of the Architect in AI Transformation for Businesses

## Source concept alignment

The unit describes the architect as bridging business strategy and
technical implementation, aligning AI with organizational objectives,
designing integration architecture, establishing responsible
AI/governance, and designing scalable solutions. It also lists
responsibilities including vision/roadmap, data architecture,
integration, security/ethics, and performance monitoring.

## Scenario

Contoso has approved exploration of the Employee Service Agent. The
architecture team must turn the business idea into a governed solution
concept.

## Learner task

Complete five architecture decision areas.

## 1. Vision and roadmap

Questions:

-   What business outcome is prioritized?
-   What is the smallest useful release?
-   What should be deferred?
-   What would trigger expansion?

Suggested release sequence:

**Release 1:** policy Q&A\
**Release 2:** guided employee processes\
**Release 3:** controlled actions\
**Release 4:** broader HR/IT integration

## 2. Data architecture

Identify:

-   authoritative policy sources,
-   content owners,
-   update frequency,
-   sensitive content,
-   access boundaries,
-   retention requirements.

Decision example:

> Only approved HR policy and onboarding sources will be used in
> Release 1. Source ownership remains with HR.

## 3. Integration

Map potential integrations:

``` text
Employee
   |
Agent
   |
   +--> HR knowledge
   +--> IT service workflow
   +--> Approval process
   +--> Employee directory/identity
```

For each integration, classify:

-   read only,
-   write/action,
-   approval required,
-   privileged.

## 4. Security and ethics

Consider:

-   identity,
-   least privilege,
-   privacy,
-   sensitive employee data,
-   auditability,
-   transparency,
-   escalation,
-   misuse.

Create at least three non-negotiable controls.

Example:

1.  Agent cannot bypass workflow authorization.
2.  Sensitive employee data is not exposed across users.
3.  Unsupported policy is escalated rather than invented.

## 5. Performance monitoring

Define:

-   business KPI,
-   quality KPI,
-   operational KPI,
-   risk KPI.

Example:

  Category     KPI
  ------------ ------------------------------
  Business     HR ticket deflection
  Quality      Grounded-answer accuracy
  Operations   Action success rate
  Risk         Unauthorized-action attempts

## Deliverable

A one-page **AI Architect Decision Canvas**.

## Challenge question

Leadership asks:

> Can we launch the agent to every employee next week?

Learners must explain what evidence they need before approving
enterprise scale.

## Expected answer themes

-   tested knowledge quality,
-   security validation,
-   responsible AI evaluation,
-   identity/access design,
-   operational support,
-   monitoring,
-   change management,
-   measurable pilot outcomes.

## Debrief

Architecture is the set of business, data, integration, security,
governance, and operational decisions that make an AI solution
trustworthy and scalable.
