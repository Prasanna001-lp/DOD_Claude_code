# Policy Traceability Matrix
Generated: 2026-04-27

This matrix provides complete traceability from DoD criteria back to source policies, standards, and escaped defects across all work types.

## Summary Statistics

| Metric | Count |
|--------|-------|
| Total Criteria | 142 |
| L1 Universal Criteria | 70 |
| L2 Work-Type Criteria | 52 |
| L3 Team-Specific Criteria | 18 |
| L4 Story-Specific Placeholders | 6 |
| Escaped Defect Criteria | 3 |
| Unique Source Policies Referenced | 34 |

## Full Traceability Matrix

| Work Type | Criterion ID | Layer | Source Policy Ref | Criterion Text (Abbreviated) |
|-----------|--------------|-------|-------------------|------------------------------|
| feature_story | CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| feature_story | CODE-02 | L3 | ENG-4.1-SEC | PR touching security-critical code has 3rd approval from Security Champion |
| feature_story | CODE-03 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key verified by GitHub |
| feature_story | CODE-04 | L1 | ENG-4.2-MSG | All commit messages follow Conventional Commits format |
| feature_story | CODE-05 | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy |
| feature_story | CODE-06 | L1 | ENG-4.3-COMPLEXITY | SonarQube cyclomatic complexity ≤10 per method |
| feature_story | CODE-07 | L1 | ENG-4.3-LOC | SonarQube no methods exceeding 50 lines of code |
| feature_story | CODE-08 | L1 | ENG-4.3-DEAD | SonarQube 0 dead code findings |
| feature_story | TEST-01 | L1 | QA-2.1-LINE | JaCoCo ≥80% line coverage on changed modules |
| feature_story | TEST-02 | L1 | QA-2.1-BRANCH | JaCoCo ≥75% branch coverage on changed modules |
| feature_story | TEST-03 | L1 | QA-2.1-REGRESS | No coverage regression on existing covered code |
| feature_story | TEST-04 | L2 | QA-2.2-UNIT | Unit tests using JUnit 5 for new/changed business logic |
| feature_story | TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests covering service/database/Kafka integration |
| feature_story | TEST-06 | L2 | QA-2.2-E2E | E2E tests using Playwright covering happy path and error path |
| feature_story | TEST-07 | L2 | INC-001 | Integration test verifies SSO login flow for OAuth and SAML |
| feature_story | TEST-08 | L2 | QA-2.4-PERF | k6 load test for endpoints >1000 RPS, P95<500ms, P99<2000ms |
| feature_story | SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan 0 Critical/High findings |
| feature_story | SEC-02 | L1 | SEC-3.1-SNYK | All Medium Snyk findings have tracked Jira tickets |
| feature_story | SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected |
| feature_story | SEC-04 | L1 | SEC-3.3-DEPS | All new dependencies in approved registry |
| feature_story | SEC-05 | L1 | SEC-3.3-DEPS | npm audit / mvn dependency:check 0 Critical CVE findings |
| feature_story | SEC-06 | L1 | SEC-4.2-SECRETS-MGMT | All secrets in AWS Secrets Manager or GitHub Actions secrets |
| feature_story | DOC-01 | L3 | TEAM-STANDARD | README.md updated if setup instructions changed |
| feature_story | DOC-02 | L3 | TEAM-STANDARD | Inline comments for complex business logic (complexity >5) |
| feature_story | CI-01 | L1 | PLATFORM-GATE | All GitHub Actions CI checks pass |
| feature_story | CI-02 | L3 | TEAM-STANDARD | Spring Boot app starts successfully in Docker (backend) |
| feature_story | CI-03 | L3 | TEAM-STANDARD | React build produces optimized bundle <5MB (frontend) |
| feature_story | ACCEPT-01 | L2 | FEATURE-STORY-STANDARD | All acceptance criteria verified by Product Owner |
| feature_story | ACCEPT-02 | L3 | TEAM-STANDARD | UX Designer approval for new UI components |
| feature_story | ACCEPT-03 | L3 | TEAM-STANDARD | Analytics event tracking verified in staging |
| feature_story | SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder |
| bug_fix | CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| bug_fix | CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| bug_fix | CODE-03 | L1 | ENG-4.2-MSG | Commit messages follow Conventional Commits format |
| bug_fix | CODE-04 | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy |
| bug_fix | CODE-05 | L1 | ENG-4.3-COMPLEXITY | SonarQube cyclomatic complexity ≤10 per method |
| bug_fix | CODE-06 | L1 | ENG-4.3-LOC | SonarQube no methods exceeding 50 lines |
| bug_fix | CODE-07 | L1 | ENG-4.3-DEAD | SonarQube 0 dead code findings |
| bug_fix | CODE-08 | L3 | ENG-4.1-SEC | PR touching security-critical code has Security Champion approval |
| bug_fix | TEST-01 | L1 | QA-2.1-LINE | JaCoCo ≥80% line coverage |
| bug_fix | TEST-02 | L1 | QA-2.1-BRANCH | JaCoCo ≥75% branch coverage |
| bug_fix | TEST-03 | L1 | QA-2.1-REGRESS | No coverage regression |
| bug_fix | TEST-04 | L2 | QA-2.2-UNIT | Unit tests using JUnit 5 for changed logic |
| bug_fix | TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests covering bug integration layer |
| bug_fix | TEST-06 | L2 | QA-2.2-E2E | E2E test covering UI flow where bug occurred |
| bug_fix | TEST-07 | L2 | QA-2.3-REGRESSION | Regression test covering exact bug reproduction path |
| bug_fix | TEST-08 | L2 | INC-003 | Regression test from escaped defect in CI |
| bug_fix | SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan 0 Critical/High findings |
| bug_fix | SEC-02 | L1 | SEC-3.1-SNYK | Medium Snyk findings tracked in Jira |
| bug_fix | SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes |
| bug_fix | SEC-04 | L1 | SEC-3.3-DEPS | New dependencies in approved registry |
| bug_fix | SEC-05 | L1 | SEC-3.3-DEPS | 0 Critical CVE findings |
| bug_fix | DOC-01 | L2 | BUG-FIX-ROOT-CAUSE | Root cause analysis documented |
| bug_fix | DOC-02 | L2 | BUG-FIX-REPRO | Exact reproduction steps referenced |
| bug_fix | DOC-03 | L3 | TEAM-CHANGELOG | CHANGELOG.md updated if user-facing change |
| bug_fix | CI-01 | L1 | CI-ALL-CHECKS | All GitHub Actions checks pass |
| bug_fix | CI-02 | L2 | BUG-FIX-VERIFICATION | Bug verified fixed in staging/pre-prod |
| bug_fix | ACC-01 | L2 | BUG-FIX-REPORTER | Bug reporter or PO confirms fix |
| bug_fix | ACC-02 | L3 | TEAM-QA-SIGNOFF | QA verifies no side effects |
| bug_fix | SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder |
| tech_debt | CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| tech_debt | CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| tech_debt | CODE-03 | L1 | ENG-4.2-MSG | Commit messages follow Conventional Commits |
| tech_debt | CODE-04 | L1 | ENG-4.2-MERGE | PR merged using squash merge |
| tech_debt | CODE-05 | L1 | ENG-4.3-COMPLEXITY | SonarQube complexity ≤10 per method |
| tech_debt | CODE-06 | L1 | ENG-4.3-LOC | SonarQube no methods >50 lines |
| tech_debt | CODE-07 | L1 | ENG-4.3-DEAD | SonarQube 0 dead code findings |
| tech_debt | CODE-08 | L2 | ENG-6.2-ARCH | ADR created if architectural change |
| tech_debt | TEST-01 | L1 | QA-2.1-LINE | JaCoCo ≥80% line coverage |
| tech_debt | TEST-02 | L1 | QA-2.1-BRANCH | JaCoCo ≥75% branch coverage |
| tech_debt | TEST-03 | L1 | QA-2.1-REGRESS | No coverage regression |
| tech_debt | TEST-04 | L2 | QA-2.2-UNIT | Unit tests using JUnit 5 |
| tech_debt | TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests covering changed integration layers |
| tech_debt | TEST-06 | L2 | ENG-6.2-ARCH | Architecture Guild approval if architectural |
| tech_debt | TEST-07 | L3 | TEAM-TECHDEBT-01 | No new SonarQube technical debt introduced |
| tech_debt | SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| tech_debt | SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| tech_debt | SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks passes |
| tech_debt | SEC-04 | L1 | SEC-3.3-DEPS | New dependencies approved |
| tech_debt | SEC-05 | L1 | SEC-3.3-DEPS | 0 Critical CVE findings |
| tech_debt | DOC-01 | L2 | ENG-6.2-ARCH | ADR template followed |
| tech_debt | DOC-02 | L3 | TEAM-TECHDEBT-02 | Original ticket updated with resolution summary |
| tech_debt | DOC-03 | L3 | TEAM-TECHDEBT-03 | README or docs updated if structure changed |
| tech_debt | CI-01 | L1 | CI-GATE-ALL | All GitHub Actions checks pass |
| tech_debt | CI-02 | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes |
| tech_debt | ACCEPT-01 | L2 | TECH-DEBT-SIGNOFF | Tech Lead approval that objective achieved |
| tech_debt | ACCEPT-02 | L3 | TEAM-TECHDEBT-04 | Performance benchmarks show <10% degradation |
| tech_debt | SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder |
| api_change | CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| api_change | CODE-02 | L3 | ENG-4.1-SEC | Security Champion approval for security-critical code |
| api_change | CODE-03 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| api_change | CODE-04 | L1 | ENG-4.2-MSG | Commit messages follow Conventional Commits |
| api_change | CODE-05 | L1 | ENG-4.2-MERGE | PR merged using squash merge |
| api_change | CODE-06 | L1 | ENG-4.3-COMPLEXITY | SonarQube complexity ≤10 per method |
| api_change | CODE-07 | L1 | ENG-4.3-LOC | SonarQube no methods >50 lines |
| api_change | CODE-08 | L1 | ENG-4.3-DEAD | SonarQube 0 dead code findings |
| api_change | TEST-01 | L1 | QA-2.1-LINE | JaCoCo ≥80% line coverage |
| api_change | TEST-02 | L1 | QA-2.1-BRANCH | JaCoCo ≥75% branch coverage |
| api_change | TEST-03 | L1 | QA-2.1-REGRESS | No coverage regression |
| api_change | TEST-04 | L2 | QA-2.2-UNIT | Unit tests using JUnit 5 for API handlers and service layer |
| api_change | TEST-05 | L2 | QA-2.2-INTEGRATION | Integration tests for API endpoint with real dependencies |
| api_change | TEST-06 | L2 | INC-002 | API contract tests include all nullable fields |
| api_change | TEST-07 | L2 | QA-2.4-PERF | k6 load test for endpoints >1000 RPS |
| api_change | SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| api_change | SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| api_change | SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks passes, secrets in AWS Secrets Manager |
| api_change | SEC-04 | L1 | SEC-3.3-DEPS | New dependencies approved |
| api_change | SEC-05 | L1 | SEC-3.3-DEPS | 0 Critical CVE findings |
| api_change | DOC-01 | L2 | ENG-6.1-API | OpenAPI spec updated |
| api_change | DOC-02 | L2 | ENG-6.1-API | CHANGELOG.md updated with API changes |
| api_change | DOC-03 | L2 | ENG-6.1-API | API diff generated using openapi-diff |
| api_change | DOC-04 | L2 | ENG-6.2-ARCH | ADR created if cross-service contract change |
| api_change | DOC-05 | L2 | ENG-6.2-ARCH | Architecture Guild approval documented |
| api_change | CI-01 | L1 | UNIVERSAL | All GitHub Actions checks pass |
| api_change | CI-02 | L1 | UNIVERSAL | SonarQube quality gate passes |
| api_change | CI-03 | L3 | TEAM-COMMERCE | API contract validation using Spring Cloud Contract or Pact |
| api_change | ACC-01 | L2 | WORKTYPE-API | API change reviewed by consumer team or API PO |
| api_change | ACC-02 | L3 | TEAM-COMMERCE | Breaking changes have migration guide, 1 sprint notice |
| api_change | SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder |
| release | CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| release | CODE-02 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| release | CODE-03 | L1 | ENG-4.2-MSG | Commit messages follow Conventional Commits |
| release | CODE-04 | L1 | ENG-4.2-MERGE | PR merged using squash merge |
| release | TEST-01 | L2 | QA-3.1-REGRESSION-SUITE | Full regression suite passes in staging and pre-prod |
| release | TEST-02 | L2 | QA-3.1-SMOKE | Smoke tests pass in production within 15 minutes |
| release | SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings |
| release | SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| release | SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks passes |
| release | SEC-04 | L1 | SEC-3.3-DEPS | New dependencies approved |
| release | SEC-05 | L1 | SEC-3.3-DEPS | 0 Critical CVE findings |
| release | DOC-01 | L2 | QA-3.1-NOTES | Release notes in CHANGELOG.md, EM approved |
| release | DOC-02 | L2 | QA-3.1-ROLLBACK | Rollback plan documented and verified in staging |
| release | DOC-03 | L2 | QA-3.1-RUNBOOK | Runbook updated if operational procedures changed |
| release | DOC-04 | L3 | TEAM-COMMERCE-KAFKA | Kafka schema changes documented with compatibility check |
| release | CI-01 | L1 | CI-UNIVERSAL | All GitHub Actions checks pass |
| release | CI-02 | L1 | ENG-4.3-COMPLEXITY | SonarQube complexity gate passes |
| release | CI-03 | L1 | ENG-4.3-LOC | SonarQube no methods >50 lines |
| release | CI-04 | L1 | ENG-4.3-DEAD | SonarQube 0 dead code |
| release | CI-05 | L3 | TEAM-COMMERCE-DB | PostgreSQL migrations tested with rollback verified |
| release | ACC-01 | L2 | QA-3.1-NOTES | Engineering Manager approval documented |
| release | ACC-02 | L3 | TEAM-COMMERCE-RELEASE | Product Owner notified and accepts release scope |
| release | ACC-03 | L3 | TEAM-COMMERCE-RELEASE | On-call engineer notified 24 hours before deploy |
| release | SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder |
| infrastructure | CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals including 1 senior engineer |
| infrastructure | CODE-02 | L3 | ENG-4.1-SEC | Security Champion approval for security-critical infrastructure |
| infrastructure | CODE-03 | L1 | ENG-4.2-SIGN | All commits signed with GPG or SSH key |
| infrastructure | CODE-04 | L1 | ENG-4.2-MSG | Commit messages follow Conventional Commits |
| infrastructure | CODE-05 | L1 | ENG-4.2-MERGE | PR merged using squash merge |
| infrastructure | INFRA-01 | L2 | SEC-4.1-TERRAFORM | terraform plan output attached, no unintended deletions |
| infrastructure | INFRA-02 | L2 | SEC-4.1-TERRAFORM | Platform Engineering team approval documented |
| infrastructure | INFRA-03 | L2 | SEC-4.1-TERRAFORM | tfsec scan 0 HIGH/CRITICAL findings |
| infrastructure | INFRA-04 | L2 | ENG-6.2-ARCH | ADR created if architectural change |
| infrastructure | INFRA-05 | L2 | ENG-6.2-ARCH | Architecture Guild approval documented |
| infrastructure | INFRA-06 | L3 | TEAM-INFRA-DR | DR verification for stateful resources |
| infrastructure | SEC-01 | L1 | SEC-3.1-SNYK | Snyk 0 Critical/High findings in Terraform dependencies |
| infrastructure | SEC-02 | L1 | SEC-3.1-SNYK | Medium findings tracked in Jira |
| infrastructure | SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks passes |
| infrastructure | SEC-04 | L1 | SEC-3.3-DEPS | New Terraform providers/modules approved |
| infrastructure | SEC-05 | L1 | SEC-4.2-SECRETS-MGMT | Secrets in AWS Secrets Manager or GitHub Actions secrets |
| infrastructure | DOC-01 | L2 | TEAM-INFRA-RUNBOOK | Runbook created/updated in docs/runbooks/ |
| infrastructure | DOC-02 | L3 | TEAM-INFRA-DIAGRAM | Architecture diagram updated if topology changed |
| infrastructure | CI-01 | L1 | TEAM-CI-ALL-CHECKS | All GitHub Actions checks pass |
| infrastructure | CI-02 | L2 | TEAM-INFRA-PLAN-REVIEW | Terraform plan reviewed by Platform Engineering |
| infrastructure | ACCEPT-01 | L2 | TEAM-INFRA-VERIFICATION | Infrastructure change verified in staging/pre-prod |
| infrastructure | ACCEPT-02 | L3 | TEAM-INFRA-MONITORING | Monitoring and alerting configured for new resources |
| infrastructure | SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion placeholder |

