# Run record guide

A result should be traceable to the exact code, inputs and method that produced it. This is a manual documentation format, not an implemented execution or recording API.

## Minimum record for every computational run

| Field | Required meaning |
|---|---|
| Run ID | Unique immutable identifier; never reuse after inputs or code change |
| Experiment ID | Link to the experiment definition and its revision |
| Timestamp | Start/end timestamps with timezone, preferably UTC |
| Status | Completed, failed, interrupted or invalid; retain failed attempts |
| Code provenance | Git commit plus dirty state and a patch/snapshot for uncommitted changes; a commit alone is insufficient |
| Software versions | Application, language, dependencies, environment/lockfile and relevant platform details |
| Model provenance | Model/tool name, version, external data or model artifacts and their exact revisions |
| System/specimen | Complete definition, units and relevant reference conventions |
| Operating conditions | Complete state and environmental inputs, units and sources |
| Configuration | All effective settings, defaults, tolerances and discretisation where applicable |
| Input parameters | Independent and controlled values, units, ranges and sampling plan revision |
| Derived parameters | Values, units, definitions and reference conventions used |
| Warnings | Diagnostic messages, convergence information and rejected inputs |
| Validity flags | In/out/unknown validity domain and interpolation/extrapolation status, with reasons |
| Randomness | Seed, generator and sampling configuration where relevant; otherwise explicitly not applicable |
| Outputs | Quantities, units, raw results, summaries and processing/plotting code revisions |
| Reproduction | Exact command, working directory, environment setup and required external resources |
| File locations | Input/output, logs and record locations; stable relative paths and content hashes where feasible |

Unknown information must be marked unknown with a reason; not applicable must
also have a reason. Neither means zero or an empty successful result. Record
the resolved settings actually used, not just a file that omitted defaults.

## Relationship to experiments and claims

An experiment can contain many runs. Link result tables and plots to run IDs,
and link claim records to those artifacts and the experiment's validity
limits. Keep raw outputs distinct from interpretation. Record exclusions and
failed cases so a later reader can reconstruct the comparison population.
