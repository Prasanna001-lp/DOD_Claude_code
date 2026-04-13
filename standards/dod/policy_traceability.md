# Policy Traceability Matrix
Generated: 2025-01-13

## Overview
This matrix provides complete traceability from every Definition-of-Done criterion to its source policy or standard document. Use this matrix to:
- Verify policy compliance coverage
- Identify criteria affected by policy changes
- Support audit and compliance reviews

---

## Feature Story Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | feature_story | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | feature_story | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | feature_story | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | feature_story | L1 | ENG-4.2-MERGE | PR uses squash merge strategy (merge commits prohibited on main). |
| CODE-05 | feature_story | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes: cyclomatic complexity ≤10 per method. |
| CODE-06 | feature_story | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-07 | feature_story | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations (unreachable or commented-out code removed). |
| CODE-08 | feature_story | L2 | ENG-4.1-SEC | PR touching security-critical code paths has approval from Security Champion. |
| TEST-01 | feature_story | L1 | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-02 | feature_story | L1 | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on changed modules in CI. |
| TEST-03 | feature_story | L1 | QA-2.1-REGRESS | CI coverage check passes: no existing covered code has lost coverage. |
| TEST-04 | feature_story | L2 | QA-2.2-UNIT | Unit tests present using JUnit 5 and Mockito, covering changed code paths. |
| TEST-05 | feature_story | L2 | QA-2.2-INTEG-STORY | Integration tests present using JUnit 5, covering service interactions. |
| TEST-06 | feature_story | L2 | QA-2.2-E2E | E2E tests present using Playwright: happy path scenario + minimum 1 error path. |
| TEST-07 | feature_story | L2 | QA-2.4-PERF-P95 | k6 load test reports P95 response time <500ms under normal load. |
| TEST-08 | feature_story | L2 | QA-2.4-PERF-P99 | k6 load test reports P99 response time <2000ms under normal load. |
| SEC-01 | feature_story | L1 | SEC-3.1-SNYK | Snyk scan in CI reports 0 Critical or High severity findings. |
| SEC-02 | feature_story | L1 | SEC-3.1-MED | All Medium severity Snyk findings have tracked Jira tickets linked in PR description. |
| SEC-03 | feature_story | L1 | SEC-3.2-SECRETS | Gitleaks scan in CI passes with 0 secrets detected. |
| SEC-04 | feature_story | L1 | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) report 0 Critical CVEs in CI. |
| SEC-05 | feature_story | L1 | SEC-4.2-NO-SECRETS | Gitleaks pre-commit hook and CI check confirm no secrets in version control. |
| DOC-01 | feature_story | L2 | ENG-6.1-API | OpenAPI specification file (api/openapi.yaml) updated to reflect API changes. |
| DOC-02 | feature_story | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-03 | feature_story | L3 | TEAM-KAFKA | Kafka event schema documented in docs/events/ if new event types introduced. |
| DOC-04 | feature_story | L3 | TEAM-POSTGRES | Database migration scripts follow Flyway naming convention (V{version}__{description}.sql) in db/migration/. |
| CI-01 | feature_story | L1 | MULTI | All GitHub Actions CI checks pass: lint, build, unit tests, integration tests, security scans. |
| CI-02 | feature_story | L2 | TEAM-SPRING | Spring Boot application starts successfully in CI environment (actuator /health returns 200). |
| ACC-01 | feature_story | L2 | AGILE-AC | All acceptance criteria defined in the story description are verified and passing. |
| ACC-02 | feature_story | L2 | AGILE-UX | UX review completed if story involves UI changes (design mockup alignment verified). |
| ACC-03 | feature_story | L3 | TEAM-ANALYTICS | Analytics event tracking implemented if feature requires product metrics (GA4/Segment). |
| ACC-04 | feature_story | L2 | INC-001 | Integration test verifies SSO login flow for all configured authentication methods. (FROM ESCAPED DEFECT) |
| SS-01 | feature_story | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (e.g., specific 3rd party API integration verified, edge case X tested). |

---

