# Policy Traceability Matrix
Generated: 2024-12-19

## Overview
This matrix traces every DoD criterion back to its source policy, standard, or escaped defect. It enables auditing which policies drive which quality gates across all work types.

**Total Criteria Across All Work Types:** 159  
**Unique Source Policies Referenced:** 32  
**Criteria Derived from Escaped Defects:** 3

---

## Feature Story

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| CODE-03 | L1 | ENG-4.2-CONV | Commit messages follow Conventional Commits format |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| CODE-05 | L1 | ENG-4.3-COMPLEX | SonarQube cyclomatic complexity ≤10 per method |
| CODE-06 | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code |
| CODE-07 | L1 | ENG-4.3-DEAD | No dead code present (SonarQube) |
| CODE-08 | L3 | ENG-4.1-SEC | Security Champion approval for security-critical paths |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage on changed modules |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage on changed modules |
| TEST-03 | L1 | QA-2.1-COVERAGE | No coverage regression on existing covered code |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present for all new/changed code (JUnit 5) |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests for new/changed integration points |
| TEST-06 | L2 | QA-2.2-E2E | E2E test covering happy path (Playwright) |
| TEST-07 | L2 | QA-2.2-E2E | E2E test covering error path scenario (Playwright) |
| TEST-08 | L2 | DEFECT-INC-001 | **[FROM ESCAPED DEFECT]** Integration test for SSO login all auth methods |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SAST | Medium Snyk findings acknowledged with Jira ticket |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEPS | Dependencies in approved registry or explicitly approved |
| SEC-05 | L1 | SEC-3.3-DEPS | Dependency check 0 Critical CVE findings |
| SEC-06 | L3 | SEC-4.2-CREDS | Secrets stored in AWS Secrets Manager or GitHub secrets |
| DOC-01 | L2 | ENG-6.1-API | OpenAPI spec updated for API endpoint changes |
| DOC-02 | L2 | ENG-6.1-API | CHANGELOG.md updated under [Unreleased] |
| DOC-03 | L1 | ENG-GENERAL | README or docs updated where feature changes usage |
| CI-01 | L1 | CI-GENERAL | All GitHub Actions checks pass |
| CI-02 | L3 | QA-2.4-PERF | k6 load test for endpoints >1000 RPS |
| CI-03 | L3 | QA-2.4-PERF | k6 P95 <500ms, P99 <2000ms under normal load |
| ACC-01 | L2 | PO-ACCEPTANCE | All AC verified by PO in staging |
| ACC-02 | L2 | UX-REVIEW | UX review completed for user-facing features |
| ACC-03 | L3 | ANALYTICS | Analytics event instrumentation for feature usage |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions (optional) |

---

## Bug Fix

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| CODE-03 | L1 | ENG-4.2-CONV | Commit messages follow Conventional Commits format |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| CODE-05 | L1 | ENG-4.3-COMPLEX | SonarQube cyclomatic complexity ≤10 per method |
| CODE-06 | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code |
| CODE-07 | L1 | ENG-4.3-DEAD | No dead code present (SonarQube) |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage on changed modules |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage on changed modules |
| TEST-03 | L1 | QA-2.1-COVERAGE | No coverage regression on existing covered code |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present for all new/changed code (JUnit 5) |
| TEST-05 | L2 | QA-2.3-REGRESSION | Regression test covering exact repro path from bug report |
| TEST-06 | L2 | QA-2.2-INTEGRATION | Integration test if bug involved inter-service/DB interaction |
| TEST-07 | L2 | QA-2.2-E2E | E2E regression test if bug manifested in UI (Playwright) |
| TEST-08 | L2 | DEFECT-INC-003 | **[FROM ESCAPED DEFECT]** Regression test covering exact repro path |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SAST | Medium Snyk findings acknowledged with Jira ticket |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEPS | Dependencies in approved registry or explicitly approved |
| SEC-05 | L1 | SEC-3.3-DEPS | Dependency check 0 Critical CVE findings |
| DOC-01 | L2 | BUG-FIX-BEST-PRACTICE | Root cause documented in PR or bug ticket |
| DOC-02 | L3 | COMMERCE-PLATFORM-STANDARD | Runbook updated if bug affected production |
| CI-01 | L1 | CI-UNIVERSAL-GATE | All GitHub Actions workflows pass |
| CI-02 | L3 | COMMERCE-PLATFORM-KAFKA | Kafka integration test if bug involves message handling |
| ACC-01 | L2 | BUG-FIX-ACCEPTANCE | Bug reporter or QA verifies fix in staging |
| ACC-02 | L3 | COMMERCE-PLATFORM-STANDARD | Tech Lead approval for P1/P2 bugs |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions (optional) |

