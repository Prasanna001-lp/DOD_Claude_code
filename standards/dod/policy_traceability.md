# Policy Traceability Matrix
Generated: 2025-06-01

## Overview
This matrix maps every DoD criterion across all work types to its source policy or standard. Each criterion is traceable to a documented requirement, ensuring audit compliance and governance transparency.

**Organisation:** Acme Engineering  
**Team:** Commerce Platform  
**Engineering Tier:** Scale-up  
**Total Criteria Across All Work Types:** 178  
**Total Unique Source Policies Referenced:** 42  

---

## Feature Story DoD Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge (verified by GitHub branch protection). |
| CODE-05 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-LOC | No method exceeds 50 lines of code (enforced by SonarQube). |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-DEAD | No dead code, unreachable code, or commented-out code present (SonarQube detects). |
| CODE-08 | L2-WORKTYPE | ENG-4.1-SEC | Security-critical PRs have approval from Security Champion in addition to standard 2 approvals. |
| TEST-01 | L1-UNIVERSAL | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-REGRESS | CI build passes coverage regression check (no covered code lost coverage). |
| TEST-04 | L2-WORKTYPE | QA-2.2-FEATURE-UNIT | Unit tests present for all changed production code (JUnit 5). |
| TEST-05 | L2-WORKTYPE | QA-2.2-FEATURE-INT | Integration tests present covering service interactions (Spring Boot Test). |
| TEST-06 | L2-WORKTYPE | QA-2.2-FEATURE-E2E | E2E tests present with happy path + at least 1 error path scenario (Playwright). |
| TEST-07 | L2-WORKTYPE | QA-2.4-PERF-P95 | k6 load test shows P95 response time < 500ms under normal load. |
| TEST-08 | L2-WORKTYPE | QA-2.4-PERF-P99 | k6 load test shows P99 response time < 2000ms under normal load. |
| TEST-09 | L2-WORKTYPE | INC-001 | **[ESCAPED DEFECT]** Integration test verifies SSO login flow for all configured auth methods (OAuth, SAML, etc.). |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in CI. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-MEDIUM | Medium severity Snyk findings acknowledged with tracked Jira ticket (ticket linked in PR). |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-GITLEAKS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | All dependencies in pom.xml/package.json exist in approved dependency registry. |
| SEC-05 | L1-UNIVERSAL | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present (Snyk). |
| SEC-06 | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit (React) or mvn dependency:check (Java) shows 0 Critical findings in CI. |
| SEC-07 | L1-UNIVERSAL | SEC-4.2-STORAGE | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified in code review). |
| DOC-01 | L3-TEAM | TEAM-STANDARD | README.md updated if feature changes setup, configuration, or API usage. |
| DOC-02 | L3-TEAM | TEAM-STANDARD | Inline Javadoc present for all new public methods and classes. |
| CI-01 | L1-UNIVERSAL | CI-STANDARD | All GitHub Actions checks pass (build, test, lint, security scans). |
| CI-02 | L3-TEAM | TEAM-STANDARD | Spring Boot application starts successfully in CI test environment. |
| CI-03 | L3-TEAM | TEAM-STANDARD | Kafka consumer/producer integration verified in CI (if applicable). |
| CI-04 | L3-TEAM | TEAM-STANDARD | PostgreSQL schema migrations apply cleanly in CI test database. |
| ACC-01 | L2-WORKTYPE | TEAM-STANDARD | All Acceptance Criteria verified by Product Owner in staging environment. |
| ACC-02 | L3-TEAM | TEAM-STANDARD | UX review completed if feature changes user-facing UI (React components). |
| ACC-03 | L3-TEAM | TEAM-STANDARD | Analytics events firing correctly if feature includes tracking requirements. |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | [Add story-specific criterion here during grooming if applicable] |

---

