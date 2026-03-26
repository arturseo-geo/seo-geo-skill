# Citation-Ready Content — Sentences, Sections, and Statistical Currency

## Citation-Ready Sentences

A citation-ready sentence can stand alone in an AI-generated answer with just the author's name attached. It is specific, claim-complete, entity-named, and requires no surrounding context.

### The Test

> "Can this sentence appear in a Perplexity answer as a direct quote with '[Author], [Source]' below it and make complete sense to a reader who has never seen the page?"

If yes — citation-ready. If no — not citation-ready.

### Rules

- The opening sentence of every H2 section should be citation-ready
- This is the strictest version of the declarative structure requirement
- It forces specificity, entity naming, and claim completeness

### Before/After Examples

**Before:** "This is where things get interesting for practitioners working in the AI search space."
- Fails: meaningless in isolation, no entity, no claim

**After:** "Extractability measures how cleanly a content section can be parsed and reused by AI systems without losing meaning."
- Passes: specific claim, named concept, standalone comprehension

**Before:** "As we discussed in the previous section, the results were significant."
- Fails: depends on prior context, vague claim

**After:** "Structural changes that improved LLM readability produced a 24 percentage point citation rate improvement in controlled testing on Perplexity."
- Passes: specific data, named platform, standalone claim

---

## Context Management

Context management failure occurs when a section switches topics mid-paragraph, uses pronouns with unresolved referents, or assumes the reader has context from an adjacent section.

### Why It Matters for GEO

An LLM processing a chunk in isolation cannot resolve "it", "this", "the system", or "as mentioned above". The chunk produces a weak or incoherent embedding that misrepresents the section's actual topic.

### The Test

Read an H2 section aloud to someone who has not read the rest of the post. If they ask "what does that refer to?" — the section has a context management failure.

### Common Failures

| Pattern | Problem | Fix |
|---------|---------|-----|
| "It also works for..." | "It" unresolved | Name the entity: "The GEO Stack also works for..." |
| "As mentioned above..." | Assumes prior context | Restate the fact |
| "This approach..." | "This" ambiguous | Name the approach: "The declarative structure approach..." |
| "The system processes..." | Which system? | "Perplexity's retrieval system processes..." |

### When Advising on Content

Flag every pronoun in a section. For each: can it be replaced with a specific named entity without changing the meaning? If yes, it should be.

---

## Statistical Currency

Statistical currency is the degree to which verifiable claims in a content section are consistent with the most recent available evidence.

### Why It's a GEO Signal (Not Just Credibility)

AI systems cross-reference claims against other sources during retrieval. An outdated statistic that contradicts more recent sources creates a consistency conflict that actively suppresses citation rate. The retrieval system cannot cite a source that contradicts the consensus it is drawing from.

### Practical Rules

- Any section with time-sensitive statistics should be reviewed every 6-12 months
- A statistic from 2021 cited alongside 2025 research from the same domain is a retrieval risk
- After updating statistics, re-run the 30-check protocol to confirm citation rate hasn't decayed
- Sections with original research / first-party data have higher retrieval rates than sections making claims without data

### When Advising on Content Updates

1. Identify every statistic and its source date
2. Flag anything >12 months old
3. Find current equivalent from named source
4. Replace and update attribution
5. Confirm opening sentences are still declarative after edits
