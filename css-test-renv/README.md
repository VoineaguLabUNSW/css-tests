# CSS Renv
Each set of related functions is written as a CRAN package and installed directly from GitHub subfolders.

## Install a package
All packages are installable directly from GitHub using the `renv` package.
```R
library(renv)
renv::install("ivlab/css:<subfolder-name>")
```

## Creating a new package
1. Copy and rename the example subfolder 
2. Modify `DESCRIPTION` `Package` and `Depends` fields
3. Add functions to `R/` - other files in this folder are also allowed

### Why this approach?
#### Strengths
- Dependency versions are at least recorded, even if not honoured, by R.
#### Weaknesses
- Poor support for conda
- Unclear how code will be shared on publication, do we make our entire GitHub repo public?
- Creating new packages requires some boilerplate, even if it's mostly identical for all R libraries



