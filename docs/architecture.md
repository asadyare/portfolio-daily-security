# Daily security Architecture

flowchart LR
    A[GitHub Schedule or Manual Trigger] --> B[Security Alerting and Reporting Workflow]

    %% Daily scan path
    B --> C[Secret Scanning]
    B --> D[Dependency Scanning]
    B --> E[SBOM Generation]
    B --> F[Filesystem Scan]

    %% Evidence collection
    C --> G[GitHub Actions Logs]
    D --> G
    E --> P[SBOM Artifact]
    P --> G

    %% Security reporting
    F --> H[SARIF Upload]
    H --> I[GitHub Security Tab]

    %% Alerting logic
    B --> J{Critical Findings}
    J -->|Yes| K[Create Security Alert Issue]
    J -->|No| L[Complete Daily Scan]

    %% Weekly governance path
    B --> M{Weekly Schedule}
    M -->|Sunday| N[Generate Weekly Security Report]
    N --> O[Weekly Report Issue]

    %% Audit trail
    K --> Q[Audit Evidence]
    O --> Q
    G --> Q
    