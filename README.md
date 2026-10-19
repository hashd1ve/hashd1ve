# Manrique

Data scientist and AI engineer. I work with financial and on-chain data, and I build with LLMs: serving them on
local hardware, agents and developer tools, and small experiments on how they work inside.

[X / Twitter: @hashd1ve](https://x.com/hashd1ve)

## What I do

- **Data science** · financial and on-chain data: analytics, research tools and data products.
- **AI engineering** · LLM serving and inference tuning (SGLang, TensorFold, EXL3 on NVIDIA DGX Spark), agents and
  coding-agent tooling, retrieval and evaluation.

## Open source

- **[SGLang](https://github.com/sgl-project/sglang)** · [#37068](https://github.com/sgl-project/sglang/pull/37068) (merged):
  a file-backed PLE table for unified-memory devices, so Qwen3.8-Flash-Next fits on one DGX Spark.
- **[edgartools](https://github.com/dgunning/edgartools)** · [4 merged PRs](https://github.com/dgunning/edgartools/pulls?q=is%3Apr+author%3Ahashd1ve+is%3Amerged) to the SEC EDGAR library.
- **[terax-ai](https://github.com/crynta/terax-ai)** · [1 merged PR](https://github.com/crynta/terax-ai/pulls?q=is%3Apr+author%3Ahashd1ve+is%3Amerged).
- **TensorFold, DeepSeek-V4.1 engine** · [#26](https://github.com/bertholomus/TensorFold/pull/26) and
  [#24](https://github.com/bertholomus/TensorFold/pull/24) (merged): a prompt prefix shared by two conversations no
  longer discards the first one's kept state; [#28](https://github.com/bertholomus/TensorFold/pull/28) and
  [#29](https://github.com/bertholomus/TensorFold/pull/29): prompts with images resume from cache, and long prompts
  no longer stop other sessions.

## Projects

- **Inference** · [deepseek-v4.1-flash-2x-dgx-spark](https://github.com/hashd1ve/deepseek-v4.1-flash-2x-dgx-spark)
  (DeepSeek-V4.1-Flash on two DGX Sparks for agent work: 1M context, 4 streams, the engine fixes it needed),
  [qwen38-flash-next-one-dgx-spark](https://github.com/hashd1ve/qwen38-flash-next-one-dgx-spark),
  [apodex-1.1-mini-one-dgx-spark](https://github.com/hashd1ve/apodex-1.1-mini-one-dgx-spark),
  [yue2-dgx-spark](https://github.com/hashd1ve/yue2-dgx-spark)
- **Agents and tools** · [agent-charts](https://github.com/hashd1ve/agent-charts) (charts for coding agents in the
  terminal), [geo-audit-skill](https://github.com/hashd1ve/geo-audit-skill)
- **Research** · [operator-universality](https://github.com/hashd1ve/operator-universality) (do independently trained
  LMs share a state-update operator?), [nanogpt-experiments](https://github.com/hashd1ve/nanogpt-experiments)
