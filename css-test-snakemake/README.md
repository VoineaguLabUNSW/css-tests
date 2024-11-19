# CSS Nextflow
Each function is written as an importable Nextflow module with defined inputs/outputs/dependencies.

## Install a package
Import directly into your workflow.
```bash
github("ivlab/css", path="workflow/Snakefile", tag="v1.0.0")
```

## Creating a new package
1. Create a new workflow (which is just a set of rules) subfolder

### Why this approach?
#### Strengths
- Script, dependencies and versioning is handled in a single file
#### Weaknesses
- Essentially scripts can only be used in Snakemake workflows
- Inputs/outputs must be files, which is quite limiting
- Whole GitHub repo would need to be public (possibly can use snakemake --archive instead)
