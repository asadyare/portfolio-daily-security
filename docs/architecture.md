# Daily Security Architecture

```mermaid
flowchart LR
    A[GitHub Schedule Trigger] --> B[Daily Security Workflow]
    B --> C[Secret Scanning]
    B --> D[Dependency Scanning]
    B --> E[SBOM Generation]
    B --> F[Filesystem Scan]

    C --> G[GitHub Actions Logs]
    D --> G
    E --> G
    F --> H[SARIF Upload]

    H --> I[GitHub Security Tab]
