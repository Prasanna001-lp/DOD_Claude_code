# Policy Traceability Matrix
Generated: 2025-01-25

## Purpose
This matrix provides bidirectional traceability between Definition-of-Done criteria and their source policies, standards, and escaped defect incidents. Every criterion in every work type DoD must trace to at least one authoritative source.

## Organisation Context
- **Organisation**: Acme Engineering
- **Engineering Tier**: scale_up
- **Team**: Commerce Platform
- **Compliance Frameworks**: SOC2, PCI-DSS
- **Regulated**: Yes

## Matrix Legend
- **Layer**: L1 (Universal), L2 (Work Type), L3 (Team), L4 (Story-Specific)
- **Source Type**: POLICY (engineering/security/QA policy), INCIDENT (escaped defect), TEAM (team-specific standard), TECH (tech stack requirement)

---

## Feature Story DoD Traceability

| Criterion ID | Layer | Source Policy Ref | Source Type | Criterion Summary | Source Document |
|---|---|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | POLICY | PR requires 2 approvals including 1 senior engineer | engineering_handbook.md §4.1 |
| CODE-02 | L2 | ENG-4.1-SEC | POLICY | Security-critical PRs require Security Champion approval | engineering_handbook.md §4.1 |
| CODE-03 | L1 | ENG-4.2-SIGN | POLICY | All commits GPG/SSH signed | engineering_handbook.md §4.2 |
| CODE-04 | L1 | ENG-4.2-FORMAT | POLICY | Conventional Commits format required | engineering_handbook.md §4.2 |
| CODE-05 | L1 | ENG-4.2-MERGE | POLICY | Squash merge strategy required | engineering_handbook.md §4.2 |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY | POLICY | Cyclomatic complexity ≤10 per method | engineering_handbook.md §4.3 |
| CODE-07 | L2 | ENG-4.3-LOC | POLICY | No method >50 lines of code | engineering_handbook.md §4.3 |
| CODE-08 | L2 | ENG-4.3-DEAD | POLICY | Zero dead code violations | engineering_handbook.md §4.3 |
| TEST-01 | L1 | QA-2.1-COVERAGE-LINE | POLICY | JaCoCo ≥80% line coverage | qa_policy.md §2.1 |
| TEST-02 | L1 | QA-2.1-COVERAGE-BRANCH | POLICY | JaCoCo ≥75% branch coverage | qa_policy.md §2.1 |
| TEST-03 | L1 | QA-2.1-NO-REGRESSION | POLICY | No coverage regression on existing code | qa_policy.md §2.1 |
| TEST-04 | L2 | QA-2.2-UNIT | POLICY | Unit tests present and passing (JUnit 5) | qa_policy.md §2.2 |
| TEST-05 | L2 | QA-2.2-INTEGRATION | POLICY | Integration tests present and passing | qa_policy.md §2.2 |
| TEST-06 | L2 | QA-2.2-E2E-HAPPY | POLICY | E2E happy path test (Playwright) | qa_policy.md §2.2 |
| TEST-07 | L2 | QA-2.2-E2E-ERROR | POLICY | E2E error path test (Playwright) | qa_policy.md §2.2 |
| TEST-08 | L2 | QA-2.4-PERF | POLICY | k6 load test for >1000 RPS endpoints (P95<500ms, P99<2000ms) | qa_policy.md §2.4 |
| SEC-01 | L1 | SEC-3.1-SNYK-CRIT | POLICY | Snyk 0 Critical/High findings | security_policy.md §3.1 |
| SEC-02 | L1 | SEC-3.1-SNYK-MED | POLICY | Medium findings have tracked Jira tickets | security_policy.md §3.1 |
| SEC-03 | L1 | SEC-3.2-GITLEAKS | POLICY | Gitleaks 0 secrets detected | security_policy.md §3.2 |
| SEC-04 | L1 | SEC-3.3-DEPS-MVN | POLICY | Maven dependency:check 0 Critical CVEs | security_policy.md §3.3 |
| SEC-05 | L1 | SEC-3.3-DEPS-NPM | POLICY | npm audit 0 Critical CVEs | security_policy.md §3.3 |
| SEC-06 | L1 | SEC-4.2-NO-SECRETS | POLICY | No hardcoded secrets in diff | security_policy.md §4.2 |
| DOC-01 | L2 | ENG-6.1-API-1 | POLICY | OpenAPI spec updated for API changes | engineering_handbook.md §6.1 |
| DOC-02 | L2 | ENG-6.1-API-2 | POLICY | CHANGELOG.md updated under [Unreleased] | engineering_handbook.md §6.1 |
| DOC-03 | L3 | TEAM-COMMERCE | TEAM | README/comments for complex business logic | team_standards.md |
| CI-01 | L1 | UNIVERSAL-CI | POLICY | All GitHub Actions checks pass | ci_policy.md |
| CI-02 | L1 | UNIVERSAL-SONAR | POLICY | SonarQube quality gate passes | engineering_handbook.md §4.3 |
| ACC-01 | L2 | FEATURE-AC | POLICY | PO verifies all acceptance criteria in staging | qa_policy.md §2.5 |
| ACC-02 | L3 | TEAM-UX | TEAM | UX review for UI changes | team_standards.md |
| ACC-03 | L3 | TEAM-ANALYTICS | TEAM | Analytics tracking implemented if required | team_standards.md |
| ESC-01 | L2 | INC-001 | INCIDENT | SSO login flow integration test for all auth methods | escaped_defects_log.csv |

