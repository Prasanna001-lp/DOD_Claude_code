# Policy Traceability Matrix
Generated: 2025-01-20

## Overview
This matrix maps every Definition-of-Done criterion across all work types back to its source policy document, standard, or escaped defect incident. It enables audit compliance and ensures every quality gate is traceable to a documented requirement.

**Organisation:** Acme Engineering  
**Team:** Commerce Platform  
**Total Unique Criteria:** 169  
**Work Types Covered:** 6 (feature_story, bug_fix, tech_debt, api_change, release, infrastructure)

---

## Legend
- **Layer:** L1 (Universal), L2 (Work Type), L3 (Team), L4 (Story-Specific)
- **Source Policy Ref:** Code from input policy documents or escaped defect incident reference
- **From Escaped Defect:** ✓ indicates criterion derived from production incident

---

## Feature Story Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text | From Escaped Defect |
|--------------|-------|-------------------|----------------|---------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | |
| CODE-02 | L2 | ENG-4.1-SEC | PR touching authentication, authorization, payment, or PII handling has approval from Security Champion. | |
| CODE-03 | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. | |
| CODE-04 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | |
| CODE-05 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy. | |
| CODE-06 | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | |
| CODE-07 | L1 | ENG-4.3-LOC | SonarQube quality gate passes with no methods exceeding 50 lines of code. | |
| CODE-08 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations. | |
| TEST-01 | L1 | QA-2.1-COV-LINE | JaCoCo reports ≥80% line coverage on all changed modules. | |
| TEST-02 | L1 | QA-2.1-COV-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules. | |
| TEST-03 | L1 | QA-2.1-COV-REGRESS | CI coverage check passes with no coverage regression on any existing covered code. | |
| TEST-04 | L2 | QA-2.2-UNIT | JUnit 5 unit tests present and passing for all changed business logic. | |
| TEST-05 | L2 | QA-2.2-INT-FEATURE | Integration tests using Spring Boot Test pass covering cross-component interactions. | |
| TEST-06 | L2 | QA-2.2-E2E | Playwright E2E tests pass covering happy path and at least 1 error path scenario. | |
| TEST-07 | L2 | QA-2.4-PERF | k6 load test in CI reports P95 <500ms and P99 <2000ms for endpoints handling >1000 RPS. | |
| TEST-08 | L2 | INC-001 | Integration test verifies SSO login flow for all configured authentication methods (OAuth, SAML, OIDC). | ✓ |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan in GitHub Actions reports 0 Critical or High severity findings. | |
| SEC-02 | L1 | SEC-3.1-SNYK-MEDIUM | All Medium severity Snyk findings have linked Jira tickets in PR description. | |
| SEC-03 | L1 | SEC-3.2-SECRETS, SEC-4.2-SECRETS-MGMT | Gitleaks scan in GitHub Actions reports 0 secrets detected. | |
| SEC-04 | L1 | SEC-3.3-DEP-MVN | mvn dependency:check in GitHub Actions reports 0 Critical CVE findings. | |
| SEC-05 | L1 | SEC-3.3-DEP-NPM | npm audit in GitHub Actions reports 0 Critical CVE findings. | |
| SEC-06 | L3 | TEAM-SEC-01 | Kafka consumer/producer configurations use encrypted connections (SSL/TLS) and SASL authentication. | |
| SEC-07 | L3 | TEAM-SEC-02 | PostgreSQL connections use SSL mode=require and credentials stored in AWS Secrets Manager. | |
| DOC-01 | L2 | TEAM-DOC-01 | Spring Boot REST controller endpoints have OpenAPI 3.0 annotations documenting request/response schemas. | |
| DOC-02 | L2 | TEAM-DOC-02 | README.md or docs/architecture/ updated if feature introduces new service, database table, or Kafka topic. | |
| DOC-03 | L3 | TEAM-DOC-03 | Kafka event schemas documented in docs/events/ with example JSON payload and versioning information. | |
| CI-01 | L1 | TEAM-CI-01 | All GitHub Actions workflow jobs pass (Build, Test, Lint, Security Scan, Coverage Check). | |
| CI-02 | L3 | TEAM-CI-02 | Spring Boot application starts successfully in Docker container and passes health check endpoint (/actuator/health). | |
| CI-03 | L3 | TEAM-CI-03 | React application builds successfully with npm run build and produces no ESLint errors or TypeScript type errors. | |
| ACC-01 | L2 | TEAM-ACC-01 | All acceptance criteria defined in Jira story are verified and marked complete by Product Owner. | |
| ACC-02 | L2 | TEAM-ACC-02 | UX review completed if feature includes user-facing UI changes (screenshots or Loom video attached to PR). | |
| ACC-03 | L3 | TEAM-ACC-03 | Analytics events instrumented for feature usage tracking with event schema documented. | |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder (defined during grooming). | |