## Bug Fix Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | bug_fix | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | bug_fix | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | bug_fix | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | bug_fix | L1 | ENG-4.2-MERGE | PR uses squash merge strategy (merge commits prohibited on main). |
| CODE-05 | bug_fix | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes: cyclomatic complexity ≤10 per method. |
| CODE-06 | bug_fix | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-07 | bug_fix | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations (unreachable or commented-out code removed). |
| CODE-08 | bug_fix | L2 | ENG-4.1-SEC | PR touching security-critical code paths has approval from Security Champion. |
| TEST-01 | bug_fix | L1 | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-02 | bug_fix | L1 | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on changed modules in CI. |
| TEST-03 | bug_fix | L1 | QA-2.1-REGRESS | CI coverage check passes: no existing covered code has lost coverage. |
| TEST-04 | bug_fix | L2 | QA-2.2-UNIT | Unit tests present using JUnit 5 and Mockito, covering changed code paths. |
| TEST-05 | bug_fix | L2 | QA-2.3-REGR, INC-003 | Regression test covering exact reproduction path from original bug report is present in CI, verified to fail pre-fix and pass post-fix. (FROM ESCAPED DEFECT) |
| TEST-06 | bug_fix | L2 | QA-2.2-INTEG-BUG | Integration tests present using JUnit 5 if bug involves service-to-service interaction (Kafka, PostgreSQL, REST calls). |
| TEST-07 | bug_fix | L2 | QA-2.2-E2E-UI-BUG | E2E test present using Playwright if bug affects UI workflow (React components). |
| TEST-08 | bug_fix | L3 | TEAM-KAFKA | If bug involves Kafka message handling, test includes verification of message ordering and idempotency. |
| SEC-01 | bug_fix | L1 | SEC-3.1-SNYK | Snyk scan in CI reports 0 Critical or High severity findings. |
| SEC-02 | bug_fix | L1 | SEC-3.1-MED | All Medium severity Snyk findings have tracked Jira tickets linked in PR description. |
| SEC-03 | bug_fix | L1 | SEC-3.2-SECRETS | Gitleaks scan in CI passes with 0 secrets detected. |
| SEC-04 | bug_fix | L1 | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) report 0 Critical CVEs in CI. |
| SEC-05 | bug_fix | L1 | SEC-4.2-NO-SECRETS | Gitleaks pre-commit hook and CI check confirm no secrets in version control. |
| DOC-01 | bug_fix | L2 | BUGFIX-ROOT-CAUSE | Root cause analysis documented in PR description including why bug occurred and what prevents recurrence. |
| DOC-02 | bug_fix | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] section if bug fix affects user-facing behavior or API contract. |
| DOC-03 | bug_fix | L3 | TEAM-POSTGRES | If bug fix includes database migration (Flyway/Liquibase), migration script reviewed by Database Admin and rollback script provided. |
| CI-01 | bug_fix | L1 | CI-ALL-CHECKS | All GitHub Actions checks pass: build, lint, test, coverage, security scan, SonarQube quality gate. |
| CI-02 | bug_fix | L2 | BUGFIX-DEPLOY-VERIFY | Bug fix verified in staging environment using exact reproduction steps from original bug report before production deployment. |
| ACC-01 | bug_fix | L2 | BUGFIX-REPORTER-VERIFY | Bug reporter or QA engineer confirms bug fix resolves original issue in staging environment. |
| ACC-02 | bug_fix | L2 | BUGFIX-NO-SIDE-EFFECTS | Code reviewer confirms no unintended side effects introduced (other features still function correctly). |
| SS-01 | bug_fix | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (defined during grooming). |

---