## Bug Fix DoD Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge (verified by GitHub branch protection). |
| CODE-05 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-LOC | No method exceeds 50 lines of code (enforced by SonarQube). |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-DEAD | No dead code, unreachable code, or commented-out code present (SonarQube detects). |
| TEST-01 | L1-UNIVERSAL | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-REGRESS | CI build passes coverage regression check (no covered code lost coverage). |
| TEST-04 | L2-WORKTYPE | QA-2.2-BUG-UNIT | Unit tests present covering the bug fix (JUnit 5). |
| TEST-05 | L2-WORKTYPE | QA-2.3-REGRESSION | Regression test present covering exact reproduction path from bug report (test fails on pre-fix code, passes on fix). |
| TEST-06 | L2-WORKTYPE | INC-003 | **[ESCAPED DEFECT]** Regression test covering exact reproduction path from original bug report present in CI suite. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in CI. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-MEDIUM | Medium severity Snyk findings acknowledged with tracked Jira ticket (ticket linked in PR). |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-GITLEAKS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | All dependencies in pom.xml/package.json exist in approved dependency registry. |
| SEC-05 | L1-UNIVERSAL | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present. |
| SEC-06 | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit (React) or mvn dependency:check (Java) shows 0 Critical findings in CI. |
| DOC-01 | L2-WORKTYPE | QA-2.3-REGRESSION | Root cause of bug documented in PR description or bug ticket. |
| DOC-02 | L2-WORKTYPE | QA-2.3-REGRESSION | Bug ticket updated with resolution notes and regression test reference. |
| DOC-03 | L3-TEAM | TEAM-STANDARD | Javadoc updated if method signature or behavior changed (Spring Boot components). |
| CI-01 | L1-UNIVERSAL | QA-2.1-LINE | All GitHub Actions CI checks pass (build, lint, test, security, coverage). |
| CI-02 | L3-TEAM | TEAM-STANDARD | Spring Boot application starts successfully in CI test environment. |
| CI-03 | L3-TEAM | TEAM-STANDARD | PostgreSQL migration scripts (if any) execute successfully in CI. |
| ACCEPT-01 | L2-WORKTYPE | QA-2.3-REGRESSION | Bug reporter or QA has verified fix in staging/test environment. |
| ACCEPT-02 | L2-WORKTYPE | QA-2.3-REGRESSION | Regression test demonstrates bug no longer reproducible (test passes). |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | Story-specific criterion added during grooming (if applicable). |

---

