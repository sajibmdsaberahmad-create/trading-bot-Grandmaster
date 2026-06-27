# M. A. Halim

**M. A. Halim** is your own AI model — not Groq, Gemini, Claude, or Ollama.

HANOON is the trading **body**. Halim is the **mind** that grows from numeric students today into a frontier model tomorrow (generative, calculative, coding, and more).

## Today (newborn phase)

Halim runs as **owned students on disk**:

| Student | File | Role |
|---------|------|------|
| Reflex | `ppo_trader.zip` | Millisecond trade policy |
| Enter/skip | `teacher_proxy.joblib` | Distilled decisions |
| Scanner | `scalper_weights.json` | Heuristic tuning |
| Memory | `council_training_dataset.jsonl` | Training gold for future Halim LM |

**No external LLM required** when native mode is on:

```bash
export HALIM_NATIVE=true
./scripts/halim_native_replay.sh
```

## Separate model repo

The frontier home lives in **`halim/`** (designed as its own git repo):

```bash
cd halim
python scripts/sync_from_tradingbot.py --source ..
git init   # when ready: github.com/YOU/halim
```

See [halim/README.md](../halim/README.md) and [halim/ROADMAP.md](../halim/ROADMAP.md).

## Growth path

```
newborn  → PPO + proxy (now, M2 8GB)
toddler  → first Halim transformer on trading data
child    → + code, math, reasoning
adult    → Halim on your hardware, zero API
frontier → full generative / calculative / coding model
```

## Identity files

- `models/halim_identity.json` — birth, phase, philosophy
- `models/halim_manifest.json` — full status (updated each evolution)
- `docs/BRAIN_DEVELOPMENT_LOG.md` — human timeline (git)

## Halim as self-developer

Halim mutates bounded params, self-improves, syncs `halim/`, and **auto-pushes git** (default on):

```bash
./scripts/halim_developer.sh       # manual: mutate + improve + push now
export HALIM_AUTO_PUSH=true        # embedded watcher (default)
export GIT_PUSH_DURING_SESSION=true
```

Log: `models/halim_developer.jsonl`

Requires `.env`: `GITHUB_TOKEN` + `GITHUB_HANOON_REPO`

## Frontier + guardrails

Halim is **not trading-only**. Roadmap: generative, coding, math, agents, web/API tools, multimodal → **frontier class**.

All external actions gated by `core/halim_guardrails.py`:

- **Kill switch:** `./scripts/halim_kill_switch.sh` or `HALIM_KILL_SWITCH=true`
- **Constitution:** `models/halim_constitution.json`
- **Audit:** `models/halim_guardrail_audit.jsonl`

Full policy: [HALIM_GUARDRAILS.md](HALIM_GUARDRAILS.md)

APIs and live internet = **tools Halim consumes**, not Halim's brain (owned weights are the brain).

### Google AI search (enabled)

Halim may **google** a topic and read only the **public AI Overview** box on Google Search (like AI mode in the browser) — **not** the Gemini API, **not** visiting result links:

```bash
./scripts/halim_google_search.sh "what is an egg"
```

- Max **50 searches/day**
- Only `google.com/search?q=...`
- `links_followed: 0` always

## Related

- [OWNED_BRAIN.md](OWNED_BRAIN.md) — technical flywheel (evolution, git, Telegram)
