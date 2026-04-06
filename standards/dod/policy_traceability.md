# Policy Traceability Matrix
Generated: 2026-04-06

## Overview
This matrix maps every DoD criterion across all work types to its source policy or standard document. It enables:
- **Audit traceability**: Every criterion links to a documented mandate
- **Impact analysis**: When a policy changes, identify affected criteria
- **Gap detection**: Policies without criteria become visible

## Matrix

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text (Summary) |
|---|---|---|---|---|
| CODE-01 | feature_story | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | feature_story | L2-WORKTYPE | ENG-4.1-SEC | Security Champion approval for auth/payment/PII paths |
| CODE-03 | feature_story | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH key |
| CODE-04 | feature_story | L1-UNIVERSAL | ENG-4.2 | Commit messages follow Conventional Commits format |
| CODE-05 | feature_story | L1-UNIVERSAL | ENG-4.2 | PR merged via squash merge only |
| CODE-06 | feature_story | L1-UNIVERSAL | ENG-4.3 | SonarQube quality gate passes, complexity ≤10 |
| CODE-07 | feature_story | L1-UNIVERSAL | ENG-4.3 | No method exceeds 50 lines of code |
| CODE-08 | feature_story | L1-UNIVERSAL | ENG-4.3 | No dead code present |
| TEST-01 | feature_story | L1-UNIVERSAL | QA-2.1 | JaCoCo reports ≥80% line coverage |
| TEST-02 | feature_story | L1-UNIVERSAL | QA-2.1 | JaCoCo reports ≥75% branch coverage |
| TEST-03 | feature_story | L1-UNIVERSAL | QA-2.1 | No existing covered code lost coverage |
| TEST-04 | feature_story | L2-WORKTYPE | QA-2.2-FEATURE | Unit tests present for new/changed business logic |
| TEST-05 | feature_story | L2-WORKTYPE | QA-2.2-FEATURE | Integration tests cover service interactions |
| TEST-06 | feature_story | L2-WORKTYPE | QA-2.2-FEATURE | E2E tests cover happy path + error path |
| TEST-07 | feature_story | L2-WORKTYPE | ESC-INC-001 | Integration test verifies SSO login for all auth methods |
| TEST-08 | feature_story | L2-WORKTYPE | QA-2.4 | k6 load test verifies P95<500ms, P99<2000ms for >1000 RPS |
| SEC-01 | feature_story | L1-UNIVERSAL | SEC-3.1 | Snyk scan shows 0 Critical/High findings |
| SEC-02 | feature_story | L1-UNIVERSAL | SEC-3.1 | Medium Snyk findings have tracked Jira tickets |
| SEC-03 | feature_story | L1-UNIVERSAL | SEC-3.2 | Gitleaks scan passes with 0 secrets detected |
| SEC-04 | feature_story | L1-UNIVERSAL | SEC-3.3 | Maven dependency:check shows 0 Critical CVEs |
| SEC-05 | feature_story | L1-UNIVERSAL | SEC-3.3 | npm audit shows 0 Critical CVEs |
| SEC-06 | feature_story | L1-UNIVERSAL | SEC-3.3 | All dependencies listed in approved registry |
| SEC-07 | feature_story | L1-UNIVERSAL | SEC-4.2 | No secrets in committed code |
| SEC-08 | feature_story | L1-UNIVERSAL | SEC-4.2 | All secrets in AWS Secrets Manager or GitHub Actions secrets |
| DOC-01 | feature_story | L3-TEAM | TEAM-STANDARD | JavaDoc comments on all new public methods |
| DOC-02 | feature_story | L3-TEAM | TEAM-STANDARD | JSDoc comments on all new exported React functions |
| DOC-03 | feature_story | L3-TEAM | TEAM-STANDARD | README.md updated if setup/env vars/dependencies changed |
| CI-01 | feature_story | L1-UNIVERSAL | TEAM-CI-TOOL | All GitHub Actions CI checks pass |
| CI-02 | feature_story | L3-TEAM | TEAM-STANDARD | Maven build passes locally and in CI |
| CI-03 | feature_story | L3-TEAM | TEAM-STANDARD | npm build and test pass locally and in CI |
| ACCEPT-01 | feature_story | L2-WORKTYPE | TEAM-STANDARD | All acceptance criteria verified by PO or QA |
| ACCEPT-02 | feature_story | L2-WORKTYPE | TEAM-STANDARD | UX review completed if feature includes UI changes |
| ACCEPT-03 | feature_story | L3-TEAM | TEAM-STANDARD | Analytics event tracking implemented if required |
| ACCEPT-04 | feature_story | L3-TEAM | TEAM-STANDARD | Feature flag configured if gradual rollout needed |
| CODE-01 | bug_fix | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | bug_fix | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH key |
| CODE-03 | bug_fix | L1-UNIVERSAL | ENG-4.2 | Commit messages follow Conventional Commits format |
| CODE-04 | bug_fix | L1-UNIVERSAL | ENG-4.2 | PR merged via squash merge only |
| CODE-05 | bug_fix | L1-UNIVERSAL | ENG-4.3 | SonarQube quality gate passes, complexity ≤10 |
| CODE-06 | bug_fix | L1-UNIVERSAL | ENG-4.3 | No method exceeds 50 lines of code |
| CODE-07 | bug_fix | L1-UNIVERSAL | ENG-4.3 | No dead code present |
| TEST-01 | bug_fix | L1-UNIVERSAL | QA-2.1 | JaCoCo reports ≥80% line coverage |
| TEST-02 | bug_fix | L1-UNIVERSAL | QA-2.1 | JaCoCo reports ≥75% branch coverage |
| TEST-03 | bug_fix | L1-UNIVERSAL | QA-2.1 | No existing covered code lost coverage |
| TEST-04 | bug_fix | L2-WORKTYPE | QA-2.2-BUG | Unit tests present for bug fix code path |
| TEST-05 | bug_fix | L2-WORKTYPE | QA-2.2-BUG | Integration tests if bug involves service/data layer |
| TEST-06 | bug_fix | L2-WORKTYPE | QA-2.2-BUG | E2E tests if bug is UI-related |
| TEST-07 | bug_fix | L2-WORKTYPE | QA-2.3, ESC-INC-003 | Regression test covering exact reproduction path from bug report |
| SEC-01 | bug_fix | L1-UNIVERSAL | SEC-3.1 | Snyk scan shows 0 Critical/High, Medium tracked |
| SEC-02 | bug_fix | L1-UNIVERSAL | SEC-3.2 | Gitleaks scan passes with 0 secrets detected |
| SEC-03 | bug_fix | L1-UNIVERSAL | SEC-3.3 | Maven/npm dependency checks show 0 Critical CVEs |
| SEC-04 | bug_fix | L1-UNIVERSAL | SEC-4.2 | No secrets in version control, all in Secrets Manager |
| DOC-01 | bug_fix | L2-WORKTYPE | IMPLICIT-BUG-FIX-STANDARD | Bug ticket updated with root cause analysis |
| DOC-02 | bug_fix | L3-TEAM | TEAM-PRACTICE | CHANGELOG.md updated if public API affected |
| CI-01 | bug_fix | L1-UNIVERSAL | IMPLICIT-CI-GATE | All GitHub Actions checks pass |
| CI-02 | bug_fix | L3-TEAM | TEAM-PRACTICE | Spring Boot application starts with fix applied |
| ACC-01 | bug_fix | L2-WORKTYPE | IMPLICIT-BUG-FIX-STANDARD | Bug reporter/QA verifies fix in staging |
| ACC-02 | bug_fix | L3-TEAM | TEAM-PRACTICE | Manual smoke test if payment/order flow affected |
| CODE-01 | tech_debt | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | tech_debt | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH key |
| CODE-03 | tech_debt | L1-UNIVERSAL | ENG-4.2 | Commit messages follow Conventional Commits format |
| CODE-04 | tech_debt | L1-UNIVERSAL | ENG-4.2 | PR merged via squash merge only |
| CODE-05 | tech_debt | L1-UNIVERSAL | ENG-4.3 | SonarQube quality gate passes, complexity ≤10 |
| CODE-06 | tech_debt | L1-UNIVERSAL | ENG-4.3 | No method exceeds 50 lines of code |
| CODE-07 | tech_debt | L1-UNIVERSAL | ENG-4.3 | No dead code present |
| CODE-08 | tech_debt | L2-WORKTYPE | QA-2.2-DEBT | No new technical debt introduced (SonarQube metric) |
| TEST-01 | tech_debt | L1-UNIVERSAL | QA-2.1 | JaCoCo reports ≥80% line coverage |
| TEST-02 | tech_debt | L1-UNIVERSAL | QA-2.1 | JaCoCo reports ≥75% branch coverage |
| TEST-03 | tech_debt | L1-UNIVERSAL | QA-2.1 | No existing covered code lost coverage |
| TEST-04 | tech_debt | L2-WORKTYPE | QA-2.2-DEBT | Unit tests cover refactored code paths |
| TEST-05 | tech_debt | L2-WORKTYPE | QA-2.2-DEBT | Integration tests if refactoring affects service boundaries |
| SEC-01 | tech_debt | L1-UNIVERSAL | SEC-3.1 | Snyk scan shows 0 Critical/High, Medium tracked |
| SEC-02 | tech_debt | L1-UNIVERSAL | SEC-3.2 | Gitleaks scan passes with 0 secrets detected |
| SEC-03 | tech_debt | L1-UNIVERSAL | SEC-3.3 | Maven/npm dependency checks show 0 Critical CVEs |
| SEC-04 | tech_debt | L1-UNIVERSAL | SEC-4.2 | No secrets in version control, all in Secrets Manager |
| ARCH-01 | tech_debt | L2-WORKTYPE | ENG-6.2 | ADR created documenting architecture change |
| ARCH-02 | tech_debt | L2-WORKTYPE | ENG-6.2 | PR approved by Architecture Guild member |
| ARCH-03 | tech_debt | L3-TEAM | TEAM-TECH-DEBT | Spring Boot dependencies upgraded to latest patch |
| DOC-01 | tech_debt | L1-UNIVERSAL | ENG-GENERAL | README.md updated if setup/build changed |
| DOC-02 | tech_debt | L2-WORKTYPE | ENG-6.2 | Inline comments explain non-obvious refactoring decisions |
| DOC-03 | tech_debt | L3-TEAM | TEAM-TECH-DEBT | Javadoc updated if public API signatures changed |
| CI-01 | tech_debt | L1-UNIVERSAL | CI-GENERAL | All GitHub Actions CI checks pass |
| CI-02 | tech_debt | L1-UNIVERSAL | QA-2.1 | JaCoCo coverage report attached to PR |
| CI-03 | tech_debt | L2-WORKTYPE | QA-TECH-DEBT | No new compiler warnings introduced |
| ACC-01 | tech_debt | L2-WORKTYPE | ENG-TECH-DEBT | Tech Lead confirms refactoring objective met with measurement |
| ACC-02 | tech_debt | L2-WORKTYPE | ENG-TECH-DEBT | No new TODO/FIXME without tracked Jira tickets |
| CODE-01 | api_change | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | api_change | L2-WORKTYPE | ENG-4.1-SEC | Security Champion approval for auth/payment/PII paths |
| CODE-03 | api_change | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH key |
| CODE-04 | api_change | L1-UNIVERSAL | ENG-4.2 | Commit messages follow Conventional Commits format |
| CODE-05 | api_change | L1-UNIVERSAL | ENG-4.2 | PR merged via squash merge only |
| CODE-06 | api_change | L1-UNIVERSAL | ENG-4.3 | SonarQube quality gate passes, complexity ≤10 |
| CODE-07 | api_change | L1-UNIVERSAL | ENG-4.3 | No method exceeds 50 lines of code |
| CODE-08 | api_change | L1-UNIVERSAL | ENG-4.3 | No dead code present |
| TEST-01 | api_change | L1-UNIVERSAL | QA-2.1 | JaCoCo reports ≥80% line coverage |
| TEST-02 | api_change | L1-UNIVERSAL | QA-2.1 | JaCoCo reports ≥75% branch coverage |
| TEST-03 | api_change | L1-UNIVERSAL | QA-2.1 | No existing covered code lost coverage |
| TEST-04 | api_change | L2-WORKTYPE | QA-2.2-API | Unit tests present for all API endpoint logic |
| TEST-05 | api_change | L2-WORKTYPE | QA-2.2-API | Integration tests cover full request/response cycle |
| TEST-06 | api_change | L2-WORKTYPE | ESC-INC-002 | API contract tests validate all nullable fields |
| TEST-07 | api_change | L2-WORKTYPE | QA-2.4 | k6 load test verifies P95<500ms, P99<2000ms for >1000 RPS |
| TEST-08 | api_change | L3-TEAM | TEAM-KAFKA | Kafka consumer/producer integration tests if applicable |
| SEC-01 | api_change | L1-UNIVERSAL | SEC-3.1 | Snyk scan shows 0 Critical/High, Medium tracked |
| SEC-02 | api_change | L1-UNIVERSAL | SEC-3.2 | Gitleaks scan passes with 0 secrets detected |
| SEC-03 | api_change | L1-UNIVERSAL | SEC-3.3 | Maven/npm dependency checks show 0 Critical CVEs |
| SEC-04 | api_change | L1-UNIVERSAL | SEC-4.2 | No secrets in version control, all in Secrets Manager |
| SEC-05 | api_change | L3-TEAM | TEAM-SPRING-SEC | Spring Security config reviewed for changed endpoints |
| DOC-01 | api_change | L2-WORKTYPE | ENG-6.1 | OpenAPI spec updated to reflect endpoint changes |
| DOC-02 | api_change | L2-WORKTYPE | ENG-6.1 | CHANGELOG.md updated with API change entry |
| DOC-03 | api_change | L2-WORKTYPE | ENG-6.1 | API diff generated and attached to PR |
| DOC-04 | api_change | L3-TEAM | TEAM-POSTMAN | Postman collection updated with example requests |
| CI-01 | api_change | L1-UNIVERSAL | CI-GATE | All GitHub Actions CI checks pass |
| CI-02 | api_change | L3-TEAM | TEAM-SONAR | SonarQube Quality Gate status = PASSED |
| CI-03 | api_change | L3-TEAM | TEAM-DOCKER | Docker image builds and passes container scan |
| ACC-01 | api_change | L3-TEAM | TEAM-API-REVIEW | API change reviewed by backend engineer outside team |
| ACC-02 | api_change | L3-TEAM | TEAM-CONSUMER | Breaking changes communicated to known API consumers |
| CODE-01 | release | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | release | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH key |
| CODE-03 | release | L1-UNIVERSAL | ENG-4.2 | Commit messages follow Conventional Commits format |
| TEST-01 | release | L2-WORKTYPE | QA-3.1 | Full regression suite passes in staging and pre-prod |
| TEST-02 | release | L2-WORKTYPE | QA-3.1 | Smoke test suite passes in production post-deploy |
| TEST-03 | release | L3-TEAM | TEAM-TECH-STACK | Kafka consumer lag verified <100 messages |
| TEST-04 | release | L3-TEAM | TEAM-TECH-STACK | PostgreSQL migrations tested with rollback verified |
| SEC-01 | release | L1-UNIVERSAL | SEC-3.1 | Snyk scan shows 0 Critical/High, Medium tracked |
| SEC-02 | release | L1-UNIVERSAL | SEC-3.2 | Gitleaks scan passes with 0 secrets detected |
| SEC-03 | release | L1-UNIVERSAL | SEC-3.3 | Maven/npm dependency checks show 0 Critical CVEs |
| SEC-04 | release | L1-UNIVERSAL | SEC-4.2 | No secrets in version control, all in Secrets Manager |
| DOC-01 | release | L2-WORKTYPE | QA-3.1 | Release notes prepared and EM approved |
| DOC-02 | release | L2-WORKTYPE | QA-3.1 | Runbook updated if operational procedures changed |
| DOC-03 | release | L3-TEAM | TEAM-TECH-STACK | API documentation updated in Confluence if applicable |
| CI-01 | release | L1-UNIVERSAL | TEAM-CI-TOOL | All GitHub Actions CI checks pass |
| CI-02 | release | L2-WORKTYPE | QA-3.1 | Rollback plan documented and tested in staging |
| CI-03 | release | L3-TEAM | TEAM-TECH-STACK | Spring Boot health checks return 200 OK all environments |
| CI-04 | release | L3-TEAM | TEAM-TECH-STACK | React bundle size regression <5% from previous release |
| ACC-01 | release | L2-WORKTYPE | QA-3.1 | Engineering Manager sign-off obtained |
| ACC-02 | release | L3-TEAM | TEAM-SCALE-UP | PO notified of deployment window and confirms readiness |
| ACC-03 | release | L3-TEAM | TEAM-DOMAIN | Payment gateway verified in production with test transactions |
| CODE-01 | infrastructure | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| CODE-02 | infrastructure | L2-WORKTYPE | ENG-6.2 | ADR created documenting infrastructure change |
| CODE-03 | infrastructure | L2-WORKTYPE | ENG-6.2 | PR approved by Architecture Guild member |
| CODE-04 | infrastructure | L2-WORKTYPE | SEC-4.1 | PR approved by Platform Engineering team member |
| CODE-05 | infrastructure | L1-UNIVERSAL | ENG-4.2 | All commits signed with GPG/SSH key |
| CODE-06 | infrastructure | L1-UNIVERSAL | ENG-4.2 | Commit messages follow Conventional Commits format |
| INFRA-01 | infrastructure | L2-WORKTYPE | SEC-4.1 | terraform plan executed with clean plan |
| INFRA-02 | infrastructure | L2-WORKTYPE | SEC-4.1 | tfsec scan passes with 0 HIGH/CRITICAL findings |
| INFRA-03 | infrastructure | L3-TEAM | TEAM-INFRA-01 | Terraform state in remote backend (S3 + DynamoDB) |
| INFRA-04 | infrastructure | L3-TEAM | TEAM-INFRA-02 | Infrastructure changes tested in non-prod first |
| INFRA-05 | infrastructure | L3-TEAM | TEAM-INFRA-03 | Disaster recovery procedure verified for stateful resources |
| SEC-01 | infrastructure | L1-UNIVERSAL | SEC-3.1 | Snyk scan shows 0 Critical/High, Medium tracked |
| SEC-02 | infrastructure | L1-UNIVERSAL | SEC-3.2 | Gitleaks scan passes with 0 secrets detected |
| SEC-03 | infrastructure | L1-UNIVERSAL | SEC-4.2 | No secrets in version control, all in Secrets Manager |
| SEC-04 | infrastructure | L3-TEAM | TEAM-SEC-01 | AWS IAM roles follow least-privilege with documented justification |
| SEC-05 | infrastructure | L3-TEAM | TEAM-SEC-02 | Security groups allow only required ports and CIDR blocks |
| DOC-01 | infrastructure | L2-WORKTYPE | INFRA-DOC-01 | Runbook updated/created with deployment and troubleshooting |
| DOC-02 | infrastructure | L2-WORKTYPE | INFRA-DOC-02 | README/docs updated to reflect infrastructure changes |
| DOC-03 | infrastructure | L3-TEAM | TEAM-DOC-01 | Terraform modules include README with inputs/outputs/examples |
| CI-01 | infrastructure | L1-UNIVERSAL | CI-GATE-01 | All GitHub Actions CI checks pass |
| CI-02 | infrastructure | L2-WORKTYPE | CI-INFRA-01 | terraform fmt check passes |
| CI-03 | infrastructure | L2-WORKTYPE | CI-INFRA-02 | terraform validate passes |
| ACC-01 | infrastructure | L2-WORKTYPE | INFRA-ACC-01 | Infrastructure deployed to staging and validated before prod |
| ACC-02 | infrastructure | L2-WORKTYPE | INFRA-ACC-02 | Rollback plan documented and verified in staging |
| ACC-03 | infrastructure | L3-TEAM | TEAM-ACC-01 | Monitoring and alerting configured for new resources |

