# GEO Retrieval Gates — Stage 0 and Fan-Out Queries

## Stage 0: Candidate Pool Eligibility

The GEO Stack (Layers 1-5) operates on content that has already been retrieved into the LLM's candidate pool. That pool is populated from the top 20-30 organic search results for the target query and its fan-out sub-queries.

**If a page does not rank in that window, Layers 1-5 interventions produce zero improvement.** Not marginal — zero. Retrieval cannot be optimised for content that was never considered.

### The Two-Stage Pipeline

| Stage | What it does | Signals |
|-------|-------------|---------|
| **Stage 1: Document-level relevance** | Classic ranking — does the page appear in the candidate pool? | Domain authority, topical relevance, backlinks, traditional SEO |
| **Stage 2: Passage-level retrieval** | LLM readability — once in the pool, does the AI extract and cite specific sections? | Extractability, entity clarity, structural authority |

Both stages must be addressed. Most GEO advice only addresses Stage 2. If Stage 1 is failing, Stage 2 interventions are inert.

### Practical Check

Before running any GEO audit on a page:
1. Verify the page ranks in the top 30 for at least one target query
2. If it does not rank, the priority is SEO — not GEO
3. Use GSC position data or manual SERP checks to confirm

### The Two Parallel Tracks

Practitioners can work both tracks simultaneously:

- **Track 1: Pipeline Optimisation (L1 + L2)** — structural changes to content format, heading architecture, declarative structure. Measurable within 4-8 weeks.
- **Track 2: Entity & Authority Building (L3 + L4 + L5)** — entity coherence, citation networks, topical authority. Compounds over months.

Do not wait for Track 1 to finish before starting Track 2. They are parallel, not sequential.

---

## Fan-Out Queries: The Hidden Retrieval Opportunity

When an LLM receives a query, it generates multiple sub-queries (fan-out queries) to retrieve passages for different facets of the answer.

### How Fan-Out Works

A page may rank well for the main query but have individual H2 sections more semantically aligned with specific fan-out sub-queries than with the main query itself.

**Example:** For "what is GEO", fan-out sub-queries might include:
- "how does retrieval probability work"
- "what is extractability in AI search"
- "GEO vs SEO differences"
- "how to measure AI citation rate"

Each H2 section is a candidate for a different fan-out query — not just the main query.

### The Implication

A page does not need every section to answer the main query. Each section needs to answer ONE query — the main query OR one of its likely fan-out sub-queries — with full semantic alignment at the section level.

A section that partially answers two queries retrieves worse than a section that fully answers one.

### Fan-Out Query Identification Protocol

1. Run target query on Perplexity
2. Record the follow-up questions Perplexity generates (these approximate fan-out sub-queries)
3. Map each H2 section on your page to one fan-out sub-query
4. Identify unmapped sections (restructuring candidates) and unmapped sub-queries (content gaps)
5. Include fan-out sub-queries in the 30-check protocol test set

### When Advising on Content Structure

Always consider fan-out queries when recommending H2 structure:
- Each H2 should target one specific query (main or fan-out)
- If a section can't be mapped to any query, it's a topical isolation failure
- Unmapped fan-out sub-queries are content gap opportunities
