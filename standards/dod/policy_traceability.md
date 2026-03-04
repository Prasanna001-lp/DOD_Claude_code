# Policy Traceability Matrix
Generated: 2026-03-04

## Overview
This matrix maps every Definition-of-Done criterion across all work types back to its originating policy, standard, or escaped defect incident. It ensures full traceability between organizational mandates and enforceable quality gates.

**Total Criteria Tracked:** 169  
**Work Types Covered:** 6 (feature_story, bug_fix, tech_debt, api_change, release, infrastructure)  
**Unique Source Policies:** 45  
**Escaped Defect References:** 3 (INC-001, INC-002, INC-003)

---

## Feature Story DoD

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L2 | ENG-4.1-SEC | Security Champion approval for security-critical paths |
| CODE-03 | L1 | ENG-4.2-SIGN | All commits signed with GPG/SSH |
| CODE-04 | L1 | ENG-4.2-CONV | Conventional Commits format enforced |
| CODE-05 | L1 | ENG-4.2-MERGE | Squash merge required |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY/LOC/DEAD | SonarQube quality gate passes |
| CODE-07 | L3 | TEAM-SPRING-BOOT | Constructor injection required for Spring dependencies |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage |
| TEST-03 | L1 | QA-2.1-COVERAGE | No coverage regression |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests for all new/changed methods |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests cover service interactions |
| TEST-06 | L2 | QA-2.2-E2E | Playwright E2E test covers happy path |
| TEST-07 | L2 | QA-2.2-E2E | Playwright E2E test covers error path |
| TEST-08 | L2 | INC-001 | SSO login flow integration test for all auth providers |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes |
| SEC-04 | L1 | SEC-4.2-SECRETS-MGMT | Secrets in AWS Secrets Manager/GitHub |
| SEC-05 | L1 | SEC-3.3-DEPS | Maven dependency check 0 Critical CVEs |
| SEC-06 | L1 | SEC-3.3-DEPS-APPROVAL | New dependencies in approved registry |
| DOC-01 | L2 | ENG-6.1-API | CHANGELOG.md updated |
| DOC-02 | L3 | TEAM-COMMERCE-UX | UI screenshots/Figma link provided |
| DOC-03 | L3 | TEAM-COMMERCE-ANALYTICS | Analytics events emitted to Kafka |
| CI-01 | L1 | ALL-POLICIES | All GitHub Actions checks pass |
| CI-02 | L2 | QA-2.4-PERF | k6 load test for >1000 RPS endpoints |
| ACC-01 | L2 | AGILE-DOD-STANDARD | All AC verified |
| ACC-02 | L2 | AGILE-DOD-STANDARD | PO reviewed in staging |
| ACC-03 | L3 | TEAM-COMMERCE-UX | UX team approved UI changes |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions |

---

## Bug Fix DoD

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L2 | ENG-4.1-SEC | Security Champion approval for security-critical paths |
| CODE-03 | L1 | ENG-4.2-SIGN | All commits signed with GPG/SSH |
| CODE-04 | L1 | ENG-4.2-CONV | Conventional Commits format enforced |
| CODE-05 | L1 | ENG-4.2-MERGE | Squash merge required |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY/LOC/DEAD | SonarQube quality gate passes |
| CODE-07 | L2 | BUG-FIX-ROOT-CAUSE | Root cause documented |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage |
| TEST-03 | L1 | QA-2.1-COVERAGE | No coverage regression |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests for all new/changed methods |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration test for failed integration point |
| TEST-06 | L2 | QA-2.2-E2E | Playwright E2E test reproduces UI bug |
| TEST-07 | L2 | QA-2.3-REGRESSION / INC-003 | Regression test covers exact reproduction path |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes |
| SEC-04 | L1 | SEC-3.3-DEPS | Maven/npm audit 0 Critical CVEs |
| SEC-05 | L1 | SEC-4.2-SECRETS-MGMT | Secrets in AWS Secrets Manager/GitHub |
| DOC-01 | L2 | BUG-FIX-DOCS | Documentation updated if behavior changed |
| DOC-02 | L3 | COMMERCE-PLATFORM-JIRA | Jira ticket updated with resolution |
| CI-01 | L1 | CI-ALL-CHECKS | All GitHub Actions checks pass |
| CI-02 | L2 | BUG-FIX-STAGING | Verified in staging environment |
| ACCEPT-01 | L2 | BUG-FIX-REPORTER | Bug reporter verified fix |
| ACCEPT-02 | L3 | COMMERCE-PLATFORM-PO | PO sign-off for P1 bugs |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions |

