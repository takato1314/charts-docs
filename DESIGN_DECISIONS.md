# Bitnami Helm charts design decisions

The following document is meant to log all reasoning and design decisions with respect to the Bitnami Helm charts.

Use the following format for contributing to this document:

```
  ## YYYY-MM-DD: <Title for the design decision>

  **TL;DR:** <brief summary> 

  <Reasoning and explanation, putting any related issues and PRs (if any)>
```


## 2021-01-20: Removal of _values-production.yaml_ files

**TL;DR:** The _values-production.yaml_ files are not supported anymore in favor of providing flexibility and documentation to customize the default _values.yaml_

Some of the Bitnami Helm Charts (40 of 80) contain a _values-production.yaml_ file apart from the _values.yaml_. The content of both values files is practically the same but the production ones have different default values in some parameters, being the most common metrics enabled, number of replicas, forced to specify a password, forced a URL, TLS enabled, and more.

There are no clear guidelines as to what is considered "production", as this concept of "production" varies according to the use case or need of each user. This is the principal reason why the Bitnami team is planning to remove the _values-production.yaml_ file in favor of providing flexibility and documentation so each user can customize the default _values.yaml_ to their particular needs.

Apart from that, there are other reasons behind this decision such as the lack of proper tests covering custom values files like the _values_production.yaml_, difficulty to maintain in sync _values.yaml_ and _values-production.yaml_, need to place the values file in the host or specify it via URL, among others.

**Issue:** https://github.com/bitnami/charts/issues/5095

## 2021-01-20: Creation of the design decisions document

**TL;DR:** In order to improve the transparency as well as making the onboarding easier for contributors, we decided to create this document.

**PR:** https://github.com/bitnami/charts-docs/pull/2
