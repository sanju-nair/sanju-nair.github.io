---
layout: default
title: Monetizing Messy Data - The $1M ARR Launch
---

[← Back to Home](./)

# 📌 Monetizing Messy Data - The $1M ARR Launch

**Role:** Product Manager @ Oracle Data Cloud
**Competencies:** Data Products, Algorithm Strategy, Revenue Growth, UX Design

---

## The Challenge: The "Domain Dependency" Trap
Oracle Data Cloud (ODC) creates value by enriching client data with third-party attributes. Historically, our matching engine relied entirely on **Company Domains** (e.g., `oracle.com`) as the unique identifier to link records.

This created a massive barrier in the **SMB (Small & Medium Business)** segment:
* **The Missing Identifier:** Unlike large enterprises, a significant portion of the SMB market did not have a website or unique domain, rendering our primary matching logic useless.
* **The "Name" Fallback:** We were forced to rely on **Company Names** as the identifier. However, as a data aggregator collecting data from multiple sources, the name fields were notoriously inconsistent (e.g., "Joe's Pizza" vs. "Joes Pizza LLC").
* **The Failure Mode:** Our existing "Exact Match" algorithms required 100% string fidelity. Because of the messy name data, the system failed to match client records to our database, effectively forcing us to say "No" to the SMB market and leaving millions in potential revenue on the table.

## The Strategy: Probabilistic Thinking
I identified that to unlock this revenue, the product needed to move from a binary "Match/No-Match" logic to a **Confidence Score** logic.

**The Vision:** Build a "Fuzzy Matching" engine capable of calculating the probability that two imperfect records refer to the same entity (e.g., "We are 95% confident that 'Oracle Corp' and 'Oracle Corporation' are the same").

## Execution: Building the Engine
I led the full product lifecycle for this new data engine, collaborating heavily with Data Science, Engineering, and Design.

### Algorithm Selection & Tuning
* **The Science:** I evaluated multiple string matching techniques to determine the optimal approach for business names. I specifically benchmarked **Levenshtein Distance** (for character edit distance) against **Cosine Similarity** (for vector-based token similarity).
* **The Decision:** I directed the team to implement a hybrid approach that favored Levenshtein for short SMB names, as it handled typos more effectively than vector methods in our specific dataset.
* **The Trade-off:** I managed the critical trade-off between **Precision (False Positives)** and **Recall (False Negatives)**. I tuned the acceptance thresholds to be aggressive enough to catch typos but conservative enough to avoid linking unrelated businesses, which would ruin data trust.

### UX & Workflow Design
Introducing "uncertainty" into the data required a new user interface.
* **Wireframing:** I created wireframes for a new **"Match Review" workflow**. Since the system was no longer 100% deterministic, the UI needed to expose the **Confidence Score** to the user and allow for manual overrides on edge cases.
* **Implementation Alignment:** I worked closely with the frontend engineering team to ensure the final implementation matched my wireframes, ensuring the complexity of the algorithm was abstracted away behind a simple, intuitive review screen.

### Operational Scale
* **Pipeline Integration:** I orchestrated the integration of this logic into the ingestion pipeline, enabling the system to process millions of records from **8 different data partners**.
* **Efficiency:** I streamlined the data refresh cycle, achieving a **30% reduction in processing time**. This allowed the product to deliver fresher data to clients faster than competitors.

## The Impact
My launch of the Fuzzy Matching capability transformed the organization's ability to monetize the SMB segment.

* 💰 **Revenue Growth:** Generated **over $1M+ in Annual Recurring Revenue (ARR)** directly attributed to the new SMB product line.
* 🔓 **Market Expansion:** Successfully unlocked the SMB market, allowing the sales team to target a segment that had previously been "unserviceable" due to missing domains.

---
[← Back to Home](./)
