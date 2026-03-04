# Policy Traceability Matrix
Generated: 2026-03-04

## Overview
This matrix traces every Definition-of-Done criterion back to its source policy, standard, or escaped defect incident. It enables auditors and Engineering Managers to verify that all organizational mandates are reflected in the DoD checklists.

**Total Criteria Across All Work Types:** 176  
**Unique Source Policies Referenced:** 34  
**Escaped Defect Criteria:** 3  

---

## Feature Story

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L2 | ENG-4.1-SEC | Security Champion approval for security-critical paths |
| CODE-03 | L1 | ENG-4.2 | All commits signed with GPG/SSH |
| CODE-04 | L1 | ENG-4.2-CONV | Conventional Commits format enforced |
| CODE-05 | L1 | ENG-4.2-MERGE | Squash merge only (no merge commits) |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY | Cyclomatic complexity ≤10 per method |
| CODE-07 | L1 | ENG-4.3-LOC | No method exceeds 50 lines |
| CODE-08 | L1 | ENG-4.3-DEAD | Zero dead code issues |
| TEST-01 | L1 | QA-2.1-COV-LINE | JaCoCo ≥80% line coverage |
| TEST-02 | L1 | QA-2.1-COV-BRANCH | JaCoCo ≥75% branch coverage |
| TEST-03 | L1 | QA-2.1-COV-REGRESS | No coverage regression |
| TEST-04 | L1 | QA-2.2-UNIT | Unit tests present and passing (JUnit 5) |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests passing in CI |
| TEST-06 | L2 | QA-2.2-E2E | E2E test covering happy path (Playwright) |
| TEST-07 | L2 | QA-2.2-E2E | E2E test covering error path (Playwright) |
| TEST-08 | L2 | QA-2.4-PERF | k6 load test for >1000 RPS endpoints |
| TEST-09 | L2 | QA-2.4-PERF | k6 P95 <500ms |
| TEST-10 | L2 | QA-2.4-PERF | k6 P99 <2000ms |
| TEST-11 | L2 | INC-001 | **[ESCAPED DEFECT]** SSO login flow integration test |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SNYK-MEDIUM | Medium findings have Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEPS | All deps in approved registry |
| SEC-05 | L1 | SEC-3.3-CVE | No Critical CVEs >5 business days |
| SEC-06 | L1 | SEC-3.3-AUDIT | npm audit 0 Critical (React) |
| SEC-07 | L1 | SEC-3.3-AUDIT | mvn dependency:check 0 Critical (Java) |
| SEC-08 | L1 | SEC-4.2-SECRETS-STORE | Secrets in AWS Secrets Manager only |
| DOC-01 | L2 | ENG-6.1-API | OpenAPI spec updated |
| DOC-02 | L2 | ENG-6.1-API | CHANGELOG.md updated under [Unreleased] |
| DOC-03 | L3 | TEAM-STANDARD | Javadoc/JSDoc for new public methods |
| DOC-04 | L3 | TEAM-STANDARD | README updated if setup changed |
| CI-01 | L1 | DERIVED-FROM-POLICY-REGISTRY | All GitHub Actions checks pass |
| CI-02 | L1 | DERIVED-FROM-SONARQUBE | SonarQube Quality Gate PASSED |
| CI-03 | L3 | TEAM-STANDARD | Spring Boot smoke test passes |
| CI-04 | L3 | TEAM-STANDARD | React build 0 errors |
| ACC-01 | L2 | WORK-TYPE-STANDARD | All AC verified and PO approved |
| ACC-02 | L2 | WORK-TYPE-STANDARD | PO approval in staging |
| ACC-03 | L3 | TEAM-STANDARD | UX review if UI changes |
| ACC-04 | L3 | TEAM-STANDARD | Analytics events verified |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific placeholder |

---