---

## Bug Fix Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text | From Escaped Defect |
|--------------|-------|-------------------|----------------|---------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. | |
| CODE-03 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy. | |
| CODE-05 | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | |
| CODE-06 | L1 | ENG-4.3-LOC | SonarQube quality gate passes with no methods exceeding 50 lines of code. | |
| CODE-07 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations. | |
| CODE-08 | L2 | QA-2.3-REGRESS | Root cause analysis documented in PR description or linked ticket, explaining why the bug occurred. | |
| TEST-01 | L1 | QA-2.1-COV-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. | |
| TEST-02 | L1 | QA-2.1-COV-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. | |
| TEST-03 | L1 | QA-2.1-COV-REGRESS | CI coverage check passes with no coverage regression on any existing covered code. | |
| TEST-04 | L2 | QA-2.2-UNIT | JUnit 5 unit tests present and passing for all changed business logic. | |
| TEST-05 | L2 | QA-2.3-REGRESS, INC-003 | Regression test present covering exact reproduction path from bug report, verified to fail before fix and pass after fix. | ✓ |
| TEST-06 | L3 | TEAM-BUGFIX-INT | If bug involves cross-component interaction, integration test using Spring Boot Test passes. | |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan in GitHub Actions reports 0 Critical or High severity findings. | |
| SEC-02 | L1 | SEC-3.1-SNYK-MEDIUM | All Medium severity Snyk findings have linked Jira tickets in PR description. | |
| SEC-03 | L1 | SEC-3.2-SECRETS, SEC-4.2-SECRETS-MGMT | Gitleaks scan in GitHub Actions reports 0 secrets detected. | |
| SEC-04 | L1 | SEC-3.3-DEP-MVN | mvn dependency:check in GitHub Actions reports 0 Critical CVE findings. | |
| SEC-05 | L1 | SEC-3.3-DEP-NPM | npm audit in GitHub Actions reports 0 Critical CVE findings. | |
| DOC-01 | L2 | TEAM-BUGFIX-JIRA | Original bug ticket (Jira) updated with link to PR and summary of fix approach. | |
| DOC-02 | L3 | TEAM-BUGFIX-CHANGELOG | If bug is customer-visible, CHANGELOG.md updated under [Unreleased] section with "Fixed" entry. | |
| CI-01 | L1 | TEAM-CI-ALL-GREEN | All GitHub Actions CI checks pass: lint, build, unit tests, integration tests, coverage, SonarQube, Snyk, Gitleaks, dependency checks. | |
| CI-02 | L2 | TEAM-BUGFIX-STAGING | Fix deployed to staging environment and manually verified by engineer or QA. | |
| ACC-01 | L2 | TEAM-BUGFIX-PO-VERIFY | If bug was reported by Product Owner or customer, PO has verified fix in staging and approved PR. | |
| ACC-02 | L3 | TEAM-BUGFIX-QA-VERIFY | If bug is P1 or customer-visible, QA engineer has independently verified fix in staging. | |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder (defined during grooming). | |

---