**Total Feature Story Criteria**: 31 (L1: 15, L2: 13, L3: 3, L4: 0)

---

## Bug Fix DoD Traceability

| Criterion ID | Layer | Source Policy Ref | Source Type | Criterion Summary | Source Document |
|---|---|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | POLICY | PR requires 2 approvals including 1 senior engineer | engineering_handbook.md §4.1 |
| CODE-02 | L2 | ENG-4.1-SEC | POLICY | Security-critical PRs require Security Champion approval | engineering_handbook.md §4.1 |
| CODE-03 | L1 | ENG-4.2-SIGN | POLICY | All commits GPG/SSH signed | engineering_handbook.md §4.2 |
| CODE-04 | L1 | ENG-4.2-FORMAT | POLICY | Conventional Commits format required | engineering_handbook.md §4.2 |
| CODE-05 | L1 | ENG-4.2-MERGE | POLICY | Squash merge strategy required | engineering_handbook.md §4.2 |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY | POLICY | Cyclomatic complexity ≤10 per method | engineering_handbook.md §4.3 |
| CODE-07 | L2 | ENG-4.3-LOC | POLICY | No method >50 lines of code | engineering_handbook.md §4.3 |
| CODE-08 | L2 | ENG-4.3-DEAD | POLICY | Zero dead code violations | engineering_handbook.md §4.3 |
| TEST-01 | L1 | QA-2.1-COVERAGE-LINE | POLICY | JaCoCo ≥80% line coverage | qa_policy.md §2.1 |
| TEST-02 | L1 | QA-2.1-COVERAGE-BRANCH | POLICY | JaCoCo ≥75% branch coverage | qa_policy.md §2.1 |
| TEST-03 | L1 | QA-2.1-NO-REGRESSION | POLICY | No coverage regression on existing code | qa_policy.md §2.1 |
| TEST-04 | L2 | QA-2.2-UNIT | POLICY | Unit tests present and passing (JUnit 5) | qa_policy.md §2.2 |
| TEST-05 | L2 | QA-2.2-INTEGRATION | POLICY | Integration test if bug is integration-related | qa_policy.md §2.2 |
| TEST-06 | L2 | QA-2.2-E2E-BUGFIX | POLICY | E2E test if UI bug | qa_policy.md §2.2 |
| TEST-07 | L2 | QA-2.3-REGRESSION | INCIDENT | Regression test covering exact bug reproduction path | qa_policy.md §2.3 / INC-003 |
| SEC-01 | L1 | SEC-3.1-SNYK-CRIT | POLICY | Snyk 0 Critical/High findings | security_policy.md §3.1 |
| SEC-02 | L1 | SEC-3.1-SNYK-MED | POLICY | Medium findings have tracked Jira tickets | security_policy.md §3.1 |
| SEC-03 | L1 | SEC-3.2-GITLEAKS | POLICY | Gitleaks 0 secrets detected | security_policy.md §3.2 |
| SEC-04 | L1 | SEC-3.3-DEPS-MVN | POLICY | Maven dependency:check 0 Critical CVEs | security_policy.md §3.3 |
| SEC-05 | L1 | SEC-3.3-DEPS-NPM | POLICY | npm audit 0 Critical CVEs | security_policy.md §3.3 |
| SEC-06 | L1 | SEC-4.2-NO-SECRETS | POLICY | No hardcoded secrets in diff | security_policy.md §4.2 |
| DOC-01 | L2 | QA-2.3-REGRESSION | POLICY | Root cause documented in ticket and PR | qa_policy.md §2.3 |
| DOC-02 | L3 | TEAM-COMMERCE | TEAM | README updated if external behavior changed | team_standards.md |
| CI-01 | L1 | CI-GATE | POLICY | All GitHub Actions checks pass | ci_policy.md |
| CI-02 | L3 | TEAM-COMMERCE | TECH | Spring Boot app starts successfully in CI | team_standards.md |
| ACC-01 | L2 | QA-2.3-REGRESSION | POLICY | QA verifies fix in staging using original repro steps | qa_policy.md §2.3 |
| ACC-02 | L2 | QA-POL-BUG | POLICY | PO accepts fix by moving to Done in Jira | qa_policy.md §2.6 |