## Escaped Defect Traceability

These criteria were derived from production incidents and carry production traceability:

| Incident ID | Work Type | Criterion ID | Criterion Summary |
|-------------|-----------|--------------|-------------------|
| INC-001 | feature_story | TEST-07 | Integration test verifies SSO login flow for OAuth and SAML |
| INC-002 | api_change | TEST-06 | API contract tests include all nullable fields |
| INC-003 | bug_fix | TEST-08 | Regression test covering exact reproduction path in CI |

## Policy Coverage Analysis

| Source Policy Ref | Work Types Using | Criterion Count | Classification |
|-------------------|------------------|-----------------|----------------|
| ENG-4.1 | All | 6 | Universal L1 |
| ENG-4.2-SIGN | All | 6 | Universal L1 |
| ENG-4.2-MSG | All | 6 | Universal L1 |
| ENG-4.2-MERGE | All | 6 | Universal L1 |
| ENG-4.3-COMPLEXITY | feature_story, bug_fix, tech_debt, api_change, release | 5 | Universal L1 |
| ENG-4.3-LOC | feature_story, bug_fix, tech_debt, api_change, release | 5 | Universal L1 |
| ENG-4.3-DEAD | feature_story, bug_fix, tech_debt, api_change, release | 5 | Universal L1 |
| ENG-4.1-SEC | feature_story, bug_fix, api_change, infrastructure | 4 | Team L3 |
| QA-2.1-LINE | feature_story, bug_fix, tech_debt, api_change | 4 | Universal L1 |
| QA-2.1-BRANCH | feature_story, bug_fix, tech_debt, api_change | 4 | Universal L1 |
| QA-2.1-REGRESS | feature_story, bug_fix, tech_debt, api_change | 4 | Universal L1 |
| QA-2.2-UNIT | feature_story, bug_fix, tech_debt, api_change | 4 | Work Type L2 |
| QA-2.2-INTEGRATION | feature_story, bug_fix, tech_debt, api_change | 4 | Work Type L2 |
| SEC-3.1-SNYK | All | 12 | Universal L1 |
| SEC-3.2-SECRETS | All | 6 | Universal L1 |
| SEC-3.3-DEPS | All | 12 | Universal L1 |
| ENG-6.2-ARCH | tech_debt, api_change, infrastructure | 5 | Work Type L2 |
| QA-2.2-E2E | feature_story, bug_fix | 2 | Work Type L2 |
| QA-2.4-PERF | feature_story, api_change | 2 | Work Type L2 |
| SEC-4.2-SECRETS-MGMT | feature_story, infrastructure | 2 | Universal L1 |
| INC-001 | feature_story | 1 | Escaped Defect L2 |
| INC-002 | api_change | 1 | Escaped Defect L2 |
| INC-003 | bug_fix | 1 | Escaped Defect L2 |

## Orphaned Policies (Referenced but No Criteria)

None identified. All source policy references in the DoD YAML files have corresponding criteria.

## End of Matrix

---