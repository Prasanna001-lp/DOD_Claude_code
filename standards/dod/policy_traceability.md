# Policy Traceability Matrix
Generated: 2026-03-16

## Overview
This matrix traces every Definition-of-Done criterion back to its source policy, standard, or escaped defect incident. It enables audit compliance and demonstrates that all mandatory requirements have been translated into verifiable DoD gates.

**Total Criteria:** 163  
**Work Types Covered:** 6 (feature_story, bug_fix, tech_debt, api_change, release, infrastructure)  
**Unique Source Policies:** 34  
**Escaped Defect Criteria:** 3  

---

## Feature Story

| Criterion ID | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | PRs touching security-critical code paths (authentication, authorization, payment processing, PII handling) have approval from Security Champion. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | PR is merged using squash merge strategy only. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes: cyclomatic complexity ≤ 10 per method. |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-LENGTH | No method exceeds 50 lines of code. |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEAD | SonarQube reports 0 dead code issues (unreachable code, commented-out code removed). |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage on all changed modules. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage on changed modules. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COVERAGE | No existing covered code has lost coverage (CI build enforces no coverage regression). |
| TEST-04 | L2-WORKTYPE | QA-2.2-UNIT | Unit tests present and passing (JUnit 5) for all changed code. |
| TEST-05 | L2-WORKTYPE | QA-2.2-INTEGRATION | Integration tests present and passing for all API/service integration points (database, Kafka, external APIs). |
| TEST-06 | L2-WORKTYPE | QA-2.2-E2E | E2E test (Playwright) covers happy path and at least 1 error path for user-facing features. |
| TEST-07 | L2-WORKTYPE | QA-2.4-PERF | k6 load test included in CI if endpoint handles >1000 RPS. P95 response time <500ms, P99 <2000ms under normal load. |
| TEST-08 | L2-WORKTYPE | **INC-001** | **[ESCAPED DEFECT]** Integration test: SSO login flow verified for all configured auth methods before merge. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK | All Medium severity Snyk findings have tracked Jira tickets before merge. |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | npm audit (React) or mvn dependency:check (Java) produces 0 Critical findings in CI. |
| SEC-05 | L3-TEAM | TEAM-SPRING-BOOT | Spring Boot Actuator endpoints secured (authentication required for /actuator/* except /health and /info). |
| DOC-01 | L2-WORKTYPE | ENG-6.1-API | OpenAPI specification file (api/openapi.yaml) updated to reflect API changes. |
| DOC-02 | L2-WORKTYPE | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-03 | L2-WORKTYPE | ENG-6.1-API | API diff generated and attached to PR. |
| DOC-04 | L3-TEAM | TEAM-KAFKA | Kafka event schema documented in schemas/ directory for new/changed event types. |
| CI-01 | L1-UNIVERSAL | IMPLICIT-CI | All CI checks pass in GitHub Actions (build, lint, test, security scans). |
| CI-02 | L3-TEAM | IMPLICIT-LINT | Code passes linting checks (ESLint for React, Checkstyle/SpotBugs for Java). |
| CI-03 | L3-TEAM | TEAM-POSTGRES | Database migration scripts tested in CI against PostgreSQL test database. |
| ACC-01 | L2-WORKTYPE | IMPLICIT-ACCEPTANCE | All acceptance criteria verified by Product Owner (documented in story comments or PR). |
| ACC-02 | L3-TEAM | TEAM-ANALYTICS | Analytics event tracking implemented for user-facing feature (if applicable). |
| ACC-03 | L3-TEAM | TEAM-UX | UX review completed for user-facing UI changes (documented in Figma or PR comments). |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable. |

---

## Bug Fix

| Criterion ID | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | PRs touching security-critical code paths have approval from Security Champion. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | PR is merged using squash merge strategy only. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes: cyclomatic complexity ≤ 10 per method. |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-LENGTH | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEAD | SonarQube reports 0 dead code issues (unreachable code, commented-out code removed). |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage on all changed modules. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage on changed modules. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COVERAGE | No existing covered code has lost coverage (CI build enforces no coverage regression). |
| TEST-04 | L2-WORKTYPE | QA-2.2-UNIT | Unit tests present and passing (JUnit 5 for Java, Jest for React) for all changed code. |
| TEST-05 | L2-WORKTYPE | QA-2.2-INTEGRATION | Integration tests present and passing covering the integration failure path if bug involved service-to-service or database interaction. |
| TEST-06 | L2-WORKTYPE | QA-2.2-E2E | E2E test (Playwright) covers UI bug reproduction and fix verification if bug affected user-facing UI. |
| TEST-07 | L2-WORKTYPE | QA-2.3-REGRESSION | Regression test present covering exact reproduction path from original bug report. |
| TEST-08 | L2-WORKTYPE | **INC-003** | **[ESCAPED DEFECT]** Regression test covering exact reproduction path from original bug report must be present in CI. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK | All Medium severity Snyk findings have tracked Jira tickets before merge. |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | npm audit (React) or mvn dependency:check (Java) produces 0 Critical findings in CI. |
| DOC-01 | L2-WORKTYPE | IMPLICIT-ROOTCAUSE | Root cause documented in bug ticket or PR description. |
| DOC-02 | L3-TEAM | TEAM-COMMERCE | If bug affected Kafka event schema or PostgreSQL data model, updated docs/data-contracts/. |
| CI-01 | L1-UNIVERSAL | IMPLICIT-CI | All CI checks pass in GitHub Actions (build, lint, test, security scans). |
| CI-02 | L1-UNIVERSAL | IMPLICIT-LINT | Code passes linting checks (ESLint for React, Checkstyle/SpotBugs for Java). |
| ACC-01 | L2-WORKTYPE | TEAM-BUG-VERIFICATION | Bug reporter or QA engineer verified fix in staging environment using exact reproduction steps. |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable. |

---

## Tech Debt

| Criterion ID | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-MERGE | PR is merged using squash merge strategy only. |
| CODE-05 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes: cyclomatic complexity ≤ 10 per method. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-LENGTH | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-DEAD | SonarQube reports 0 dead code issues (unreachable, commented-out code removed). |
| CODE-08 | L2-WORKTYPE | ENG-6.2-ARCH | Architecture Decision Record (ADR) created in docs/adr/ for architectural changes. |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage on all changed modules. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage on changed modules. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COVERAGE | No existing covered code has lost coverage (CI build enforces no coverage regression). |
| TEST-04 | L2-WORKTYPE | QA-2.2-UNIT | Unit tests present and passing (JUnit 5) for all changed code. |
| TEST-05 | L3-TEAM | TEAM-TECH-DEBT-01 | No new technical debt introduced (SonarQube Debt Ratio does not increase). |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK | All Medium severity Snyk findings have tracked Jira tickets before merge. |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | npm audit (React) or mvn dependency:check (Java) produces 0 Critical findings in CI. |
| ARCH-01 | L2-WORKTYPE | ENG-6.2-ARCH | Architecture Guild review completed and approval documented in PR. |
| ARCH-02 | L3-TEAM | TEAM-TECH-DEBT-02 | Tech debt retirement tracked: Jira ticket updated with "before" and "after" metrics. |
| DOC-01 | L3-TEAM | TEAM-TECH-DEBT-03 | Tech debt justification documented in PR. |
| DOC-02 | L2-WORKTYPE | IMPLICIT-DOC | Documentation updated for architectural changes (README, runbooks, architecture diagrams). |
| CI-01 | L1-UNIVERSAL | IMPLICIT-CI | All CI checks pass in GitHub Actions (build, lint, test, security scans). |
| CI-02 | L1-UNIVERSAL | IMPLICIT-LINT | Code passes linting checks (ESLint for React, Checkstyle/SpotBugs for Java). |
| ACC-01 | L3-TEAM | TEAM-TECH-DEBT-04 | Tech Lead or Engineering Manager sign-off documented in PR. |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable. |

---

## API Change

| Criterion ID | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | PRs touching security-critical code paths have approval from Security Champion. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | PR is merged using squash merge strategy only. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes: cyclomatic complexity ≤ 10 per method. |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-LENGTH | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEAD | SonarQube reports 0 dead code issues (unreachable, commented-out code removed). |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage on all changed modules. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage on changed modules. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COVERAGE | No existing covered code has lost coverage (CI build enforces no coverage regression). |
| TEST-04 | L2-WORKTYPE | QA-2.2-UNIT | Unit tests present and passing (JUnit 5) for all changed code. |
| TEST-05 | L2-WORKTYPE | QA-2.2-INTEGRATION | Integration tests present and passing for all API/service integration points. |
| TEST-06 | L2-WORKTYPE | **INC-002** | **[ESCAPED DEFECT]** API contract test includes all nullable fields documented in the OpenAPI spec. |
| TEST-07 | L2-WORKTYPE | QA-2.4-PERF | k6 load test included in CI, P95 response time < 500ms and P99 < 2000ms under normal load. |
| TEST-08 | L3-TEAM | TEAM-KAFKA | Kafka event schema changes include contract tests verifying consumer compatibility. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK | All Medium severity Snyk findings have tracked Jira tickets before merge. |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS, SEC-4.2-SECRETS | Gitleaks scan passes with 0 secrets detected. All secrets stored in AWS Secrets Manager or GitHub Actions secrets. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | npm audit (React) or mvn dependency:check (Java) produces 0 Critical findings in CI. |
| DOC-01 | L2-WORKTYPE | ENG-6.1-API | OpenAPI specification file (api/openapi.yaml) updated to reflect API changes. |
| DOC-02 | L2-WORKTYPE | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-03 | L2-WORKTYPE | ENG-6.1-API | API diff generated and attached to PR. |
| DOC-04 | L2-WORKTYPE | ENG-6.2-ARCH | Architecture Decision Record (ADR) created in docs/adr/ for architectural changes. |
| DOC-05 | L2-WORKTYPE | ENG-6.2-ARCH | Architecture Guild review completed and approval documented in PR. |
| DOC-06 | L3-TEAM | TEAM-API-DOCS | API documentation in README.md or docs/api/ updated with request/response examples. |
| CI-01 | L1-UNIVERSAL | IMPLICIT-CI | All CI checks pass in GitHub Actions (build, lint, test, security scans). |
| CI-02 | L1-UNIVERSAL | IMPLICIT-LINT | Code passes linting checks (ESLint for React, Checkstyle/SpotBugs for Java). |
| CI-03 | L3-TEAM | TEAM-SPRING-BOOT | Spring Boot Actuator health endpoint returns UP status in staging environment. |
| ACC-01 | L3-TEAM | TEAM-API-CONSUMER | Breaking API changes communicated to consumer teams minimum 5 business days before merge. |
| ACC-02 | L3-TEAM | TEAM-VERSIONING | API version number incremented according to semantic versioning. |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable. |

---

## Release

| Criterion ID | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-MERGE | PR is merged using squash merge strategy only. |
| CODE-05 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes: cyclomatic complexity ≤ 10 per method. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-LENGTH | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-DEAD | SonarQube reports 0 dead code issues (unreachable, commented-out code removed). |
| CODE-08 | L2-WORKTYPE | IMPLICIT-LINT | Code passes linting checks (ESLint for React, Checkstyle/SpotBugs for Java). |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage on all changed modules. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage on changed modules. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COVERAGE | No existing covered code has lost coverage (CI build enforces no coverage regression). |
| TEST-04 | L2-WORKTYPE | QA-3.1-REGRESSION-SUITE | Full regression test suite passes in staging and pre-prod environments. |
| TEST-05 | L2-WORKTYPE | QA-3.1-SMOKE | Smoke test suite passes in production environment post-deploy. |
| TEST-06 | L2-WORKTYPE | QA-3.1-ROLLBACK | Rollback plan documented and tested successfully in staging environment. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK | All Medium severity Snyk findings have tracked Jira tickets before merge. |
| SEC-03 | L1-UNIVERSAL | SEC-3.2, SEC-4.2 | Gitleaks scan passes. All secrets stored in AWS Secrets Manager or GitHub Actions secrets. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | npm audit (React) or mvn dependency:check (Java) produces 0 Critical findings in CI. |
| DOC-01 | L2-WORKTYPE | QA-3.1-NOTES | Release notes prepared and approved by Engineering Manager. |
| DOC-02 | L2-WORKTYPE | QA-3.1-RUNBOOK | Runbook updated if operational procedures changed. |
| DOC-03 | L3-TEAM | COMMERCE-PLATFORM-STANDARD | CHANGELOG.md updated with all user-facing changes. |
| CI-01 | L1-UNIVERSAL | IMPLICIT-CI | All CI checks pass in GitHub Actions (build, lint, test, security scans). |
| CI-02 | L3-TEAM | COMMERCE-PLATFORM-KAFKA | Kafka consumer lag monitored post-deploy; no critical lag (>10k messages) detected. |
| CI-03 | L3-TEAM | COMMERCE-PLATFORM-DB | PostgreSQL migration scripts executed successfully in pre-prod before production release. |
| ACC-01 | L2-WORKTYPE | QA-3.1-NOTES | Engineering Manager sign-off obtained. |
| ACC-02 | L3-TEAM | COMMERCE-PLATFORM-RELEASE | Product Owner notified of release completion and user-facing changes. |
| ACC-03 | L3-TEAM | COMMERCE-PLATFORM-ONCALL | On-call engineer briefed on release changes and potential issues. |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable. |

---

## Infrastructure

| Criterion ID | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | PR touching security-critical infrastructure has approval from Security Champion. |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | PR is merged using squash merge strategy only. |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes: cyclomatic complexity ≤ 10 per method. |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-LENGTH | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEAD | SonarQube reports 0 dead code issues (unreachable, commented-out code removed). |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage on all changed modules. |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage on changed modules. |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COVERAGE | No existing covered code has lost coverage (CI build enforces no coverage regression). |
| TEST-04 | L3-TEAM | TEAM-INFRA-01 | Terraform plan executed successfully with no errors. |
| TEST-05 | L3-TEAM | TEAM-INFRA-02 | Infrastructure validation tests pass (Terratest or equivalent) in non-production environment. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK | All Medium severity Snyk findings have tracked Jira tickets before merge. |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | npm audit or mvn dependency:check produces 0 Critical findings in CI. |
| SEC-05 | L2-WORKTYPE | SEC-4.1-TERRAFORM | terraform plan produces clean plan with no unintended resource deletions. |
| SEC-06 | L2-WORKTYPE | SEC-4.1-TERRAFORM | Platform Engineering team review completed and documented in PR. |
| SEC-07 | L2-WORKTYPE | SEC-4.1-TERRAFORM | tfsec scan passes with 0 HIGH or CRITICAL findings. |
| SEC-08 | L1-UNIVERSAL | SEC-4.2-SECRETS | No hardcoded secrets in code. All secrets stored in AWS Secrets Manager or GitHub Actions secrets. |
| ARCH-01 | L2-WORKTYPE | ENG-6.2-ARCH | ADR created in docs/adr/ for changes to VPC, service mesh, IAM policies, or cross-service networking. |
| ARCH-02 | L2-WORKTYPE | ENG-6.2-ARCH | Architecture Guild review completed and approval documented in PR. |
| DOC-01 | L2-WORKTYPE | QA-3.1-RUNBOOK | Runbook updated if operational procedures changed. |
| DOC-02 | L3-TEAM | TEAM-INFRA-03 | Terraform module README.md updated with input variables, outputs, and usage examples. |
| DOC-03 | L3-TEAM | TEAM-INFRA-04 | Infrastructure change documented in CHANGELOG.md under [Unreleased] section. |
| CI-01 | L1-UNIVERSAL | IMPLICIT-CI | All CI checks pass in GitHub Actions (build, lint, terraform validate, tfsec, Snyk, Gitleaks, tests). |
| CI-02 | L3-TEAM | TEAM-INFRA-05 | Terraform fmt check passes (code is formatted per Terraform standard style). |
| CI-03 | L3-TEAM | TEAM-INFRA-06 | Terraform plan successfully applied in staging or dev environment before merge to main. |
| DR-01 | L3-TEAM | TEAM-INFRA-07 | Disaster recovery procedures verified in non-production environment if infrastructure change affects stateful services. |
| DR-02 | L3-TEAM | TEAM-INFRA-08 | Rollback plan documented and tested successfully in staging environment. |
| ACC-01 | L3-TEAM | TEAM-INFRA-09 | Engineering Manager sign-off documented in PR for changes affecting production infrastructure. |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable. |

---

## Summary by Source Policy

| Source Policy | Criteria Count | Work Types |
|---|---|---|
| ENG-4.1 | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.1-SEC | 4 | feature_story, bug_fix, api_change, infrastructure |
| ENG-4.2-SIGN | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.2-FORMAT | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.2-MERGE | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.3-COMPLEXITY | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.3-LENGTH | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.3-DEAD | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| QA-2.1-COVERAGE | 18 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| QA-2.2-UNIT | 4 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-INTEGRATION | 3 | feature_story, bug_fix, api_change |
| QA-2.2-E2E | 2 | feature_story, bug_fix |
| QA-2.3-REGRESSION | 1 | bug_fix |
| QA-2.4-PERF | 2 | feature_story, api_change |
| QA-3.1-REGRESSION-SUITE | 1 | release |
| QA-3.1-SMOKE | 1 | release |
| QA-3.1-ROLLBACK | 1 | release |
| QA-3.1-NOTES | 2 | release |
| QA-3.1-RUNBOOK | 2 | release, infrastructure |
| SEC-3.1-SNYK | 12 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| SEC-3.2-SECRETS | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| SEC-3.3-DEPS | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| SEC-4.1-TERRAFORM | 3 | infrastructure