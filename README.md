## Gustavo Rosas

Computer Science student at the University of Florida focused on systems programming, real-time pipelines, and AI-native developer tooling. I build end-to-end: backend engines, live data layers, and the frontends that wire them together.

---

### Projects

**[CoMeet](https://github.com/GusDawn123/CoMeet)** — Real-Time AI Meeting Assistant  
`TypeScript · React · Node.js · WebSocket · Deepgram Nova-3 · Gemini · PostgreSQL`

Built a live meeting assistant that transcribes speech in real time and routes it through an AI coaching engine. Replaced a polling-based Whisper pipeline with a persistent Deepgram WebSocket connection piping raw PCM directly from WASAPI loopback — reducing transcription latency 94%, from ~5 s per chunk to under 300 ms. The intent classifier runs a regex fast-path (~20 patterns) before touching any LLM, classifying in under 1 ms with zero cold-start. A multi-provider fallback chain (Gemini 2.5 Flash → GPT-4o → Groq Llama 3.3 70B) delivers the first streaming token under 300 ms across an isolated per-session context window.

**[Arch Copilot](https://github.com/GusDawn123/arch-copilot)** — AI Architecture Copilot  
`Python · FastAPI · Anthropic Claude · React · TypeScript · Tauri`

A 10-phase architecture workflow engine that takes a project description through product framing, feature definition, actor modeling, use cases, quality attributes, constraints, pattern recommendations, architecture planning, implementation milestones, and prompt generation — each phase driven by YAML strategy files and Claude. Includes an architecture-aware code review engine that reviews submitted code against the approved architecture artifacts (not generic best practices), flagging issues by severity with self-scored confidence ratings and a compliance table.

**[Order Book Engine](https://github.com/GusDawn123/orderbook)** — C++20 Limit Order Book  
`C++20 · CMake · Google Test · Node.js · Express · React · PostgreSQL · Docker`

A limit order book and matching engine in C++20 handling GoodTillCancel and FillAndKill order types with strict price-time priority. Pre-caches order positions at insertion time for O(1) cancellation regardless of book depth. Full-stack: REST + WebSocket API in Node/Express pushes every state change to connected clients in under 10 ms. Containerized with Docker Compose, 40+ passing unit tests in CI.

---

### Skills

```
Languages    C++20 · TypeScript · Python · JavaScript · SQL
Backend      Node.js · Express · FastAPI · Prisma · WebSocket
Frontend     React · Vite · Tailwind CSS
AI / Data    Deepgram Nova-3 · Gemini · GPT-4o · Anthropic Claude
Systems      CMake · STL · Google Test · Docker · GitHub Actions
```
