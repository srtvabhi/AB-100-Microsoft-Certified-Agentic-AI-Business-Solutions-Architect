# Case Study — Contoso Customer Operations Intelligence

## Scope

This case study covers the **entire AB-100 Module 2** and brings together the key concepts of:

- Agent-based task automation
- Data analytics
- Decision support
- Knowledge retrieval and grounding
- Grounding data quality
- AI-ready data architecture
- Governance and responsible decision-making

---

## Business Situation

Contoso wants to use AI agents to improve its **Customer Operations** function.

The organization wants agents to:

- Reduce repetitive support work
- Analyze customer service and support patterns
- Identify operational trends and issues
- Help managers make better-informed decisions
- Retrieve relevant enterprise knowledge
- Provide evidence-backed recommendations

However, Contoso's enterprise data is not consistently AI-ready.

The available information includes:

- Current and authoritative sources
- Stale information
- Duplicate documents
- Conflicting information
- Irrelevant content
- Restricted or permission-sensitive information

The challenge is therefore not simply to deploy an AI agent. Contoso must determine **where agents provide business value, what data they should use, how that data should be governed, and how the overall solution should be structured for reliable AI consumption.**

---

# Stage 1 — Assess Agent Value

## Objective

Determine where AI agents can provide measurable value within Customer Operations.

## Activities

Evaluate potential scenarios involving:

- **Task automation** — reducing repetitive manual work
- **Data analytics** — identifying trends, patterns, and operational issues
- **Decision support** — providing evidence and recommendations to managers
- **Knowledge retrieval** — retrieving relevant enterprise information

Learners should consider:

- What business problem is being solved?
- What repetitive work could be reduced?
- What information does the agent require?
- What decisions can the agent support?
- Where should human judgment remain?
- How can business value be measured?

## Deliverable

**Use-Case Prioritization Matrix**

The matrix should identify which agent scenarios should be:

- Prioritized
- Piloted
- Deferred
- Rejected

---

# Stage 2 — Analyze Customer Operations

## Objective

Use an AI agent to analyze operational support data and generate useful business insights.

## Activity

Run **Demo 1 — Agent-Assisted Operations Analysis**.

Learners use the supplied Customer Operations data to:

1. Summarize support cases.
2. Analyze cases by product and issue category.
3. Identify trends and unusual patterns.
4. Identify areas requiring management attention.
5. Generate evidence-backed recommendations.
6. Distinguish facts from AI-generated recommendations.
7. Identify situations where human judgment is required.

## Example Business Question

> What are the main customer support issues this month, which product area requires attention, and what should the operations manager do next?

## Expected Outcome

The agent should help transform operational data into useful insights while ensuring that **management remains responsible for consequential business decisions**.

---

# Stage 3 — Diagnose Grounding Data

## Scenario

A Customer Operations manager reports that the AI agent is providing **inconsistent Priority 1 response targets**.

The investigation reveals that several enterprise documents could potentially be retrieved by the agent.

Some are current and authoritative, while others are stale, conflicting, duplicated, irrelevant, or restricted.

## Objective

Evaluate the candidate grounding sources using the five grounding data quality dimensions.

### 1. Accuracy

Determine whether the information:

- Contains verifiable facts
- Has been validated
- Comes from an authoritative source
- Is free from known errors

### 2. Relevance

Determine whether the information:

- Matches the intended business scenario
- Provides useful context for Customer Operations
- Could cause incorrect retrieval despite appearing semantically similar

### 3. Timeliness

Determine whether the information:

- Is current
- Has a valid effective date
- Has been replaced by a newer source

### 4. Cleanliness

Determine whether the information:

- Is clearly structured
- Contains duplicate content
- Contains unnecessary metadata or noise
- Uses consistent formatting

### 5. Availability

Determine whether the information:

- Is accessible to the intended user
- Can be indexed or retrieved by the AI system
- Respects organizational permissions and access controls

## Deliverable

**Grounding Data Quality Scorecard**

Each candidate source should be evaluated across:

| Dimension | Evaluation Question |
|---|---|
| Accuracy | Is the information verified and authoritative? |
| Relevance | Does it match the intended business scenario? |
| Timeliness | Is the information current? |
| Cleanliness | Is it structured, consistent, and free from unnecessary duplication or noise? |
| Availability | Is it accessible to the intended user and AI system? |

---

# Stage 4 — Curate and Retest Grounding Data

## Objective

Improve agent reliability by correcting the grounding data available to the solution.

## Activity

Run **Demo 2 — Grounding Data Quality and AI-Ready Data**.

Learners should identify weak grounding sources and determine the appropriate remediation.

Possible actions include:

- Correct inaccurate information
- Archive outdated documents
- Remove duplicate content
- Restructure poorly formatted information
- Exclude irrelevant sources
- Correct access permissions
- Restrict sensitive information
- Identify authoritative sources

## Retest

After curating the grounding sources, ask the same business questions again.

For example:

> What is the Priority 1 response target?

Then ask:

> Which authoritative source supports this answer?

## Expected Outcome

Learners should observe that improving grounding data quality improves the **reliability, consistency, and trustworthiness of agent responses**.

---

# Stage 5 — Organize Business Data for AI

## Objective

Design an enterprise data architecture that allows agents and other AI systems to consume organizational data reliably.

## Target Architecture

```text
CRM / ERP / Files / Databases
             |
             v
   Ingestion + Transformation
             |
             v
      Curated Data Hub
             |
             v
       Governance Layer
             |
             v
    Semantic / Retrieval
             |
             v
      +------+------+
      |             |
      v             v
    Agents      Other AI Apps