## Tech Debt Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | tech_debt | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | tech_debt | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | tech_debt | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | tech_debt | L1 | ENG-4.2-MERGE | PR uses squash merge strategy (merge commits prohibited on main). |
| CODE-05 | tech_debt | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes: cyclomatic complexity ≤10 per method. |
| CODE-06 | tech_debt | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-07 | tech_debt | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations (unreachable or commented-out code removed). |
| CODE-08 | tech_debt | L3 | TEAM-JAVA-SPRING | Spring Boot application context starts successfully with all auto-configurations loaded. |
| TEST-01 | tech_debt | L1 | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-02 | tech_debt | L1 | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on changed modules in CI. |
| TEST-03 | tech_debt | L1 | QA-2.1-REGRESS | CI coverage check passes: no existing covered code has lost coverage. |
| TEST-04 | tech_debt | L2 | QA-2.2-UNIT | Unit tests present using JUnit 5 and Mockito, covering changed code paths. |
| TEST-05 | tech_debt | L3 | TEAM-KAFKA | Kafka consumer/producer changes include embedded Kafka integration tests verifying message serialization. |
| SEC-01 | tech_debt | L1 | SEC-3.1-SNYK | Snyk scan in CI reports 0 Critical or High severity findings. |
| SEC-02 | tech_debt | L1 | SEC-3.1-MED | All Medium severity Snyk findings have tracked Jira tickets linked in PR description. |
| SEC-03 | tech_debt | L1 | SEC-3.2-SECRETS | Gitleaks scan in CI passes with 0 secrets detected. |
| SEC-04 | tech_debt | L1 | SEC-4.2-NO-SECRETS | Gitleaks pre-commit hook and CI check confirm no secrets in version control. |
| SEC-05 | tech_debt | L1 | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) report 0 Critical CVEs in CI. |
| DOC-01 | tech_debt | L2 | ENG-6.2-ARCH | Architecture Decision Record (ADR) created in docs/adr/ directory if tech debt involves structural changes. |
| DOC-02 | tech_debt | L2 | ENG-6.2-ARCH | PR has approval from at least 1 member of Architecture Guild if ADR required. |
| DOC-03 | tech_debt | L3 | TEAM-STANDARDS | README.md updated if tech debt changes build process, deployment steps, or local dev setup. |
| DOC-04 | tech_debt | L3 | TEAM-JAVA-SPRING | JavaDoc updated for public APIs if method signatures or contracts changed. |
| CI-01 | tech_debt | L1 | CI-GATE | All GitHub Actions workflows pass: build, test, lint, security scans. |
| CI-02 | tech_debt | L1 | SONARQUBE-GATE | SonarQube quality gate passes with no new code smells, bugs, or vulnerabilities introduced. |
| CI-03 | tech_debt | L3 | TEAM-JAVA-BUILD | Maven build completes with "BUILD SUCCESS" message; no compilation warnings in changed modules. |
| TD-01 | tech_debt | L2 | TECH-DEBT-POLICY | Root cause of technical debt documented in Jira ticket description or linked ADR. |
| TD-02 | tech_debt | L2 | TECH-DEBT-POLICY | No new technical debt introduced by this change (SonarQube technical debt metric does not increase). |
| TD-03 | tech_debt | L3 | TEAM-POSTGRES | Database migration scripts tested in staging with rollback script verified if schema changes included. |
| ACCEPT-01 | tech_debt | L2 | TECH-LEAD-SIGN-OFF | Tech Lead has reviewed and approved the refactoring approach. |
| ACCEPT-02 | tech_debt | L3 | TEAM-RETRO | Lessons learned from this tech debt item documented for next retrospective if root cause was process-related. |
| SS-01 | tech_debt | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (e.g., specific performance benchmark, migration validation step). |

---

## API Change Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | api_change | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | api_change | L2 | ENG-4.1-SEC | PR touching security-critical code paths has approval from Security Champion. |
| CODE-03 | api_change | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | api_change | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | api_change | L1 | ENG-4.2-MERGE | PR uses squash merge strategy (merge commits prohibited on main). |
| CODE-06 | api_change | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes: cyclomatic complexity ≤10 per method. |
| CODE-07 | api_change | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-08 | api_change | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations (unreachable or commented-out code removed). |
| TEST-01 | api_change | L1 | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. |
| TEST-02 | api_change | L1 | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on changed modules in CI. |
| TEST-03 | api_change | L1 | QA-2.1-REGRESS | CI coverage check passes: no existing covered code has lost coverage. |
| TEST-04 | api_change | L2 | QA-2.2-UNIT | Unit tests present using JUnit 5 and Mockito, covering changed code paths. |
| TEST-05 | api_change | L2 | QA-2.2-INTEG-STORY | Integration tests present using JUnit 5, covering service interactions. |
| TEST-06 | api_change | L2 | INC-002 | API contract tests include test cases for all nullable fields defined in OpenAPI spec. (FROM ESCAPED DEFECT) |
| TEST-07 | api_change | L2 | QA-2.4-PERF-P95 | k6 load test reports P95 response time <500ms under normal load. |
| TEST-08 | api_change | L2 | QA-2.4-PERF-P99 | k6 load test reports P99 response time <2000ms under normal load. |
| SEC-01 | api_change | L1 | SEC-3.1-SNYK | Snyk scan in CI reports 0 Critical or High severity findings. |
| SEC-02 | api_change | L1 | SEC-3.1-MED | All Medium severity Snyk findings have tracked Jira tickets linked in PR description. |
| SEC-03 | api_change | L1 | SEC-3.2-SECRETS | Gitleaks scan in CI passes with 0 secrets detected. |
| SEC-04 | api_change | L1 | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) report 0 Critical CVEs in CI. |
| SEC-05 | api_change | L1 | SEC-4.2-NO-SECRETS | Gitleaks pre-commit hook and CI check confirm no secrets in version control. |
| DOC-01 | api_change | L2 | ENG-6.1-API | OpenAPI specification file (api/openapi.yaml) updated to reflect API changes. |
| DOC-02 | api_change | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-03 | api_change | L2 | ENG-6.1-API | API diff document generated and attached to PR as comment or file. |
| DOC-04 | api_change | L2 | ENG-6.2-ARCH | Architecture Decision Record (ADR) created in docs/adr/ directory (if structural API change). |
| DOC-05 | api_change | L2 | ENG-6.2-ARCH | PR has approval from at least 1 member of Architecture Guild (if structural API change). |
| DOC-06 | api_change | L3 | TEAM-KAFKA | If API change affects Kafka event schemas, event schema registry updated with new version. |
| CI-01 | api_change | L1 | CI-UNIVERSAL | All GitHub Actions checks pass (build, lint, test, security scan). |
| CI-02 | api_change | L3 | TEAM-SPRING | Spring Boot application starts successfully in CI test environment. |
| CI-03 | api_change | L3 | TEAM-REACT | React build completes successfully with 0 TypeScript errors (if frontend API integration affected). |
| ACC-01 | api_change | L2 | API-STAKEHOLDER | API consumers notified of breaking changes with minimum 1 sprint advance notice. |
| ACC-02 | api_change | L3 | TEAM-POSTMAN | Postman collection updated with new/modified endpoints and example requests. |
| SS-01 | api_change | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable during grooming. |