## Tech Debt DoD Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge (verified by GitHub branch protection). |
| CODE-05 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-LOC | No method exceeds 50 lines of code (enforced by SonarQube). |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-DEAD | No dead code, unreachable code, or commented-out code present (SonarQube detects). |
| CODE-08 | L2-WORKTYPE | ENG-6.2-ADR | ADR created in docs/adr/ documenting architectural change if refactoring impacts system architecture or data model. |
| TEST-01 | L1-UNIVERSAL | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-REGRESS | CI build passes coverage regression check (no covered code lost coverage). |
| TEST-04 | L2-WORKTYPE | QA-2.2-TECH-UNIT | Unit tests present for all refactored code (JUnit 5). |
| TEST-05 | L2-WORKTYPE | QA-2.2-TECH-INT | Integration tests present for refactored components (Spring Boot Test). |
| TEST-06 | L3-TEAM | TEAM-TECH-STACK | No new technical debt introduced: SonarQube Maintainability Rating remains A or B. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in CI. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-MEDIUM | Medium severity Snyk findings acknowledged with tracked Jira ticket (ticket linked in PR). |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-GITLEAKS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | All dependencies in pom.xml/package.json exist in approved dependency registry. |
| SEC-05 | L1-UNIVERSAL | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present. |
| SEC-06 | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit (React) or mvn dependency:check (Java) shows 0 Critical findings in CI. |
| DOC-01 | L2-WORKTYPE | ENG-6.2-ADR | Architecture Guild review approval recorded in PR if refactoring impacts system architecture, data model, or cross-service contracts. |
| DOC-02 | L3-TEAM | TEAM-TECH-STACK | Code-level documentation updated: JavaDoc/JSDoc for public APIs, inline comments for complex logic blocks refactored. |
| DOC-03 | L3-TEAM | TEAM-TECH-STACK | README.md or docs/ updated if refactoring changes module structure, configuration, or deployment process. |
| CI-01 | L1-UNIVERSAL | CI-UNIVERSAL | All GitHub Actions CI checks pass: build, lint, test, security scan, coverage. |
| CI-02 | L3-TEAM | TEAM-TECH-STACK | Java code passes Checkstyle linting with 0 violations (configured in GitHub Actions). |
| CI-03 | L3-TEAM | TEAM-TECH-STACK | React code passes ESLint with 0 errors (configured in GitHub Actions). |
| CI-04 | L3-TEAM | TEAM-TECH-STACK | PostgreSQL schema changes verified: migration scripts tested in CI with rollback verification. |
| ACC-01 | L2-WORKTYPE | TECH-DEBT-ACCEPTANCE | Tech Lead confirms refactoring achieves stated technical goal (performance improvement, maintainability increase, debt reduction). |
| ACC-02 | L2-WORKTYPE | TECH-DEBT-ACCEPTANCE | No regressions introduced: all existing tests pass, no new bugs reported in staging environment. |
| ACC-03 | L3-TEAM | TEAM-TECH-STACK | Kafka consumer/producer refactoring verified: integration tests confirm message processing unchanged, no message loss. |
| SS-01 | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (e.g., specific performance benchmark, library version upgrade verification). |

---

## API Change DoD Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | Security-critical PRs have approval from Security Champion in addition to standard 2 approvals. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge (verified by GitHub branch protection). |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-LOC | No method exceeds 50 lines of code (enforced by SonarQube). |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEAD | No dead code, unreachable code, or commented-out code present (SonarQube detects). |
| TEST-01 | L1-UNIVERSAL | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-REGRESS | CI build passes coverage regression check (no covered code lost coverage). |
| TEST-04 | L2-WORKTYPE | QA-2.2-API-UNIT | Unit tests present for API endpoint logic (JUnit 5). |
| TEST-05 | L2-WORKTYPE | QA-2.2-API-INT | Integration tests present for API endpoint (Spring Boot Test with MockMvc). |
| TEST-06 | L2-WORKTYPE | INC-002 | **[ESCAPED DEFECT]** API contract test includes test cases for all nullable fields documented in OpenAPI spec. |
| TEST-07 | L2-WORKTYPE | QA-2.4-PERF-P95 | k6 load test shows P95 response time < 500ms under normal load. |
| TEST-08 | L2-WORKTYPE | QA-2.4-PERF-P99 | k6 load test shows P99 response time < 2000ms under normal load. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in CI. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-MEDIUM | Medium severity Snyk findings acknowledged with tracked Jira ticket (ticket linked in PR). |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-GITLEAKS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | All dependencies in pom.xml/package.json exist in approved dependency registry. |
| SEC-05 | L1-UNIVERSAL | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present. |
| SEC-06 | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit (React) or mvn dependency:check (Java) shows 0 Critical findings in CI. |
| SEC-07 | L1-UNIVERSAL | SEC-4.2-STORAGE | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified in code review). |
| DOC-01 | L2-WORKTYPE | ENG-6.1-API | OpenAPI specification file (api/openapi.yaml) updated to reflect API changes. |
| DOC-02 | L2-WORKTYPE | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] describing API change. |
| DOC-03 | L2-WORKTYPE | ENG-6.1-API | API diff generated and attached to PR (using openapi-diff or equivalent). |
| DOC-04 | L3-TEAM | TEAM-COMMERCE-PLATFORM | Kafka event schema updated in schemas/ directory if API change publishes events. |
| CI-01 | L1-UNIVERSAL | UNIVERSAL-CI | All GitHub Actions checks pass (lint, build, test, security scan). |
| CI-02 | L2-WORKTYPE | QA-2.4-PERF-K6 | k6 load test included in CI for endpoints handling > 1000 RPS. |
| CI-03 | L3-TEAM | TEAM-COMMERCE-PLATFORM | PostgreSQL migration scripts executed successfully in CI test database. |
| ACC-01 | L3-TEAM | TEAM-COMMERCE-PLATFORM | API changes reviewed by at least 1 backend engineer familiar with existing API contracts. |
| ACC-02 | L3-TEAM | TEAM-COMMERCE-PLATFORM | Breaking API changes communicated to consuming teams via Slack #api-changes channel. |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | [Add story-specific criterion here if applicable] |

