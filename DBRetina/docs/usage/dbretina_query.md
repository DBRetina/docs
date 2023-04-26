# 5. Query

The Query command in DBRetina is designed to retrieve information from the generated index. The command requires the index prefix.

```
Usage: DBRetina query [OPTIONS]

  Query DBRetina index.

Options:
  -q, --query PATH         query line separated file  [required]
  -i, --index-prefix TEXT  index file prefix  [required]
  -o, --output TEXT        output file prefix  [required]
  --help                   Show this message and exit.
```

## 5.1 Command arguments

<span style="color:orange;">** -q, --query PATH         query line separated file  [required] **<span/>

A single-column file containing the list of features to be queried.

<span style="color:orange;">** -i, --index-prefix TEXT  Index file prefix  [required] **<span/>

This is the user-defined prefix that was used in the indexing step.


<span style="color:orange;">** -o, --output TEXT        output file prefix  [required] **<span/>

The output prefix that should be unique for this query.

---

## 5.2 Output files format

<span style="color:orange;">** {output_prefix}_feature_to_groups.tsv **<span/>

A TSV file containing two columns, the first column is the feature name and the second column is the list of supergroups that contain that feature, separated by the pipe character '|'. 

<span style="color:orange;">** {output_prefix}_features_count_per_group.tsv **<span/>

A TSV file containing two columns, the first column is the supergroup name and the second column is the number of features that are contained in that supergroup.