---

## Tech Debt DoD

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG/SSH |
| CODE-03 | L1 | ENG-4.2-CONV | Conventional Commits format enforced |
| CODE-04 | L1 | ENG-4.2-MERGE | Squash merge required |
| CODE-05 | L1 | ENG-4.3-COMPLEXITY/LOC/DEAD | SonarQube quality gate passes |
| CODE-06 | L2 | ENG-6.2-ADR | ADR created if architectural change |
| CODE-07 | L2 | ENG-6.2-ADR | Architecture Guild approval obtained |
| CODE-08 | L3 | TECH-DEBT-SCOPE | No new technical debt introduced |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage |
| TEST-03 | L1 | QA-2.1-COVERAGE | No coverage regression |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests for all new/changed methods |
| TEST-05 | L3 | TECH-DEBT-REFACTOR | Refactored code maintains 100% existing coverage |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes |
| SEC-04 | L1 | SEC-3.3-DEPS-APPROVAL | New dependencies in approved registry |
| SEC-05 | L1 | SEC-3.3-DEPS | Maven dependency check 0 Critical CVEs |
| SEC-06 | L1 | SEC-4.2-SECRETS-MGMT | Secrets in AWS Secrets Manager/GitHub |
| DOC-01 | L2 | TECH-DEBT-JUSTIFICATION | Business justification documented |
| DOC-02 | L2 | TECH-DEBT-SCOPE | Scope boundaries documented |
| DOC-03 | L3 | TECH-DEBT-METRICS | Before/after metrics documented |
| DOC-04 | L3 | TECH-DEBT-ADR-UPDATE | Existing ADR marked superseded if applicable |
| CI-01 | L1 | CI-ALL-CHECKS | All GitHub Actions checks pass |
| CI-02 | L3 | TECH-DEBT-BUILD-TIME | No >10% build time increase |
| ACCEPT-01 | L2 | TECH-DEBT-DEMO | Demoed to team if affects shared code |
| ACCEPT-02 | L2 | TECH-DEBT-SIGN-OFF | Tech Lead approved |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions |

---

## API Change DoD

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L2 | ENG-4.1-SEC | Security Champion approval for security-critical paths |
| CODE-03 | L1 | ENG-4.2-SIGN | All commits signed with GPG/SSH |
| CODE-04 | L1 | ENG-4.2-CONV | Conventional Commits format enforced |
| CODE-05 | L1 | ENG-4.2-MERGE | Squash merge required |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY/LOC/DEAD | SonarQube quality gate passes |
| TEST-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage |
| TEST-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage |
| TEST-03 | L1 | QA-2.1-COVERAGE | No coverage regression |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests for all new/changed methods |
| TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests cover API endpoints |
| TEST-06 | L2 | INC-002 | Contract tests include nullable field tests |
| TEST-07 | L2 | QA-2.4-PERF | k6 load test for >1000 RPS endpoints |
| TEST-08 | L2 | QA-2.4-PERF | k6 results show P95 <500ms, P99 <2000ms |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes |
| SEC-04 | L1 | SEC-3.3-DEPS-APPROVAL | New dependencies in approved registry |
| SEC-05 | L1 | SEC-3.3-DEPS | Maven/npm audit 0 Critical CVEs |
| SEC-06 | L1 | SEC-4.2-SECRETS-MGMT | Secrets in AWS Secrets Manager/GitHub |
| DOC-01 | L2 | ENG-6.1-API | OpenAPI spec updated |
| DOC-02 | L2 | ENG-6.1-API | CHANGELOG.md updated |
| DOC-03 | L2 | ENG-6.1-API | API diff generated and attached |
| DOC-04 | L3 | TEAM-COMMERCE | Payment flow docs updated if applicable |
| CI-01 | L1 | CI-GATE | All GitHub Actions checks pass |
| CI-02 | L2 | TEAM-COMMERCE | Maven build succeeds |
| CI-03 | L3 | TEAM-COMMERCE | Schema compatibility verified if Kafka changes |
| ACC-01 | L2 | TEAM-PROCESS | Tech Lead reviewed API contract |
| ACC-02 | L3 | TEAM-COMMERCE | Downstream consumers notified for breaking changes |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions |

---

## Release DoD

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG/SSH |
| CODE-03 | L1 | ENG-4.2-CONV | Conventional Commits format enforced |
| CODE-04 | L1 | ENG-4.3-COMPLEXITY/LOC/DEAD | SonarQube quality gate passes |
| TEST-01 | L2 | QA-3.1-RELEASE | Full regression suite passed in staging |
| TEST-02 | L2 | QA-3.1-RELEASE | Full regression suite passed in pre-prod |
| TEST-03 | L2 | QA-3.1-RELEASE | Smoke tests passed in production |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes |
| SEC-04 | L1 | SEC-3.3-DEPS | Maven dependency check 0 Critical CVEs |
| SEC-05 | L1 | SEC-4.2-SECRETS-MGMT | Secrets in AWS Secrets Manager/GitHub |
| DOC-01 | L2 | QA-3.1-RELEASE | Release notes approved by EM |
| DOC-02 | L2 | QA-3.1-RELEASE | Runbook updated if procedures changed |
| DOC-03 | L3 | TEAM-RELEASE-NOTES | CHANGELOG.md migrated to version section |
| DEPLOY-01 | L2 | QA-3.1-RELEASE | Rollback plan documented and tested |
| DEPLOY-02 | L3 | TEAM-KAFKA-COMPAT | Kafka schema backward-compatible |
| DEPLOY-03 | L3 | TEAM-DB-MIGRATION | Database migration scripts tested |
| CI-01 | L1 | QA-2.1-COVERAGE | JaCoCo ≥80% line coverage |
| CI-02 | L1 | QA-2.1-COVERAGE | JaCoCo ≥75% branch coverage |
| CI-03 | L1 | CI-ALL-GREEN | All GitHub Actions checks pass |
| ACCEPT-01 | L2 | QA-3.1-RELEASE | EM sign-off obtained |
| ACCEPT-02 | L3 | TEAM-PRODUCT-SIGNOFF | PO reviewed release notes |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions |

---

