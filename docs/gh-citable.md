# Make a repository citable
The easiest way to make your repository citable is to add a `CITATION.cff` file to the repository, as it is supported by both
[Zenodo's](https://zenodo.org/) and it's [Github integration](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content) and [Github](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files) itself.

A simple `CITATION.cff` file can look as suggested below:
```yaml
cff-version: 1.2.0
message: "If you use this software, please cite it as below."
authors:
- family-names: "Dokken"
  given-names: "Jørgen S."
  orcid: "https://orcid.org/0000-0001-6489-8858"
title: "Scientific Computing - A webpage for reproducible research"
version: x.y.z
date-released: YYYY-MM-DD
```

To generate a `cff` file for your repository, you can use the [CFF-generator](https://citation-file-format.github.io/cff-initializer-javascript/#/start) where you fill in the relevnt information.
