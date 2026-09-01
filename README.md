<img src="https://capsule-render.vercel.app/api?type=waving&color=0:ffafcc,50:ff8fab,100:fb6f92&height=160&section=header&text=varshitha%20sai%20kolupuri&fontSize=38&fontColor=ffffff&fontAlignY=35&desc=distributed%20systems%20%C2%B7%20ai%20agents%20%C2%B7%20things%20that%20go%20bump%20in%20the%20runtime&descSize=14&descAlignY=58&animation=fadeIn" width="100%" alt="header" />

<div align="center">

cs @ scaler school of technology + bits pilani · bengaluru

<a href="https://linkedin.com/in/varshitha-kolupuri"><img src="https://img.shields.io/badge/linkedin-fb6f92?style=for-the-badge&logo=linkedin&logoColor=white" alt="linkedin" /></a>&nbsp;
<a href="https://rank-forge-web.vercel.app/"><img src="https://img.shields.io/badge/rankforge_%E2%80%94_live-ff8fab?style=for-the-badge&logo=vercel&logoColor=white" alt="rankforge" /></a>&nbsp;
<a href="https://speedcheck-1mi.pages.dev/"><img src="https://img.shields.io/badge/speed_test_%E2%80%94_live-ffafcc?style=for-the-badge&logo=cloudflare&logoColor=white" alt="speed test" /></a>

</div>

<br/>

i build backend systems and ai agents — the kind of software where the hard part is invisible and the bugs only appear after midnight. conveniently, that's when i start working.

off the clock i'm into paranormal investigation, which turns out to be the same job as debugging: something impossible happened, nobody witnessed it, and the logs are useless. i believe every haunting has a root cause. so far, it has always been a race condition.

also: cats. 🐈‍⬛

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:ffafcc,100:fb6f92&height=2" width="100%" alt="" />

### 🌸 field work

other people's codebases, other people's hauntings. **10 PRs merged across 7 upstream projects**, two of them cncf graduated — plus node.js core.

<ul>
  <li><b>apicurio registry</b> — <a href="https://github.com/Apicurio/apicurio-registry/pull/8684">#8684</a> merged. then found <a href="https://github.com/Apicurio/apicurio-registry/issues/8926">#8926</a>: MCP tool annotations were being validated against the wrong schema entirely, so not one of the four hints anyone wrote was ever checked. <b>fix merged</b> — <a href="https://github.com/Apicurio/apicurio-registry/pull/9055">#9055</a>.</li>
  <li><b>opentelemetry</b> <sub>go compile-time instrumentation</sub> — <a href="https://github.com/open-telemetry/opentelemetry-go-compile-instrumentation/pull/856">#856</a> merged. then found <a href="https://github.com/open-telemetry/opentelemetry-go-compile-instrumentation/issues/886">#886</a>: struct rules cheerfully matched things that were not structs, and inside a grouped <code>type</code> block a field could land on a struct nobody named. <b>fix merged</b> — <a href="https://github.com/open-telemetry/opentelemetry-go-compile-instrumentation/pull/887">#887</a>.</li>
  <li><b>kubeflow pipelines</b> — <a href="https://github.com/kubeflow/pipelines/pull/13780">#13780</a> merged: the python sdk was quietly adding <code>--trusted-host</code> to every pip call. opt-in now.</li>
  <li><b>microsoft/vscode</b> — <a href="https://github.com/microsoft/vscode/pull/324571">#324571</a> and <a href="https://github.com/microsoft/vscode/pull/324734">#324734</a> merged in v1.129.0: a rerun-last-task regression, and a pinned tab that refused to let go when dragged.</li>
  <li><b>nodejs/node</b> — <a href="https://github.com/nodejs/node/pull/64365">#64365</a> &nbsp;·&nbsp; <b>fedora-infra/bodhi</b> — <a href="https://github.com/fedora-infra/bodhi/pull/6121">#6121</a> &nbsp;·&nbsp; <b>nansen-cli</b> — <a href="https://github.com/nansen-ai/nansen-cli/pull/465">#465</a></li>
  <li><sub>in review: vscode <a href="https://github.com/microsoft/vscode/pull/326451">#326451</a> · <a href="https://github.com/microsoft/vscode/pull/326447">#326447</a> · <a href="https://github.com/microsoft/vscode/pull/325654">#325654</a> · <a href="https://github.com/microsoft/vscode/pull/324682">#324682</a> · <a href="https://github.com/microsoft/vscode/pull/324369">#324369</a> &nbsp;·&nbsp; kserve <a href="https://github.com/kserve/kserve/pull/5909">#5909</a> &nbsp;·&nbsp; textualize/textual <a href="https://github.com/Textualize/textual/pull/6631">#6631</a> · <a href="https://github.com/Textualize/textual/pull/6630">#6630</a></sub></li>