**Total Bug Fix Criteria**: 26 (L1: 14, L2: 11, L3: 2, L4: 0)

---

## Tech Debt DoD Traceability

| Criterion ID | Layer | Source Policy Ref | Source Type | Criterion Summary | Source Document |
|---|---|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | POLICY | PR requires 2 approvals including 1 senior engineer | engineering_handbook.md §4.1 |
| CODE-02 | L1 | ENG-4.2-SIGN | POLICY | All commits GPG/SSH signed | engineering_handbook.md §4.2 |
| CODE-03 | L1 | ENG-4.2-FORMAT | POLICY | Conventional Commits format required | engineering_handbook.md §4.2 |
| CODE-04 | L1 | ENG-4.2-MERGE | POLICY | Squash merge strategy required | engineering_handbook.md §4.2 |
| CODE-05 | L1 | ENG-4.3-COMPLEXITY | POLICY | Cyclomatic complexity ≤10 per method | engineering_handbook.md §4.3 |
| CODE-06 | L2 | ENG-4.3-LOC | POLICY | No method >50 lines of code | engineering_handbook.md §4.3 |
| CODE-07 | L2 | ENG-4.3-DEAD | POLICY | Zero dead code violations | engineering_handbook.md §4.3 |
| CODE-08 | L2 | ENG-6.2-ADR-1 | POLICY | ADR for architecture/data model changes | engineering_handbook.md §6.2 |
| TEST-01 | L1 | QA-2.1-COVERAGE-LINE | POLICY | JaCoCo ≥80% line coverage | qa_policy.md §2.1 |
| TEST-02 | L1 | QA-2.1-COVERAGE-BRANCH | POLICY | JaCoCo ≥75% branch coverage | qa_policy.md §2.1 |
| TEST-03 | L1 | QA-2.1-NO-REGRESSION | POLICY | No coverage regression on existing code | qa_policy.md §2.1 |
| TEST-04 | L2 | QA-2.2-UNIT | POLICY | Unit tests present and passing (JUnit 5) | qa_policy.md §2.2 |
| TEST-05 | L2 | TECH-DEBT-SPECIFIC | POLICY | No new tech debt introduced (SonarQube gate) | Work type mandate |
| SEC-01 | L1 | SEC-3.1-SNYK-CRIT | POLICY | Snyk 0 Critical/High findings | security_policy.md §3.1 |
| SEC-02 | L1 | SEC-3.1-SNYK-MED | POLICY | Medium findings have tracked Jira tickets | security_policy.md §3.1 |
| SEC-03 | L1 | SEC-3.2-GITLEAKS | POLICY | Gitleaks 0 secrets detected | security_policy.md §3.2 |
| SEC-04 | L1 | SEC-3.3-DEPS-MVN | POLICY | Maven dependency:check 0 Critical CVEs | security_policy.md §3.3 |
| SEC-05 | L1 | SEC-3.3-DEPS-NPM | POLICY | npm audit 0 Critical CVEs | security_policy.md §3.3 |
| SEC-06 | L1 | SEC-4.2-NO-SECRETS | POLICY | No hardcoded secrets in diff | security_policy.md §4.2 |
| ARCH-01 | L2 | ENG-6.2-ADR-2 | POLICY | Architecture Guild approval recorded | engineering_handbook.md §6.2 |
| ARCH-02 | L3 | TECH-STACK-SPRING | TECH | Spring Boot best practices followed | team_standards.md / Spring docs |
| DOC-01 | L2 | ENG-6.1-API-2 | POLICY | CHANGELOG.md updated if user-facing | engineering_handbook.md §6.1 |
| DOC-02 | L3 | TECH-DEBT-JUSTIFICATION | TEAM | "Why Now" justification documented | team_standards.md |
| CI-01 | L1 | CI-ALL-CHECKS | POLICY | All GitHub Actions checks pass | ci_policy.md |
| CI-02 | L3 | TECH-STACK-KAFKA | TECH | Kafka integration tests pass if Kafka changed | team_standards.md |
| ACCEPT-01 | L2 | TECH-DEBT-VALIDATION | POLICY | Tech Lead confirms goal achieved with metrics | Work type mandate |
| ACCEPT-02 | L3 | SONARQUBE-QUALITY-GATE | TECH | SonarQube A rating on Maintainability | dod-config.yaml |

