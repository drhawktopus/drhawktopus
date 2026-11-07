# Nick Crowley

**Systems & AI engineer.** I build and run AI systems end to end on hardware I own: a local LLM orchestrator with per-user RAG and governance, a 32B model fine-tuned on a 24 GB consumer GPU, a self-engineering deploy loop under human gates, and distributed evaluation across a heterogeneous fleet.

### → Portfolio: **[portfolio.hawktopus.org](https://portfolio.hawktopus.org)**

The full write-ups — architecture, evaluation methodology, reliability investigations, and the operating doctrine the lab's AI agents run under — live there.

## What's public here

The lab's code isn't all public yet. I'm working toward releasing the orchestration so you can rebuild it on your own hardware. The person models and the identities that go with them stay home. For now, these are the pieces I've opened up:

- **[home-ai](https://github.com/drhawktopus/home-ai)** — *Home AI without breaking the bank*: the whole lab as one local assistant across everyday PCs, cast-off gear and eleven tablets, with every result measured, including what didn't work. Also on [the blog](https://blog.hawktopus.org/home-ai).
- **[flux2-32b-qlora-rocm-windows](https://github.com/drhawktopus/flux2-32b-qlora-rocm-windows)** — a working recipe, config, and patches for training a 32B FLUX.2 [dev] QLoRA on a single 24 GB AMD RX 7900 XTX, native ROCm on Windows. A hardware, OS, and framework combination with no published recipe I could find at that model size.
- **Upstream driver report — [ROCm/TheRock #6824](https://github.com/ROCm/TheRock/issues/6824)** — I investigated a silent GPU compute stall that every Windows-side health check reported as normal, narrowed it to its best-supported explanation, a queue-arbitration collision in the on-GPU firmware scheduler (AMD's MES), and filed the repro, probe data, and mitigation upstream. It isn't a closed case.
- **[fellowship-gauntlet-results](https://github.com/drhawktopus/fellowship-gauntlet-results)** — the full result matrix from a 688-cell model-by-hardware evaluation across an 11-node ARM cluster: every cell's outcome, per-model and per-lane scores, reliability, and timings. The methodology is [written up here](https://portfolio.hawktopus.org/gauntlet).

More of the work is written up on the [portfolio](https://portfolio.hawktopus.org) than is open-sourced here so far.

## How I work

I design and operate the systems, and I direct AI coding agents that write most of the implementation. I read and review Python, PowerShell, and Bash fluently — enough to catch when an agent is stuck, rebuilding a mechanism the lab already has, or arguing from a guess — and nothing reaches the live system until I have verified it. The [operating doctrine](https://portfolio.hawktopus.org/doctrine) those agents run under is twenty-one failure classes, each anchored to a real incident I caught: my judgment about the systems, written down and enforced in the tooling.

## Currently

Field-service operations supervisor for a regional technician team, and the architect and operator of an independent engineering lab at home.

**Reach me:** [nickcrowley97@gmail.com](mailto:nickcrowley97@gmail.com)
