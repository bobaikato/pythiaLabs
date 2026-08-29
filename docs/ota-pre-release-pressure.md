# Ota Pre-release Pressure

Status: fork-only pre-release pressure. This is not an upstream pull request, endorsement, or
claim that PythiaLabs is governed by Ota.

## Inputs

- upstream revision: `17df87775c0d5407c07e86f278455d912ed51305`
- fork branch: `bobai/ota-pre-release-pressure`
- Ota source: Core `cd99c9abd2c0225b454371e897eca2486319db26`, reporting v1.6.27
- Ota bootstrap: contract-owned, immutable `git_rev`

## Evidence Matrix

| Surface | Fork workflow exercise | Expected evidence | Not proved |
| --- | --- | --- | --- |
| Contract shape | `ota validate --json` | Validation result and exact Ota source version | Task execution or agent authority |
| Declared lane posture | `ota tasks --json` | Four distinct, non-agent-safe contributor lanes | Hydration, runtime availability, or successful task behavior |
| Readiness diagnosis | `ota doctor --json` | Current blockers and warnings as Ota observes them | Repository-wide readiness or remediation |
| Conservative CI discovery | `ota detect --candidate-out ... --json` | Candidate, source inventory, evidence, closure, and unresolved findings | Candidate application, execution, or promotion to agent-safe authority |
| Artifact retention | `actions/upload-artifact` | Machine-readable outputs and exit statuses for the exact fork run | Receipt, archive, assurance, or third-party attestation |

The workflow does not run `ota run`, `ota up`, Mix, Cargo, Node, Python, provider calls, a merge,
or any external mutation. It is separate and non-required, but failures remain visible. It exists to
pressure Ota's declaration, diagnostic, and conservative discovery surfaces before the v1.6.27
release.

## Execution Matrix

`.github/workflows/ota-pre-release-execution-pressure.yml` is a separate visible fork-only matrix.
It observes the `core`, `mcp`, `worker`, and `site` workflow previews, then runs the selected
non-credentialed tasks through `ota run` and retains each lane's text output and exit status. The workflow
previews are expected to remain blocked until a crossing authority exists; they are evidence of
that refusal, not green execution gates.

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

`.github/workflows/ota-pre-release-container-pressure.yml` is a separate Linux-only, fork-only
matrix. It uses the contract's `node` execution context, pinned to
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
