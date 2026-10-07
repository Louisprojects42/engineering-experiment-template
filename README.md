# Engineering Experiment Template

A manual experiment-planning and evidence-recording template extracted from an existing engineering workflow. It helps separate a question, assumptions, variable roles, method, observations and conclusions without pretending that paperwork validates a result.

## Use the template

Copy [template/experiment](template/experiment) for a new study and give it a local name. Fill in its README and illustrative inputs YAML before running anything. The YAML is a planning aid, not a runnable schema. Null and unresolved fields mean a decision is still required; they are not zeroes or defaults.

Keep original inputs in inputs/, analysis code in scripts/, raw outputs in results/ and derived figures in plots/. These folder names are conveniences; adapt them to your workflow. Preserve failed and excluded attempts with reasons.

The supporting records are optional manual formats:

- [Run record](template/run-record.md): exact inputs, resolved settings, versions, outputs and reproduction evidence.
- [Decision record](template/decision-record.md): context, choice, consequences, investigated alternatives and open questions.
- [Change entry](template/change-entry.md): affected files, reasoning, contributors and observed checks.

Read the [run guide](docs/run-record-guide.md), [decision guide](docs/decision-record-guide.md) and [evidence-log guide](docs/evidence-log-guide.md) for the underlying process.

## Example and limits

[Rectangle-area study](examples/rectangle-study/README.md) is a fictional example with synthetic inputs and arithmetic outputs. It is not a laboratory result, private experiment or executed solver run.

This repository contains no solver, recorder, scientific acceptance method, research roadmap or execution engine. It does not prescribe numerical thresholds, establish model accuracy, prove student understanding or enforce an agent workflow. Record only what you actually observed and keep uncertainty visible.

## Check the documents

The adapted local-link checker needs only Python 3.11+:

```text
python scripts/check_links.py --root .
```

This is a document/template repository, so no runtime package or artificial solver test suite is supplied. The checker verifies local reference existence; CI runs that check. See [provenance](docs/provenance.md), [contribution guidance](CONTRIBUTING.md) and [LICENSE](LICENSE).