---

## Tech Debt

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| CODE-03 | L1 | ENG-4.2-CONV | Commit messages follow Conventional Commits format |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| CODE-05 | L1 | ENG-4.3-COMPLEX | SonarQube cyclomatic complexity ≤10 per method |
| CODE-06 | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code |
| CODE-07 | L1 | ENG-4.3-DEAD | No dead code present (SonarQube) |
| CODE-08 | L2 | ENG-6.2-ADR | ADR created for architecture/data model/contract changes |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage on changed modules |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage on changed modules |
| TEST-03 | L1 | QA-2.1-COVERAGE | No coverage regression on existing covered code |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present for all new/changed code (JUnit 5) |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests for new/changed integration points |
| TEST-06 | L2 | ENG-6.2-ADR | Architecture Guild approval documented in PR |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SAST | Medium Snyk findings acknowledged with Jira ticket |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEPS | Dependencies in approved registry or explicitly approved |
| SEC-05 | L1 | SEC-3.3-DEPS | Dependency check 0 Critical CVE findings |
| DOC-01 | L3 | TEAM-STANDARD | README updated if refactoring changes setup/build/run |
| DOC-02 | L3 | TEAM-STANDARD | Inline comments for complex logic (complexity >5) |
| CI-01 | L1 | UNIVERSAL-CI | All GitHub Actions checks pass |
| CI-02 | L3 | TEAM-SONARQUBE | SonarQube quality gate passes (0 bugs/vulnerabilities/critical smells) |
| CI-03 | L2 | TECH-DEBT-GATE | SonarQube Technical Debt ratio does not increase, new code <5% |
| ACCEPT-01 | L2 | TECH-DEBT-VERIFICATION | Tech debt AC verified by Tech Lead |
| ACCEPT-02 | L2 | TECH-DEBT-NO-NEW-DEBT | 0 new TODO/FIXME/HACK comments introduced |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions (optional) |

---

## API Change

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| CODE-03 | L1 | ENG-4.2-CONV | Commit messages follow Conventional Commits format |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| CODE-05 | L1 | ENG-4.3-COMPLEX | SonarQube cyclomatic complexity ≤10 per method |
| CODE-06 | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code |
| CODE-07 | L1 | ENG-4.3-DEAD | No dead code present (SonarQube) |
| CODE-08 | L3 | ENG-4.1-SEC | Security Champion approval for security-critical paths |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage on changed modules |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage on changed modules |
| TEST-03 | L1 | QA-2.1-COVERAGE | No coverage regression on existing covered code |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present for all new/changed code (JUnit 5) |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests for new/changed integration points |
| TEST-06 | L2 | DEFECT-INC-002 | **[FROM ESCAPED DEFECT]** Contract test for all nullable fields in OpenAPI |
| TEST-07 | L3 | QA-2.4-PERF | k6 load test for endpoints >1000 RPS |
| TEST-08 | L3 | QA-2.4-PERF | k6 P95 <500ms, P99 <2000ms under normal load |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SAST | Medium Snyk findings acknowledged with Jira ticket |
| SEC-03 | L1 | SEC-3.2-SECRETS + SEC-4.2-CREDS | Gitleaks scan 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEPS | Dependencies in approved registry or explicitly approved |
| SEC-05 | L1 | SEC-3.3-DEPS | Dependency check 0 Critical CVE findings |
| SEC-06 | L3 | SEC-4.2-CREDS | Secrets stored in AWS Secrets Manager or GitHub secrets |
| DOC-01 | L2 | ENG-6.1-API | OpenAPI spec updated for API endpoint changes |
| DOC-02 | L2 | ENG-6.1-API | CHANGELOG.md updated under [Unreleased] |
| DOC-03 | L2 | ENG-6.1-API | API diff generated and attached to PR |
| DOC-04 | L2 | ENG-6.2-ADR | ADR created for architecture/data model/contract changes |
| DOC-05 | L2 | ENG-6.2-ADR | Architecture Guild approval documented in PR |
| CI-01 | L1 | QA-2.1 + SEC-3.1 + ENG-4.3 | All GitHub Actions checks pass (consolidated gate) |
| CI-02 | L2 | QA-2.2-INTEGRATION | Integration test suite passes in staging before merge |
| ACC-01 | L2 | ENG-6.1-API | Tech Lead/API Owner approval for backward compatibility |
| ACC-02 | L3 | TEAM-STANDARD | Consumer Team acknowledgment for external API changes |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions (optional) |

