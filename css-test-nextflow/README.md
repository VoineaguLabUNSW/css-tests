# CSS Nextflow
Each function is written as an importable Nextflow module with defined inputs/outputs/dependencies.

## Install a package
Import directly into your workflow.
```bash
nf-core modules install -R ivlab/css --sha <specific-commit-sha> <module-name>
```

## Creating a new package
1. Create a new subfolder in the modules folder
2. Translate script into a Nextflow module file-based inputs/outputs (but you can output e.g. custom rds files)

### Why this approach?
#### Strengths
- Script, dependencies and versioning is handled in a single file
- First class HPC support
- Since modules are pulled into your workflow folder, no need to make all our modules public
#### Weaknesses
- Essentially scripts can only be used in Nextflow workflows
- Inputs/outputs must be files, which is quite limiting
- Subworkflows are another thing that should probably get supported, so it does get confusing