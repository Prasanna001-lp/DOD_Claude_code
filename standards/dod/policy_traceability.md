# Policy Traceability Matrix
Generated: 2024-12-19

## Overview
This matrix maps every DoD criterion across all work types to its source policy, enabling audit trails and compliance verification.

**Total Unique Criteria**: 162  
**Total Unique Source Policies**: 47  
**Work Types Covered**: 6 (feature_story, bug_fix, tech_debt, api_change, release, infrastructure)

---

## Feature Story

| Criterion ID | Layer | Source Policy Ref | Criterion Text (truncated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author... |
| CODE-02 | L2 | ENG-4.1-SEC | Security-critical PRs have approval from Security Champion... |
| CODE-03 | L1 | ENG-4.2-SIGNING | All commits are signed with GPG or SSH key... |
| CODE-04 | L1 | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format... |
| CODE-05 | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy... |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10... |
| CODE-07 | L2 | ENG-4.3-LENGTH | SonarQube reports 0 methods exceeding 50 lines... |
| CODE-08 | L1 | ENG-4.3-DEADCODE | SonarQube reports 0 dead code issues... |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage on all changed modules... |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage... |
| TEST-03 | L1 | QA-2.1-COVERAGE | CI build verifies no existing covered code has lost coverage... |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present for all changed production code... |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests present and passing in CI... |
| TEST-06 | L2 | QA-2.2-E2E | Playwright E2E test covers happy path... |
| TEST-07 | L2 | QA-2.2-E2E | Playwright E2E test covers at least 1 error path... |
| TEST-08 | L2 | DEFECT-INC-001 | Integration test verifies SSO login flow for all configured auth methods... |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan shows 0 Critical/High findings... |
| SEC-02 | L1 | SEC-3.1-SAST | All Medium severity Snyk findings have tracked Jira tickets... |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected... |
| SEC-04 | L1 | SEC-3.3-DEPS | npm audit or mvn dependency:check produces 0 Critical CVE findings... |
| SEC-05 | L2 | SEC-3.3-DEPS | All dependencies listed in approved dependency registry... |
| SEC-06 | L2 | SEC-4.2-SECRETS | All secrets stored in AWS Secrets Manager or GitHub Actions secrets... |
| DOC-01 | L2 | ENG-6.1-API | OpenAPI specification file updated to reflect endpoint changes... |
| DOC-02 | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased]... |
| DOC-03 | L2 | ENG-6.1-API | API diff generated and attached to pull request... |
| DOC-04 | L3 | TEAM-COMMERCE | Kafka event schema updated in docs/events/... |
| CI-01 | L1 | TEAM-CI | All GitHub Actions CI checks pass with green status... |
| CI-02 | L3 | TEAM-COMMERCE | PostgreSQL migration scripts pass flyway validation... |
| CI-03 | L3 | TEAM-COMMERCE | React component builds without errors... |
| ACC-01 | L2 | FEATURE-STORY-DEF | All acceptance criteria verified by Product Owner... |
| ACC-02 | L2 | FEATURE-STORY-DEF | UX review completed if feature includes UI changes... |
| ACC-03 | L2 | FEATURE-STORY-DEF | Analytics event tracking implemented if required... |
| ACC-04 | L2 | QA-2.4-PERF | k6 load test present for endpoints handling >1000 RPS... |

---

## Bug Fix

