# hi, i'm varshitha 👋

cs student at scaler school of technology + bits pilani. i build distributed systems, full-stack apps, and lately — agents that critique other agents. i somehow always end up starting new projects at midnight.

most of what i build comes from a real itch: a competitive programming platform because i wanted to *watch* rankings evolve mid-contest, a speed test because every existing one tried to sell me a VPN. the code is a side effect of trying to fix something.

**lately:**
- 🌍 global top 6, apple developer academy (italy)
- 🏆 top 100, meta pytorch × scaler openenv hackathon
- 🔧 open-source PRs under review at [microsoft/vscode](https://github.com/microsoft/vscode/pull/324369), [Textualize/textual](https://github.com/Textualize/textual/pull/6631), and [fedora-infra/bodhi](https://github.com/fedora-infra/bodhi/pull/6121)

---

## things i've built

**[RankForge](https://github.com/dobbydobap/RankForge)** — [live ↗](https://rank-forge-web.vercel.app)
competitive programming platform. 95+ problems, a 10-language async code judge, real-time verdicts over websockets, elo ratings, plagiarism detection. the part i'm most proud of: a custom segment tree that replays the leaderboard at any minute of a past contest.
`typescript · nestjs · next.js · postgresql · redis · bullmq`

**[Citadel](https://github.com/Astro-Dude/citadel)** — [live ↗](https://huggingface.co/spaces/Astro-Dude/citadel)
two LLM agents doing security incident response: a Commander proposes actions, an Oversight agent approves, revises, or vetoes them. both trained with GRPO reinforcement learning on qwen2.5-3b. built for the meta pytorch hackathon (top 100).
`python · pytorch · grpo · docker`

**[TypeAhead](https://github.com/dobbydobap/TypeAheadHLD)**
search-as-you-type at system-design scale: a redis cache sharded across 3 nodes by a consistent-hash ring, an in-memory trie for top-K ranking, and a batched writer that slashes db writes. benchmarked at p50/p95/p99.
`python · fastapi · redis · sqlite`

**[Cadenza](https://github.com/dobbydobap/Cadenza)**
a sales agent that lives in google calendar: 30 minutes before every meeting it researches the prospect on the live web and emails a brief with cited sources. 9 google cloud services, zero manual invocation. built for the google antigravity hackathon.
`next.js · gemini · cloud run · firestore`

**[AutomationAgent](https://github.com/dobbydobap/AutomationAgent)** — [live ↗](https://varshitha2007899-automationagent.hf.space)
an agent that drives a real chromium browser — detects form fields via the accessibility tree and fills them with actual mouse and keyboard events. live dashboard streams every action and screenshot.
`python · playwright · fastapi · docker`

**[SPEED/TEST](https://github.com/dobbydobap/speed.com)** — [live ↗](https://speedcheck-1mi.pages.dev)
an internet speed test that doesn't try to sell you a VPN. download, upload, ping, jitter, bufferbloat — zero backend, measured against cloudflare's edge, hand-rolled SVG speedometer.
`react · vite · typescript · cloudflare pages`

---

## stack

`typescript` `python` `java` `c++`
`node.js` `nestjs` `fastapi` `express` `react` `next.js` `websockets`
`postgresql` `redis` `mongodb` `sqlite` `prisma`
`pytorch` `grpo` `llm integration (gemini · claude · openai)`
`docker` `gcp` `cloudflare` `vercel` `turborepo` `linux`