---

## Release DoD Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge (verified by GitHub branch protection). |
| TEST-01 | L2-WORKTYPE | QA-3.1-REGRESSION-FULL | Full regression test suite passed in staging and pre-prod environments. |
| TEST-02 | L2-WORKTYPE | QA-3.1-SMOKE | Smoke test suite passed in production environment after deployment. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-04 | L1-UNIVERSAL | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. |
| TEST-05 | L1-UNIVERSAL | QA-2.1-REGRESS | CI build passes coverage regression check (no covered code lost coverage). |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in CI. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-MEDIUM | Medium severity Snyk findings acknowledged with tracked Jira ticket (ticket linked in PR). |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-GITLEAKS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | All dependencies in pom.xml/package.json exist in approved dependency registry. |
| SEC-05 | L1-UNIVERSAL | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present. |
| SEC-06 | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit (React) or mvn dependency:check (Java) shows 0 Critical findings in CI. |
| SEC-07 | L1-UNIVERSAL | SEC-4.2-STORAGE | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified in code review). |
| DOC-01 | L2-WORKTYPE | QA-3.1-NOTES | Release notes prepared and approved by Engineering Manager. |
| DOC-02 | L2-WORKTYPE | QA-3.1-ROLLBACK | Rollback plan documented and tested successfully in staging environment. |
| DOC-03 | L2-WORKTYPE | QA-3.1-RUNBOOK | Runbook updated if operational procedures changed. |
| DOC-04 | L3-TEAM | TEAM-COMMERCE | CHANGELOG.md updated with all user-facing changes under [Unreleased] section. |
| CI-01 | L2-WORKTYPE | TEAM-COMMERCE | All GitHub Actions CI checks pass (build, test, lint, security). |
| CI-02 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CI-03 | L1-UNIVERSAL | ENG-4.3-LOC | No method exceeds 50 lines of code (enforced by SonarQube). |
| CI-04 | L1-UNIVERSAL | ENG-4.3-DEAD | No dead code, unreachable code, or commented-out code present (SonarQube detects). |
| CI-05 | L3-TEAM | TEAM-COMMERCE | Deployment pipeline (GitHub Actions) executed successfully to production environment. |
| ACC-01 | L2-WORKTYPE | QA-3.1-NOTES | Engineering Manager sign-off recorded for release. |
| ACC-02 | L3-TEAM | TEAM-COMMERCE | Product Owner sign-off recorded confirming all release features meet acceptance criteria. |
| ACC-03 | L3-TEAM | TEAM-COMMERCE | Production health check passed post-deployment (all services healthy, zero 5xx errors). |
| ACC-04 | L3-TEAM | TEAM-COMMERCE | Database migrations (if any) executed successfully in production with zero rollback. |
| SS-01 | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (e.g., specific compliance validation, customer-requested verification). |

---