| Criterion ID | Layer | Source Policy Ref | Criterion Text (truncated) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author... |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | Security-critical PRs have approval from Security Champion... |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-SIGNING | All commits are signed with GPG or SSH key... |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format... |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge strategy... |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10... |
| CODE-07 | L2-WORKTYPE | ENG-4.3-LENGTH | SonarQube reports 0 methods exceeding 50 lines... |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEADCODE | SonarQube reports 0 dead code issues... |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage... |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage... |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COVERAGE | CI build verifies no existing covered code has lost coverage... |
| TEST-04 | L2-WORKTYPE | QA-2.2-UNIT | Unit tests present for all changed production code... |
| TEST-05 | L2-WORKTYPE | QA-2.2-INTEGRATION | Integration tests present and passing if bug was integration-level... |
| TEST-06 | L2-WORKTYPE | QA-2.2-E2E | Playwright E2E test present and passing if bug was UI-level... |
| TEST-07 | L2-WORKTYPE | QA-2.3-REGRESSION, DEFECT-INC-003 | Regression test covering exact reproduction path from original bug... |
| TEST-08 | L3-TEAM | TEAM-TECH-STACK | If bug involves Kafka: Mockito test verifies message serialization... |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SAST | Snyk scan shows 0 Critical or High severity findings... |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SAST | All Medium severity Snyk findings have tracked Jira tickets... |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected... |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | npm audit or mvn dependency:check produces 0 Critical CVE findings... |
| SEC-05 | L2-WORKTYPE | SEC-3.3-DEPS | All dependencies listed in approved dependency registry... |
| DOC-01 | L2-WORKTYPE | BUG-FIX-STANDARD | Root cause documented in PR description or linked post-mortem... |
| DOC-02 | L3-TEAM | TEAM-PRACTICE | If bug affects public API: CHANGELOG.md updated under [Unreleased]... |
| DOC-03 | L3-TEAM | TEAM-PRACTICE | If bug required data fix: runbook updated with incident reference... |
| CI-01 | L1-UNIVERSAL | CI-STANDARD | All GitHub Actions checks pass (build, test, lint, security)... |
| CI-02 | L3-TEAM | TEAM-CI | SonarQube quality gate status = PASSED... |
| ACC-01 | L2-WORKTYPE | BUG-FIX-STANDARD | Original bug reporter or QA verifies fix in staging before merge... |
| ACC-02 | L3-TEAM | TEAM-PRACTICE | If bug was P1 severity: post-fix monitoring plan documented... |

---

## Tech Debt

| Criterion ID | Layer | Source Policy Ref | Criterion Text (truncated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author... |
| CODE-02 | L1 | ENG-4.2-SIGNING | All commits are signed with GPG or SSH key... |
| CODE-03 | L1 | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format... |
| CODE-04 | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy... |
| CODE-05 | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10... |
| CODE-06 | L2 | ENG-4.3-LENGTH | No method exceeds 50 lines of code... |
| CODE-07 | L1 | ENG-4.3-DEADCODE | SonarQube reports 0 dead code issues... |
| CODE-08 | L3 | TEAM-TECH-STACK | No new technical debt introduced: SonarQube technical debt ratio ≤5%... |
| ARCH-01 | L2 | ENG-6.2-ADR | Architecture Decision Record created in docs/adr/... |
| ARCH-02 | L2 | ENG-6.2-ADR | Architecture Guild approval documented in PR... |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage... |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage... |
| TEST-03 | L1 | QA-2.1-COVERAGE | CI build verifies no existing covered code has lost coverage... |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present for all changed production code... |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests present and passing if tech debt affects integration points... |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan shows 0 Critical or High severity findings... |
| SEC-02 | L1 | SEC-3.1-SAST | All Medium severity Snyk findings have tracked Jira tickets... |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected... |
| SEC-04 | L1 | SEC-3.3-DEPS | Dependency vulnerability scan produces 0 Critical CVE findings... |
| SEC-05 | L2 | SEC-3.3-DEPS | All new or updated dependencies are listed in approved registry... |
| DOC-01 | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] if observable behavior affected... |
| DOC-02 | L3 | TEAM-TECH-STACK | Inline code documentation updated for modified public methods... |
| CI-01 | L1 | TEAM-CI-TOOL | All GitHub Actions CI checks pass (build, lint, test, security scan)... |
| CI-02 | L3 | TEAM-TECH-STACK | Spring Boot application starts successfully in CI environment... |
| ACC-01 | L2 | TEAM-WORKFLOW | Tech Lead has reviewed and approved reduction in technical debt metrics... |
| ACC-02 | L3 | TEAM-WORKFLOW | Jira ticket status updated to "Ready for Merge" by QA or Tech Lead... |

---

## API Change