**Total Tech Debt Criteria**: 23 (L1: 11, L2: 9, L3: 4, L4: 0)

---

## API Change DoD Traceability

| Criterion ID | Layer | Source Policy Ref | Source Type | Criterion Summary | Source Document |
|---|---|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | POLICY | PR requires 2 approvals including 1 senior engineer | engineering_handbook.md §4.1 |
| CODE-02 | L2 | ENG-4.1-SEC | POLICY | Security-critical PRs require Security Champion approval | engineering_handbook.md §4.1 |
| CODE-03 | L1 | ENG-4.2-SIGN | POLICY | All commits GPG/SSH signed | engineering_handbook.md §4.2 |
| CODE-04 | L1 | ENG-4.2-FORMAT | POLICY | Conventional Commits format required | engineering_handbook.md §4.2 |
| CODE-05 | L1 | ENG-4.2-MERGE | POLICY | Squash merge strategy required | engineering_handbook.md §4.2 |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY | POLICY | Cyclomatic complexity ≤10 per method | engineering_handbook.md §4.3 |
| CODE-07 | L2 | ENG-4.3-LOC | POLICY | No method >50 lines of code | engineering_handbook.md §4.3 |
| CODE-08 | L2 | ENG-4.3-DEAD | POLICY | Zero dead code violations | engineering_handbook.md §4.3 |
| API-01 | L2 | ENG-6.1-API-1 | POLICY | OpenAPI spec updated | engineering_handbook.md §6.1 |
| API-02 | L2 | ENG-6.1-API-2 | POLICY | CHANGELOG.md updated | engineering_handbook.md §6.1 |
| API-03 | L2 | ENG-6.1-API-3 | POLICY | API diff attached to PR | engineering_handbook.md §6.1 |
| API-04 | L2 | ENG-6.2-ADR-1 | POLICY | ADR for architecture changes | engineering_handbook.md §6.2 |
| API-05 | L2 | ENG-6.2-ADR-2 | POLICY | Architecture Guild approval | engineering_handbook.md §6.2 |
| API-06 | L3 | TEAM-STACK-SPRING | TECH | Spring REST Docs generated | team_standards.md |
| TEST-01 | L1 | QA-2.1-COVERAGE-LINE | POLICY | JaCoCo ≥80% line coverage | qa_policy.md §2.1 |
| TEST-02 | L1 | QA-2.1-COVERAGE-BRANCH | POLICY | JaCoCo ≥75% branch coverage | qa_policy.md §2.1 |
| TEST-03 | L1 | QA-2.1-NO-REGRESSION | POLICY | No coverage regression | qa_policy.md §2.1 |
| TEST-04 | L2 | QA-2.2-UNIT | POLICY | Unit tests present (JUnit 5) | qa_policy.md §2.2 |
| TEST-05 | L2 | QA-2.2-INTEGRATION | POLICY | Integration tests present | qa_policy.md §2.2 |
| TEST-06 | L2 | INC-002 | INCIDENT | Contract test includes all nullable fields | escaped_defects_log.csv |
| TEST-07 | L2 | QA-2.4-PERF | POLICY | k6 load test for >1000 RPS endpoints | qa_policy.md §2.4 |
| TEST-08 | L3 | TEAM-STACK-KAFKA | TECH | Kafka schema compatibility test | team_standards.md |
| SEC-01 | L1 | SEC-3.1-SNYK-CRIT | POLICY | Snyk 0 Critical/High findings | security_policy.md §3.1 |
| SEC-02 | L1 | SEC-3.1-SNYK-MED | POLICY | Medium findings tracked | security_policy.md §3.1 |
| SEC-03 | L1 | SEC-3.2-GITLEAKS | POLICY | Gitleaks 0 secrets | security_policy.md §3.2 |
| SEC-04 | L1 | SEC-3.3-DEPS-MVN | POLICY | Maven 0 Critical CVEs | security_policy.md §3.3 |
| SEC-05 | L1 | SEC-3.3-DEPS-NPM | POLICY | npm 0 Critical CVEs | security_policy.md §3.3 |
| SEC-06 | L1 | SEC-4.2-NO-SECRETS | POLICY | No hardcoded secrets | security_policy.md §4.2 |
| SEC-07 | L3 | TEAM-STACK-POSTGRES | TECH | Parameterized SQL queries only | team_standards.md / security_best_practices.md |
| CI-01 | L1 | CI-GATE-ALL | POLICY | All CI checks pass | ci_policy.md |
| CI-02 | L3 | TEAM-STACK-SPRING | TECH | Spring Boot app starts in CI | team_standards.md |
| DOC-01 | L1 | DOC-UPDATE | POLICY | README updated if behavior changed | engineering_handbook.md §6.1 |
| ACC-01 | L2 | API-CONSUMER-REVIEW | POLICY | Consumer teams notified of breaking changes | api_governance_policy.md |
| ACC-02 | L3 | TEAM-PRODUCT-SIGN-OFF | TEAM | PO sign-off for user-facing changes | team_standards.md |

