# Portfolio Daily Security

[![Security alerting and reporting](https://github.com/asadyare/portfolio-daily-security/actions/workflows/security-alerting-and-reporting.yml/badge.svg)](https://github.com/asadyare/portfolio-daily-security/actions/workflows/security-alerting-and-reporting.yml)

![Security](https://img.shields.io/badge/security-automated-blue)
![Schedule](https://img.shields.io/badge/schedule-daily-green)
![Scope](https://img.shields.io/badge/scope-post--merge-orange)

## Overview

This repository runs scheduled security scans across the portfolio. It detects newly disclosed vulnerabilities even when no pull requests or deployments occur.

### Why this exists

PR based security misses newly published CVEs. This repository closes that gap by scanning on a fixed schedule.

## Security Coverage

- Secret scanning
- Dependency vulnerability scanning
- Container filesystem scanning
- SBOM generation
- Security result reporting

## Scheduling

### Daily Execution

- Runs every day at 17:00 UTC.
- Performs full security scanning.
- Automatically creates a GitHub Issue if critical findings are detected.

### Weekly Reporting

- Runs every Sunday at 18:00 UTC.
- Creates a single weekly security report issue.
- Summarises scan coverage and points to existing evidence.

### Alerting Model

Critical findings trigger an automatic GitHub Issue.
Alerts link directly to the workflow run that detected the issue.
No external services are required.
Alerts remain as a permanent audit trail.

### Weekly Reporting Model

One issue is created per week.
Reports summarise coverage, execution, and evidence.
Open security alert issues are referenced for follow up.

### Workflow Design

This repository uses a single GitHub Actions workflow.
The workflow handles daily scanning, alerting, and weekly reporting.
This avoids duplication and keeps logic easy to reason about.

## Evidence and Auditability

All scan results are available in GitHub Actions logs.
SARIF results appear in the GitHub Security tab.
Alerts and reports are tracked as GitHub Issues.

## Related Repositories

   Frontend Application

1. [Fronteend Application](https://github.com/asadyare/portfolio-frontend)

   Shared CI and Security Workflows

2. [CI CD and security pipelines](https://github.com/asadyare/portfolio-ci-cd-security)

   Kubernetes Security Projects
3. [Kubernetes Deployment and security](https://github.com/asadyare/portfolio-k8s-microservices-deployment)

## Central Portfolio Reference

Primary portfolio index and documentation
[Central reposittory](https://github.com/asadyare/devsecops-portfolio-asad)

## Contact

You can contact me via [walasaqo@gmail.com](mailto:walasaqo@gmail.com) or connect with me on [LinkedIn](https://www.linkedin.com/in/asad-hassan-20b540313/).

## License

This portfolio is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