## Bug Fix

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | Security Champion approval for security-critical paths |
| CODE-03 | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-CONV | Conventional Commits format enforced |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | Squash merge only |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | Cyclomatic complexity ≤10 |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-LOC | No method >50 lines |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEAD | Zero dead code |
| BUG-01 | L2-WORKTYPE | BUG-FIX-STANDARD | Root cause analysis documented |
| BUG-02 | L2-WORKTYPE | BUG-FIX-STANDARD | Bug ticket linked with repro steps |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COV-LINE | JaCoCo ≥80% line coverage |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COV-BRANCH | JaCoCo ≥75% branch coverage |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COV-REGRESS | No coverage regression |
| TEST-04 | L1-UNIVERSAL | QA-2.2-UNIT | Unit tests passing (JUnit 5) |
| TEST-05 | L2-WORKTYPE | QA-2.3-REGRESSION / INC-003 | **[ESCAPED DEFECT]** Regression test covering exact repro path |
| TEST-06 | L2-WORKTYPE | QA-2.3-REGRESSION | Regression test fails pre-fix, passes post-fix |
| TEST-07 | L2-WORKTYPE | QA-2.2-INTEGRATION | Integration test if bug was integration-level |
| TEST-08 | L2-WORKTYPE | QA-2.2-E2E | E2E test if bug was UI-level |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk 0 Critical/High |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK-MEDIUM | Medium findings have Jira tickets |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks 0 secrets |
| SEC-04 | L1-UNIVERSAL | SEC-4.2-SECRETS-STORE | Secrets in AWS Secrets Manager |
| SEC-05 | L1-UNIVERSAL | SEC-3.3-CVE | No Critical CVEs >5 days |
| SEC-06 | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit 0 Critical |
| SEC-07 | L1-UNIVERSAL | SEC-3.3-AUDIT | mvn dependency:check 0 Critical |
| DOC-01 | L2-WORKTYPE | BUG-FIX-STANDARD | CHANGELOG.md updated if user-facing |
| DOC-02 | L3-TEAM | TEAM-COMMERCE-DOC | API docs updated if behavior changed |
| CI-01 | L1-UNIVERSAL | CI-GATE-STANDARD | All GitHub Actions checks pass |
| CI-02 | L3-TEAM | TEAM-COMMERCE-CI | Spring Boot startup passes |
| CI-03 | L3-TEAM | TEAM-COMMERCE-CI | PostgreSQL migration passes |
| ACC-01 | L2-WORKTYPE | BUG-FIX-STANDARD | Bug reporter or QA verifies in staging |
| ACC-02 | L2-WORKTYPE | BUG-FIX-STANDARD | Bug ticket status updated to Fixed |
| SS-01 | L4-STORY | PO-OR-TECH-LEAD | Story-specific placeholder |

---

## Tech Debt

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH |
| CODE-03 | L1-UNIVERSAL | ENG-4.2-CONV | Conventional Commits format |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-MERGE | Squash merge only |
| CODE-05 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | Cyclomatic complexity ≤10 |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-LOC | No method >50 lines |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-DEAD | Zero dead code |
| CODE-08 | L2-WORKTYPE | ENG-6.2-ARCH | ADR created for structural changes |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COV-LINE | JaCoCo ≥80% line coverage |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COV-BRANCH | JaCoCo ≥75% branch coverage |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COV-REGRESS | No coverage regression |
| TEST-04 | L1-UNIVERSAL | QA-2.2-UNIT | Unit tests passing (JUnit 5) |
| TEST-05 | L2-WORKTYPE | QA-2.2-INTEGRATION | Integration tests passing |
| TEST-06 | L3-TEAM | TEAM-TECH-STACK | SonarQube tech debt ratio does not increase |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk 0 Critical/High |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK-MEDIUM | Medium findings have Jira tickets |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks 0 secrets |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-DEPS | All deps in approved registry |
| SEC-05 | L1-UNIVERSAL | SEC-3.3-CVE | No Critical CVEs >5 days |
| SEC-06 | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit 0 Critical |
| SEC-07 | L1-UNIVERSAL | SEC-3.3-AUDIT | mvn dependency:check 0 Critical |
| SEC-08 | L1-UNIVERSAL | SEC-4.2-SECRETS-STORE | Secrets in AWS Secrets Manager |
| DOC-01 | L2-WORKTYPE | ENG-6.2-ARCH | Architecture Guild review approval |
| DOC-02 | L3-TEAM | TEAM-PRACTICE | Tech debt tracked with before/after metrics |
| CI-01 | L1-UNIVERSAL | CI-GATE | All GitHub Actions checks pass |
| CI-02 | L3-TEAM | TEAM-SONARQUBE | SonarQube Quality Gate PASSED |
| ACCEPT-01 | L2-WORKTYPE | TECH-DEBT-PRACTICE | Tech Lead verified and approved |
| ACCEPT-02 | L3-TEAM | TEAM-PRACTICE | Refactoring does not break functionality |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific placeholder |

