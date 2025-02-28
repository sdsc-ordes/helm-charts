<p align="center">
  <img src="./docs/assets/logo.svg" alt="project logo" width="250">
</p>

<h1 align="center">
  helm-charts
</h1>
<p align="center">
</p>
<p align="center">
  <a href="https://github.com/sdsc-ordes/helm-charts/releases">
    <img alt="GitHub Downloads (all assets, all releases)" src="https://img.shields.io/github/downloads/sdsc-ordes/helm-charts/total">
  </a>
  <a href="https://sdsc-ordes.github.io/helm-charts">
    <img alt="github pages" src="https://img.shields.io/website?url=https%3A%2F%2Fsdsc-ordes.github.io%2Fhelm-charts">
  </a>
  <a href="http://www.apache.org/licenses/LICENSE-2.0.html">
    <img src="https://img.shields.io/badge/License-Apache2.0-blue.svg?" alt="License label" />
  </a>
</p>

**Authors:**

- [Laure Vancauwenberghe](mailto:laure.vancauwenberghe@epfl.ch)
- [Cyril Matthey-Doret](mailto:cyril.matthey-doret@epfl.ch)


## Usage

Charts can be installed directly from the releases, for example:

```sh
helm install shacl-api https://github.com/sdsc-ordes/helm-charts/releases/download/shacl-api-0.0.2/shacl-api-0.0.2.tgz
```

The github pages website can also be added as a helm repository:

```sh
helm repo add sdsc-ordes https://sdsc-ordes.github.io/helm-charts
# render manifests from charts:
helm template gimie-api sdsc-ordes/gimie-api
```

Alternatively, you may define a wrapper chart that uses these as dependency:

```sh
apiVersion: v2
name: shacl-api-external
description: A Helm chart for sdsc-ordes/shacl-api
type: application
version: 0.1.0
appVersion: "0.1.0"
dependencies:
  - name: "shacl-api"
    version: "0.0.1"
    repository: "https://sdsc-ordes.github.io/helm-charts"
    alias: "shacl-api"
```

## Development

Read first the [Contribution Guidelines](/CONTRIBUTING.md).

For technical documentation on setup and development, see the
[Development Guide](docs/development-guide.md)

## Copyright

Copyright © 2025-2028 Swiss Data Science Center (SDSC),
[www.datascience.ch](http://www.datascience.ch/). All rights reserved. The SDSC
is jointly established and legally represented by the École Polytechnique
Fédérale de Lausanne (EPFL) and the Eidgenössische Technische Hochschule Zürich
(ETH Zürich). This copyright encompasses all materials, software, documentation,
and other content created and developed by the SDSC.
