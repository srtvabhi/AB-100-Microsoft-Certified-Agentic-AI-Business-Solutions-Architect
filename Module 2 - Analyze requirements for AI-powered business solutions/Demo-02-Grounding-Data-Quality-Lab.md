# Hands-on Demo 2 --- Grounding Data Quality and AI-Ready Data

## Unit mapping

**Primary:** Review Data for Grounding\
**Supporting:** Organize Business Solution Data to Be Available for
Other AI Systems \## Objective Demonstrate that agent reliability
depends on the grounding layer, not only the model. \## Data Use all
files in `Training-Data/Grounding-Challenge/`. \## Five-dimension
scorecard \| Dimension \| Test \| \|---\|---\| \| Accuracy \| Is it
verified and authoritative? \| \| Relevance \| Does it match the agent's
intended business scenario? \| \| Timeliness \| Is it current? \| \|
Cleanliness \| Is it structured, deduplicated, and low-noise? \| \|
Availability \| Is it accessible/indexable for the intended user? \| \##
Lab 1. Review every candidate source. 2. Ask: **What is the Priority 1
response target?** 3. Identify the stale, conflicting, duplicate/noisy,
irrelevant, and restricted sources. 4. Score each source 1--5 across the
five dimensions. 5. Curate the grounding set. 6. Retest: **What is the
Priority 1 response target and which authoritative source supports it?**
7. Ask: **Is the 2024 target still valid?** 8. Discuss why a useful
restricted document is not automatically valid grounding for every user.
9. Create a remediation plan: correct, archive, deduplicate,
restructure, reclassify permissions, or exclude. \## Target architecture

``` text
Business Sources
      |
Ingestion / Transformation
      |
Curated Enterprise Data
      |
Governance + Permissions
      |
Semantic / Retrieval Layer
      |
Agents / Copilots / RAG Apps
```

## Success criteria

Learners can explain exactly how accuracy, relevance, timeliness,
cleanliness, and availability affect retrieval and trustworthy agent
behavior.