| Criterion ID | Layer | Source Policy Ref | Criterion Text (truncated) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author... |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | Security-critical PRs have approval from Security Champion... |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-SIGNING | All commits are signed with GPG or SSH key... |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format... |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge strategy... |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10... |
| CODE-07 | L2-WORKTYPE | ENG-4.3-LENGTH | SonarQube reports 0 methods exceeding 50 lines... |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEADCODE | SonarQube reports 0 dead code issues... |
| API-01 | L2-WORKTYPE | ENG-6.1-API | OpenAPI specification file updated to reflect endpoint changes... |
| API-02 | L2-WORKTYPE | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased]... |
| API-03 | L2-WORKTYPE | ENG-6.1-API | API diff generated and attached to pull request... |
| API-04 | L2-WORKTYPE | ENG-6.2-ADR | Architecture Decision Record created if API change involves cross-service contracts... |
| API-05 | L3-TEAM | TEAM-TECH-STACK | Spring Boot @RestController or @Controller annotation present... |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥80% line coverage... |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COVERAGE | JaCoCo reports ≥75% branch coverage... |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COVERAGE | CI build verifies no existing covered code has lost coverage... |
| TEST-04 | L2-WORKTYPE | QA-2.2-UNIT | Unit tests present for all changed production code... |
| TEST-05 | L2-WORKTYPE | QA-2.2-INTEGRATION | Integration tests present and passing in CI... |
| TEST-06 | L2-WORKTYPE | DEFECT-INC-002 | API contract test includes all nullable fields documented in OpenAPI... |
| TEST-07 | L2-WORKTYPE | QA-2.4-PERF | k6 load test present for endpoints handling >1000 RPS... |
| TEST-08 | L3-TEAM | TEAM-TECH-STACK | Mockito mocks used for external dependencies in integration tests... |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SAST | Snyk scan shows 0 Critical or High severity findings... |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SAST | All Medium severity Snyk findings have tracked Jira tickets... |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected... |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | All dependencies listed in approved registry... |
| SEC-05 | L2-WORKTYPE | SEC-4.2-SECRETS | All secrets stored in AWS Secrets Manager or GitHub Actions secrets... |
| DOC-01 | L1-UNIVERSAL | ENG-GENERAL | Code comments updated where logic has changed... |
| DOC-02 | L3-TEAM | TEAM-TECH-STACK | README.md updated if API change affects local development setup... |
| CI-01 | L1-UNIVERSAL | CI-GENERAL | All GitHub Actions checks pass with green status... |
| CI-02 | L3-TEAM | TEAM-CI-TOOL | GitHub Actions workflow "API Contract Validation" passes... |
| ACC-01 | L2-WORKTYPE | TEAM-PROCESS | Product Owner or API consumer team has reviewed and approved API change... |

---

## Release

| Criterion ID | Layer | Source Policy Ref | Criterion Text (truncated) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author... |
| CODE-02 | L1-UNIVERSAL | ENG-4.2-SIGNING | All commits are signed with GPG or SSH key... |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format... |
| TEST-01 | L2-WORKTYPE | QA-3.1-RELEASE | Full regression test suite passes in staging and pre-prod... |
| TEST-02 | L2-WORKTYPE | QA-3.1-RELEASE | Smoke test suite passes in production environment post-deploy... |
| TEST-03 | L3-TEAM | TEAM-TECH-STACK | Kafka event schema compatibility verified for all changed event types... |
| TEST-04 | L3-TEAM | TEAM-TECH-STACK | Database migration tested in staging with production-equivalent data volume... |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SAST | Snyk scan shows 0 Critical or High severity findings... |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SAST | All Medium severity Snyk findings have tracked Jira tickets... |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected... |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | npm audit and mvn dependency:check produce 0 Critical CVE findings... |
| DOC-01 | L2-WORKTYPE | QA-3.1-RELEASE | Release notes prepared and approved by Engineering Manager... |
| DOC-02 | L2-WORKTYPE | QA-3.1-RELEASE | Runbook updated if operational procedures changed... |
| DOC-03 | L3-TEAM | TEAM-TECH-STACK | API documentation version incremented and published to API portal... |
| DEPLOY-01 | L2-WORKTYPE | QA-3.1-RELEASE | Rollback plan documented and tested in staging environment... |
| DEPLOY-02 | L3-TEAM | TEAM-CI-TOOL | GitHub Actions deployment workflow validated in pre-prod... |
| DEPLOY-03 | L3-TEAM | TEAM-TECH-STACK | Spring Boot health endpoints return "UP" status for all services in pre-prod... |
| DEPLOY-04 | L3-TEAM | TEAM-TECH-STACK | PostgreSQL connection pool metrics verified healthy in pre-prod... |
| CI-01 | L1-UNIVERSAL | TEAM-CI-TOOL | All GitHub Actions checks pass (lint, build, test, security scan)... |
| CI-02 | L3-TEAM | TEAM-SONARQUBE | SonarQube quality gate passes for release branch... |
| ACCEPT-01 | L2-WORKTYPE | QA-3.1-RELEASE | Engineering Manager approval documented in PR... |
| ACCEPT-02 | L3-TEAM | TEAM-DOMAIN | Product Owner sign-off obtained for all user-facing changes... |
| ACCEPT-03 | L3-TEAM | TEAM-DOMAIN | Customer Success team notified of release contents 48 hours prior... |

