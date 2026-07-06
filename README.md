<div align="center">

# varshitha sai kolupuri

cs @ scaler school of technology + bits pilani · bengaluru

distributed systems · ai agents · things that go bump in the runtime

[linkedin](https://linkedin.com/in/varshitha-kolupuri) · [rankforge, live](https://rank-forge-web.vercel.app) · [speed test, live](https://speedcheck-1mi.pages.dev)

</div>

---

i build backend systems and ai agents, usually starting at midnight.

off the clock i'm into paranormal investigation — which, it turns out, is the same job as debugging: something impossible happened, nobody witnessed it, and the logs are useless. i believe every haunting has a root cause. so far it has always been a race condition.

also: cats. 🐈‍⬛

---

### case files

**[RankForge](https://github.com/dobbydobap/RankForge)** — [live ↗](https://rank-forge-web.vercel.app)
competitive programming platform. 95+ problems, a 10-language async code judge, real-time verdicts over websockets, elo ratings, plagiarism detection. favourite part: a custom segment tree that replays the leaderboard at any minute of a past contest — time travel, but auditable.
<sub>`typescript · nestjs · next.js · postgresql · redis · bullmq`</sub>

**[Citadel](https://github.com/Astro-Dude/citadel)** — [live ↗](https://huggingface.co/spaces/Astro-Dude/citadel)
two LLM agents doing security incident response: a Commander proposes actions, an Oversight agent approves, revises, or vetoes. both trained with GRPO reinforcement learning on qwen2.5-3b. top 100, meta pytorch × scaler openenv hackathon.
<sub>`python · pytorch · grpo · docker`</sub>

**[TypeAhead](https://github.com/dobbydobap/TypeAheadHLD)**
search-as-you-type at system-design scale: a redis cache sharded across 3 nodes by a consistent-hash ring, an in-memory trie for top-K ranking, a batched writer that slashes db writes. benchmarked at p50/p95/p99.
<sub>`python · fastapi · redis · sqlite`</sub>

**[Cadenza](https://github.com/dobbydobap/Cadenza)**
a sales agent that haunts your google calendar (benevolently): 30 minutes before every meeting it researches the prospect on the live web and emails a brief with cited sources. 9 google cloud services, zero manual invocation.
<sub>`next.js · gemini · cloud run · firestore`</sub>

**[AutomationAgent](https://github.com/dobbydobap/AutomationAgent)** — [live ↗](https://varshitha2007899-automationagent.hf.space)
a poltergeist you can hire: drives a real chromium browser with actual mouse and keyboard events, detects form fields via the accessibility tree, streams every action and screenshot to a live dashboard.
<sub>`python · playwright · fastapi · docker`</sub>

**[SPEED/TEST](https://github.com/dobbydobap/speed.com)** — [live ↗](https://speedcheck-1mi.pages.dev)
an internet speed test that doesn't try to sell you a VPN. download, upload, ping, jitter, bufferbloat — zero backend, measured against cloudflare's edge, hand-rolled SVG speedometer.
<sub>`react · vite · typescript · cloudflare pages`</sub>

---

### evidence

- 🌍 global top 6 — apple developer academy, italy
- 🏆 top 100 — meta pytorch × scaler openenv hackathon
- 🔧 open-source PRs under review: [microsoft/vscode](https://github.com/microsoft/vscode/pull/324369) · [Textualize/textual](https://github.com/Textualize/textual/pull/6631) · [fedora-infra/bodhi](https://github.com/fedora-infra/bodhi/pull/6121)

### equipment

`typescript` `python` `java` `c++`
`nestjs` `fastapi` `express` `react` `next.js` `websockets`
`postgresql` `redis` `mongodb` `sqlite`
`pytorch` `grpo` `gemini · claude · openai`
`docker` `gcp` `cloudflare` `vercel` `linux`

---

<div align="center">

```
 /\_/\
( o.o )   the qa lead. reviews everything.
 > ^ <    has never once approved a pull request.
```

<sub>if your codebase does something that can't be explained, i want to hear about it.</sub>

</div>
