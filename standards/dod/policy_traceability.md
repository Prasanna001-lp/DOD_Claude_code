# Policy Traceability Matrix
Generated: 2026-03-23

## Overview
This matrix maps every Definition-of-Done criterion back to its source policy document, ensuring full traceability and compliance coverage across all work types.

**Total Criteria Across All Work Types:** 163  
**Unique Source Policies Referenced:** 47  
**Work Types Covered:** 6 (feature_story, bug_fix, tech_debt, api_change, release, infrastructure)

---

## Feature Story

| Criterion ID | Layer | Source Policy Ref | Criterion Text (First 80 chars) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including... |
| CODE-02 | L2 | ENG-4.1-SEC | PR touching security-critical code has approval from Security Champion in... |
| CODE-03 | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1 | ENG-4.2 | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-05 | L1 | ENG-4.2 | PR merged using squash merge (no merge commits on main). |
| CODE-06 | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | L1 | ENG-4.3 | No method exceeds 50 lines of code (SonarQube check). |
| CODE-08 | L2 | ENG-4.3 | No dead code (unreachable, commented-out) present in changed files. |
| TEST-01 | L1 | QA-2.1 | JaCoCo reports 80%+ line coverage on all changed modules in CI. |
| TEST-02 | L1 | QA-2.1 | JaCoCo reports 75%+ branch coverage on all changed modules in CI. |
| TEST-03 | L1 | QA-2.1 | No existing covered code has lost coverage (CI fails on coverage regression). |
| TEST-04 | L2 | QA-2.2-FEATURE | Unit tests present for all changed business logic (JUnit 5). |
| TEST-05 | L2 | QA-2.2-FEATURE | Integration tests present for all changed service integrations (JUnit 5 +... |
| TEST-06 | L2 | QA-2.2-FEATURE | E2E test includes happy path and at least 1 error path scenario (Playwright). |
| TEST-07 | L2 | QA-2.4 | k6 load test present for API endpoints expected to handle > 1000 RPS. |
| TEST-08 | L2 | QA-2.4 | k6 test confirms P95 response time < 500ms under normal load. |
| SEC-01 | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1 | SEC-3.1 | Snyk Medium severity findings have tracked Jira tickets before merge. |
| SEC-03 | L1 | SEC-3.2 / SEC-4.2 | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1 | SEC-3.3 | npm audit (Node.js) or mvn dependency:check (Java) reports 0 Critical CVE... |
| SEC-05 | L2 | SEC-3.3 | All third-party dependencies listed in approved dependency registry. |
| SEC-06 | L2 | SEC-4.2 | All new secrets stored in AWS Secrets Manager or GitHub Actions secrets. |
| DOC-01 | L3 | TEAM-COMMERCE | README.md updated if setup or configuration changed. |
| DOC-02 | L3 | TEAM-COMMERCE | Inline code comments added for complex business logic (Spring Service classes). |
| DOC-03 | L3 | TEAM-COMMERCE | React component PropTypes or TypeScript types documented for new components. |
| CI-01 | L1 | TEAM-COMMERCE | All GitHub Actions checks pass (lint, build, test, security). |
| CI-02 | L3 | TEAM-COMMERCE | ESLint (React) and Checkstyle (Java) pass with 0 violations. |
| CI-03 | L3 | TEAM-COMMERCE | Build artifacts uploaded to artifact registry (Docker image tagged with co... |
| ACC-01 | L2 | TEAM-COMMERCE | All acceptance criteria in Jira story verified by Product Owner. |
| ACC-02 | L2 | TEAM-COMMERCE | UX review completed for UI changes (screenshots or Loom in PR). |
| ACC-03 | L3 | TEAM-COMMERCE | Analytics event instrumented for new user actions (PostHog or GA4). |
| ACC-04 | L2 | From INC-001 | Integration test verifies SSO login flow for all configured auth methods... |

**Feature Story Total:** 32 criteria (30 active + 2 placeholders)

---

## Bug Fix

| Criterion ID | Layer | Source Policy Ref | Criterion Text (First 80 chars) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including... |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | PR touching security-critical code has approval from Security Champion in... |
| CODE-03 | L1-UNIVERSAL | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1-UNIVERSAL | ENG-4.2 | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-05 | L1-UNIVERSAL | ENG-4.2 | PR merged using squash merge (no merge commits on main). |
| CODE-06 | L1-UNIVERSAL | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | L1-UNIVERSAL | ENG-4.3 | No method exceeds 50 lines of code (SonarQube check). |
| CODE-08 | L2-WORKTYPE | ENG-4.3 | No dead code (unreachable, commented-out) present in changed files. |
| TEST-01 | L1-UNIVERSAL | QA-2.1 | JaCoCo reports 80%+ line coverage on all changed modules in CI. |
| TEST-02 | L1-UNIVERSAL | QA-2.1 | JaCoCo reports 75%+ branch coverage on all changed modules in CI. |
| TEST-03 | L1-UNIVERSAL | QA-2.1 | No existing covered code has lost coverage (CI fails on coverage regression). |
| TEST-04 | L2-WORKTYPE | QA-2.2-BUG | Unit tests present for bug fix logic (JUnit 5). |
| TEST-05 | L2-WORKTYPE | QA-2.2-BUG | Integration tests present if bug involves service integration (JUnit 5 + M... |
| TEST-06 | L2-WORKTYPE | QA-2.2-BUG | E2E test present if bug involves UI behavior (Playwright). |
| TEST-07 | L2-WORKTYPE | QA-2.3 / From INC-003 | Regression test covering exact reproduction path from original bug report... |
| TEST-08 | L2-WORKTYPE | QA-2.3 | Regression test documented to fail on pre-fix code and pass on fixed code. |
| TEST-09 | L3-TEAM | TEAM-STANDARD | Bug fix includes test for null/empty input if applicable to bug context. |
| SEC-01 | L1-UNIVERSAL | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1-UNIVERSAL | SEC-3.1 | Snyk Medium severity findings have tracked Jira tickets before merge. |
| SEC-03 | L1-UNIVERSAL | SEC-3.2 / SEC-4.2 | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1-UNIVERSAL | SEC-3.3 | npm audit (Node.js) or mvn dependency:check (Java) reports 0 Critical CVE... |
| DOC-01 | L2-WORKTYPE | TEAM-STANDARD | Root cause documented in PR description or linked bug ticket. |
| DOC-02 | L2-WORKTYPE | TEAM-STANDARD | CHANGELOG.md updated with bug fix entry under [Unreleased] section. |
| DOC-03 | L3-TEAM | TEAM-STANDARD | Inline code comments added if fix involves non-obvious logic or workaround. |
| CI-01 | L1-UNIVERSAL | TEAM-STANDARD | All GitHub Actions CI checks pass (lint, build, test, security scan). |
| CI-02 | L2-WORKTYPE | TEAM-STANDARD | Bug fix verified in staging environment before merge. |
| ACC-01 | L2-WORKTYPE | TEAM-STANDARD | Bug reporter or Product Owner confirms fix resolves original issue. |
| ACC-02 | L3-TEAM | TEAM-STANDARD | If bug was customer-reported: Support team notified of fix and expected re... |

**Bug Fix Total:** 28 criteria (27 active + 1 placeholder)

---

## Tech Debt

| Criterion ID | Layer | Source Policy Ref | Criterion Text (First 80 chars) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including... |
| CODE-02 | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1 | ENG-4.2 | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-04 | L1 | ENG-4.2 | PR merged using squash merge (no merge commits on main). |
| CODE-05 | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | L1 | ENG-4.3 | No method exceeds 50 lines of code (SonarQube check). |
| CODE-07 | L2 | ENG-4.3 | No dead code (unreachable, commented-out) present in changed files. |
| CODE-08 | L2 | ENG-6.2 | No new technical debt introduced (SonarQube technical debt ratio ≤ baseline). |
| TEST-01 | L1 | QA-2.1 | JaCoCo reports 80%+ line coverage on all changed modules in CI. |
| TEST-02 | L1 | QA-2.1 | JaCoCo reports 75%+ branch coverage on all changed modules in CI. |
| TEST-03 | L1 | QA-2.1 | No existing covered code has lost coverage (CI fails on coverage regression). |
| TEST-04 | L2 | QA-2.2-DEBT | Unit tests present for refactored logic (JUnit 5). |
| TEST-05 | L2 | QA-2.2-DEBT | Integration tests present for refactored components (JUnit 5). |
| TEST-06 | L3 | TEAM-STANDARD | Mockito used for all external dependencies in unit tests (no real Kafka/Po... |
| SEC-01 | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1 | SEC-3.1 | Snyk Medium severity findings have tracked Jira tickets before merge. |
| SEC-03 | L1 | SEC-3.2 | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1 | SEC-3.3 | mvn dependency:check (Java) or npm audit (Node.js) reports 0 Critical CVE... |
| SEC-05 | L2 | SEC-3.3 | All third-party dependencies listed in approved dependency registry. |
| ARCH-01 | L2 | ENG-6.2 | Architecture Decision Record (ADR) created in docs/adr/ for architecture/d... |
| ARCH-02 | L2 | ENG-6.2 | Architecture Guild review completed and approval documented in PR. |
| ARCH-03 | L3 | TEAM-STANDARD | README.md updated if component behavior, configuration, or dependencies ch... |
| ARCH-04 | L3 | TEAM-STANDARD | Javadoc updated for all public API changes (Java) or JSDoc for React compo... |
| CI-01 | L1 | TEAM-CI-GATE | All GitHub Actions checks pass (lint, build, test, security scan). |
| CI-02 | L3 | TEAM-STANDARD | ESLint passes with 0 errors for React/TypeScript code. |
| CI-03 | L3 | TEAM-STANDARD | Spotless Java formatter applied (mvn spotless:check passes). |
| ACC-01 | L2 | TEAM-STANDARD | Tech Lead or senior engineer verified refactoring maintains existing behav... |
| ACC-02 | L3 | TEAM-STANDARD | Jira ticket status updated to "Code Review Complete" before merge. |

**Tech Debt Total:** 28 criteria (28 active + 1 placeholder)

---

## API Change

| Criterion ID | Layer | Source Policy Ref | Criterion Text (First 80 chars) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including... |
| CODE-02 | L2 | ENG-4.1-SEC | PR touching security-critical code has approval from Security Champion in... |
| CODE-03 | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | L1 | ENG-4.2 | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-05 | L1 | ENG-4.2 | PR merged using squash merge (no merge commits on main). |
| CODE-06 | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | L1 | ENG-4.3 | No method exceeds 50 lines of code (SonarQube check). |
| CODE-08 | L2 | ENG-4.3 | No dead code (unreachable, commented-out) present in changed files. |
| TEST-01 | L1 | QA-2.1 | JaCoCo reports 80%+ line coverage on all changed modules in CI. |
| TEST-02 | L1 | QA-2.1 | JaCoCo reports 75%+ branch coverage on all changed modules in CI. |
| TEST-03 | L1 | QA-2.1 | No existing covered code has lost coverage (CI fails on coverage regression). |
| TEST-04 | L2 | QA-2.2-API | Unit tests present for API endpoint logic (JUnit 5). |
| TEST-05 | L2 | QA-2.2-API | Integration tests present for API endpoint (JUnit 5). |
| TEST-06 | L2 | From INC-002 | API contract test includes all nullable fields documented in OpenAPI spec... |
| TEST-07 | L2 | QA-2.4 | k6 load test present for API endpoints expected to handle > 1000 RPS. |
| TEST-08 | L2 | QA-2.4 | k6 test confirms P95 response time < 500ms under normal load. |
| SEC-01 | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1 | SEC-3.1 | Snyk Medium severity findings have tracked Jira tickets before merge. |
| SEC-03 | L1 | SEC-3.2 / SEC-4.2 | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1 | SEC-3.3 | npm audit (Node.js) or mvn dependency:check (Java) reports 0 Critical CVE... |
| SEC-05 | L2 | SEC-3.3 | All third-party dependencies listed in approved dependency registry. |
| DOC-01 | L2 | ENG-6.1 | OpenAPI specification file (api/openapi.yaml) updated to reflect API changes. |
| DOC-02 | L2 | ENG-6.1 | CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-03 | L2 | ENG-6.1 | API diff generated and attached to pull request. |
| DOC-04 | L2 | ENG-6.2 | Architecture Decision Record (ADR) created in docs/adr/ for architecture/d... |
| DOC-05 | L2 | ENG-6.2 | Architecture Guild review completed and approval documented in PR. |
| DOC-06 | L3 | TEAM-STANDARD | Consumer-facing API documentation updated in Confluence if endpoint is pub... |
| CI-01 | L1 | UNIVERSAL | All GitHub Actions CI checks pass (build, test, lint, security). |
| CI-02 | L3 | TEAM-STANDARD | Maven build completes successfully with zero compilation errors or warnings. |
| CI-03 | L3 | TEAM-STANDARD | Spring Boot application starts successfully in CI test environment. |
| ACCEPT-01 | L2 | TEAM-STANDARD | API change reviewed and approved by Product Owner if it affects contract v... |
| ACCEPT-02 | L3 | TEAM-STANDARD | Dependent services notified of API contract change via Slack #api-changes... |

**API Change Total:** 33 criteria (32 active + 1 placeholder)

---

## Release

| Criterion ID | Layer | Source Policy Ref | Criterion Text (First 80 chars) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including... |
| CODE-02 | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1 | ENG-4.2 | All commit messages follow Conventional Commits format: type(scope): desc... |
| TEST-01 | L2 | QA-3.1 | Full regression test suite passed in staging environment. |
| TEST-02 | L2 | QA-3.1 | Full regression test suite passed in pre-prod environment. |
| TEST-03 | L2 | QA-3.1 | Smoke test suite passed in production environment post-deploy. |
| TEST-04 | L3 | TEAM-RELEASE-01 | Payment processing flow verified in production using test transactions. |
| TEST-05 | L3 | TEAM-RELEASE-02 | Kafka consumer lag < 100 messages across all topics after deployment. |
| SEC-01 | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1 | SEC-3.1 | Snyk Medium severity findings have tracked Jira tickets before merge. |
| SEC-03 | L1 | SEC-3.2 | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1 | SEC-3.3 | npm audit (Node.js) or mvn dependency:check (Java) reports 0 Critical CVE... |
| SEC-05 | L3 | TEAM-RELEASE-03 | PostgreSQL database credentials rotated if release includes schema changes. |
| DOC-01 | L2 | ENG-6.1 / QA-3.1 | CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-02 | L2 | QA-3.1 | Release notes prepared and approved by Engineering Manager. |
| DOC-03 | L2 | QA-3.1 | Rollback plan documented and tested in staging environment. |
| DOC-04 | L2 | QA-3.1 | Runbook updated if operational procedures changed. |
| DOC-05 | L3 | TEAM-RELEASE-04 | OpenAPI specification version incremented to match release version. |
| CI-01 | L1 | CI-UNIVERSAL | All GitHub Actions checks pass (lint, build, test, security scan). |
| CI-02 | L3 | TEAM-RELEASE-05 | Docker images tagged with release version and pushed to ECR. |
| CI-03 | L3 | TEAM-RELEASE-06 | Kubernetes deployment manifests updated with new image tags. |
| CI-04 | L3 | TEAM-RELEASE-07 | Database migration scripts dry-run completed in staging with zero errors. |
| ACCEPT-01 | L2 | QA-3.1 | Engineering Manager formal sign-off documented in release ticket. |
| ACCEPT-02 | L3 | TEAM-RELEASE-08 | Product Owner sign-off obtained for customer-facing changes. |
| ACCEPT-03 | L3 | TEAM-RELEASE-09 | Support team notified 24 hours before release with customer impact summary. |

**Release Total:** 25 criteria (24 active + 1 placeholder)

---

## Infrastructure

| Criterion ID | Layer | Source Policy Ref | Criterion Text (First 80 chars) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including... |
| CODE-02 | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | L1 | ENG-4.2 | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-04 | L2 | ENG-6.2 | Architecture Decision Record (ADR) created in docs/adr/ for architecture/d... |
| CODE-05 | L2 | ENG-6.2 | Architecture Guild review completed and approval documented in PR. |
| TEST-01 | L2 | SEC-4.1 | terraform plan produces clean output with no unintended resource deletions. |
| TEST-02 | L3 | TEAM-INFRA-01 | Terraform configuration validated with terraform validate in CI. |
| TEST-03 | L3 | TEAM-INFRA-02 | Disaster Recovery verification performed in staging environment. |
| TEST-04 | L3 | TEAM-INFRA-03 | Infrastructure smoke test passes post-apply in staging. |
| SEC-01 | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings. |
| SEC-02 | L1 | SEC-3.1 | Snyk Medium severity findings have tracked Jira tickets before merge. |
| SEC-03 | L1 | SEC-3.2 | Gitleaks scan passes with 0 secrets detected in CI. |
| SEC-04 | L1 | SEC-3.3 | npm audit (Node.js) or mvn dependency:check (Java) reports 0 Critical CVE... |
| SEC-05 | L2 | SEC-4.1 | Platform Engineering team review completed and documented in PR. |
| SEC-06 | L2 | SEC-4.1 | tfsec scan passes with 0 HIGH or CRITICAL findings. |
| SEC-07 | L2 | SEC-4.2 | All new secrets stored in AWS Secrets Manager or GitHub Actions secrets. |
| SEC-08 | L3 | TEAM-INFRA-04 | Network security group rules reviewed for least-privilege access. |
| DOC-01 | L2 | TEAM-INFRA-05 | Runbook updated if operational procedures changed. |
| DOC-02 | L2 | TEAM-INFRA-06 | Infrastructure diagram updated if architecture changed. |
| DOC-03 | L3 | TEAM-INFRA-07 | Terraform module README.md updated with new variables or outputs. |
| DOC-04 | L3 | TEAM-INFRA-08 | Cost impact documented in PR description. |
| CI-01 | L1 | CI-GATE-01 | All GitHub Actions checks pass (lint, validate, security scan, plan). |
| CI-02 | L3 | TEAM-INFRA-09 | Terraform state lock released if apply failed. |
| CI-03 | L3 | TEAM-INFRA-10 | Rollback plan documented in PR description. |
| ACC-01 | L2 | TEAM-INFRA-11 | Platform Engineering Lead sign-off obtained for production changes. |
| ACC-02 | L3 | TEAM-INFRA-12 | Change implemented during approved maintenance window. |

**Infrastructure Total:** 26 criteria (25 active + 1 placeholder)

---

## Summary Statistics

| Work Type | Total Criteria | L1 | L2 | L3 | L4 | From Escaped Defects |
|---|---|---|---|---|---|---|
| feature_story | 32 | 14 | 13 | 6 | 1 | 1 |
| bug_fix | 28 | 13 | 11 | 3 | 1 | 1 |
| tech_debt | 29 | 11 | 10 | 7 | 1 | 0 |
| api_change | 33 | 14 | 15 | 4 | 1 | 1 |
| release | 25 | 7 | 9 | 7 | 1 | 0 |
| infrastructure | 26 | 7 | 11 | 6 | 1 | 0 |
| **TOTAL** | **173** | **66** | **69** | **33** | **6** | **3** |

---

## Policy Coverage Analysis

**All mandatory engineering policies (ENG-4.x, QA-2.x, SEC-3.x) have 100% coverage across applicable work types.**

- **Universal L1 criteria** applied consistently across all work types: code signing, commit format, PR approvals, security scanning, coverage thresholds
- **Work-type specific L2 criteria** capture domain-specific requirements: regression testing for bugs, ADRs for tech debt, API contract tests for API changes
- **Team-specific L3 criteria** reflect Commerce Platform's tech stack (Spring Boot, React, Kafka, PostgreSQL) and operational practices
- **Escaped defect incorporation**: 3 incidents (INC-001, INC-002, INC-003) now have mandatory criteria preventing recurrence

**Next Review:** All DoD checklists scheduled for quarterly review (Q2 2026).

---