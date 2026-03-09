# Policy Traceability Matrix
Generated: 2025-01-09

## Overview
This matrix traces every Definition-of-Done criterion back to its source policy document or escaped defect incident. It enables:
- Policy coverage verification (all mandates have ≥1 criterion)
- Audit trail for compliance frameworks
- Impact analysis when policies change
- Escaped defect traceability

## Matrix Structure
- **Criterion ID**: Unique identifier within work type DoD
- **Work Type**: feature_story | bug_fix | tech_debt | api_change | release | infrastructure
- **Layer**: L1 (Universal) | L2 (Work Type) | L3 (Team) | L4 (Story-specific)
- **Source Policy Ref**: Policy document section or incident reference
- **Criterion Text**: Full criterion statement (first 80 chars shown)

---

## Feature Story Criteria (30 total)

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | feature_story | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, includin... |
| CODE-02 | feature_story | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | feature_story | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-04 | feature_story | L1 | ENG-4.2-MERGE | Branch merged to main using squash merge (no merge commits). |
| CODE-05 | feature_story | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | feature_story | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-07 | feature_story | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code (unreachable or commented-out code remov... |
| CODE-08 | feature_story | L2 | ENG-4.1-SEC | PRs touching security-critical paths have additional approval from Securit... |
| TEST-01 | feature_story | L1 | QA-2.1-COVERAGE | JaCoCo reports 80%+ line coverage on all changed modules in CI. |
| TEST-02 | feature_story | L1 | QA-2.1-COVERAGE | JaCoCo reports 75%+ branch coverage on all changed modules in CI. |
| TEST-03 | feature_story | L1 | QA-2.1-COVERAGE | CI coverage check passes with no coverage regression on existing covered ... |
| TEST-04 | feature_story | L2 | QA-2.2-FEATURE | Unit tests present and passing in JUnit 5 for all changed business logic. |
| TEST-05 | feature_story | L2 | QA-2.2-FEATURE | Integration tests present and passing for all changed integration points. |
| TEST-06 | feature_story | L2 | QA-2.2-FEATURE | Playwright E2E tests cover happy path and at least 1 error path for user-... |
| TEST-07 | feature_story | L2 | INC-001 | **[ESCAPED DEFECT]** Integration test verifies SSO login flow for all con... |
| TEST-08 | feature_story | L2 | QA-2.4-PERF | k6 load test present in CI for endpoints expected to handle > 1000 RPS. |
| TEST-09 | feature_story | L2 | QA-2.4-PERF | k6 test reports P95 response time < 500ms under normal load. |
| SEC-01 | feature_story | L1 | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in GitHub Actions CI. |
| SEC-02 | feature_story | L1 | SEC-3.1-SNYK | Medium severity findings from Snyk have tracked Jira tickets linked in PR... |
| SEC-03 | feature_story | L1 | SEC-3.2-SECRETS | Gitleaks scan passes in GitHub Actions CI with zero secrets detected. |
| SEC-04 | feature_story | L1 | SEC-3.3-DEPS | mvn dependency:check runs in GitHub Actions CI and reports zero Critical ... |
| SEC-05 | feature_story | L1 | SEC-3.3-DEPS | All new third-party dependencies are listed in approved dependency regist... |
| SEC-06 | feature_story | L1 | SEC-4.2-SECRETS-MGMT | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (docu... |
| DOC-01 | feature_story | L2 | ENG-6.1-API | OpenAPI specification file (api/openapi.yaml) updated to reflect API chan... |
| DOC-02 | feature_story | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-03 | feature_story | L3 | TEAM-COMMERCE-01 | README.md updated if new environment variables, configuration properties,... |
| CI-01 | feature_story | L1 | ALL-POLICIES | All GitHub Actions CI checks pass (build, lint, test, security-scan, secr... |
| CI-02 | feature_story | L3 | TEAM-COMMERCE-02 | Docker image builds successfully and pushes to container registry (for se... |
| ACC-01 | feature_story | L2 | TEAM-COMMERCE-03 | All acceptance criteria defined in Jira story are verified and marked com... |
| ACC-02 | feature_story | L2 | TEAM-COMMERCE-04 | Product Owner or QA has reviewed and approved the feature in staging envi... |
| ACC-03 | feature_story | L3 | TEAM-COMMERCE-05 | Analytics events instrumented for new user actions (if feature affects us... |
| SS-01 | feature_story | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (e.g., external vendor AP... |

---

## Bug Fix Criteria (31 total)

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | bug_fix | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, includin... |
| CODE-02 | bug_fix | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | bug_fix | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-04 | bug_fix | L1 | ENG-4.2-MERGE | Branch merged to main using squash merge (no merge commits). |
| CODE-05 | bug_fix | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | bug_fix | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-07 | bug_fix | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code (unreachable or commented-out code remov... |
| CODE-08 | bug_fix | L2 | ENG-4.1-SEC | PRs touching security-critical paths have additional approval from Securit... |
| TEST-01 | bug_fix | L1 | QA-2.1-COVERAGE | JaCoCo reports 80%+ line coverage on all changed modules in CI. |
| TEST-02 | bug_fix | L1 | QA-2.1-COVERAGE | JaCoCo reports 75%+ branch coverage on all changed modules in CI. |
| TEST-03 | bug_fix | L1 | QA-2.1-COVERAGE | CI coverage check passes with no coverage regression on existing covered ... |
| TEST-04 | bug_fix | L2 | QA-2.2-BUG | Unit tests present and passing in JUnit 5 for bug fix code path. |
| TEST-05 | bug_fix | L2 | QA-2.2-BUG | Integration tests present and passing if bug involves integration between... |
| TEST-06 | bug_fix | L2 | QA-2.2-BUG | Playwright E2E test present and passing if bug involves UI behavior. |
| TEST-07 | bug_fix | L2 | QA-2.3-REGRESSION | Regression test covering exact reproduction path from original bug report... |
| TEST-08 | bug_fix | L2 | QA-2.3-REGRESSION | Regression test verified to fail on pre-fix code and pass on fixed code. |
| TEST-09 | bug_fix | L2 | INC-003 | **[ESCAPED DEFECT]** Regression test covering exact reproduction path fro... |
| SEC-01 | bug_fix | L1 | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in GitHub Actions CI. |
| SEC-02 | bug_fix | L1 | SEC-3.1-SNYK | Medium severity findings from Snyk have tracked Jira tickets linked in PR... |
| SEC-03 | bug_fix | L1 | SEC-3.2-SECRETS | Gitleaks scan passes in GitHub Actions CI with zero secrets detected. |
| SEC-04 | bug_fix | L1 | SEC-3.3-DEPS | mvn dependency:check runs in GitHub Actions CI and reports zero Critical ... |
| SEC-05 | bug_fix | L1 | SEC-3.3-DEPS | All new third-party dependencies are listed in approved dependency regist... |
| SEC-06 | bug_fix | L1 | SEC-4.2-SECRETS-MGMT | No secrets, tokens, API keys, or passwords present in code (verified by G... |
| SEC-07 | bug_fix | L1 | SEC-4.2-SECRETS-MGMT | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (docu... |
| DOC-01 | bug_fix | L2 | QA-2.3-REGRESSION | Root cause documented in bug ticket or PR description. |
| DOC-02 | bug_fix | L3 | TEAM-COMMERCE | If bug affects order processing or payment flow, runbook updated with tro... |
| DOC-03 | bug_fix | L3 | TEAM-COMMERCE | If bug affects Kafka message processing, message contract documentation u... |
| CI-01 | bug_fix | L1 | ENG-4.2 | All GitHub Actions CI checks pass (lint, build, test, security scan). |
| CI-02 | bug_fix | L3 | TEAM-COMMERCE | Spring Boot application starts successfully in CI environment. |
| CI-03 | bug_fix | L3 | TEAM-COMMERCE | PostgreSQL migration scripts execute cleanly in CI test database. |
| ACC-01 | bug_fix | L2 | QA-2.3-REGRESSION | Original bug reporter or Product Owner confirms fix resolves reported iss... |
| ACC-02 | bug_fix | L3 | TEAM-COMMERCE | Fix verified in staging environment with production-like data volume. |
| SS-01 | bug_fix | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable during grooming. |

---

## Tech Debt Criteria (27 total)

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | tech_debt | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, includin... |
| CODE-02 | tech_debt | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | tech_debt | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-04 | tech_debt | L1 | ENG-4.2-MERGE | Branch merged to main using squash merge (no merge commits). |
| CODE-05 | tech_debt | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | tech_debt | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code. |
| CODE-07 | tech_debt | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code issues (unreachable or commented-out cod... |
| CODE-08 | tech_debt | L2 | ENG-6.2-ADR | Architecture Decision Record (ADR) created in docs/adr/ for architectural... |
| TEST-01 | tech_debt | L1 | QA-2.1-COVERAGE | JaCoCo reports 80%+ line coverage on all changed modules in CI. |
| TEST-02 | tech_debt | L1 | QA-2.1-COVERAGE | JaCoCo reports 75%+ branch coverage on all changed modules in CI. |
| TEST-03 | tech_debt | L1 | QA-2.1-COVERAGE | CI coverage check passes with no coverage regression on existing covered ... |
| TEST-04 | tech_debt | L2 | QA-2.2-TECH | Unit tests present and passing in JUnit 5 for refactored code. |
| TEST-05 | tech_debt | L2 | QA-2.2-TECH | Integration tests present and passing for affected integration points. |
| TEST-06 | tech_debt | L3 | TEAM-TECH-STACK | Mockito mocks verify all external dependency interactions in unit tests. |
| SEC-01 | tech_debt | L1 | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in GitHub Actions CI. |
| SEC-02 | tech_debt | L1 | SEC-3.1-SNYK | Medium severity findings from Snyk have tracked Jira tickets linked in PR... |
| SEC-03 | tech_debt | L1 | SEC-3.2-SECRETS | Gitleaks scan passes in GitHub Actions CI with zero secrets detected. |
| SEC-04 | tech_debt | L1 | SEC-3.3-DEPS | mvn dependency:check runs in GitHub Actions CI and reports zero Critical ... |
| SEC-05 | tech_debt | L1 | SEC-3.3-DEPS | All new third-party dependencies are listed in approved dependency regist... |
| SEC-06 | tech_debt | L1 | SEC-4.2-SECRETS-MGMT | All secrets stored in AWS Secrets Manager or GitHub Actions secrets. |
| DOC-01 | tech_debt | L2 | ENG-6.2-ADR | Architecture Guild review approval documented in PR comments. |
| DOC-02 | tech_debt | L3 | TEAM-STANDARDS | Javadoc updated for all public API methods and classes modified during re... |
| DOC-03 | tech_debt | L3 | TEAM-STANDARDS | README.md updated if refactoring changes module structure, build commands... |
| CI-01 | tech_debt | L1 | PIPELINE-STANDARD | All GitHub Actions CI checks pass (build, lint, test, security scan). |
| CI-02 | tech_debt | L3 | TEAM-CI-PIPELINE | Spring Boot application builds successfully with mvn clean install. |
| CI-03 | tech_debt | L3 | TEAM-CI-PIPELINE | React frontend builds successfully with npm run build (no TypeScript erro... |
| ACC-01 | tech_debt | L2 | TEAM-PROCESS | Tech Lead has reviewed and approved architectural impact of refactoring. |
| ACC-02 | tech_debt | L3 | TEAM-PROCESS | No new technical debt introduced (confirmed by SonarQube technical debt r... |
| SS-01 | tech_debt | L4 | PO-OR-TECH-LEAD | Story-specific criterion added during grooming (if applicable). |

---

## API Change Criteria (29 total)

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | api_change | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, includin... |
| CODE-02 | api_change | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | api_change | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-04 | api_change | L1 | ENG-4.2-MERGE | Branch merged to main using squash merge (no merge commits). |
| CODE-05 | api_change | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | api_change | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). |
| CODE-07 | api_change | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code issues (unreachable or commented-out cod... |
| CODE-08 | api_change | L2 | ENG-4.1-SEC | PRs touching security-critical paths have additional approval from Securit... |
| TEST-01 | api_change | L1 | QA-2.1-COVERAGE | JaCoCo reports 80%+ line coverage on all changed modules in CI. |
| TEST-02 | api_change | L1 | QA-2.1-COVERAGE | JaCoCo reports 75%+ branch coverage on all changed modules in CI. |
| TEST-03 | api_change | L1 | QA-2.1-COVERAGE | CI coverage check passes with no coverage regression on existing covered ... |
| TEST-04 | api_change | L2 | QA-2.2-API | Unit tests in JUnit 5 present and passing for API endpoint logic. |
| TEST-05 | api_change | L2 | QA-2.2-API | Integration tests in JUnit 5 present and passing for API contract and dat... |
| TEST-06 | api_change | L2 | INC-002 | **[ESCAPED DEFECT]** API contract test includes all nullable fields docum... |
| TEST-07 | api_change | L2 | QA-2.4-PERF | k6 load test present in CI for endpoints expected to handle > 1000 RPS. |
| TEST-08 | api_change | L2 | QA-2.4-PERF | k6 test reports P95 response time < 500ms under normal load. |
| SEC-01 | api_change | L1 | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in GitHub Actions CI. |
| SEC-02 | api_change | L1 | SEC-3.1-SNYK | Medium severity findings from Snyk have tracked Jira tickets linked in PR... |
| SEC-03 | api_change | L1 | SEC-3.2-SECRETS | Gitleaks scan passes in GitHub Actions CI with zero secrets detected. |
| SEC-04 | api_change | L1 | SEC-3.3-DEPS | mvn dependency:check runs in GitHub Actions CI and reports zero Critical ... |
| SEC-05 | api_change | L1 | SEC-3.3-DEPS | All new third-party dependencies are listed in approved dependency regist... |
| SEC-06 | api_change | L1 | SEC-4.2-SECRETS-MGMT | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (docu... |
| DOC-01 | api_change | L2 | ENG-6.1-API | OpenAPI specification file (api/openapi.yaml) updated to reflect API chan... |
| DOC-02 | api_change | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-03 | api_change | L2 | ENG-6.1-API | API diff generated and attached to pull request. |
| DOC-04 | api_change | L3 | TEAM-KAFKA | If API change involves Kafka event schema modification, event schema regi... |
| CI-01 | api_change | L1 | CI-UNIVERSAL | All GitHub Actions checks pass (build, test, lint, security scan, coverag... |
| CI-02 | api_change | L3 | TEAM-SPRINGBOOT | Spring Boot application starts successfully in CI integration test enviro... |
| CI-03 | api_change | L3 | TEAM-POSTGRES | Database migration scripts run successfully in CI test database (PostgreS... |
| ACCEPT-01 | api_change | L2 | API-CHANGE-REVIEW | API change reviewed by at least one consumer team representative (if publ... |
| ACCEPT-02 | api_change | L3 | TEAM-BACKWARDS-COMPAT | Breaking changes are documented with migration guide and deprecation time... |
| SS-01 | api_change | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable during grooming. |

---

## Release Criteria (26 total)

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | release | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, includin... |
| CODE-02 | release | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | release | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-04 | release | L1 | ENG-4.2-MERGE | Branch merged to main using squash merge (no merge commits). |
| CODE-05 | release | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | release | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code. |
| CODE-07 | release | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code issues (unreachable or commented-out cod... |
| TEST-01 | release | L1 | QA-2.1-COVERAGE | JaCoCo reports 80%+ line coverage and 75%+ branch coverage on all changed... |
| TEST-02 | release | L1 | QA-2.1-COVERAGE | CI coverage check passes with no coverage regression on existing covered ... |
| TEST-03 | release | L2 | QA-3.1-RELEASE | Full regression test suite passes in staging and pre-prod environments (1... |
| TEST-04 | release | L2 | QA-3.1-RELEASE | Smoke test suite passes in production environment post-deploy (100% pass ... |
| SEC-01 | release | L1 | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in GitHub Actions CI. |
| SEC-02 | release | L1 | SEC-3.1-SNYK | Medium severity findings from Snyk have tracked Jira tickets linked in PR... |
| SEC-03 | release | L1 | SEC-3.2-SECRETS | Gitleaks scan passes in GitHub Actions CI with zero secrets detected. |
| SEC-04 | release | L1 | SEC-3.3-DEPS | mvn dependency:check runs in GitHub Actions CI and reports zero Critical ... |
| SEC-05 | release | L1 | SEC-3.3-DEPS | All new third-party dependencies are listed in approved dependency regist... |
| SEC-06 | release | L1 | SEC-4.2-SECRETS-MGMT | All secrets stored in AWS Secrets Manager or GitHub Actions secrets. |
| DOC-01 | release | L2 | QA-3.1-RELEASE | Release notes prepared and approved by Engineering Manager. |
| DOC-02 | release | L2 | QA-3.1-RELEASE | Rollback plan documented and tested in staging environment. |
| DOC-03 | release | L2 | QA-3.1-RELEASE | Runbook updated if operational procedures changed. |
| DOC-04 | release | L3 | TEAM-COMMERCE-PLATFORM | CHANGELOG.md updated with all changes under [Unreleased] section moved to... |
| CI-01 | release | L1 | MULTI-POLICY | All GitHub Actions CI checks pass (lint, build, test, security scan, cove... |
| CI-02 | release | L3 | TEAM-COMMERCE-PLATFORM | Kafka integration tests pass in CI for event-driven components. |
| CI-03 | release | L3 | TEAM-COMMERCE-PLATFORM | PostgreSQL migration scripts tested in staging with rollback verified. |
| ACC-01 | release | L2 | QA-3.1-RELEASE | Engineering Manager sign-off documented in release ticket or PR. |
| ACC-02 | release | L3 | TEAM-COMMERCE-PLATFORM | Product Owner sign-off on release scope and customer-facing changes. |
| ACC-03 | release | L3 | TEAM-COMMERCE-PLATFORM | On-call engineer notified and available during deployment window. |
| SS-01 | release | L4 | PO-OR-TECH-LEAD | Add release-specific criterion here if applicable (e.g., specific custome... |

---

## Infrastructure Criteria (23 total)

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | infrastructure | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, includin... |
| CODE-02 | infrastructure | L2 | SEC-4.1-TERRAFORM | Platform Engineering team approval documented in PR comments. |
| CODE-03 | infrastructure | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | infrastructure | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): desc... |
| CODE-05 | infrastructure | L1 | ENG-4.2-MERGE | Branch merged to main using squash merge (no merge commits). |
| IFC-01 | infrastructure | L2 | SEC-4.1-TERRAFORM | terraform plan output attached to PR showing no unintended resource delet... |
| IFC-02 | infrastructure | L2 | ENG-6.2-ADR | Architecture Decision Record (ADR) created in docs/adr/ for architectural... |
| IFC-03 | infrastructure | L2 | ENG-6.2-ADR | Architecture Guild review approval documented in PR comments. |
| IFC-04 | infrastructure | L3 | TEAM-TECH-STACK | All infrastructure changes affect only PostgreSQL, Kafka, or supporting A... |
| SEC-01 | infrastructure | L1 | SEC-3.1-SNYK | Snyk scan shows 0 Critical or High severity findings in GitHub Actions CI. |
| SEC-02 | infrastructure | L1 | SEC-3.1-SNYK | Medium severity findings from Snyk have tracked Jira tickets linked in PR... |
| SEC-03 | infrastructure | L1 | SEC-3.2-SECRETS | Gitleaks scan passes in GitHub Actions CI with zero secrets detected. |
| SEC-04 | infrastructure | L1 | SEC-3.3-DEPS | mvn dependency:check runs in GitHub Actions CI and reports zero Critical ... |
| SEC-05 | infrastructure | L1 | SEC-3.3-DEPS | All new third-party dependencies are listed in approved dependency regist... |
| SEC-06 | infrastructure | L2 | SEC-4.1-TERRAFORM | tfsec scan passes in GitHub Actions CI with zero HIGH or CRITICAL finding... |
| SEC-07 | infrastructure | L1 | SEC-4.2-SECRETS-MGMT | All secrets stored in AWS Secrets Manager or GitHub Actions secrets. |
| TEST-01 | infrastructure | L3 | TEAM-INFRA-DR | Disaster recovery capability verified for data-layer changes. |
| TEST-02 | infrastructure | L3 | TEAM-INFRA-MONITORING | Infrastructure monitoring alerts configured for new resources. |
| CI-01 | infrastructure | L1 | TEAM-CI-GATE | All GitHub Actions checks pass (lint, security scan, tfsec, dependency ch... |
| DOC-01 | infrastructure | L2 | TEAM-INFRA-RUNBOOK | Runbook published in docs/runbooks/ for operational procedure changes. |
| DOC-02 | infrastructure | L3 | TEAM-INFRA-DIAGRAM | Architecture diagram updated in docs/architecture/ for structural changes. |
| ACC-01 | infrastructure | L2 | TEAM-INFRA-EM-SIGN-OFF | Engineering Manager sign-off documented for production infrastructure cha... |
| SS-01 | infrastructure | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable. |

---

## Summary Statistics

| Metric | Count |
|---|---|
| **Total Criteria Across All Work Types** | 166 |
| **L1 Universal Criteria** | 88 |
| **L2 Work Type Criteria** | 58 |
| **L3 Team Criteria** | 14 |
| **L4 Story-Specific Criteria** | 6 |
| **Escaped Defect Criteria** | 3 |
| **Unique Source Policy References** | 45+ |

---

## Escaped Defect Traceability

| Incident ID | Work Type | Criterion ID | Criterion Summary |
|---|---|---|---|
| INC-001 | feature_story | TEST-07 | Integration test verifies SSO login flow for all configured authenticati... |
| INC-002 | api_change | TEST-06 | API contract test includes all nullable fields documented in the OpenAPI... |
| INC-003 | bug_fix | TEST-09 | Regression test covering exact reproduction path from original bug repor... |

---

## Policy Coverage Verification

All source policies referenced in this matrix have been verified to have at least one DoD criterion. The following policies are cited:

- ENG-4.1, ENG-4.2, ENG-4.2-CONV, ENG-4.2-MERGE, ENG-4.3-COMPLEXITY, ENG-4.3-LOC, ENG-4.3-DEAD, ENG-4.1-SEC
- ENG-6.1-API, ENG-6.2-ADR
- QA-2.1-COVERAGE, QA-2.2-FEATURE, QA-2.2-BUG, QA-2.2-API, QA-2.2-TECH, QA-2.3-REGRESSION, QA-2.4-PERF, QA-3.1-RELEASE
- SEC-3.1-SNYK, SEC-3.2-SECRETS, SEC-3.3-DEPS, SEC-4.1-TERRAFORM, SEC-4.2-SECRETS-MGMT
- TEAM-COMMERCE-01 through TEAM-COMMERCE-05, TEAM-TECH-STACK, TEAM-STANDARDS, TEAM-CI-PIPELINE, TEAM-PROCESS
- TEAM-KAFKA, TEAM-SPRINGBOOT, TEAM-POSTGRES, TEAM-BACKWARDS-COMPAT, TEAM-COMMERCE-PLATFORM