## Infrastructure DoD Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | Security-critical infrastructure changes have approval from Security Champion in addition to standard 2 approvals. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge (verified by GitHub branch protection). |
| CODE-06 | L2-WORKTYPE | ENG-6.2-ADR | ADR created in docs/adr/ documenting architectural change. |
| CODE-07 | L2-WORKTYPE | ENG-6.2-ADR | Architecture Guild review approval recorded in PR (reviewer tagged @arch-guild). |
| CODE-08 | L3-TEAM | TEAM-INFRA-01 | Terraform configuration follows Commerce Platform naming conventions (env-region-service format). |
| TEST-01 | L2-WORKTYPE | INFRA-TEST-01 | Terraform validate passes with 0 errors. |
| TEST-02 | L2-WORKTYPE | INFRA-TEST-02 | Terraform plan shows expected resource changes only (no unintended additions or deletions). |
| TEST-03 | L3-TEAM | TEAM-INFRA-02 | Infrastructure changes tested in staging environment before production deployment. |
| TEST-04 | L3-TEAM | TEAM-INFRA-03 | Health checks verify infrastructure components are operational after deployment. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in CI. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-MEDIUM | Medium severity Snyk findings acknowledged with tracked Jira ticket (ticket linked in PR). |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-GITLEAKS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L2-WORKTYPE | SEC-4.1-TF-PLAN | terraform plan output attached to PR shows no unintended resource deletions. |
| SEC-05 | L2-WORKTYPE | SEC-4.1-TF-REVIEW | Platform Engineering team approval recorded in PR (reviewer tagged @platform-eng). |
| SEC-06 | L2-WORKTYPE | SEC-4.1-TFSEC | tfsec scan shows 0 HIGH or CRITICAL findings in CI. |
| SEC-07 | L1-UNIVERSAL | SEC-4.2-STORAGE | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified in code review). |
| SEC-08 | L3-TEAM | TEAM-INFRA-04 | AWS IAM policies follow principle of least privilege (tfsec checks aws-iam-* rules). |
| DOC-01 | L2-WORKTYPE | INFRA-DOC-01 | Terraform module documentation updated in README.md (inputs, outputs, providers). |
| DOC-02 | L2-WORKTYPE | INFRA-DOC-02 | Runbook updated or created in docs/runbooks/ if operational procedures changed. |
| DOC-03 | L3-TEAM | TEAM-INFRA-05 | Architecture diagram updated in docs/architecture/ if infrastructure topology changed. |
| DOC-04 | L2-WORKTYPE | INFRA-DOC-03 | Disaster Recovery plan verified and documented if infrastructure change affects DR capabilities. |
| CI-01 | L1-UNIVERSAL | CI-GATE-01 | All GitHub Actions workflow checks pass (build, test, lint, security scans). |
| CI-02 | L2-WORKTYPE | INFRA-CI-01 | Terraform fmt check passes (code formatted correctly). |
| CI-03 | L2-WORKTYPE | INFRA-CI-02 | Terraform state lock released successfully after plan operation. |
| CI-04 | L3-TEAM | TEAM-INFRA-06 | Terraform backend state stored in Commerce Platform S3 bucket with versioning enabled. |
| ACC-01 | L2-WORKTYPE | INFRA-ACC-01 | Infrastructure change tested and validated by Platform Engineering team in staging. |
| ACC-02 | L2-WORKTYPE | INFRA-ACC-02 | Rollback procedure documented and tested successfully in staging environment. |
| ACC-03 | L3-TEAM | TEAM-INFRA-07 | Change scheduled during approved maintenance window (if production impact expected). |
| ACC-04 | L3-TEAM | TEAM-INFRA-08 | Monitoring alerts configured or updated for new infrastructure components. |
| SS-01 | L4 | PO-OR-TECH-LEAD | [Add story-specific criterion here if applicable] |

---

## Summary Statistics by Layer

| Layer | Total Criteria | Percentage of All Criteria |
|---|---|---|
| L1-UNIVERSAL | 87 | 48.9% |
| L2-WORKTYPE | 56 | 31.5% |
| L3-TEAM | 29 | 16.3% |
| L4-STORY | 6 | 3.4% |

---

## Escaped Defect Criteria Summary

| Work Type |