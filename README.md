# Annotation Guideline Templates

Reusable, project-agnostic templates for writing clear annotator guidelines — the kind of document that decides whether a labeling project produces consistent data or noise.

> All examples in this repo are **synthetic** and written for demonstration. Nothing here comes from any client or platform project.

## What's inside

| File | Purpose |
|---|---|
| [`guidelines/text-classification-guideline.md`](guidelines/text-classification-guideline.md) | Template for single-label text classification (topic, intent, sentiment) |
| [`guidelines/llm-response-rating-guideline.md`](guidelines/llm-response-rating-guideline.md) | Template for rating AI model responses on a 1–5 scale |
| [`templates/edge-case-log.md`](templates/edge-case-log.md) | Log for ambiguous items and the decisions made about them |

## Principles behind the templates

1. **Define every label with a positive example, a negative example, and a boundary case.** Most disagreement happens at the boundaries.
2. **Give a decision order.** When two labels seem to fit, annotators need to know which rule wins.
3. **Separate "what" from "how sure".** Confidence or "unsure" flags are recorded separately from the label itself.
4. **Keep an edge-case log.** Guidelines improve when every ambiguous item becomes a documented decision.
5. **Version the guideline.** Labels made under v1 and v2 should never be silently mixed.

## How to use

Copy a template, replace the `<placeholders>`, and add at least three worked examples per label before annotation starts.

## License

MIT
