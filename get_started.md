# Get started with the DBRetina package

## 1. Installation

The DBRetina package is currently available on Pypi. You can install it using the following command 

```bash
pip install DBRetina
```

## 2. Commands

### 2.1 Sketching

#### 2.1.1 Input file formats

The sketch command of DBRetina requires two files, namely the association file and the names file. The Association File is a two-column TSV (tab-separated values) file with an included header. The first column denotes groups, while the second column indicates the genes associated with each respective group. Each row signifies a single gene and its corresponding group.

The Names File is another two-column TSV file, also including a header. The first column represents the group names from the Association File, and the second column specifies the corresponding supergroup or alias name. The Names File serves to allow the grouping of related groups under a broader category or supergroup.

To illustrate this within the context of diseases:

Consider an Association File containing a list of diseases and their associated genes. In this scenario, the diseases represent the groups, and each gene is assigned to a specific disease group. For instance, "Breast Cancer" could be a disease group, with genes related to breast cancer listed in the second column of the Association File.

Now, assume that certain diseases are connected and can be categorized under a more comprehensive classification, such as "Cancer" or "Neurological Disorders." In this case, "Cancer" or "Neurological Disorders" would serve as the supergroups and be defined in the Names File alongside their corresponding group names. For example, the groups "Breast Cancer" and "Lung Cancer" would both be associated with the supergroup "Cancer" in the Names File. The second column of the Names File identifies the alias or supergroup name corresponding to each group in the first column.

#### 2.1.2 Output file formats

```
Usage: DBRetina [OPTIONS] COMMAND [ARGS]...

Options:
  --version    Show the version and exit.
  -q, --quiet
  --help       Show this message and exit.

Commands:
  sketch    Sketch a DBRetina files.
  index     Index hashes JSON file.
  pairwise  Generate containment pairwise matrix.
  cluster   Clustering.
  export    Export DBRetina pairwise to multiple formats.
```