</ul>

the half i like best: find it myself, report it, then fix it.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:ffafcc,100:fb6f92&height=2" width="100%" alt="" />

### 🌸 case files

#### [RankForge ↗](https://rank-forge-web.vercel.app/)

a competitive programming platform, built end to end — 95+ problems, an async code judge that speaks 10 languages, real-time verdicts over websockets, elo ratings, plagiarism detection.

the favourite child: a custom segment tree that can replay the leaderboard at any minute of any past contest. time travel, but auditable.

<sub>`typescript` · `nestjs` · `next.js` · `postgresql` · `redis` · `bullmq` &nbsp;—&nbsp; [source](https://github.com/dobbydobap/RankForge)</sub>

#### [Citadel ↗](https://huggingface.co/spaces/Astro-Dude/citadel)

security incident response, run by two LLM agents keeping each other honest — a Commander proposes actions, an Oversight agent approves, revises, or vetoes.

both agents trained with GRPO reinforcement learning on qwen2.5-3b. placed top 100 at the meta pytorch × scaler openenv hackathon.

<sub>`python` · `pytorch` · `grpo` · `docker` &nbsp;—&nbsp; [source](https://github.com/Astro-Dude/citadel)</sub>

#### [TypeAhead](https://github.com/dobbydobap/TypeAheadHLD)

search-as-you-type, built like it has to survive production — a redis cache sharded across 3 nodes on a consistent-hash ring, an in-memory trie serving top-K suggestions, a batched writer that collapses thousands of db writes into a handful.

benchmarked properly: p50, p95, p99.

<sub>`python` · `fastapi` · `redis` · `sqlite`</sub>

#### [Cadenza](https://github.com/dobbydobap/Cadenza)

a sales agent that haunts your google calendar, benevolently. thirty minutes before every meeting, it researches the prospect on the live web and emails you a brief with cited sources.

nine google cloud services stitched together, zero manual invocation. it just shows up, prepared — like you wish you did.

<sub>`next.js` · `gemini` · `cloud run` · `firestore`</sub>

#### [AutomationAgent ↗](https://varshitha2007899-automationagent.hf.space/)

a poltergeist you can hire. it drives a real chromium browser with actual mouse and keyboard events, finds form fields through the accessibility tree, and streams every action and screenshot to a live dashboard.

so you can watch the ghost work.

<sub>`python` · `playwright` · `fastapi` · `docker` &nbsp;—&nbsp; [source](https://github.com/dobbydobap/AutomationAgent)</sub>

#### [SPEED/TEST ↗](https://speedcheck-1mi.pages.dev/)

an internet speed test that doesn't try to sell you a VPN. download, upload, ping, jitter, bufferbloat — measured against cloudflare's edge with zero backend, rendered on a hand-rolled SVG speedometer.

<sub>`react` · `vite` · `typescript` · `cloudflare pages` &nbsp;—&nbsp; [source](https://github.com/dobbydobap/speed.com)</sub>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:ffafcc,100:fb6f92&height=2" width="100%" alt="" />

### 🌸 evidence

<ul>
  <li><b>global top 6</b> — apple developer academy, italy</li>
  <li><b>top 100</b> — meta pytorch × scaler openenv hackathon</li>
</ul>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:ffafcc,100:fb6f92&height=2" width="100%" alt="" />

### 🌸 equipment

`typescript` `python` `go` `java` `c++` `nestjs` `fastapi` `quarkus` `express` `react` `next.js` `websockets` `postgresql` `redis` `mongodb` `sqlite` `pytorch` `grpo` `gemini · claude · openai` `docker` `gcp` `cloudflare` `vercel` `linux`

<pre>
 /\_/\
( o.o )   
 &gt; ^ &lt;    
</pre>

<div align="center">

*if your codebase does something that can't be explained — i want to hear about it.*

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:ffafcc,50:ff8fab,100:fb6f92&height=100&section=footer" width="100%" alt="footer" />