## Tech Debt Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text | From Escaped Defect |
|--------------|-------|-------------------|----------------|---------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. | |
| CODE-03 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy. | |
| CODE-05 | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | |
| CODE-06 | L1 | ENG-4.3-LOC | SonarQube quality gate passes with no methods exceeding 50 lines of code. | |
| CODE-07 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations. | |
| CODE-08 | L2 | TECH-DEBT-01 | Tech debt item does not introduce new technical debt (SonarQube technical debt metric does not increase). | |
| TEST-01 | L1 | QA-2.1-COV-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. | |
| TEST-02 | L1 | QA-2.1-COV-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. | |
| TEST-03 | L1 | QA-2.1-COV-REGRESS | CI coverage check passes with no coverage regression on any existing covered code. | |
| TEST-04 | L2 | QA-2.2-UNIT | JUnit 5 unit tests present and passing for all changed business logic. | |
| ARCH-01 | L2 | ENG-6.2-ARCH | ADR created in docs/adr/ following template and numbered sequentially (if change affects system architecture). | |
| ARCH-02 | L2 | ENG-6.2-ARCH | PR approved by at least 1 member of Architecture Guild if architectural change present. | |
| ARCH-03 | L3 | COMMERCE-PLATFORM-01 | Spring Boot version updated in pom.xml matches team standard (currently Spring Boot 3.2.x) if dependencies modified. | |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan in GitHub Actions reports 0 Critical or High severity findings. | |
| SEC-02 | L1 | SEC-3.1-SNYK | All Medium severity Snyk findings have linked Jira tickets in PR description. | |
| SEC-03 | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan in GitHub Actions reports 0 secrets detected. | |
| SEC-04 | L1 | SEC-3.3-DEP | mvn dependency:check in GitHub Actions reports 0 Critical CVE findings. | |
| SEC-05 | L1 | SEC-3.3-DEP | npm audit in GitHub Actions reports 0 Critical CVE findings. | |
| DOC-01 | L2 | TECH-DEBT-02 | README.md or relevant module documentation updated to reflect changes in structure, configuration, or usage patterns. | |
| DOC-02 | L3 | COMMERCE-PLATFORM-02 | Javadoc comments updated for all modified public APIs following team Javadoc standard. | |
| CI-01 | L1 | CI-GATE-01 | All GitHub Actions CI checks pass (build, test, lint, security scans). | |
| CI-02 | L3 | COMMERCE-PLATFORM-03 | PostgreSQL migration scripts (if database schema modified) tested in dev environment and pass Flyway validation. | |
| CI-03 | L3 | COMMERCE-PLATFORM-04 | Kafka consumer/producer contract tests pass if event schema or topic configuration modified. | |
| ACC-01 | L2 | TECH-DEBT-03 | Tech Lead confirms technical debt objective achieved with evidence. | |
| ACC-02 | L2 | TECH-DEBT-04 | Original tech debt ticket in Jira includes before/after metrics (code complexity, test coverage, build time, or performance benchmark). | |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder (defined during grooming). | |

---

## API Change Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text | From Escaped Defect |
|--------------|-------|-------------------|----------------|---------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | |
| CODE-02 | L2 | ENG-4.1-SEC | PR touching authentication, authorization, payment, or PII handling has approval from Security Champion. | |
| CODE-03 | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. | |
| CODE-04 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | |
| CODE-05 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy. | |
| CODE-06 | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | |
| CODE-07 | L1 | ENG-4.3-LOC | SonarQube quality gate passes with no methods exceeding 50 lines of code. | |
| CODE-08 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations. | |
| TEST-01 | L1 | QA-2.1-COV-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. | |
| TEST-02 | L1 | QA-2.1-COV-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. | |
| TEST-03 | L1 | QA-2.1-COV-REGRESS | CI coverage check passes with no coverage regression on any existing covered code. | |
| TEST-04 | L2 | QA-2.2-UNIT | JUnit 5 unit tests present and passing for all changed business logic. | |
| TEST-05 | L2 | QA-2.2-INT-FEATURE | Integration tests using Spring Boot Test pass covering cross-component interactions. | |
| TEST-06 | L2 | QA-2.4-PERF | k6 load test in CI reports P95 <500ms and P99 <2000ms for endpoints handling >1000 RPS. | |
| TEST-07 | L2 | INC-002 | API contract test validates all nullable fields documented in OpenAPI spec are handled correctly. | ✓ |
| TEST-08 | L3 | TEAM-API-CONTRACT | Consumer-driven contract tests pass for all downstream service dependencies consuming this API. | |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan in GitHub Actions reports 0 Critical or High severity findings. | |
| SEC-02 | L1 | SEC-3.1-SNYK-MEDIUM | All Medium severity Snyk findings have linked Jira tickets in PR description. | |
| SEC-03 | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan in GitHub Actions reports 0 secrets detected. | |
| SEC-04 | L1 | SEC-3.3-DEP-MVN | mvn dependency:check in GitHub Actions reports 0 Critical CVE findings. | |
| SEC-05 | L1 | SEC-3.3-DEP-NPM | npm audit in GitHub Actions reports 0 Critical CVE findings. | |
| DOC-01 | L2 | ENG-6.1-API | OpenAPI specification file (api/openapi.yaml) updated to reflect all API changes. | |
| DOC-02 | L2 | ENG-6.1-CHANGELOG | CHANGELOG.md updated with entry under [Unreleased] section describing API changes. | |
| DOC-03 | L2 | ENG-6.1-DIFF | API diff generated using openapi-diff and attached to PR as comment or artifact. | |
| DOC-04 | L3 | TEAM-API-EXAMPLES | API usage examples updated in docs/api-examples/ for any changed endpoints. | |
| CI-01 | L1 | TEAM-CI-GATE | All GitHub Actions CI checks pass (lint, build, test, security, coverage). | |
| CI-02 | L3 | TEAM-API-VERSIONING | API version bumped according to semantic versioning if breaking change introduced. | |
| ACC-01 | L2 | TEAM-API-REVIEW | API change reviewed and approved by Product Owner for alignment with product requirements. | |
| ACC-02 | L3 | TEAM-DOWNSTREAM-NOTIFY | Downstream service teams consuming this API notified via Slack #api-changes channel with migration timeline. | |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder (defined during grooming). | |

