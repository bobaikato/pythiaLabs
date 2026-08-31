# Ota Pre-release Pressure

Status: fork-only pre-release pressure. This is not an upstream pull request, endorsement, or
claim that PythiaLabs is governed by Ota.

## Inputs

- upstream revision: `17df87775c0d5407c07e86f278455d912ed51305`
- fork branch: `bobai/ota-pre-release-pressure`
- Ota source: Core `52b53517f312b8dba66bd4a4dce53d96350bff69`, reporting v1.6.27
- Ota bootstrap: contract-owned, immutable `git_rev`

## Evidence Matrix

| Job | Surface | Expected evidence | Not proved |
| --- | --- | --- | --- |
| Declaration and discovery | `ota validate`, `ota tasks`, `ota doctor`, and conservative `ota detect` on Ubuntu | Contract shape, lane posture, readiness observations, and candidate evidence | Task execution or agent authority |
| Native Ubuntu | All selected non-credentialed lanes through `ota run` | Linux execution output and per-lane exit status | Provider calls, merge, or credentialed CAEP |
| Native macOS | The same selected native lanes | macOS compatibility evidence for the declared contributor surface | Container parity or external authority |
| Native Windows | The same selected native lanes | Windows compatibility evidence for the declared contributor surface | Non-Windows container parity or external authority |
| Linux container | MCP smoke and site build through `--mode container` | Selected Node-container context and retained command output | Pythia Dockerfile, multi-language image, or image provenance beyond the pinned digest |

The matrix is fork-only and non-blocking: each job uses `continue-on-error: true`, so it cannot
affect upstream CI badges. Failures remain visible and retained. Credentialed provider calls,
GitHub merge, Gmail/GitHub communication, and the Liminal multi-repository lifecycle remain
excluded.

## Execution Matrix

The native matrix observes the `core`, `mcp`, `worker`, and `site` workflow previews, then runs
the selected non-credentialed tasks through `ota run` on Ubuntu, macOS, and Windows. It retains
each lane's text output and exit status. Workflow previews are expected to remain blocked until a
crossing authority exists; they are evidence of refusal, not green execution gates.

| Lane family | Included execution | Hydration posture | Deliberate limit |
| --- | --- | --- | --- |
| Elixir core | format and test | Explicit reviewed Mix/Hex setup tasks | Mix/Hex is not yet an Ota typed hydration source |
| MCP | Node syntax and smoke | No package hydration; smoke owns a fake Mix executable | Does not prove a real MCP host loaded or enforced Pythia |
| Rust worker | release build and test | Explicit reviewed `cargo fetch` task | Current Cargo resolution is mutable because no lockfile is retained |
| Site | `npm ci`, build, and format check | Typed npm CI hydration in `site/` | Does not prove Pages deployment or Lighthouse publication |
| Python conformance | Action Envelope, VCE, ACI, and local CAEP verified-evidence tests | Explicit reviewed `python -m pip install` tasks | Excludes credentialed CAEP provider calls and the authority-boundary pilot |

The native execution matrix does not run provider calls, GitHub merge, Gmail/GitHub communication,
or the Liminal multi-repository lifecycle. It is distinct from the Ota-owned container matrix below.

## Ota-Owned Container Matrix

The Linux container job uses the contract's `node` execution context, pinned to
`node:20-bookworm@sha256:cacf10e99285cbbc891452e31249c1b5ec3ba225f40028fae946b75aeaf1b66a`
for `linux/amd64`, invokes Ota with `--mode container --stream`, and retains the child command
output with Ota's selected-context summary.

| Lane | Closure exercised | What the artifact witnesses | Not proved |
| --- | --- | --- | --- |
| MCP smoke | syntax dependencies plus smoke harness | Ota selected the container context and executed the complete Node closure | Real Mix, MCP-host loading, or provider enforcement |
| Site build | typed `npm ci` in `site/` plus `npm run build` | Ota preserved the declared working directory and hydrated/build state through the container closure | Pages deployment, formatting conformance, or image provenance beyond the pinned digest |

This does **not** use or validate Pythia's Dockerfile. The Dockerfile currently installs Rust through
a mutable network bootstrap and remains outside Ota container authority. The matrix also does not
prove container isolation beyond Ota's declared execution behavior, agent authority, provider
contact, arbitrary repository immutability, or non-Linux container portability.

## Assumptions And Boundaries

- The declared Elixir, MCP, worker, and site commands are contributor-lane proposals, not proof
  that their prerequisite hydration, toolchains, or effects are safe for an agent.
- Credentialed CAEP providers, GitHub merge behavior, Gmail/GitHub synchronization, and the
  Liminal multi-repository lifecycle are intentionally excluded.
- Pythia `ALLOW` remains input evidence only. It grants no Ota execution authority.
- MCP files and smoke output do not prove a real host loaded or enforced Pythia.
- The container matrix proves only the declared Linux Node contexts and selected closures. It does
  not establish Pythia's Dockerfile, a multi-language image, or macOS/Windows container parity.
- A successful fork workflow is pre-release Ota pressure evidence only. It does not replace a
  released-binary run, independently administered policy, provider attestation, or Aleksei's
  written review.

After Ota v1.6.27 is released, the proposed upstream draft PR must replace the bootstrap source
with the released version and add a separate review matrix that binds the final fork revision,
workflow URL, retained artifacts, exercised assumptions, and unproved boundaries.