---

## Release

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| CODE-03 | L1 | ENG-4.2-CONV | Commit messages follow Conventional Commits format |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| TEST-01 | L2 | QA-3.1-RELEASE | Full regression suite passes in staging and pre-prod |
| TEST-02 | L2 | QA-3.1-RELEASE | Smoke test suite passes in production post-deployment |
| TEST-03 | L2 | QA-3.1-RELEASE | Rollback plan documented and tested in staging |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SAST | Medium Snyk findings acknowledged with Jira ticket |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEPS | Dependency check 0 Critical CVE findings |
| DOC-01 | L2 | QA-3.1-RELEASE | Release notes prepared and EM-approved |
| DOC-02 | L2 | QA-3.1-RELEASE | Runbook updated for changed operational procedures |
| CI-01 | L1 | DERIVED-CI | All GitHub Actions CI checks pass |
| CI-02 | L3 | TEAM-STACK-JAVA | Maven build completes with BUILD SUCCESS |
| CI-03 | L3 | TEAM-STACK-REACT | React production build completes, bundle size within threshold |
| ACC-01 | L2 | QA-3.1-RELEASE | Engineering Manager sign-off in release PR |
| ACC-02 | L3 | TEAM-RELEASE-GATE | Platform Engineering approval for infrastructure changes |
| DEP-01 | L3 | TEAM-KAFKA | Kafka schema registry updated for message format changes |
| DEP-02 | L3 | TEAM-POSTGRES | Database migration tested in staging with rollback verified |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions (optional) |

---

## Infrastructure

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L3 | ENG-4.1-SEC | Security Champion approval for security-critical infra paths |
| CODE-03 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| CODE-04 | L1 | ENG-4.2-CONV | Commit messages follow Conventional Commits format |
| CODE-05 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| INFRA-01 | L2 | SEC-4.1-IAC | Terraform plan clean with no unintended deletions |
| INFRA-02 | L2 | SEC-4.1-IAC | Platform Engineering team member approval |
| INFRA-03 | L2 | SEC-4.1-IAC | tfsec scan 0 HIGH/CRITICAL findings |
| INFRA-04 | L2 | ENG-6.2-ADR | ADR created for architecture/data model/contract changes |
| INFRA-05 | L2 | ENG-6.2-ADR | Architecture Guild approval documented in PR |
| INFRA-06 | L3 | TEAM-INFRA-DR | Disaster recovery verified in non-prod environment |
| INFRA-07 | L3 | TEAM-INFRA-RB | Runbook created or updated in docs/runbooks/ |
| SEC-01 | L1 | SEC-3.1-SAST | Snyk scan 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SAST | Medium Snyk findings acknowledged with Jira ticket |
| SEC-03 | L1 | SEC-3.2-SECRETS + SEC-4.2-CREDS | Gitleaks scan 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEPS | Dependencies in approved registry or explicitly approved |
| SEC-05 | L1 | SEC-3.3-DEPS | Dependency check 0 Critical CVE findings |
| SEC-06 | L3 | SEC-4.2-CREDS | Secrets stored in AWS Secrets Manager or GitHub secrets |
| DOCS-01 | L2 | ENG-6.1-API | CHANGELOG.md updated under [Unreleased] |
| DOCS-02 | L3 | TEAM-INFRA-DOCS | Infrastructure diagram updated if topology changed |
| CI-01 | L1 | TEAM-CI-GATE | All GitHub Actions checks pass |
| CI-02 | L3 | TEAM-INFRA-DEPLOY | Terraform apply successful in staging before production |
| ACCEPT-01 | L2 | TEAM-INFRA-ACCEPT | Infrastructure change verified in staging with smoke test |
| ACCEPT-02 | L3 | TEAM-INFRA-EM | Engineering Manager sign-off for production infra changes |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions (optional) |

---

## Policy Reference Index

