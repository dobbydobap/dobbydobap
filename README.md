<img src="https://capsule-render.vercel.app/api?type=waving&color=0:e8c0cd,50:d9a3b5,100:c88da1&height=160&section=header&text=varshitha%20sai%20kolupuri&fontSize=38&fontColor=ffffff&fontAlignY=35&desc=distributed%20systems%20%C2%B7%20ai%20agents%20%C2%B7%20things%20that%20go%20bump%20in%20the%20runtime&descSize=14&descAlignY=58&animation=fadeIn" width="100%" alt="header" />

<div align="center">

cs @ scaler school of technology + bits pilani · bengaluru

<a href="https://linkedin.com/in/varshitha-kolupuri"><img src="https://img.shields.io/badge/linkedin-c88da1?style=for-the-badge&logo=linkedin&logoColor=white" alt="linkedin" /></a>&nbsp;
<a href="https://rank-forge-web.vercel.app/"><img src="https://img.shields.io/badge/rankforge_live-d9a3b5?style=for-the-badge&logo=vercel&logoColor=white" alt="rankforge" /></a>

</div>

<br/>

i build backend systems and ai agents. the kind of software where the hard part is invisible and the bugs only appear after midnight. conveniently, that's when i start working.

off the clock i'm into paranormal investigation, which turns out to be the same job as debugging. something impossible happened, nobody witnessed it, and the logs are useless. i believe every haunting has a root cause. so far, it has always been a race condition.

also: cats. 🐈‍⬛

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:e8c0cd,100:c88da1&height=2" width="100%" alt="" />

### 🌸 field work

other people's codebases, other people's hauntings.

**14 PRs merged across 8 upstream projects.** two of them cncf graduated, plus node.js core.

