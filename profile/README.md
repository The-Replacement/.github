# The-Replacement

A private internet radio, built out loud.

The station streams from a small always-on box in the Sierras de los
Comechingones, Argentina. The music is not curated: it is **composed by a
program from a seed**. Same seed, same machine, same audio — byte for byte. The
voice between tracks is a local text-to-speech model, not a recording.

Three ideas hold the org together:

1. **Determinism over taste.** A track is a hashable plan rendered to audio. If
   it cannot be reproduced, it does not belong on the stream.
2. **One door.** The stream, the player and the camera are reachable only
   through a token-gated proxy. Nothing else publishes a port.
3. **The gates decide, not the author.** Measurements (loudness, latency,
   config assertions, mutation tests) run in CI. A green check means something
   was measured, not that someone was in a hurry.

## Repositories

| Repository | What it is |
|---|---|
| [radio](https://github.com/The-Replacement/radio) | The station: Liquidsoap + Icecast + Caddy + MediaMTX + the player page, orchestrated with Docker Compose. |
| [indiegenerator](https://github.com/The-Replacement/indiegenerator) | The composer: batch, offline, deterministic music generation (DSP in Python) that fills the library. |
| [infra](https://github.com/The-Replacement/infra) | Deploy, monitoring, runbooks and backup for the host. |
| [n3rv](https://github.com/The-Replacement/n3rv) | The active engineering harness: agent memory, skills, subagent dispatch, and the SDD pipeline. |

## How work happens here

Feature work runs through a spec-driven pipeline — explore, propose, spec,
design, tasks, apply, verify, archive — tracked on the
[The-Replacement Roadmap](https://github.com/orgs/The-Replacement/projects/1)
board. Commits are conventional. Every claim in a document is expected to be
checkable, and the gates that check them live next to the code they judge.

## Listening

The station is private. Access is by invitation link.