---

## API Change

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L2-WORKTYPE | ENG-4.1-SEC | Security Champion approval for security-critical paths |
| CODE-03 | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH |
| CODE-04 | L1-UNIVERSAL | ENG-4.2-CONV | Conventional Commits format |
| CODE-05 | L1-UNIVERSAL | ENG-4.2-MERGE | Squash merge only |
| CODE-06 | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | Cyclomatic complexity ≤10 |
| CODE-07 | L1-UNIVERSAL | ENG-4.3-LOC | No method >50 lines |
| CODE-08 | L1-UNIVERSAL | ENG-4.3-DEAD | Zero dead code |
| TEST-01 | L1-UNIVERSAL | QA-2.1-COV-LINE | JaCoCo ≥80% line coverage |
| TEST-02 | L1-UNIVERSAL | QA-2.1-COV-BRANCH | JaCoCo ≥75% branch coverage |
| TEST-03 | L1-UNIVERSAL | QA-2.1-COV-REGRESS | No coverage regression |
| TEST-04 | L1-UNIVERSAL | QA-2.2-UNIT | Unit tests passing (JUnit 5) |
| TEST-05 | L2-WORKTYPE | QA-2.2-INTEGRATION | Integration tests passing |
| TEST-06 | L2-WORKTYPE | QA-2.4-PERF | k6 load test for >1000 RPS |
| TEST-07 | L2-WORKTYPE | QA-2.4-PERF | k6 P95 <500ms |
| TEST-08 | L2-WORKTYPE | QA-2.4-PERF | k6 P99 <2000ms |
| API-01 | L2-WORKTYPE | ENG-6.1-API | OpenAPI spec updated |
| API-02 | L2-WORKTYPE | ENG-6.1-API | API diff attached to PR |
| API-03 | L2-WORKTYPE | INC-002 | **[ESCAPED DEFECT]** Contract test includes all nullable fields |
| API-04 | L3-TEAM | TEAM-CONTEXT | Consumer contract tests pass |
| SEC-01 | L1-UNIVERSAL | SEC-3.1-SNYK | Snyk 0 Critical/High |
| SEC-02 | L1-UNIVERSAL | SEC-3.1-SNYK-MEDIUM | Medium findings have Jira tickets |
| SEC-03 | L1-UNIVERSAL | SEC-3.2-SECRETS | Gitleaks 0 secrets |
| SEC-04 | L1-UNIVERSAL | SEC-3.3-CVE | No Critical CVEs >5 days |
| SEC-05 | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit 0 Critical |
| SEC-06 | L1-UNIVERSAL | SEC-3.3-AUDIT | mvn dependency:check 0 Critical |
| SEC-07 | L1-UNIVERSAL | SEC-4.2-SECRETS-STORE | Secrets in AWS Secrets Manager |
| DOC-01 | L2-WORKTYPE | ENG-6.1-API | CHANGELOG.md updated |
| DOC-02 | L3-TEAM | TEAM-CONTEXT | API versioning strategy documented if breaking |
| DOC-03 | L3-TEAM | TEAM-CONTEXT | Postman collection updated |
| CI-01 | L1-UNIVERSAL | UNIVERSAL | All GitHub Actions checks pass |
| CI-02 | L3-TEAM | TEAM-CONTEXT | API backward compatibility check passes |
| ACC-01 | L2-WORKTYPE | WORKTYPE-STANDARD | API consumers notified |
| ACC-02 | L3-TEAM | TEAM-CONTEXT | API Guild review if cross-team |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific placeholder |

