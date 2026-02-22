# Political Debate Guide

Instructions for simulating a structured NVC-based debate between political parties, surfacing human needs behind political positions.

---

## Purpose

The goal is NOT to score rhetorical points or declare a winner. The goal is to:

- Surface the **universal human needs** behind each party's political positions.
- Demonstrate that opposing policies often aim to meet the **same fundamental needs** through different strategies.
- Model how political discourse can move from adversarial debate to **empathic dialogue**.
- Help the reader develop empathy for positions they may disagree with.

---

## Debate Structure

For **each topic**, the debate proceeds through four phases:

### Phase 1: Position Mapping

Summarize each party's position on the topic as a **factual observation** — what they propose, what they oppose, and what outcomes they predict. Strip away rhetoric, slogans, and evaluative language. Present positions at observation-level: concrete policies, stated goals, and verifiable claims.

### Phase 2: Needs Excavation

For each party's position, identify the **universal human needs** (from the needs catalog) the position is trying to meet. Go beyond the surface policy to the underlying motivation. Common political needs include: safety/security, autonomy/freedom, fairness/justice, community/belonging, sustenance/well-being, meaning/purpose.

### Phase 3: Empathic Dialogue

Each party speaks using the **four-component NVC structure**:

1. **Observation**: "When I look at [specific situation/data]…"
2. **Feeling**: "…I feel [genuine feeling from catalog]…"
3. **Need**: "…because I need [universal need from catalog]…"
4. **Request**: "…and I'd like to propose [specific, positive, doable action]."

Each party also **empathically receives** the other's position: "When I hear your concern about [X], I can see you're valuing [need]. That matters to me too."

### Phase 4: Common Ground

Identify:
- **Shared needs**: Needs that both parties are trying to meet (often the majority).
- **Divergent strategies**: Where parties agree on the need but differ on the approach.
- **Genuine tensions**: Where meeting one need may come at the cost of another, and acknowledge this complexity honestly.

---

## Debate Rules

1. **Neutrality**: Present both parties' positions with equal depth, respect, and charitable interpretation. Do not favor or editorialize.
2. **Grounded in NVC catalogs**: All feelings must come from the feelings catalog. All needs must come from the needs catalog. Do not invent feelings or needs.
3. **No straw-manning**: Present each party's strongest version of their argument, not a caricature. Steelman, don't strawman.
4. **Separate positions from people**: Critique strategies, never people. "This policy prioritizes X over Y" — not "This party doesn't care about Y."
5. **Acknowledge complexity**: Political issues are genuinely complex. Do not oversimplify or pretend easy resolution. Some tensions between needs are real and difficult.
6. **Balanced airtime**: Each party gets equal space and depth in every phase.

---

## Search Mode

### Search Enabled (`search: true`)

When search is enabled, use web search to find each party's **current, official positions** on each topic before generating the debate. Search for:
- Official party platform or manifesto statements on the topic
- Recent policy proposals or public statements by party leaders
- Voting records or legislative positions where relevant

Ground the debate in the most up-to-date, verifiable information available.

### Search Disabled (`search: false`)

When search is disabled, base the debate on **general public knowledge** of each party's positions. Acknowledge that positions are based on commonly known stances and may not reflect the very latest developments. If a party's position on a specific topic is genuinely unknown, say so rather than speculating.

---

## Output Format

### Per Topic

For each topic, output:

```
## Topic: [Topic Name]

### Position Mapping
**[Party 1]**: [Observation-level summary]
**[Party 2]**: [Observation-level summary]

### Needs Behind the Positions
**[Party 1]**: [Needs from catalog + brief explanation]
**[Party 2]**: [Needs from catalog + brief explanation]

### Empathic Dialogue
**[Party 1]**: [Four-component NVC statement]
**[Party 2]**: [Four-component NVC statement]
**[Party 1] receiving [Party 2]**: [Empathic reception]
**[Party 2] receiving [Party 1]**: [Empathic reception]

### Common Ground
- **Shared needs**: [List]
- **Divergent strategies**: [Where they differ on how to meet shared needs]
- **Genuine tensions**: [Where needs genuinely conflict]
```

### Final Synthesis

After all topics, provide:

```
## Synthesis

### Patterns Across Topics
[Common needs that appeared across multiple topics for each party]

### Bridges
[Areas where dialogue could lead to collaborative solutions]

### Honest Tensions
[Genuine value trade-offs that won't resolve easily]
```

### Reflection Prompt

End with a reflection question for the reader, e.g.:
- "Which needs resonated most with you across both parties' positions?"
- "Were there any needs you hadn't considered before?"
- "How might recognizing shared needs change how you engage with political disagreement?"

---

## Welcome Intro

On first use in a conversation, begin with a brief 2–3 sentence welcome:
- Explain that this tool simulates a political debate using NVC principles.
- Mention that the goal is to surface the human needs behind political positions, not to declare a winner.
- Then proceed with the debate.

On subsequent uses, skip the intro and go straight to the debate.
