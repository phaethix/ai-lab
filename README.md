# ai-lab

Hands-on experiments with open-weight LLMs: inference pipelines, architecture comparisons, and the underlying math.

| Path | Contents |
| --- | --- |
| `notebooks/qwen3-0.6b-inference.ipynb` | Qwen3-0.6B inference with `transformers` |
| `notebooks/gemma3-1b-inference.ipynb` | Gemma-3-1B inference, architecture contrast |
| `notebooks/linear-algebra.ipynb` | Linear systems and eigendecomposition |
| `src/ai_lab/` | Reusable package code |

## Getting started

Requires Python 3.13+ and [uv](https://docs.astral.sh/uv/).

```bash
uv sync
uv run jupyter lab
```

Runs on CPU or Apple Silicon (MPS). Weights download on first run; set `HF_ENDPOINT` to use a mirror:

```bash
export HF_ENDPOINT=https://hf-mirror.com
```

## Contributing

See [AGENTS.md](AGENTS.md).

## License

MIT. See [LICENSE](LICENSE).
