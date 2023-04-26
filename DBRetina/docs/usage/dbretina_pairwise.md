# 2. Pairwise

The Pairwise command in DBRetina is designed to perform pairwise comparisons between supergroups based on their shared features. This command takes the index prefix and the number of cores as input parameters.


```
Usage: DBRetina pairwise [OPTIONS]

  Generate pairwise TSV.

Options:
  -i, --index-prefix TEXT  Index file prefix  [required]
  -t, --threads INTEGER    number of cores
  --help                   Show this message and exit.
```

## 2.1 Command arguments

<span style="color:orange;">** -i, --index-prefix TEXT  Index file prefix  [required] **<span/>

This is the user-defined prefix that was used in the indexing step.

<span style="color:orange;">** -t, --threads INTEGER    number of cores **<span/>

The number of processing cores to be used for parallel computation during the pairwise comparisons.

---

## 2.2 Output files format

<span style="color:orange;">** {perfix}_DBRetina_pairwise.tsv **<span/>

A TSV file that provides information about shared features between each pair of supergroups. The TSV columns are defined as follows:


<table>
  <tbody>
    <tr>
      <td><strong>group_1_ID</strong></td>
      <td>ID of the first supergroup in a pair</td>
    </tr>
    <tr>
      <td><strong>group_2_ID</strong></td>
      <td>ID of the second supergroup in a pair</td>
    </tr>
    <tr>
      <td><strong>group_1_name</strong></td>
      <td>name of the first supergroup in a pair</td>
    </tr>
    <tr>
      <td><strong>group_2_name</strong></td>
      <td>name of the second supergroup in a pair</td>
    </tr>
    <tr>
      <td><strong>shared_features</strong></td>
      <td>number of features shared between the two supergroups</td>
    </tr>
    <tr>
      <td><strong>min_containment</strong></td>
      <td>minimum containment between the two supergroups</td>
    </tr>
    <tr>
      <td><strong>avg_containment</strong></td>
      <td>average containment between the two supergroups</td>
    </tr>
    <tr>
      <td><strong>max_containment</strong></td>
      <td>maximum containment between the two supergroups</td>
    </tr>
    <tr>
      <td><strong>ochiai</strong></td>
      <td>Ochiai distance between the two supergroups</td>
    </tr>
    <tr>
      <td><strong>jaccard</strong></td>
      <td>Jaccard distance between the two supergroups</td>
    </tr>
  </tbody>
</table>