**apicurio registry** · [#8684](https://github.com/Apicurio/apicurio-registry/pull/8684) · [#9055](https://github.com/Apicurio/apicurio-registry/pull/9055) · [#9850](https://github.com/Apicurio/apicurio-registry/pull/9850)

found [#8926](https://github.com/Apicurio/apicurio-registry/issues/8926): MCP tool annotations were being validated against the wrong schema entirely, so not one of the four hints anyone wrote was ever checked. reported it, then fixed it.

**opentelemetry** <sub>go compile-time instrumentation</sub> · [#856](https://github.com/open-telemetry/opentelemetry-go-compile-instrumentation/pull/856) · [#887](https://github.com/open-telemetry/opentelemetry-go-compile-instrumentation/pull/887)

found [#886](https://github.com/open-telemetry/opentelemetry-go-compile-instrumentation/issues/886): struct rules cheerfully matched things that were not structs, and inside a grouped `type` block a field could land on a struct nobody named. reported it, then fixed it.

**kubeflow pipelines** · [#13780](https://github.com/kubeflow/pipelines/pull/13780) · [#14169](https://github.com/kubeflow/pipelines/pull/14169)

the python sdk was quietly adding `--trusted-host` to every pip call. opt-in now. also closed a concurrency hole that let you retry an archived run.

**microsoft/vscode** · [#324571](https://github.com/microsoft/vscode/pull/324571) · [#324734](https://github.com/microsoft/vscode/pull/324734) · [#324369](https://github.com/microsoft/vscode/pull/324369)

a rerun-last-task regression, a pinned tab that refused to let go when dragged, and configure-snippets now lists the active editor language first.

**also merged** · nodejs/node [#64365](https://github.com/nodejs/node/pull/64365) · fedora-infra/bodhi [#6121](https://github.com/fedora-infra/bodhi/pull/6121) · nansen-cli [#465](https://github.com/nansen-ai/nansen-cli/pull/465) · fedora-infra/anitya [#2105](https://github.com/fedora-infra/anitya/pull/2105)

<sub>in review · vscode [#326451](https://github.com/microsoft/vscode/pull/326451) [#326447](https://github.com/microsoft/vscode/pull/326447) [#325654](https://github.com/microsoft/vscode/pull/325654) [#324682](https://github.com/microsoft/vscode/pull/324682) · nodejs/node [#65695](https://github.com/nodejs/node/pull/65695) [#65981](https://github.com/nodejs/node/pull/65981) · textualize/textual [#6631](https://github.com/Textualize/textual/pull/6631) [#6630](https://github.com/Textualize/textual/pull/6630) · datahub [#38](https://github.com/datahub-project/datahub-skills/pull/38)</sub>

the half i like best: find it myself, report it, then fix it.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:e8c0cd,100:c88da1&height=2" width="100%" alt="" />

### 🌸 leaderboards

on [kaggle](https://www.kaggle.com/varshithakolupuri) the modelling is there: a coatnet + 2.5d convnext MIL ensemble on **rsna knee abnormality detection**, dinov2 features, multi-reader blends.

but the four notebooks i've actually made public are the ones where i went looking for what was wrong.

**rsna knee: real scores of every public notebook**

reported scores against what they actually reproduce. my most-upvoted thing by a distance.

**playground s6e10**

three notebooks. is the test set different from train, which features actually matter, and how much of the leaderboard is just noise.

**kaggriculture front-run agents**

a public dataset, for the agents that trade ahead of the market.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:e8c0cd,100:c88da1&height=2" width="100%" alt="" />

### 🌸 case files

#### RankForge

a competitive programming platform, built end to end. 95+ problems, an async code judge that speaks 10 languages, real-time verdicts over websockets, elo ratings, plagiarism detection.

the favourite child: a custom segment tree that can replay the leaderboard at any minute of any past contest. time travel, but auditable.

<sub>`typescript` · `nestjs` · `next.js` · `postgresql` · `redis` · `bullmq` &nbsp;·&nbsp; [live](https://rank-forge-web.vercel.app/) &nbsp;·&nbsp; [source](https://github.com/dobbydobap/RankForge)</sub>

#### Citadel

security incident response, run by two LLM agents keeping each other honest. a Commander proposes actions, an Oversight agent approves, revises, or vetoes.

both agents trained with GRPO reinforcement learning on qwen2.5-3b. placed top 100 at the meta pytorch × scaler openenv hackathon.

<sub>`python` · `pytorch` · `grpo` · `docker` &nbsp;·&nbsp; [demo](https://huggingface.co/spaces/Astro-Dude/citadel) &nbsp;·&nbsp; [source](https://github.com/Astro-Dude/citadel)</sub>

#### TypeAhead

search-as-you-type, built like it has to survive production. a redis cache sharded across 3 nodes on a consistent-hash ring, an in-memory trie serving top-K suggestions, a batched writer that collapses thousands of db writes into a handful.

benchmarked properly: p50, p95, p99.

<sub>`python` · `fastapi` · `redis` · `sqlite` &nbsp;·&nbsp; [source](https://github.com/dobbydobap/TypeAheadHLD)</sub>

#### Cadenza

a sales agent that haunts your google calendar, benevolently. thirty minutes before every meeting it researches the prospect on the live web and emails you a brief with cited sources.

nine google cloud services stitched together, zero manual invocation. it just shows up prepared, like you wish you did.

<sub>`next.js` · `gemini` · `cloud run` · `firestore` &nbsp;·&nbsp; [source](https://github.com/dobbydobap/Cadenza)</sub>

#### AutomationAgent

a poltergeist you can hire. it drives a real chromium browser with actual mouse and keyboard events, finds form fields through the accessibility tree, and streams every action and screenshot to a live dashboard.

so you can watch the ghost work.

<sub>`python` · `playwright` · `fastapi` · `docker` &nbsp;·&nbsp; [source](https://github.com/dobbydobap/AutomationAgent)</sub>

#### SPEED/TEST

an internet speed test that doesn't try to sell you a VPN. download, upload, ping, jitter, bufferbloat, measured against cloudflare's edge with zero backend and rendered on a hand-rolled SVG speedometer.

<sub>`react` · `vite` · `typescript` · `cloudflare pages` &nbsp;·&nbsp; [source](https://github.com/dobbydobap/speed.com)</sub>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:e8c0cd,100:c88da1&height=2" width="100%" alt="" />

### 🌸 evidence

**global top 6** · apple developer academy, italy

**top 100** · meta pytorch × scaler openenv hackathon

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:e8c0cd,100:c88da1&height=2" width="100%" alt="" />

### 🌸 equipment

`typescript` `python` `go` `java` `c++` `nestjs` `fastapi` `quarkus` `express` `react` `next.js` `websockets` `postgresql` `redis` `mongodb` `sqlite` `pytorch` `grpo` `gemini · claude · openai` `docker` `gcp` `cloudflare` `vercel` `linux`

<pre>
 /\_/\
( o.o )   
 &gt; ^ &lt;    
</pre>

<div align="center">

*if your codebase does something that can't be explained, i want to hear about it.*

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:e8c0cd,50:d9a3b5,100:c88da1&height=100&section=footer" width="100%" alt="footer" />
