<p align="center">
  <img src="autor3search.png" alt="" width="96" height="96">
</p>

<h1 align="center">autor3search</h1>

<p align="center">
  <em>Autoresearch for your codebase. Point your coding agent at your repo, come back to faster code.</em><br>
  <a href="https://autor3search.dev">autor3search.dev</a>
</p>

---

Your agent proposes an optimization. A frozen harness measures it. The verdict is
**KEEP** or **DISCARD** — every experiment measured, nothing taken on faith.

Tests are frozen and restored before every run. The metric lives in a compiled
binary the agent cannot reach. Noise is discarded, regressions are rejected.
Accepted changes land as one commit each; every experiment, including the
failures, lands as one row in `results.tsv`. Stop the run whenever you like —
nothing already accepted is thrown away.

## Pick your language

| | repository | install | status |
| --- | --- | --- | --- |
| **Go** | [`autor3search/go`](https://github.com/autor3search/go) | `go install …@latest` | early but working |
| **TypeScript** | [`autor3search/typescript`](https://github.com/autor3search/typescript) | `npm install --save-dev autor3search-typescript` | on npm · measures your `*.bench.ts` benchmarks |
| **JavaScript** | [`autor3search/javascript`](https://github.com/autor3search/javascript) | `npm install -g autor3search-javascript` | on npm · standalone, measures vitest benchmarks |
| **Python** | [`autor3search/python`](https://github.com/autor3search/python) | `uv tool install autor3search-python` | early but working — validated on humanize |
| **Java** | [`autor3search/java`](https://github.com/autor3search/java) | release jar + launcher | early but working — validated on org.json |
| **C#** | [`autor3search/csharp`](https://github.com/autor3search/csharp) | `dotnet tool install -g autor3search-csharp` | on nuget · early but working |
| **Rust** | [`autor3search/rust`](https://github.com/autor3search/rust) | `cargo install --locked autor3search-rust` | on crates.io · measures with criterion |

Same loop, same rules in every port. They differ only in how the harness installs
and what it must not touch.

## Start a run

Copy the agent prompt for your language — the `## Start here` block of that repo's
README, or the whole set at
[autor3search.dev/llms-full.txt](https://autor3search.dev/llms-full.txt) — and
paste it into your coding agent from inside the repository you want to optimize.

## Does it work?

[One overnight run, p<0.0001](https://github.com/autor3search/go/blob/main/docs/case-study.md).
Real measurements, never illustrations. Validated on go-humanize, mapstructure
and google/uuid.

---

MIT. Takes after [karpathy/autoresearch](https://github.com/karpathy/autoresearch).