---

## Infrastructure

| Criterion ID | Layer | Source Policy Ref | Criterion Text (truncated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author... |
| CODE-02 | L2 | ENG-4.1-SEC | Security-critical PRs have approval from Security Champion... |
| CODE-03 | L1 | ENG-4.2-SIGNING | All commits are signed with GPG or SSH key... |
| CODE-04 | L1 | ENG-4.2-FORMAT | All commit messages follow Conventional Commits format... |
| CODE-05 | L2 | SEC-4.1-IAC | Platform Engineering team approval documented in PR... |
| IAC-01 | L2 | SEC-4.1-IAC | Terraform plan executed and shows no unintended resource deletions... |
| IAC-02 | L2 | SEC-4.1-IAC | tfsec scan passes with 0 HIGH or CRITICAL findings in CI... |
| IAC-03 | L3 | TEAM-INFRA-01 | All Terraform changes include state backend configuration... |
| IAC-04 | L3 | TEAM-INFRA-02 | Infrastructure changes affecting PostgreSQL or Kafka include migration plan... |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan shows 0 Critical or High severity findings... |
| SEC-02 | L1 | SEC-3.1-SAST | All Medium severity Snyk findings have tracked Jira tickets... |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected... |
| SEC-04 | L2 | SEC-4.2-SECRETS | All secrets stored in AWS Secrets Manager or GitHub Actions secrets... |
| SEC-05 | L1 | SEC-3.3-DEPS | npm audit or mvn dependency:check produces 0 Critical CVE findings... |
| SEC-06 | L2 | SEC-3.3-DEPS | All dependencies listed in approved dependency registry... |
| TEST-01 | L3 | TEAM-INFRA-03 | Infrastructure validation tests present and passing in CI... |
| TEST-02 | L3 | TEAM-INFRA-04 | Disaster recovery procedure verified in staging before production... |
| DOC-01 | L2 | ENG-6.2-ADR | Architecture Decision Record created in docs/adr/ for structural changes... |
| DOC-02 | L2 | ENG-6.2-ADR | Architecture Guild approval documented in PR before merge... |
| DOC-03 | L3 | TEAM-INFRA-05 | Runbook updated with operational procedures if deployment workflows changed... |
| DOC-04 | L3 | TEAM-INFRA-06 | Infrastructure diagram updated if topology or network boundaries changed... |
| CI-01 | L1 | TEAM-CI-01 | All GitHub Actions checks pass (lint, build, security scan, IaC validation)... |
| CI-02 | L2 | TEAM-INFRA-07 | Deployment plan includes blue-green or canary strategy for production changes... |
| ACC-01 | L2 | TEAM-INFRA-08 | Platform Engineering Lead sign-off documented in PR... |
| ACC-02 | L3 | TEAM-INFRA-09 | Rollback plan tested in staging environment and documented in PR... |

---

## Policy Coverage Analysis

| Source Policy | Occurrence Count | Work Types Using |
|---|---|---|
| ENG-4.1 | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.1-SEC | 4 | feature_story, bug_fix, api_change, infrastructure |
| ENG-4.2-SIGNING | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.2-FORMAT | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.2-MERGE | 5 | feature_story, bug_fix, tech_debt, api_change (no explicit merge in release/infra) |
| ENG-4.3-COMPLEXITY | 5 | feature_story, bug_fix, tech_debt, api_change (no explicit in release) |
| ENG-4.3-LENGTH | 5 | feature_story, bug_fix, tech_debt, api_change (no explicit in release) |
| ENG-4.3-DEADCODE | 5 | feature_story, bug_fix, tech_debt, api_change (no explicit in release) |
| QA-2.1-COVERAGE | 5 | feature_story, bug_fix, tech_debt, api_change (3 criteria each) |
| QA-2.2-UNIT | 4 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-INTEGRATION | 4 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-E2E | 2 | feature_story (2 criteria), bug_fix (1 criterion) |
| QA-2.3-REGRESSION | 1 | bug_fix (TEST-07) |
| QA-2.4-PERF | 2 | feature_story (ACC-04), api_change (TEST-07) |
| QA-3.1-RELEASE | 5 | release (5 criteria) |
| SEC-3.1-SAST | 6 | All work types (2 criteria each) |
| SEC-3.2-SECRETS | 6 | All work types (1 criterion each) |
| SEC-3.3-DEPS | 6 | All work types (2 criteria each) |
| SEC-4.1-IAC | 3 | infrastructure (3 criteria) |
| SEC-4.2-SECRETS | 3 | feature_story, api_change, infrastructure |
| ENG-6.1-API | 3 | feature_story (3 criteria), api_change (2 criteria) |
| ENG-6.2-ADR | 4 | tech_debt (2 criteria), api_change (1), infrastructure (2) |
| TEAM-TECH-STACK | 9 | Multiple work types (tech stack specific criteria) |
| TEAM-COMMERCE | 3 | feature_story (3 criteria) |
| TEAM-CI | 2 | feature_story, bug_fix |
| TEAM-CI-TOOL | 3 | release, api_change, infrastructure |
| TEAM-SONARQUBE | 1 | release (CI-02) |
| TEAM-PRACTICE | 3 | bug_fix (3 criteria) |
| TEAM-WORKFLOW | 2 | tech_debt (2 criteria) |
| TEAM-DOMAIN | 2 | release (2 criteria) |
| TEAM-INFRA-01 through TEAM-INFRA-09 | 9 | infrastructure (9 criteria) |
| FEATURE-STORY-DEF | 3 | feature_story (3 criteria) |
| BUG-FIX-STANDARD | 2 | bug_fix (2 criteria) |
| CI-STANDARD | 1 | bug_fix (CI-01) |
| CI-GENERAL | 1 | api_change (CI-01) |
| ENG-GENERAL | 1 | api_change (DOC-01) |
| TEAM-PROCESS | 1 | api_change (ACC-01) |
| DEFECT-INC-001 | 1 | feature_story (TEST-08) |
| DEFECT-INC-002 | 1 | api_change (TEST-06) |
| DEFECT-INC-003 | 1 | bug_fix (TEST-07) |
| PO-OR-TECH-LEAD | 6 | All work types (L4 story-specific placeholder) |

---

## Audit Notes

1. **Universal L1 Criteria**: ENG-4.1, ENG-4.2-SIGNING, ENG-4.2-FORMAT, SEC-3.1-SAST (2), SEC-3.2-SECRETS, SEC-3.3-DEPS (2), QA-2.1-COVERAGE (3) appear consistently across all work types.

2. **Escaped Defect Integration**: 3 criteria derived from incident reports (INC-001, INC-002, INC-003) have been successfully incorporated into feature_story, api_change, and bug_fix DoDs.

3. **Team-Specific Criteria**: TEAM-COMMERCE (3), TEAM-TECH-STACK (9), TEAM-INFRA-* (9) demonstrate customization for Commerce Platform team's technology stack (Java/Spring Boot, React, PostgreSQL, Kafka).

4. **Compliance Readiness**: All 6 work types include L1 security criteria (Snyk, Gitleaks, dependency CVE checks), supporting future SOC2/PCI-DSS compliance requirements.

5. **Gap Identification**: No criteria explicitly address accessibility (WCAG), chaos engineering, or consumer-driven contract testing (all listed in future_candidates).

---

## Matrix Maintenance

- **Next Review Date**: 2025-03-19 (quarterly review)
- **Drift Check**: Run `--drift-check` to identify source policy changes or new escaped defects
- **Ownership**: QA Lead (criteria maintenance), Engineering Manager (policy approval), Security Champion (SEC-* policy updates)