---

## Release

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2 | All commits signed with GPG/SSH |
| CODE-03 | L1 | ENG-4.2-CONV | Conventional Commits format |
| TEST-01 | L2 | QA-3.1-REL-REGRESSION | Full regression suite passes in staging |
| TEST-02 | L2 | QA-3.1-REL-REGRESSION | Full regression suite passes in pre-prod |
| TEST-03 | L2 | QA-3.1-REL-SMOKE | Smoke tests pass post-deploy in production |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High |
| SEC-02 | L1 | SEC-3.1-SNYK-MEDIUM | Medium findings have Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks 0 secrets |
| SEC-04 | L1 | SEC-3.3-CVE | No Critical CVEs >5 days |
| SEC-05 | L1 | SEC-4.2-SECRETS-STORE | Secrets in AWS Secrets Manager |
| DOC-01 | L2 | QA-3.1-REL-NOTES | Release notes prepared with EM approval |
| DOC-02 | L2 | QA-3.1-REL-ROLLBACK | Rollback plan documented and tested |
| DOC-03 | L2 | QA-3.1-REL-RUNBOOK | Runbook updated if operational changes |
| CI-01 | L3 | TEAM-TECH-STACK | All GitHub Actions checks pass |
| CI-02 | L3 | TEAM-TECH-STACK | Spring Boot build passes |
| CI-03 | L3 | TEAM-TECH-STACK | React build passes |
| CI-04 | L3 | TEAM-TECH-STACK | Database migration passes in staging |
| ACC-01 | L2 | QA-3.1-REL-NOTES | EM approval recorded |
| ACC-02 | L3 | TEAM-RELEASE-PROCESS | PO sign-off confirmed |
| ACC-03 | L3 | TEAM-RELEASE-PROCESS | Deployment window scheduled and communicated |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific placeholder |

---

## Infrastructure

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2 | All commits signed with GPG/SSH |
| CODE-03 | L1 | ENG-4.2-CONV | Conventional Commits format |
| CODE-04 | L2 | ENG-6.2-ARCH | ADR created for structural changes |
| CODE-05 | L2 | ENG-6.2-ARCH | Architecture Guild review approval |
| TEST-01 | L3 | TEAM-INFRA-01 | Terraform validate, plan, fmt pass |
| TEST-02 | L3 | TEAM-INFRA-02 | DR procedure verified in staging |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High |
| SEC-02 | L1 | SEC-3.1-SNYK-MEDIUM | Medium findings have Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks 0 secrets |
| SEC-04 | L1 | SEC-3.3-DEPS | All deps in approved registry |
| SEC-05 | L1 | SEC-3.3-CVE | No Critical CVEs >5 days |
| SEC-06 | L1 | SEC-4.2-SECRETS-STORE | Secrets in AWS Secrets Manager |
| SEC-07 | L2 | SEC-4.1-TERRAFORM | Terraform plan clean (no unintended deletions) |
| SEC-08 | L2 | SEC-4.1-TERRAFORM | Platform Engineering review approval |
| INFRA-01 | L2 | SEC-4.1-TERRAFORM | tfsec 0 HIGH/CRITICAL |
| INFRA-02 | L3 | TEAM-INFRA-03 | State backend encryption + versioning verified |
| INFRA-03 | L3 | TEAM-INFRA-04 | Resource tagging follows standard |
| INFRA-04 | L3 | TEAM-INFRA-05 | PostgreSQL migration + rollback plan |
| INFRA-05 | L3 | TEAM-INFRA-06 | Kafka topic retention ≥7 days |
| DOC-01 | L1 | ENG-4.1 | Documentation updated where changed |
| DOC-02 | L2 | TEAM-INFRA-07 | Runbook published for operational changes |
| DOC-03 | L3 | TEAM-INFRA-08 | Network topology diagram updated |
| CI-01 | L1 | ENG-4.1 | All GitHub Actions checks pass |
| CI-02 | L3 | TEAM-INFRA-09 | Terraform plan reviewed if >10 resource changes |
| ACC-01 | L2 | TEAM-INFRA-10 | Tested in staging before production |
| ACC-02 | L3 | TEAM-INFRA-11 | Monitoring/alerting configured |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific placeholder |

