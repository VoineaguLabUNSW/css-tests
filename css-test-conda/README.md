# CSS Conda
Each set of related scripts is grouped into a subfolder that gets automatically turned into a conda package everytime a commit is made (using GitHub Actions).

## Install a package
All packages are automatically built to the ivlab Anaconda channel when changes are comitted.
```bash
conda install -c ivlab <subfolder-name>
```

## Creating a new package
1. Copy and rename the example subfolder 
2. Modify meta.yml `name` and `dependency` fields
3. Add functions to `src/main.R` - other files in this folder are also allowed

### Why this approach?
#### Strengths
- Installation (at least from conda) does not require using GitHub at all.
- Dependencies are installed and conflicts are actively avoided using Conda.
- GitHub UI can be used to make changes
- Easily supports non-R libraries/dependencies, including AI/ML
#### Weaknesses
- Unclear how code will be shared on publication, do we make our entire conda channel public?
- Creating new packages requires some boilerplate, even if it's mostly identical for all R libraries
