# Ota Pre-release Pressure

Status: fork-only pre-release pressure. This is not an upstream pull request, endorsement, or
claim that PythiaLabs is governed by Ota.

## Inputs

- upstream revision: `17df87775c0d5407c07e86f278455d912ed51305`
- fork branch: `bobai/ota-pre-release-pressure`
- Ota source: Core `6fcffbdb551c2c452c47f9d0c4b83c607785960f`, reporting v1.6.27
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
or any external mutation. It is non-blocking by design and exists to pressure Ota's declaration,
diagnostic, and conservative discovery surfaces before the v1.6.27 release.

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