## Source Policy Coverage Summary

| Source Policy | Total Criteria Referencing | Work Types |
|---|---|---|
| ENG-4.1 | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.2 | 18 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ENG-4.3 | 18 | feature_story, bug_fix, tech_debt, api_change |
| ENG-6.1 | 3 | api_change |
| ENG-6.2 | 6 | tech_debt, infrastructure |
| QA-2.1 | 18 | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-FEATURE | 3 | feature_story |
| QA-2.2-BUG | 3 | bug_fix |
| QA-2.2-DEBT | 3 | tech_debt |
| QA-2.2-API | 2 | api_change |
| QA-2.3 | 1 | bug_fix |
| QA-2.4 | 2 | feature_story, api_change |
| QA-3.1 | 6 | release |
| SEC-3.1 | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| SEC-3.2 | 6 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| SEC-3.3 | 12 | feature_story, bug_fix, tech_debt, api_change, release |
| SEC-4.1 | 2 | infrastructure |
| SEC-4.2 | 12 | feature_story, bug_fix, tech_debt, api_change, release, infrastructure |
| ESC-INC-001 | 1 | feature_story |
| ESC-INC-002 | 1 | api_change |
| ESC-INC-003 | 1 | bug_fix |
| TEAM-STANDARD | 9 | feature_story |
| TEAM-PRACTICE | 3 | bug_fix |
| TEAM-TECH-DEBT | 3 | tech_debt |
| TEAM-KAFKA | 1 | api_change |
| TEAM-SPRING-SEC | 1 | api_change |
| TEAM-POSTMAN | 1 | api_change |
| TEAM-SONAR | 1 | api_change |
| TEAM-DOCKER | 1 | api_change |
| TEAM-API-REVIEW | 1 | api_change |
| TEAM-CONSUMER | 1 | api_change |
| TEAM-TECH-STACK | 5 | release |
| TEAM-SCALE-UP | 1 | release |
| TEAM-DOMAIN | 1 | release |
| TEAM-INFRA-01 | 1 | infrastructure |
| TEAM-INFRA-02 | 1 | infrastructure |
| TEAM-INFRA-03 | 1 | infrastructure |
| TEAM-SEC-01 | 1 | infrastructure |
| TEAM-SEC-02 | 1 | infrastructure |
| TEAM-DOC-01 | 1 | infrastructure |
| TEAM-CI-TOOL | 2 | feature_story, release |
| CI-GATE | 1 | api_change |
| CI-GATE-01 | 1 | infrastructure |
| CI-INFRA-01 | 1 | infrastructure |
| CI-INFRA-02 | 1 | infrastructure |
| INFRA-DOC-01 | 1 | infrastructure |
| INFRA-DOC-02 | 1 | infrastructure |
| INFRA-ACC-01 | 1 | infrastructure |
| INFRA-ACC-02 | 1 | infrastructure |
| TEAM-ACC-01 | 1 | infrastructure |
| ENG-GENERAL | 1 | tech_debt |
| CI-GENERAL | 1 | tech_debt |
| ENG-TECH-DEBT | 2 | tech_debt |
| QA-TECH-DEBT | 1 | tech_debt |
| IMPLICIT-BUG-FIX-STANDARD | 2 | bug_fix |
| IMPLICIT-CI-GATE | 1 | bug_fix |

## Escaped Defect Traceability

| Incident Reference | Criterion ID | Work Type | Criterion Summary |
|---|---|---|---|
| INC-001 | TEST-07 | feature_story | Integration test verifies SSO login for all auth methods |
| INC-002 | TEST-06 | api_change | API contract tests validate all nullable fields |
| INC-003 | TEST-07 | bug_fix | Regression test covering exact reproduction path |

**Total Escaped Defects Incorporated**: 3

---