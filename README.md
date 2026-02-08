# Portfolio Daily Security

[![CI Status Badge](https://github.com/asadyare/portfolio-daily-security/actions/workflows/daily-security.yml/badge.svg)](https://github.com/asadyare/portfolio-daily-security/actions/workflows/daily-security.yml)

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

### Evidence

All findings appear in GitHub Actions logs and uploaded security reports.

## Related Repositories

[https://github.com/asadyare/portfolio-ci-cd-security]

[https://github.com/asadyare/portfolio-frontend]

[https://github.com/asadyare/portfolio-k8s-security]