---

## Release Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | release | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | release | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | release | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | release | L1-UNIVERSAL | ENG-4.2-MERGE | PR uses squash merge strategy (merge commits prohibited on main). |
| TEST-01 | release | L2-WORKTYPE | QA-3.1-REG-SUITE | Full regression test suite passes in staging and pre-prod environments. |
| TEST-02 | release | L2-WORKTYPE | QA-3.1-SMOKE | Smoke test suite passes in production environment post-deployment. |
| TEST-03 | release | L3-TEAM | TEAM-COMMERCE-001 | Payment gateway integration tests pass in pre-prod using sandbox credentials. |
| TEST-04 | release | L3-TEAM | TEAM-COMMERCE-002 | Kafka event schema compatibility verified using schema registry validation. |
| SEC-01 | release | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan in CI reports 0 Critical or High severity findings. |
| SEC-02 | release | L1-UNIVERSAL | SEC-3.1-MED | All Medium severity Snyk findings have tracked Jira tickets linked in PR description. |
| SEC-03 | release | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan in CI passes with 0 secrets detected. |
| SEC-04 | release | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) report 0 Critical CVEs in CI. |
| SEC-05 | release | L3-TEAM | TEAM-COMMERCE-003 | PCI-DSS compliance verification: no cardholder data stored in application logs or database. |
| DOC-01 | release | L2-WORKTYPE | QA-3.1-NOTES | Release notes document prepared and approved by Engineering Manager. |
| DOC-02 | release | L2-WORKTYPE | QA-3.1-ROLLBACK | Rollback plan documented in runbook and tested successfully in staging. |
| DOC-03 | release | L2-WORKTYPE | QA-3.1-RUNBOOK | Runbook updated if operational procedures changed (verified in docs/runbooks/ directory). |
| DOC-04 | release | L3-TEAM | TEAM-COMMERCE-004 | Monitoring dashboard links verified in runbook for all Commerce Platform services. |
| CI-01 | release | L1-UNIVERSAL | ENG-4.3-COMPLEX | SonarQube quality gate passes: cyclomatic complexity ≤10 per method. |
| CI-02 | release | L1-UNIVERSAL | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). |
| CI-03 | release | L1-UNIVERSAL | ENG-4.3-DEAD | SonarQube reports zero dead code violations (unreachable or commented-out code removed). |
| CI-04 | release | L3-TEAM | TEAM-COMMERCE-005 | Database migration scripts reviewed and tested in pre-prod with rollback verification. |
| CI-05 | release | L3-TEAM | TEAM-COMMERCE-006 | Deployment pipeline "blue-green" or "canary" strategy validated in staging. |
| ACCEPT-01 | release | L2-WORKTYPE | QA-3.1-NOTES | Engineering Manager has approved release via PR approval. |
| ACCEPT-02 | release | L3-TEAM | TEAM-COMMERCE-007 | Product Owner sign-off: release scope matches sprint commitment documented in Jira. |
| ACCEPT-03 | release | L3-TEAM | TEAM-COMMERCE-008 | On-call engineer notified and confirmed deployment window availability. |
| SS-01 | release | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable during grooming. |