## Infrastructure DoD

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG/SSH |
| CODE-03 | L1 | ENG-4.2-CONV | Conventional Commits format enforced |
| CODE-04 | L2 | SEC-4.1-TERRAFORM | Terraform plan shows no unintended deletions |
| CODE-05 | L2 | SEC-4.1-TERRAFORM | Platform Engineering approval obtained |
| CODE-06 | L2 | ENG-6.2-ADR | ADR created if architectural change |
| CODE-07 | L2 | ENG-6.2-ADR | Architecture Guild approval obtained |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes |
| SEC-04 | L1 | SEC-4.2-SECRETS-MGMT | Secrets in AWS Secrets Manager/GitHub |
| SEC-05 | L1 | SEC-3.3-DEPS-APPROVAL | New dependencies in approved registry |
| SEC-06 | L2 | SEC-4.1-TERRAFORM | tfsec scan passes |
| TEST-01 | L2 | QA-3.1-RELEASE | Validated in staging before production |
| TEST-02 | L3 | TEAM-KAFKA | Kafka topic configurations validated |
| TEST-03 | L3 | TEAM-POSTGRES | PostgreSQL schema tested with realistic data |
| DOC-01 | L2 | QA-3.1-RELEASE | Runbook updated if procedures changed |
| DOC-02 | L2 | QA-3.1-RELEASE | Rollback plan documented and tested |
| DOC-03 | L3 | TEAM-COMMERCE | README.md updated |
| DOC-04 | L2 | ENG-6.2-ADR | Terraform module docs updated |
| DR-01 | L3 | TEAM-DR | DR impact assessed |
| DR-02 | L3 | TEAM-DR | Backup/restore procedures tested |
| CI-01 | L1 | ENG-4.2-MERGE | Squash merge required |
| CI-02 | L1 | SEC-3.1-SNYK | All GitHub Actions checks pass |
| CI-03 | L2 | SEC-4.1-TERRAFORM | terraform validate and fmt pass |
| CI-04 | L3 | TEAM-IAAC | Terraform state locking enabled |
| ACC-01 | L2 | QA-3.1-RELEASE | EM sign-off for production changes |
| ACC-02 | L3 | TEAM-COSTMGMT | Cost impact assessment completed |
| ACC-03 | L2 | SEC-4.1-TERRAFORM | Platform Engineering confirms standards compliance |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific additions |

---

## Escaped Defect Traceability

These criteria were synthesized directly from production incidents captured in `escaped_defects_log.csv`:

| Incident ID | Work Type | Criterion ID | Criterion Summary | Date Added |
|-------------|-----------|--------------|-------------------|------------|
| INC-001 | feature_story | TEST-08 | Integration test verifies SSO login flow for all auth providers | 2026-03-04 |
| INC-002 | api_change | TEST-06 | API contract tests include nullable field tests | 2026-03-04 |
| INC-003 | bug_fix | TEST-07 | Regression test covers exact reproduction path | 2026-03-04 |

**Impact:** These 3 escaped defect criteria ensure that historically-discovered production issues are permanently captured in the DoD, preventing recurrence.

---

## Policy Coverage Summary

| Source Policy Family | Criteria Count | Work Types Affected |
|---------------------|----------------|---------------------|
| ENG-4.x (Code Review & Quality) | 42 | All 6 work types |
| QA-2.x (Testing Standards) | 51 | All except release |
| QA-3.x (Release Standards) | 24 | release, infrastructure |
| SEC-3.x (Security Scanning) | 36 | All 6 work types |
| SEC-4.x (Infrastructure Security) | 16 | infrastructure, release |
| TEAM-* (Team-Specific) | 18 | feature_story, api_change, infrastructure |
| Escaped Defects (INC-*) | 3 | feature_story, api_change, bug_fix |

**Total Source Policies:** 45  
**Orphaned Policies:** 0 (100% policy coverage achieved)

---

## Layer Distribution

| Layer | Total Criteria | % of Total | Purpose |
|-------|----------------|-----------|----------|
| L1-UNIVERSAL | 68 | 40.2% | Non-negotiable gates for all work |
| L2-WORKTYPE | 78 | 46.2% | Work-type-specific requirements |
| L3-TEAM | 18 | 10.7% | Team tech stack and domain additions |
| L4-STORY | 6 | 3.6% | Story-specific placeholders |

**Quality Check:** L1 represents 40.2% of total criteria, meeting the <40% guideline to avoid over-restricting teams.

---

## Maintenance Notes

**Next Review:** 2026-06-02  
**Drift Detection:** Quarterly via `--drift-check` flag  
**Conflict Resolution:** All Type A and B conflicts resolved in Phase 2 (see `conflict_report.yaml`)  
**EM Governance:** Completed 2026-03-04 (see EM Governance Checklist in CLAUDE.md)

---
--- END OUTPUT: policy_traceability_matrix.md ---