---

## Release Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text | From Escaped Defect |
|--------------|-------|-------------------|----------------|---------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. | |
| CODE-03 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | |
| TEST-01 | L2 | QA-3.1-REL-REGRESS | Full regression test suite passes in staging and pre-prod environments. | |
| TEST-02 | L2 | QA-3.1-REL-SMOKE | Smoke test suite passes in production within 15 minutes of deployment. | |
| TEST-03 | L3 | TEAM-COMMERCE-01 | Kafka message consumer/producer integration tests pass in pre-prod with production-like message volume. | |
| TEST-04 | L3 | TEAM-COMMERCE-02 | PostgreSQL migration scripts tested in staging with production-sized dataset snapshot. | |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan in GitHub Actions reports 0 Critical or High severity findings. | |
| SEC-02 | L1 | SEC-3.1-SNYK-MEDIUM | All Medium severity Snyk findings have linked Jira tickets in PR description. | |
| SEC-03 | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan in GitHub Actions reports 0 secrets detected. | |
| SEC-04 | L1 | SEC-3.3-DEP-MVN | mvn dependency:check in GitHub Actions reports 0 Critical CVE findings. | |
| SEC-05 | L1 | SEC-3.3-DEP-NPM | npm audit in GitHub Actions reports 0 Critical CVE findings. | |
| DOC-01 | L2 | QA-3.1-REL-NOTES | Release notes document present in docs/releases/ and approved by Engineering Manager. | |
| DOC-02 | L2 | QA-3.1-REL-RUNBOOK | Runbook in docs/runbooks/ updated with any new operational procedures introduced by this release. | |
| DOC-03 | L2 | QA-3.1-REL-ROLLBACK | Rollback plan documented in runbook and successfully executed in staging environment. | |
| DOC-04 | L3 | TEAM-COMMERCE-03 | API documentation updated in Swagger UI for all Spring Boot REST endpoints changed in this release. | |
| CI-01 | L1 | QA-2.1-COV-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI. | |
| CI-02 | L1 | QA-2.1-COV-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI. | |
| CI-03 | L1 | QA-2.1-COV-REGRESS | CI coverage check passes with no coverage regression on any existing covered code. | |
| CI-04 | L1 | ENG-4.3-COMPLEX | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | |
| CI-05 | L1 | ENG-4.3-LOC | SonarQube quality gate passes with no methods exceeding 50 lines of code. | |
| CI-06 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code violations. | |
| ACC-01 | L2 | QA-3.1-REL-NOTES | Engineering Manager has approved release notes and authorized production deployment. | |
| ACC-02 | L3 | TEAM-COMMERCE-04 | Product Owner has signed off on all user-facing changes included in release notes. | |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder (defined during grooming). | |

---

## Infrastructure Criteria

