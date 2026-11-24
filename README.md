# Manrique

AI engineer. I make large models run fast on small hardware, I train small models that companies pay for, and I open
models up to see how they work. My lab is two NVIDIA DGX Sparks (GB10, Blackwell) linked at 200 Gb/s over RoCE.

Every speedup here ships with its check: the same perplexity, or output identical bit for bit. When I get something
wrong, the correction goes at the top of the README.

[X / Twitter: @hashd1ve](https://x.com/hashd1ve)

## Highlights

- **[Inkling 2 Mini on 2× DGX Spark](https://github.com/hashd1ve/inkling-2-mini-2x-dgx-spark)** · **54.1 → 101.1
  tok/s** on agent steps (one Spark with the official recipe → two Sparks at vLLM TP=2), from three exact patches:
  adaptive speculative verification for Inkling's drafter, an RDMA all-reduce over RoCE (8.7 µs against NCCL's 46 µs,
  same sum bit for bit) and a 12-bit bf16 GEMV that rebuilds the same weights (1.23–1.32× on those reads).
  Perplexity unchanged.
- **[SGLang #37068](https://github.com/sgl-project/sglang/pull/37068) (merged)** · a file-backed PLE table for
  unified-memory devices, so [Qwen3.8-Flash-Next](https://github.com/hashd1ve/qwen38-flash-next-one-dgx-spark) serves
  a 126.0 GiB checkpoint on a 121.63 GiB machine, across its full 262k context.
- **[Apodex-1.1-mini](https://github.com/hashd1ve/apodex-1.1-mini-one-dgx-spark)** · **+33% decode on code, +43% on
  prose** from quantising one tensor, found by counting which bytes a decode step actually reads. No kernel work.
- **[DeepSeek-V4.1-Flash on 2× DGX Spark](https://github.com/hashd1ve/deepseek-v4.1-flash-2x-dgx-spark)** · the full
  1M-token window and 4 streams for daily agent work; five fixes merged into the TensorFold engine.
- **A model I sell** · a document anonymiser: small multilingual encoders fine-tuned on synthetic data I generate with
  LLMs, running entirely in the browser on a WebGPU runtime I wrote, so documents never leave the machine. Closed
  source; sold to companies and in daily use.

## Training and research

- **[nanogpt-experiments](https://github.com/hashd1ve/nanogpt-experiments)** · fully instrumented runs on how LLMs
  learn: training dynamics, optimizers, generalization and the structure of the weights. One variable at a time, with
  controls, and the negatives recorded.
- **[operator-universality](https://github.com/hashd1ve/operator-universality)** · do independently trained LMs share
  an executable state-update operator? A basis-free, causally validated comparison across Pythia, GPT-2, GPT-Neo and
  OPT (working draft).

## Open source contributions

- **[SGLang](https://github.com/sgl-project/sglang)** · [#37068](https://github.com/sgl-project/sglang/pull/37068)
  (merged): the file-backed PLE table above.
- **TensorFold, DeepSeek-V4.1 engine** · [#24](https://github.com/bertholomus/TensorFold/pull/24),
  [#25](https://github.com/bertholomus/TensorFold/pull/25), [#26](https://github.com/bertholomus/TensorFold/pull/26),
  [#28](https://github.com/bertholomus/TensorFold/pull/28) and [#29](https://github.com/bertholomus/TensorFold/pull/29)
  (merged): shared prompt prefixes keep their state, prompts with images resume from cache, and long prompts no
  longer stall the other sessions.
- **[edgartools](https://github.com/dgunning/edgartools)** · [4 merged PRs](https://github.com/dgunning/edgartools/pulls?q=is%3Apr+author%3Ahashd1ve+is%3Amerged) to the SEC EDGAR library.
- **[terax-ai](https://github.com/crynta/terax-ai)** · [1 merged PR](https://github.com/crynta/terax-ai/pulls?q=is%3Apr+author%3Ahashd1ve+is%3Amerged).

## More projects

- **Inference** · [yue2-dgx-spark](https://github.com/hashd1ve/yue2-dgx-spark) (full songs with an editable score, 29%
  faster with byte-identical output),
  [qwen38-flash-next-one-dgx-spark](https://github.com/hashd1ve/qwen38-flash-next-one-dgx-spark),
  [apodex-1.1-mini-one-dgx-spark](https://github.com/hashd1ve/apodex-1.1-mini-one-dgx-spark)
- **Data** · [openrouter-pulse](https://github.com/hashd1ve/openrouter-pulse) (what the LLM market is actually doing,
  from OpenRouter's public data). By day I also do data science on financial and on-chain data.
- **Agents and tools** · [agent-charts](https://github.com/hashd1ve/agent-charts) (charts for coding agents in the
  terminal), [geo-audit-skill](https://github.com/hashd1ve/geo-audit-skill)
