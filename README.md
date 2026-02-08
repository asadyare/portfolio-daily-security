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

### Schedule

- Runs daily at 17:00 UTC
- Supports manual execution
- Weekly Reporting
  A weekly security report is generated automatically.
- Reports summarise daily scan execution and reference supporting evidence in GitHub Actions  and the Security tab.

### Evidence

All findings appear in GitHub Actions logs and uploaded security reports.

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
