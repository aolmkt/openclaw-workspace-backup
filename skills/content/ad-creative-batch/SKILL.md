---
name: ad-creative-batch
description: Generate creative batches for cold-traffic campaigns with hooks, angles, and video prompts. Use when launching new creative tests or refreshing fatigued ads.
---

# Ad Creative Batch

## Inputs

- `niche`
- `offer`
- `audience`
- `language`
- `constraints` (optional: claims/compliance/style)

## Process

1. Generate hooks (target 20):
   - pain
   - curiosity
   - contradiction
   - warning
   - benefit promise
2. Generate angles (target 10):
   - hidden mechanism
   - common mistake
   - fast path
   - before/after shift
   - belief reframe
3. Generate video prompts (target 30):
   - reels/short format
   - close-up texture/motion
   - POV and before/after variants
   - clear visual tension and payoff
4. Keep outputs concrete and test-ready.

## Output

Provide both:

- Markdown list for quick human review
- JSON structure for automation

Schema:

```json
{
  "hooks": ["..."],
  "angles": ["..."],
  "video_prompts": ["..."]
}
```
