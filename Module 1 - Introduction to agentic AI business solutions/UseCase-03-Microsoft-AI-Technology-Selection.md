# Use Case 3 --- Select Microsoft AI Technologies for the Employee Service Solution

## Unit mapping

**Unit:** Overview of Microsoft AI Technologies

## Source concept alignment

The unit introduces Azure AI services, tools/SDKs, Copilot solutions,
development environments, APIs, and the business value of generative AI.
It encourages measurable outcomes, responsible implementation, and cloud
scalability.

## Scenario

Contoso knows what the Employee Service solution must accomplish. The
architecture team now needs to map requirements to Microsoft AI
capabilities without selecting technology merely because it is
available.

## Learner task 1 --- Requirement-to-capability mapping

  ---------------------------------------------------------------------------
  Requirement             Capability category         Architecture question
  ----------------------- --------------------------- -----------------------
  Natural-language        Copilot/agent experience    Where will users access
  employee interaction                                it?

  Grounded responses      Enterprise knowledge +      Which sources are
                          generative AI               authoritative?

  Custom orchestration    Agent tools/actions         What may the agent
                                                      invoke?

  Specialized AI          Azure AI services where     Is a prebuilt AI
  capability              required                    service needed?

  Custom development      SDK/API/tooling             Is low-code sufficient?

  Enterprise workflow     Connectors/workflows/APIs   How is authorization
                                                      enforced?

  Monitoring              Platform/solution telemetry Which KPIs and logs are
                                                      required?
  ---------------------------------------------------------------------------

## Learner task 2 --- Choose, don't over-engineer

For each requirement, classify:

-   **OOB/configuration**
-   **Low-code extension**
-   **Custom development**
-   **Not required for Release 1**

This prevents an architecture that uses every service unnecessarily.

## Learner task 3 --- Produce a logical architecture

``` text
Employee Channel
      |
      v
Employee Service Agent
      |
 +----+------------------+
 |                       |
Knowledge              Actions
 |                       |
Approved HR docs      Workflow/API
                         |
                    Enterprise system
```

Optional specialized Azure AI capabilities should be added only when
justified by requirements.

## Learner task 4 --- Technology decision record

For each selected component document:

-   Requirement served.
-   Why selected.
-   Alternative considered.
-   Security implication.
-   Scaling implication.
-   Operational owner.

## Example decision

**Decision:** Start with Copilot Studio for the Employee Service Agent.

**Reason:** The module positions Copilot Studio around
prebuilt/customizable agents and business workflow use cases; it
provides an appropriate learning path for the OOB-agent sections.

**Future extension:** Add custom Azure AI/SDK components only where
business requirements exceed the configured agent capabilities.

## Anti-pattern exercise

Identify what is wrong with:

> We have Azure AI, Copilot, APIs, SDKs, Machine Learning, and Power
> Platform, so the architecture should use all of them.

Expected response:

Technology should be selected based on requirements, measurable
outcomes, risk, and maintainability---not platform inventory.

## Deliverable

A **Requirement-to-Technology Decision Matrix** plus a logical
architecture diagram.

## Debrief

The architect's job is to select the minimum sufficient architecture
that satisfies business outcomes while remaining secure, scalable,
responsible, and maintainable.