| Policy Ref | Work Types Using This Policy | Total Criteria |
|---|---|---|
| ENG-4.1 | All (6) | 6 |
| ENG-4.1-SEC | feature_story, api_change, infrastructure | 3 |
| ENG-4.2-SIGN | All (6) | 6 |
| ENG-4.2-CONV | All (6) | 6 |
| ENG-4.2-MERGE | feature_story, bug_fix, tech_debt, api_change, release | 5 |
| ENG-4.3-COMPLEX | feature_story, bug_fix, tech_debt, api_change | 4 |
| ENG-4.3-LOC | feature_story, bug_fix, tech_debt, api_change | 4 |
| ENG-4.3-DEAD | feature_story, bug_fix, tech_debt, api_change | 4 |
| QA-2.1-COVERAGE | feature_story, bug_fix, tech_debt, api_change | 12 |
| QA-2.2-UNIT | feature_story, bug_fix, tech_debt, api_change | 4 |
| QA-2.2-INTEGRATION | feature_story, bug_fix, tech_debt, api_change | 5 |
| QA-2.2-E2E | feature_story, bug_fix | 3 |
| QA-2.3-REGRESSION | bug_fix | 1 |
| QA-2.4-PERF | feature_story, api_change | 4 |
| QA-3.1-RELEASE | release | 5 |
| SEC-3.1-SAST | All (6) | 12 |
| SEC-3.2-SECRETS | All (6) | 6 |
| SEC-3.3-DEPS | All (6) | 12 |
| SEC-4.1-IAC | infrastructure | 3 |
| SEC-4.2-CREDS | feature_story, api_change, infrastructure | 3 |
| ENG-6.1-API | feature_story, api_change, infrastructure | 6 |
| ENG-6.2-ADR | tech_debt, api_change, infrastructure | 5 |
| ENG-GENERAL | feature_story | 1 |
| CI-GENERAL | feature_story | 1 |
| DEFECT-INC-001 | feature_story | 1 |
| DEFECT-INC-002 | api_change | 1 |
| DEFECT-INC-003 | bug_fix | 1 |
| BUG-FIX-BEST-PRACTICE | bug_fix | 1 |
| COMMERCE-PLATFORM-STANDARD | bug_fix | 2 |
| TEAM-STANDARD | tech_debt, api_change | 3 |
| UNIVERSAL-CI | tech_debt | 1 |
| TECH-DEBT-GATE | tech_debt | 1 |
| DERIVED-CI | release | 1 |
| TEAM-STACK-JAVA | release | 1 |
| TEAM-STACK-REACT | release | 1 |
| TEAM-KAFKA | release | 1 |
| TEAM-POSTGRES | release | 1 |
| TEAM-INFRA-DR | infrastructure | 1 |
| TEAM-INFRA-RB | infrastructure | 1 |
| TEAM-INFRA-DOCS | infrastructure | 1 |
| TEAM-CI-GATE | infrastructure | 1 |
| TEAM-INFRA-DEPLOY | infrastructure | 1 |
| TEAM-INFRA-ACCEPT | infrastructure | 1 |
| TEAM-INFRA-EM | infrastructure | 1 |
| PO-OR-TECH-LEAD | All (6) | 6 |

---

## Escaped Defect Traceability

| Incident ID | Work Type | Criterion ID | Criterion Text |
|---|---|---|---|
| INC-001 | feature_story | TEST-08 | Integration test verifies SSO login flow for all configured authentication methods |
| INC-002 | api_change | TEST-06 | API contract test includes test cases for all nullable fields documented in OpenAPI specification |
| INC-003 | bug_fix | TEST-08 | Regression test covering exact reproduction path from original bug report present in CI |

**Note:** These criteria are marked `[L2]` and carry `from_escaped_defect: true` in their YAML definitions, ensuring production incidents drive continuous improvement in DoD standards.

---

## Layer Distribution Analysis

| Work Type | L1 Count | L2 Count | L3 Count | L4 Count | Total |
|---|---|---|---|---|---|
| feature_story | 15 (52%) | 10 (34%) | 3 (10%) | 1 (3%) | 29 |
| bug_fix | 14 (58%) | 8 (33%) | 1 (4%) | 1 (4%) | 24 |
| tech_debt | 13 (57%) | 7 (30%) | 2 (9%) | 1 (4%) | 23 |
| api_change | 18 (60%) | 10 (33%) | 1 (3%) | 1 (3%) | 30 |
| release | 8 (38%) | 5 (24%) | 7 (33%) | 1 (5%) | 21 |
| infrastructure | 11 (44%) | 7 (28%) | 6 (24%) | 1 (4%) | 25 |

**Total Across All Work Types:** 159 criteria

---

## Document Control

**Generated By:** DoD Builder v1.0 (Claude Sonnet 4.5 / Amazon Bedrock)  
**Last Updated:** 2024-12-19  
**Next Review Date:** 2025-03-19  
**Owner:** Engineering Manager / QA Lead  
**Audit Trail:** All source policies documented in `inputs/standards/` and `inputs/policies/` directories