**Total API Change Criteria**: 33 (L1: 14, L2: 14, L3: 4, L4: 1)

---

## Release DoD Traceability

| Criterion ID | Layer | Source Policy Ref | Source Type | Criterion Summary | Source Document |
|---|---|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | POLICY | PR requires 2 approvals including 1 senior engineer | engineering_handbook.md §4.1 |
| CODE-02 | L1 | ENG-4.2-SIGN | POLICY | All commits GPG/SSH signed | engineering_handbook.md §4.2 |
| CODE-03 | L1 | ENG-4.2-FORMAT | POLICY | Conventional Commits format required | engineering_handbook.md §4.2 |
| CODE-04 | L2 | ENG-6.1-API-2 | POLICY | CHANGELOG.md updated | engineering_handbook.md §6.1 |
| TEST-01 | L2 | QA-3.1-REGRESSION-SUITE | POLICY | Full regression suite passed in staging and pre-prod | qa_policy.md §3.1 |
| TEST-02 | L2 | QA-3.1-SMOKE | POLICY | Smoke tests passed in production post-deploy | qa_policy.md §3.1 |
| TEST-03 | L3 | TEAM-TECH-STACK | TECH | Kafka consumer lag <100ms post-deploy | team_standards.md |
| TEST-04 | L3 | TEAM-TECH-STACK | TECH | PostgreSQL connection pool healthy post-deploy | team_standards.md |
| SEC-01 | L1 | SEC-3.1-SNYK-CRIT | POLICY | Snyk 0 Critical/High findings | security_policy.md §3.1 |
| SEC-02 | L1 | SEC-3.1-SNYK-MED | POLICY | Medium findings tracked | security_policy.md §3.1 |
| SEC-03 | L1 | SEC-3.2-GITLEAKS | POLICY | Gitleaks 0 secrets | security_policy.md §3.2 |
| SEC-04 | L1 | SEC-3.3-DEPS-MVN | POLICY | Maven 0 Critical CVEs | security_policy.md §3.3 |
| SEC-05 | L1 | SEC-3.3-DEPS-NPM | POLICY | npm 0 Critical CVEs | security_policy.md §3.3 |
| SEC-06 | L1 | SEC-4.2-NO-SECRETS | POLICY | No hardcoded secrets | security_policy.md §4.2 |
| CI-01 | L1 | ENG-4.3-COMPLEXITY | POLICY | SonarQube quality gate passes | engineering_handbook.md §4.3 |
| CI-02 | L3 | TEAM-SONARQUBE | TECH | Overall quality gate PASSED for release branch | dod-config.yaml |
| CI-03 | L2 | TEAM-CI-RELEASE | TECH | Release pipeline completed all stages | team_standards.md |
| DOC-01 | L2 | QA-3.1-RELEASE-NOTES | POLICY | Release notes approved by EM | qa_policy.md §3.1 |
| DOC-02 | L2 | QA-3.1-ROLLBACK | POLICY | Rollback plan tested in staging | qa_policy.md §3.1 |
| DOC-03 | L2 | QA-3.1-RUNBOOK | POLICY | Runbook updated if procedures changed | qa_policy.md §3.1 |
| DOC-04 | L3 | TEAM-TECH-STACK | TECH | Spring Boot config changes documented | team_standards.md |
| ACCEPT-01 | L2 | QA-3.1-RELEASE-NOTES | POLICY | EM approval documented | qa_policy.md §3.1 |
| ACCEPT-02 | L3 | TEAM-RELEASE-GOVERNANCE | TEAM | PO sign-off for user-facing changes | team_standards.md |
| ACCEPT-03 | L3 | TEAM-RELEASE-GOVERNANCE | TEAM | On-call rotation updated if needed | team_standards.md |