---

## Policy Coverage Summary

| Source Policy | Referenced By Criteria Count | Work Types |
|---|---|---|
| ENG-4.1 | 14 | All |
| ENG-4.2 | 6 | All |
| ENG-4.2-CONV | 6 | All |
| ENG-4.2-MERGE | 5 | feature_story, bug_fix, tech_debt, api_change |
| ENG-4.3-COMPLEXITY | 5 | feature_story, bug_fix, tech_debt, api_change |
| ENG-4.3-LOC | 5 | feature_story, bug_fix, tech_debt, api_change |
| ENG-4.3-DEAD | 5 | feature_story, bug_fix, tech_debt, api_change |
| ENG-4.1-SEC | 4 | feature_story, bug_fix, api_change |
| ENG-6.1-API | 5 | feature_story, api_change |
| ENG-6.2-ARCH | 4 | tech_debt, infrastructure |
| QA-2.1-COV-LINE | 5 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.1-COV-BRANCH | 5 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.1-COV-REGRESS | 5 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-UNIT | 5 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-INTEGRATION | 4 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-E2E | 3 | feature_story, bug_fix, api_change |
| QA-2.3-REGRESSION | 2 | bug_fix |
| QA-2.4-PERF | 6 | feature_story, api_change |
| QA-3.1-REL-REGRESSION | 2 | release |
| QA-3.1-REL-SMOKE | 1 | release |
| QA-3.1-REL-NOTES | 2 | release |
| QA-3.1-REL-ROLLBACK | 1 | release |
| QA-3.1-REL-RUNBOOK | 1 | release |
| SEC-3.1-SNYK | 6 | All |
| SEC-3.1-SNYK-MEDIUM | 6 | All |
| SEC-3.2-SECRETS | 6 | All |
| SEC-3.3-DEPS | 3 | feature_story, tech_debt, infrastructure |
| SEC-3.3-CVE | 6 | All |
| SEC-3.3-AUDIT | 10 | feature_story, bug_fix, tech_debt, api_change |
| SEC-4.1-TERRAFORM | 4 | infrastructure |
| SEC-4.2-SECRETS-STORE | 6 | All |
| INC-001 | 1 | feature_story (ESCAPED DEFECT) |
| INC-002 | 1 | api_change (ESCAPED DEFECT) |
| INC-003 | 1 | bug_fix (ESCAPED DEFECT) |
| TEAM-* | 27 | Various team-specific standards |

---

## Escaped Defect Traceability

| Incident ID | Work Type | Criterion ID | Criterion Summary |
|---|---|---|---|
| INC-001 | feature_story | TEST-11 | SSO login flow integration test required |
| INC-002 | api_change | API-03 | Contract tests must include all nullable fields |
| INC-003 | bug_fix | TEST-05 | Regression test covering exact repro path mandatory |

**All 3 escaped defects from the log have been incorporated into work-type-specific DoD checklists.**

--- END OUTPUT: policy_traceability_matrix.md ---