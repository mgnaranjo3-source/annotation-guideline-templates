# <Project Name> — Text Classification Guideline (v1.0)

## 1. Task summary
You will read one short text at a time and assign **exactly one** label from the list below.

- **Unit of annotation:** one text item (message, review, sentence)
- **Output:** one label + optional "unsure" flag + optional comment
- **Language(s):** <EN / ES / both>

## 2. Label definitions

### `POSITIVE`
The author expresses an overall favorable opinion.
- ✅ Example: "Delivery was fast and the product works perfectly."
- ❌ Not this label: "Delivery was fast, but the product broke in a day." → `NEGATIVE` (the final judgment is negative)
- ⚖️ Boundary: "Not bad at all." → `POSITIVE` (negated negative = mild positive)

### `NEGATIVE`
The author expresses an overall unfavorable opinion.
- ✅ Example: "Customer service never answered my emails."
- ❌ Not this label: "Is customer service open on Sundays?" → `NEUTRAL` (a question, no opinion)
- ⚖️ Boundary: "Great, another update that breaks everything." → `NEGATIVE` (sarcasm: label the intended meaning)

### `NEUTRAL`
No opinion, or factual information only.
- ✅ Example: "The package arrived on Tuesday."
- ⚖️ Boundary: "It's okay." → `NEUTRAL` unless context adds a clear direction

### `MIXED`
Clear positive **and** clear negative opinions with no dominant one.
- ✅ Example: "Love the camera, hate the battery."

## 3. Decision order
When more than one label seems to apply, check in this order:
1. Is there any opinion at all? If no → `NEUTRAL`
2. Is there a final/overall judgment? If yes → label that judgment
3. Are positive and negative roughly equal? If yes → `MIXED`

## 4. Special cases
| Case | Rule |
|---|---|
| Sarcasm | Label the intended meaning, add comment `sarcasm` |
| Emojis only | Label by the emoji's common meaning; flag `unsure` if ambiguous |
| Code-switching (EN/ES mixed) | Label the whole text; do not split by language |
| Spam / non-language | Use `NEUTRAL` + comment `invalid` |

## 5. Quality expectations
- Read the whole text before labeling.
- Do not use outside knowledge about the product or brand.
- Use the "unsure" flag honestly; it is a signal, not a penalty.

## 6. Changelog
| Version | Date | Change |
|---|---|---|
| 1.0 | <date> | Initial version |