**Total Release Criteria**: 25 (L1: 10, L2: 11, L3: 4, L4: 0)

---

## Infrastructure DoD Traceability

| Criterion ID | Layer | Source Policy Ref | Source Type | Criterion Summary | Source Document |
|---|---|---|---|---|---|
| CODE-01 | L1 | ENG-4.1 | POLICY | PR requires 2 approvals including 1 senior engineer | engineering_handbook.md §4.1 |
| CODE-02 | L2 | ENG-4.1-SEC | POLICY | Security-critical PRs require Security Champion approval | engineering_handbook.md §4.1 |
| CODE-03 | L1 | ENG-4.2-SIGN | POLICY | All commits GPG/SSH signed | engineering_handbook.md §4.2 |
| CODE-04 | L1 | ENG-4.2-FORMAT | POLICY | Conventional Commits format required | engineering_handbook.md §4.2 |
| CODE-05 | L2 | SEC-4.1-TERRAFORM-PLAN | POLICY | Terraform plan shows no unintended deletions | security_policy.md §4.1 |
| CODE-06 | L2 | SEC-4.1-TERRAFORM-REVIEW | POLICY | Platform Engineering approval recorded | security_policy.md §4.1 |
| CODE-07 | L2 | ENG-6.2-ADR-1 | POLICY | ADR for architecture changes | engineering_handbook.md §6.2 |
| CODE-08 | L2 | ENG-6.2-ADR-2 | POLICY | Architecture Guild approval | engineering_handbook.md §6.2 |
| SEC-01 | L1 | SEC-3.1-SNYK-CRIT | POLICY | Snyk 0 Critical/High findings | security_policy.md §3.1 |
| SEC-02 | L1 | SEC-3.1-SNYK-MED | POLICY | Medium findings tracked | security_policy.md §3.1 |
| SEC-03 | L1 | SEC-3.2-GITLEAKS | POLICY | Gitleaks 0 secrets | security_policy.md §3.2 |
| SEC-04 | L1 | SEC-4.2-NO-SECRETS | POLICY | No hardcoded secrets | security_policy.md §4.2 |
| SEC-05 | L2 | SEC-4.1-TERRAFORM-TFSEC | POLICY | tfsec 0 HIGH/CRITICAL findings | security_policy.md §4.1 |
| SEC-06 | L3 | TEAM-INFRA-SEC-1 | TEAM | IAM follows least-privilege (no wildcards without ADR) | team_standards.md |
| SEC-07 | L3 | TEAM-INFRA-SEC-2 | TEAM | All S3 buckets encrypted at rest | team_standards.md / AWS policy |
| SEC-08 | L3 | TEAM-INFRA-SEC-3 | TEAM | All RDS encrypted + automated backups | team_standards.md / AWS policy |
| TEST-01 | L2 | TEAM-INFRA-TEST-1 | TEAM | terraform validate passes | team_standards.md |
| TEST-02 | L2 | TEAM-INFRA-TEST-2 | TEAM | terraform fmt check passes | team_standards.md |
| TEST-03 | L3 | TEAM-INFRA-TEST-3 | TEAM | Terraform plan in staging shows expected changes | team_standards.md |
| TEST-04 | L3 | TEAM-INFRA-TEST-4 | TEAM | Smoke tests pass in staging post-apply | team_standards.md |
| TEST-05 | L3 | TEAM-INFRA-TEST-5 | TEAM | Rollback tested in staging | team_standards.md |
| DOC-01 | L2 | QA-3.1-RUNBOOK | POLICY | Runbook updated if procedures changed | qa_policy.md §3.1 |
| DOC-02 | L3 | TEAM-INFRA-DOC-1 | TEAM | README updated for new resources | team_standards.md |
| DOC-03 | L3 | TEAM-INFRA-DOC-2 | TEAM | DR plan updated if RTO/RPO impacted | team_standards.md |
| DOC-04 | L3 | TEAM-INFRA-DOC-3 | TEAM | Terraform module docs updated | team_standards.md |
| CI-01 | L1 | CI-GATE-ALL | POLICY | All CI checks pass | ci_policy.md |
| CI-02 | L3 | TEAM-INFRA-CI-1 | TEAM | No manual tfstate modifications | team_standards.md |
| CI-03 | L3 | TEAM-INFRA-CI-2 | TEAM | Backend config verified (S3 + DynamoDB) | team_standards.md |
| DR-01 | L3 | TEAM-INFRA-DR-1 | TEAM | Multi-AZ for production-critical resources | team_standards.md / AWS Well-Architected |
| DR-02 | L3 | TEAM-INFRA-DR-2 | TEAM | Backup retention ≥7 days for production data | team_standards.md / compliance |
| DR-03 | L3 | TEAM-INF