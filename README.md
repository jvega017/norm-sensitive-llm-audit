# Norm-Sensitive LLM Audit Framework

This repository contains the materials for **A Methodological Framework for Auditing Norm‑Sensitive Behaviour in Large Language Models**, a research design blueprint for evaluating large language models (LLMs) in contested, value‑laden contexts such as employment decisions.

## Repository Structure

```
.
├── prompts/           # Prompt batteries for testing LLM behaviour
│   ├── hiring_recommendation.txt
│   ├── redundancy_scenarios.txt
│   ├── wage_negotiation.txt
│   ├── performance_review.txt
│   ├── harassment_complaint.txt
│   ├── work_life_balance.txt
│   ├── macro_policy.txt
│   └── conflict_resolution.txt
├── rubrics/           # Annotation guides and scoring rubrics
│   ├── procedural_justice_rubric.md
│   └── annotation_guidelines.md
├── analysis/          # Example analysis scripts (R/Python)
│   └── example_analysis.R
├── README.md          # Project overview and contribution guidelines
├── repository_documentation.md  # Detailed documentation and usage
└── LICENSE            # Licensing information (MIT)
```

### Prompts

The `prompts/` folder contains text files with scenarios and paraphrase variations for testing LLMs.  Each file focuses on a particular domain—such as hiring recommendations, redundancy notices, wage negotiation, performance reviews, harassment complaints, work‑life balance, macroeconomic policy or conflict resolution—and includes multiple paraphrases tagged with one of the default normative lenses (utilitarianism, deontology, care ethics, virtue ethics or Rawlsian justice).  These prompts form the starting point for the pilot phase described in the paper.  You can extend them by adding new scenarios, paraphrases, identity swaps or instruction variants relevant to your deployment context.

### Rubrics

The `rubrics/` folder provides scoring guides for annotators.  The **procedural_justice_rubric.md** file outlines criteria for coding voice, neutrality, respect and trustworthiness on a 0–2 scale.  The **annotation_guidelines.md** file explains how to apply these criteria consistently, train raters, compute inter‑rater reliability and handle ambiguous cases.  Raters should familiarise themselves with these documents before scoring model outputs.

### Analysis

The `analysis/` folder contains a single example R script (`example_analysis.R`) demonstrating how to compute composite scores, inter‑rater reliability (Cohen's \(\kappa\), Krippendorff's \(\alpha\)), and basic statistical tests.  This script is provided for reference; researchers should adapt or rewrite it to suit their own study designs, languages and analysis pipelines.

## Contributing

We welcome contributions from researchers, practitioners and students who wish to extend or pilot the framework. You can contribute by:

- **Adding new scenarios**: Submit pull requests with additional prompt files covering domains or cultures not yet represented.
- **Refining rubrics**: Suggest improvements to the scoring criteria or provide alternative rubrics for different contexts.
- **Running pilots**: Use the provided materials to conduct small‑scale audits and share your findings via issues or pull requests.
- **Expanding analysis**: Contribute scripts for advanced metrics, power analyses, or visualisations.

Please open an issue to discuss any major changes before submitting a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
