# Daily security Architecture

flowchart LR
    A[GitHub Schedule Trigger] --> B[Security Alerting and Reporting Workflow]

    B --> C[Secret Scanning]
    B --> D[Dependency Scanning]
    B --> E[SBOM Generation]
    B --> F[Filesystem Scan]

    C --> G[GitHub Actions Logs]
    D --> G
    E --> G

    F --> H[SARIF Upload]
    H --> I[GitHub Security Tab]

    B --> J{Critical Findings}

    J -->|Yes| K[Create Security Alert Issue]
    J -->|No| L[Continue Normal Execution]

    B --> M{Weekly Schedule}

    M -->|Sunday| N[Generate Weekly Security Report]
    N --> O[Weekly Report Issue]
