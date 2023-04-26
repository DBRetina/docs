# 3. Cluster

Graph-based clustering of the pairwise TSV file.

```
Usage: DBRetina cluster [OPTIONS]

  Graph-based clustering of the pairwise TSV file.

Options:
  -c, --cutoff FLOAT RANGE  cluster the supergroups with (distance > cutoff)
                            [default: 0.0; 0<=x<=1]
  -i, --index-prefix TEXT   Index file prefix  [required]
  -d, --dist-type TEXT      select from ['min_cont', 'avg_cont', 'max_cont',
                            'ochiai', 'jaccard']  [default: max_cont]
  --help                    Show this message and exit.
```

## 3.1 Command arguments

<span style="color:orange;">** -c, --cutoff FLOAT RANGE  cluster the supergroups with (distance > cutoff)  [default: 0.0; 0<=x<=1] **<span/>

The cutoff value for clustering the supergroups. The default value is 0.0, which means that all supergroups will be clustered together. The cutoff value can be between 0 and 1. The higher the cutoff value, the more stringent the clustering will be.

<span style="color:orange;">** -i, --index-prefix TEXT   Index file prefix  [required] **<span/>

This is the user-defined prefix that was used in the indexing step.

<span style="color:orange;">** -d, --dist-type TEXT      select from ['min_containment', 'avg_containment', 'max_containment', 'ochiai', 'jaccard']  [default: max_cont] **<span/>

The distance metric to be used for clustering. The default value is 'max_containment', which means that the maximum containment between two supergroups will be used as the distance between them. The other options are 'min_containment', 'avg_containment', 'ochiai', and 'jaccard'.

---

## 3.2 Output files format

<span style="color:orange;">** {prefix}_DBRetina_clusters_{cutoff}%.txt **<span/>

Each line in the file represents a cluster of supergroups separated by a pipe character.