---

## Infrastructure Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | infrastructure | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | infrastructure | L1-UNIVERSAL | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | infrastructure | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-04 | infrastructure | L1-UNIVERSAL | ENG-4.2-MERGE | PR uses squash merge strategy (merge commits prohibited on main). |
| SEC-01 | infrastructure | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk scan in CI reports 0 Critical or High severity findings. |
| SEC-02 | infrastructure | L1-UNIVERSAL | SEC-3.1-MED | All Medium severity Snyk findings have tracked Jira tickets linked in PR description. |
| SEC-03 | infrastructure | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan in CI passes with 0 secrets detected. |
| SEC-04 | infrastructure | L1-UNIVERSAL | SEC-4.2-NO-SECRETS | Gitleaks pre-commit hook and CI check confirm no secrets in version control. |
| SEC-05 | infrastructure | L2-WORKTYPE | SEC-4.1-TFSEC | tfsec scan in CI reports 0 HIGH or CRITICAL findings. |
| SEC-06 | infrastructure | L2-WORKTYPE | ENG-4.1-SEC | PR touching security-critical infrastructure (IAM, network rules, encryption) has approval from Security Champion. |
| IFC-01 | infrastructure | L2-WORKTYPE | SEC-4.1-TF-PLAN | terraform plan output attached to PR showing no unintended resource deletions. |
| IFC-02 | infrastructure | L2-WORKTYPE | SEC-4.1-TF-REVIEW | PR has approval from at least 1 member of Platform Engineering team. |
| IFC-03 | infrastructure | L3-TEAM | TEAM-TECH-STACK | Terraform code follows Commerce Platform module structure (modules/ directory, consistent naming). |
| IFC-04 | infrastructure | L3-TEAM | TEAM-TECH-STACK | Infrastructure changes affecting PostgreSQL or Kafka clusters include capacity review. |
| TEST-01 | infrastructure | L3-TEAM | TEAM-INFRA-VALIDATION | terraform validate passes with 0 errors on all modified modules. |
| TEST-02 | infrastructure | L3-TEAM | TEAM-INFRA-VALIDATION | terraform fmt check passes (all .tf files formatted consistently). |
| DOC-01 | infrastructure | L2-WORKTYPE | ENG-6.2-ARCH | Architecture Decision Record (ADR) created in docs/adr/ directory for structural infrastructure changes. |
| DOC-02 | infrastructure | L2-WORKTYPE | ENG-6.2-ARCH | PR has approval from at least 1 member of Architecture Guild for structural changes. |
| DOC-03 | infrastructure | L2-WORKTYPE | QA-3.1-RUNBOOK | Runbook updated if operational procedures changed (verified in docs/runbooks/ directory). |
| DOC-04 | infrastructure | L3-TEAM | TEAM-INFRA-DOCS | Terraform module README.md updated with input/output variable changes. |
| DR-01 | infrastructure | L3-TEAM | TEAM-DR-POLICY | Infrastructure changes affecting stateful resources (databases, queues) include disaster recovery verification. |
| DR-02 | infrastructure | L3-TEAM | TEAM-DR-POLICY | Multi-AZ or multi-region changes verified in staging environment before production apply. |
| CI-01 | infrastructure | L1-UNIVERSAL | ENG-CI-GATE | All GitHub Actions workflow checks pass (lint, validate, security scan, tfsec, Gitleaks). |
| CI-02 | infrastructure | L2-WORKTYPE | INFRA-APPLY-GATE | terraform apply only proceeds after manual approval in staging environment. |
| ACC-01 | infrastructure | L2-WORKTYPE | INFRA-PROD-GATE | Infrastructure changes to production require Engineering Manager sign-off before merge. |
| ACC-02 | infrastructure | L3-TEAM | TEAM-CHANGE-WINDOW | Production infrastructure changes scheduled during approved change window (Tuesday/Thursday 10am-2pm EST). |
| SS-01 | infrastructure | L4-STORY | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (e.g., specific compliance requirement, vendor integration validation). |

---

## Summary Statistics

| Work Type | Total Criteria | L1 Count | L2 Count | L3 Count | L4 Count | Escaped Defect Count |
|---|---|---|---|---|---|---|
| feature_story | 32 | 13 | 15 | 3 | 1 | 1 |
| bug_fix | 28 | 13 | 13 | 2 | 1 | 1 |
| tech_debt | 30 | 13 | 10 | 6 | 1 | 0 |
| api_change |