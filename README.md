# Trivy

Trivy is a comprehensive and versatile open-source security scanner from Aqua Security that finds vulnerabilities, misconfigurations, secrets, and SBOM in containers, Kubernetes, code repositories, clouds, and more. Trivy runs as a CLI tool, in client/server mode with an HTTP API, and as a Kubernetes Operator that continuously scans clusters generating security reports as native Kubernetes Custom Resources.

**Website:** [https://trivy.dev/](https://trivy.dev/)
**GitHub:** [https://github.com/aquasecurity/trivy](https://github.com/aquasecurity/trivy)

---

## APIs and Interfaces

### Trivy Server API
HTTP API exposed when running Trivy in client/server mode. Server maintains vulnerability databases and exposes health check and version endpoints on port 4954.

- **Documentation:** [Client/Server Mode](https://trivy.dev/latest/docs/references/modes/client-server/)
- **OpenAPI:** [openapi/trivy-server-openapi.yml](openapi/trivy-server-openapi.yml)

### Trivy Operator
Kubernetes-native operator that auto-scans clusters and generates security reports as CRDs. Defines 12 custom resource types.

- **Documentation:** [https://aquasecurity.github.io/trivy-operator/](https://aquasecurity.github.io/trivy-operator/)
- **GitHub:** [https://github.com/aquasecurity/trivy-operator](https://github.com/aquasecurity/trivy-operator)

### Trivy CLI
Primary interface for scanning container images, filesystems, Git repos, Kubernetes clusters, VMs, and SBOMs. Outputs JSON, SARIF, CycloneDX, SPDX, and table formats.

- **Documentation:** [https://trivy.dev/latest/docs/](https://trivy.dev/latest/docs/)

---

## Artifacts

### OpenAPI Specifications
| Spec | Description |
|---|---|
| [trivy-server-openapi.yml](openapi/trivy-server-openapi.yml) | Trivy server mode HTTP API |

### Kubernetes CRDs (Trivy Operator)
| CRD | Description |
|---|---|
| [aquasecurity.github.io_vulnerabilityreports.yaml](crd/aquasecurity.github.io_vulnerabilityreports.yaml) | Workload vulnerability reports |
| [aquasecurity.github.io_configauditreports.yaml](crd/aquasecurity.github.io_configauditreports.yaml) | Kubernetes config audit reports |
| [aquasecurity.github.io_exposedsecretreports.yaml](crd/aquasecurity.github.io_exposedsecretreports.yaml) | Exposed secrets detection reports |
| [aquasecurity.github.io_sbomreports.yaml](crd/aquasecurity.github.io_sbomreports.yaml) | Software Bill of Materials reports |
| [aquasecurity.github.io_clustercompliancereports.yaml](crd/aquasecurity.github.io_clustercompliancereports.yaml) | Cluster compliance reports |
| [aquasecurity.github.io_clusterconfigauditreports.yaml](crd/aquasecurity.github.io_clusterconfigauditreports.yaml) | Cluster-wide config audit reports |
| [aquasecurity.github.io_clusterinfraassessmentreports.yaml](crd/aquasecurity.github.io_clusterinfraassessmentreports.yaml) | Cluster infrastructure assessments |
| [aquasecurity.github.io_clusterrbacassessmentreports.yaml](crd/aquasecurity.github.io_clusterrbacassessmentreports.yaml) | Cluster RBAC assessments |
| [aquasecurity.github.io_clustersbomreports.yaml](crd/aquasecurity.github.io_clustersbomreports.yaml) | Cluster SBOM reports |
| [aquasecurity.github.io_clustervulnerabilityreports.yaml](crd/aquasecurity.github.io_clustervulnerabilityreports.yaml) | Cluster vulnerability reports |
| [aquasecurity.github.io_infraassessmentreports.yaml](crd/aquasecurity.github.io_infraassessmentreports.yaml) | Infrastructure assessment reports |
| [aquasecurity.github.io_rbacassessmentreports.yaml](crd/aquasecurity.github.io_rbacassessmentreports.yaml) | RBAC assessment reports |

### JSON Schemas
| Schema | Description |
|---|---|
| [trivy-vulnerability-report-schema.json](json-schema/trivy-vulnerability-report-schema.json) | Vulnerability report with CVEs |
| [trivy-scan-result-schema.json](json-schema/trivy-scan-result-schema.json) | Single scan result per target layer |

### JSON Structure
| File | Description |
|---|---|
| [trivy-scan-structure.json](json-structure/trivy-scan-structure.json) | Structure documentation for scan objects |

### JSON-LD Context
| File | Description |
|---|---|
| [trivy-context.jsonld](json-ld/trivy-context.jsonld) | Linked data context for Trivy security vocabulary |

### Spectral Rules
| Ruleset | Description |
|---|---|
| [trivy-rules.yml](rules/trivy-rules.yml) | API linting rules for Trivy server API |

### Naftiko Capabilities
| Capability | Description |
|---|---|
| [security-scanning.yaml](capabilities/security-scanning.yaml) | Security scanning workflow |

**Shared Definitions:**
| File | Description |
|---|---|
| [shared/trivy-server.yaml](capabilities/shared/trivy-server.yaml) | Trivy server API consumed definition |

### Examples
| Example | Description |
|---|---|
| [trivy-vulnerability-report-example.json](examples/trivy-vulnerability-report-example.json) | Container image vulnerability scan output |
| [trivy-health-check-example.json](examples/trivy-health-check-example.json) | Trivy server health check |

### Vocabulary
| File | Description |
|---|---|
| [trivy-vocabulary.yml](vocabulary/trivy-vocabulary.yml) | Domain vocabulary for security scanning concepts |

---

## Common Resources

- **Aqua Security GitHub:** [https://github.com/aquasecurity](https://github.com/aquasecurity)
- **GitHub Action:** [https://github.com/aquasecurity/trivy-action](https://github.com/aquasecurity/trivy-action)
- **VS Code Extension:** [https://github.com/aquasecurity/trivy-vscode-extension](https://github.com/aquasecurity/trivy-vscode-extension)
- **Helm Chart:** [https://artifacthub.io/packages/helm/aqua/trivy-operator](https://artifacthub.io/packages/helm/aqua/trivy-operator)
- **Docker Image:** [https://hub.docker.com/r/aquasec/trivy](https://hub.docker.com/r/aquasec/trivy)
- **Releases:** [https://github.com/aquasecurity/trivy/releases](https://github.com/aquasecurity/trivy/releases)

---

*Profiled: 2026-05*
