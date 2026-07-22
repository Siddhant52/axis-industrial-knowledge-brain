# AXIS — Unified Asset & Operations Brain

**ET AI Hackathon 2026 — Problem Statement 8: AI for Industrial Knowledge Intelligence**

AXIS is a prototype AI platform that unifies fragmented industrial documents — P&IDs, CMMS work orders, SOPs, inspection reports, and regulatory standards — into a single, queryable knowledge layer. It answers operational questions with cited sources and proactively surfaces cross-functional risk patterns that no single document or team would catch alone.

## Live Prototype
Open `industrial-knowledge-brain.html` directly in any browser — no build step, no server required. Runs entirely client-side.

## What it demonstrates
- **Knowledge Corpus** — 6 ingested documents across 5 document types (P&ID, work order, SOP, inspection report, regulatory standard, near-miss report), all resolved onto shared equipment tags.
- **Expert Knowledge Copilot** — ask a question in plain language, get an answer grounded strictly in the retrieved documents, with a confidence score and source citations.
- **Live Knowledge Graph** — visualizes which documents and entities were used to answer each query.
- **Cross-Functional Signals** — an RCA agent and a Compliance agent that surface patterns spanning multiple document types (e.g. a pump's repeated bearing failures linked to a previously silenced vibration alarm; a vessel's corrosion rate cross-referenced against its regulatory inspection interval).

## Try these queries
- "What's the maintenance and incident history for P-207A?"
- "Is vessel V-112 compliant with its inspection interval under OISD-STD-118?"
- "What's the startup sequence for Compressor C-305?"
- "What safety concerns exist around Reactor R-101's feed line?"

## Architecture
See `docs/architecture-diagram.png` and the detailed submission document for the full six-layer architecture (Sources → Ingestion → Knowledge Layer → Agentic Intelligence → Experience Layer → Users) and the production-scale technology roadmap.

## Tech stack (prototype vs. production direction)
| Layer | This prototype | Production direction |
|---|---|---|
| Ingestion | Structured mock corpus | OCR / Document Intelligence + Computer Vision for P&ID parsing |
| Retrieval | Client-side lexical scoring | Embedding-based semantic vector search |
| Copilot | Offline extractive synthesis | Server-hosted LLM generation |
| Knowledge layer | In-browser entity graph | Graph database (e.g. Neo4j) + vector index |
| Agents | Rule-based demo signals | Scheduled/event-driven agents over the live graph |

## Team
Team AXIS — ET AI Hackathon 2026

## Files
- `industrial-knowledge-brain.html` — the working prototype
- `docs/` — architecture diagram, detailed submission document, and supporting materials
