# Roadmap

Planned MCP tools beyond the current `thought_clarifier`.

## Module 2: Message Transformer ✅

**Tool**: `transform_message` — **Implemented**

**Input**: `{ text: string }` — any message (email, chat, feedback, etc.)

**Behavior**: Rewrites the message using NVC principles. Offers two modes: one-shot (direct rewrite with "What changed" summary) or guided (step-by-step clarification through observation → feelings → needs → request). Strips evaluations, translates faux feelings, identifies underlying needs, and reformulates the message using the four-component structure.

**Use case**: "Rewrite this angry email to my colleague using NVC."

---

## Module 3: NVC Trainer ✅

**Tool**: `nvc_trainer` — **Implemented**

**Input**: `{ topic: "observations" | "feelings" | "needs" | "requests", difficulty?: "beginner" | "intermediate" | "advanced" }` — an NVC building block to practice and optional difficulty level (default: beginner).

**Behavior**: Generates interactive exercises on the chosen NVC building block. Format varies by difficulty: beginner uses multiple-choice identification, intermediate adds nuanced distractors and short open-ended prompts, advanced uses complex real-world open-ended reformulation. Provides detailed feedback grounded in the knowledge base, referencing NVC concepts by name.

**Use case**: "Give me a practice exercise on distinguishing feelings from faux feelings."

---

## Module 4: Political Talk Show ✅

**Tool**: `political_debate` — **Implemented**

**Input**: `{ party1: string, party2: string, topics: string[] (1–10), search?: boolean }` — two party names, debate topics, and optional web search for latest positions.

**Behavior**: Simulates a structured NVC debate between two political parties. For each topic, proceeds through four phases: Position Mapping (observation-level summaries), Needs Excavation (mapping positions to the needs catalog), Empathic Dialogue (each party speaks in four-component NVC), and Common Ground (shared needs, divergent strategies, genuine tensions). Concludes with a cross-topic synthesis and reflection prompt. When `search` is enabled, instructs the host LLM to look up current party positions before generating.

**Use case**: "Simulate a debate between the Democrats and Republicans on healthcare and immigration, using NVC."
