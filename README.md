# Trivy (trivy)

Trivy is a comprehensive and versatile open-source security scanner from Aqua Security that finds vulnerabilities, misconfigurations, secrets, and SBOM in containers, Kubernetes, code repositories, clouds, and more. Trivy runs as a CLI tool, in client/server mode with an HTTP API, and as a Kubernetes Operator (trivy-operator) that continuously scans clusters and generates security reports as native Kubernetes Custom Resources.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/trivy/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/trivy/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Containers
- Kubernetes
- SBOM
- Security
- Vulnerability Scanning
- Open Source
- DevSecOps
- Cloud Security

## Timestamps

- **Created:** 2026-03-26
- **Modified:** 2026-05-19

## APIs

### Trivy Server API

Trivy can run in client/server mode where the server maintains vulnerability databases and clients submit scan requests. The server exposes HTTP endpoints including /healthz for liveness checks and /version for server version information. Authentication is via token-based header (Trivy-Token).

- **Human URL:** [https://trivy.dev/latest/docs/references/modes/client-server/](https://trivy.dev/latest/docs/references/modes/client-server/)
- **Base URL:** `http://localhost:4954`

#### Tags

- Security
- Vulnerability Scanning
- Server Mode
- HTTP API

#### Properties

- [Documentation](https://trivy.dev/latest/docs/references/modes/client-server/)
- [GitHub Repository](https://github.com/aquasecurity/trivy)
- [OpenAPI](openapi/trivy-server-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/trivy-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trivy-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Trivy Operator

The Trivy Operator is a Kubernetes-native security toolkit that automatically scans clusters and generates security reports as Kubernetes Custom Resources. It defines 12 CRDs covering vulnerability reports, config audit reports, exposed secret reports, SBOM reports, RBAC assessment reports, infrastructure assessment reports, and compliance reports.

- **Human URL:** [https://github.com/aquasecurity/trivy-operator](https://github.com/aquasecurity/trivy-operator)
- **Base URL:** `https://kubernetes.default.svc`

#### Tags

- Kubernetes
- Security
- CRD
- Operator
- Vulnerability Scanning

#### Properties

- [Documentation](https://aquasecurity.github.io/trivy-operator/)
- [GitHub Repository](https://github.com/aquasecurity/trivy-operator)
- [Kubernetes C R D](crd/aquasecurity.github.io_vulnerabilityreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_configauditreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_exposedsecretreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_sbomreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_clustercompliancereports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_clusterconfigauditreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_clusterinfraassessmentreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_clusterrbacassessmentreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_clustersbomreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_clustervulnerabilityreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_infraassessmentreports.yaml)
- [Kubernetes C R D](crd/aquasecurity.github.io_rbacassessmentreports.yaml)
- [Postman Collection](collections/trivy-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trivy-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Trivy CLI

The primary interface for Trivy is its command-line tool, which scans container images, filesystems, Git repositories, Kubernetes clusters, virtual machine images, and SBOMs. Supports multiple output formats including JSON, SARIF, CycloneDX, SPDX, and table output for CI/CD integration.

- **Human URL:** [https://trivy.dev/latest/docs/](https://trivy.dev/latest/docs/)
- **Base URL:** `https://trivy.dev`

#### Tags

- CLI
- Security
- DevSecOps
- Containers
- Kubernetes

#### Properties

- [Documentation](https://trivy.dev/latest/docs/)
- [Getting Started](https://trivy.dev/latest/getting-started/installation/)
- [GitHub Repository](https://github.com/aquasecurity/trivy)
- [Postman Collection](collections/trivy-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trivy-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://trivy.dev/)
- [Documentation](https://aquasecurity.github.io/trivy/)
- [Getting Started](https://aquasecurity.github.io/trivy/latest/getting-started/installation/)
- [GitHub Organization](https://github.com/aquasecurity)
- [GitHub Repository](https://github.com/aquasecurity/trivy)
- [Trivy  Operator](https://github.com/aquasecurity/trivy-operator)
- [Git Hub  Action](https://github.com/aquasecurity/trivy-action)
- [V S  Code  Extension](https://github.com/aquasecurity/trivy-vscode-extension)
- [Helm  Chart](https://artifacthub.io/packages/helm/aqua/trivy-operator)
- [Docker  Image](https://hub.docker.com/r/aquasec/trivy)
- [Releases](https://github.com/aquasecurity/trivy/releases)
- [OpenAPI](openapi/trivy-server-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](json-schema/trivy-vulnerability-report-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/trivy-scan-result-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [J S O N  Structure](json-structure/trivy-scan-structure.json)
- [JSON-LD](json-ld/trivy-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral  Rules](rules/trivy-rules.yml)
- [Vocabulary](vocabulary/trivy-vocabulary.yml)
- [x-profiled](2026-05)
- [Integrations](https://trivy.dev/partners)
- [M C P Server](https://github.com/aquasecurity/trivy-mcp)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
