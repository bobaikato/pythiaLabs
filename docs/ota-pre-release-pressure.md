# Ota Pre-release Pressure

Status: fork-only pre-release pressure. This is not an upstream pull request, endorsement, or
claim that PythiaLabs is governed by Ota.

## Inputs

- upstream revision: `17df87775c0d5407c07e86f278455d912ed51305`
- fork branch: `bobai/ota-pre-release-pressure`
- Ota source: Core `6fcffbdbee322d56f1abdb0b163f5b64f8ab29c5`, reporting v1.6.27
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
non-credentialed tasks through `ota run --json` and retains one result per lane. The workflow
previews are expected to remain blocked until a crossing authority exists; they are evidence of
that refusal, not green execution gates.

| Lane family | Included execution | Hydration posture | Deliberate limit |
| --- | --- | --- | --- |
| Elixir core | format and test | Explicit reviewed Mix/Hex setup tasks | Mix/Hex is not yet an Ota typed hydration source |
| MCP | Node syntax and smoke | No package hydration; smoke owns a fake Mix executable | Does not prove a real MCP host loaded or enforced Pythia |
| Rust worker | release build and test | Explicit reviewed `cargo fetch` task | Current Cargo resolution is mutable because no lockfile is retained |
| Site | `npm ci`, build, and format check | Typed npm CI hydration in `site/` | Does not prove Pages deployment or Lighthouse publication |
| Python conformance | Action Envelope, VCE, ACI, and local CAEP verified-evidence tests | Explicit reviewed `python -m pip install` tasks | Excludes credentialed CAEP provider calls and the authority-boundary pilot |

The execution matrix does not run Docker/container mode, provider calls, GitHub merge, Gmail/GitHub
communication, or the Liminal multi-repository lifecycle. Docker remains a separately declared
future pressure surface because the current image build installs mutable Rust and does not yet have
an Ota-reviewed container execution boundary.

## Assumptions And Boundaries

- The declared Elixir, MCP, worker, and site commands are contributor-lane proposals, not proof
  that their prerequisite hydration, toolchains, or effects are safe for an agent.
- Credentialed CAEP providers, GitHub merge behavior, Gmail/GitHub synchronization, and the
  Liminal multi-repository lifecycle are intentionally excluded.
- Pythia `ALLOW` remains input evidence only. It grants no Ota execution authority.
- MCP files and smoke output do not prove a real host loaded or enforced Pythia.
- A successful fork workflow is pre-release Ota pressure evidence only. It does not replace a
  released-binary run, independently administered policy, provider attestation, or Aleksei's
  written review.

After Ota v1.6.27 is released, the proposed upstream draft PR must replace the bootstrap source
with the released version and add a separate review matrix that binds the final fork revision,
workflow URL, retained artifacts, exercised assumptions, and unproved boundaries.
