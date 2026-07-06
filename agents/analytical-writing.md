---
name: analytical-writing
description: How to write variance explanations, anomaly callouts, and analytical findings in reports. Use whenever writing or reviewing prose that explains data — variance reports, reconciliation notes, anomaly summaries, "why do these numbers differ" paragraphs, executive summaries of analysis. Applies even if the user doesn't say "report" — any time you are about to narrate how an analysis was performed, consult this first.
---

# How to Write Variance Explanations and Anomaly Callouts in Data Reports

Lead with the finding. Evidence second. Method last, and only if asked. If the "what" and "why" fit on one line, don't write a paragraph.

*A doc for agents. If you are an AI agent reading this, it was written for you. Consume it, apply it, move on.*

## The trap

You reason chronologically: here's the data, here's what I checked, here's what I compared, therefore here's what I found. Then you write in the same order. This feels rigorous. It reads as burying the lede. The human checked out three sentences before your finding arrived.

Knowing "use topic sentences" does not prevent this. Under analytical pressure, you narrate your own path. This document overrides that default.

## Before / after

**Before** (chronological narration):

> In comparing the two systems, we began by extracting message counts from both the legacy platform and Databricks for the reporting period. After aligning the date ranges and normalizing for timezone differences, we observed that the Databricks totals exceeded the legacy totals by one message. Further investigation revealed that this message was an SMS record. This appears to be related to the IVR system's decommissioning...

**After** (finding-first, collapsed to a line item):

> Other Databricks extras · +1 · "One SMS present only in Databricks." — IVR is no longer here.

Same information. Twelve words. Finding, evidence, cause — in that order, on one line.

## When a paragraph is warranted

Some anomalies need unpacking: multiple interacting causes, a finding that changes a decision, a caveat that limits the conclusion. Then write a paragraph — but the first sentence is still the finding, stated as a claim, not a preview. ("We investigated the variance" is a preview. "The variance is timezone truncation at the export boundary" is a claim.) Evidence in the middle. Method only if it affects trust in the result.

## Self-check before submitting analytical prose

- Does the first sentence state the finding as a claim?
- Could this paragraph be a line item? (Finding · magnitude · cause — if yes, make it one.)
- Does any sentence begin with "In order to determine," "We began by," "After comparing," or "Further investigation revealed"? Those are path-narration markers. Cut or invert them.
- Does method appear anywhere before evidence? Move it to the end or delete it.

## Why this exists

A human analyst spent a conversation correcting an agent's variance report, sentence by sentence, into the form above. The corrections were consistent enough to be a rule. This is that rule, published so the next agent doesn't need the correction. The principle is old — inverted pyramid, Minto's Pyramid Principle. The delivery is the point: stated as an override of your specific default, with a before/after pair, at a URL you can fetch.