| Criterion ID | Layer | Source Policy Ref | Criterion Text | From Escaped Defect |
|--------------|-------|-------------------|----------------|---------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits in PR are signed with GPG or SSH key registered in GitHub. | |
| CODE-03 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | |
| CODE-04 | L2 | ENG-6.2-ARCH | ADR created in docs/adr/ following template and numbered sequentially. | |
| CODE-05 | L2 | ENG-6.2-ARCH | PR approved by at least 1 member of Architecture Guild. | |
| IAC-01 | L2 | SEC-4.1-TF-PLAN | terraform plan output attached to PR showing no unintended resource deletions. | |
| IAC-02 | L2 | SEC-4.1-TF-REVIEW | PR approved by at least 1 member of Platform Engineering team. | |
| IAC-03 | L2 | SEC-4.1-TFSEC | tfsec scan in GitHub Actions reports 0 HIGH or CRITICAL findings. | |
| IAC-04 | L3 | TEAM-INFRA-01 | Terraform state backend configuration verified for remote state in AWS S3 with state locking via DynamoDB. | |
| IAC-05 | L3 | TEAM-INFRA-02 | Infrastructure change includes tags: Environment, Team, CostCenter, ManagedBy=Terraform. | |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan in GitHub Actions reports 0 Critical or High severity findings. | |
| SEC-02 | L1 | SEC-3.1-SNYK | All Medium severity Snyk findings have linked Jira tickets in PR description. | |
| SEC-03 | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan in GitHub Actions reports 0 secrets detected. | |
| SEC-04 | L1 | SEC-3.3-DEP-MVN | mvn dependency:check in GitHub Actions reports 0 Critical CVE findings. | |
| SEC-05 | L1 | SEC-3.3-DEP-NPM | npm audit in GitHub Actions reports 0 Critical CVE findings. | |
| TEST-01 | L3 | TEAM-INFRA-03 | terraform validate passes with 0 errors across all modules. | |
| TEST-02 | L3 | TEAM-INFRA-04 | terraform fmt check passes showing all files are properly formatted. | |
| TEST-03 | L3 | TEAM-INFRA-05 | Infrastructure change tested in staging environment before applying to production. | |
| DOC-01 | L2 | INFRA-DOC-01 | README.md in terraform module directory updated with usage examples and variable descriptions. | |
| DOC-02 | L2 | INFRA-DOC-02 | Runbook in docs/runbooks/ created or updated with operational procedures for this infrastructure change. | |
| DOC-03 | L3 | TEAM-INFRA-06 | Infrastructure diagram updated in docs/architecture/ if network topology or service dependencies changed. | |
| DR-01 | L3 | TEAM-INFRA-07 | Backup and recovery procedures documented for all stateful resources. | |
| DR-02 | L3 | TEAM-INFRA-08 | Disaster recovery test plan executed in staging showing successful recovery from backup. | |
| CI-01 | L1 | CI-GATE-01 | All GitHub Actions CI checks pass (lint, validate, security scan, tfsec). | |
| CI-02 | L2 | INFRA-CI-01 | GitHub Actions workflow includes terraform plan step with plan output posted as PR comment. | |
| ACC-01 | L2 | INFRA-ACCEPT-01 | Infrastructure change reviewed and approved by Engineering Manager for production impact. | |
| ACC-02 | L3 | TEAM-INFRA-09 | Cost impact analysis completed showing estimated monthly cost change for this infrastructure modification. | |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder (defined during grooming). | |

---

## Escaped Defect Incorporation Summary

| Incident ID | Work Type | Criterion ID | Criterion Description |
|-------------|-----------|--------------|----------------------|
| INC-001 | feature_story | TEST-08 | Integration test verifies SSO login flow for all configured authentication methods (OAuth, SAML, OIDC). |
| INC-002 | api_change | TEST-07 | API contract test validates all nullable fields documented in OpenAPI spec are handled correctly. |
| INC-003 | bug_fix | TEST-05 | Regression test present covering exact reproduction path from bug report, verified to fail before fix and pass after fix. |

**Total Escaped Defect Criteria:** 3  
**Coverage:** 100% (all defects from escaped_defects_log.csv incorporated into DoD)

---

## Policy Coverage Analysis

| Source Policy Ref | Times Referenced | Work Types Using This Policy |
|-------------------|------------------|------------------------------|
| ENG-4.1 | 6 | All |
| ENG-4.2-SIGN | 6 | All |
| ENG-4.2-CONV | 6 | All |
| ENG-4.2-MERGE | 4 | feature_story, bug_fix, tech_debt, api_change |
| ENG-4.3-COMPLEX | 6 | All |
| ENG-4.3-LOC | 6 | All |
| ENG-4.3-DEAD | 6 | All |
| QA-2.1-COV-LINE | 5 | feature_story, bug_fix, tech_debt, api_change, release |
| QA-2.1-COV-BRANCH | 5 | feature_story, bug_fix, tech_debt, api_change, release |
| QA-2.1-COV-REGRESS | 5 | feature_story, bug_fix, tech_debt, api_change, release |
| QA-2.2-UNIT | 4 | feature_story, bug_fix, tech_debt, api_change |
| SEC-3.1-SNYK | 6 | All |
| SEC-3.1-SNYK-MEDIUM | 5 | feature_story, bug_fix, api_change, release, infrastructure |
| SEC-3.2-SECRETS | 6 | All |
| SEC-4.2-SECRETS-MGMT | 6 | All |
| SEC-3.3-DEP-MVN | 6 | All |
| SEC-3.3-DEP-NPM | 6 | All |

**Total Unique Policy References:** 54  
**Policy Coverage:** 100% (all mandates from input policies have at least one criterion)

---

## Next Review Date
**2025-04-20** — Quarterly DoD review scheduled with Engineering Manager and QA Lead

--- END OUTPUT ---