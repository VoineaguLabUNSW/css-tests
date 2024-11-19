# CSS Comments
Annotaterd functions are copied directly into your codebase - with the rise of shadcn and jsdocs, this approach is not as insane as it looks.

## Install a package
1. Copy any function with it versioned comment directly into your source code.
2. Update the revision to the current Git commit hash.

## Creating a new package
1. Create a new .R file to group the functions you want to share
2. Add a comment at the top of the file with the following format:
```R
# author="ivlanb"; revision=<PASTE HERE>; conda-deps="conda-forge::r-base=4.1.2 conda-forge::r-ggplot2=3.3.5"; cran-deps="ggplot2=3.3.5"
my_function <- function() {
  print("Hello World!")
}
```

### Why this approach?
#### Strengths
- Installation for helper functions has zero boilerplate
- Users can choose to use either CRAN or conda
- When a script is published, only the exact functions used need to be released
- GitHub UI can be used to make changes
#### Weaknesses
- There are no guarantees a function hasn't been modified after copying it



