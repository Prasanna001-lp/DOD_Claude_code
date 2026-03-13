# Policy Traceability Matrix
Generated: 2026-03-13

## Overview
This matrix provides bidirectional traceability between source policies/standards and Definition-of-Done criteria across all work types. Each row represents a unique criterion and links it back to its authoritative source.

**Legend:**
- **L1** = Universal (applies to all work items)
- **L2** = Work-type specific (applies to all items of this type)
- **L3** = Team-specific (based on tech stack/domain)
- **L4** = Story-specific (added during grooming)

---

## Feature Story

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers, including 1 from senior engineer or tech lead |
| CODE-02 | L2 | ENG-4.1-SEC | Security-critical PRs include approval from designated Security Champion |
| CODE-03 | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub |
| CODE-04 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format |
| CODE-05 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10 per method |
| CODE-07 | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code |
| CODE-08 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code issues |
| TEST-01 | L1 | QA-2.1-COV | JaCoCo reports ≥80% line coverage on all changed modules |
| TEST-02 | L1 | QA-2.1-COV | JaCoCo reports ≥75% branch coverage on all changed modules |
| TEST-03 | L1 | QA-2.1-COV | CI confirms no existing covered code has lost coverage |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present and passing for all new/changed business logic (JUnit 5) |
| TEST-05 | L2 | QA-2.2-INT | Integration tests present and passing for service-to-service interactions |
| TEST-06 | L2 | QA-2.2-E2E | E2E test covers happy path and at least 1 error path scenario (Playwright) |
| TEST-07 | L2 | DEFECT-INC-001 | Integration test verifies SSO login flow for all configured auth methods |
| TEST-08 | L2 | QA-2.4-PERF | k6 load test present for endpoints handling >1000 RPS, verifying P95 <500ms and P99 <2000ms |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan reports 0 Critical or High severity findings |
| SEC-02 | L1 | SEC-3.1-SNYK | All Medium severity findings have tracked Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEP | mvn dependency:check reports 0 Critical CVE findings |
| SEC-05 | L1 | SEC-3.3-DEP | npm audit reports 0 Critical CVE findings |
| SEC-06 | L2 | SEC-4.2-SECRETS-MGMT | All new secrets documented as stored in AWS Secrets Manager or GitHub Actions secrets |
| DOC-01 | L1 | L1-UNIVERSAL-DOC | Documentation updated where changes impact user-facing behavior or operations |
| DOC-02 | L2 | ENG-6.1-API | OpenAPI specification file updated to reflect API changes |
| DOC-03 | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] |
| DOC-04 | L2 | ENG-6.1-API | API diff document generated and attached to PR |
| CI-01 | L1 | L1-UNIVERSAL-CI | All CI checks pass: lint, build, unit tests, integration tests, security scans |
| CI-02 | L3 | TEAM-SPRING-BOOT | Spring Boot application starts successfully in CI |
| CI-03 | L3 | TEAM-REACT | React frontend builds successfully with 0 TypeScript errors and 0 ESLint errors |
| ACCEPT-01 | L2 | QA-POLICY-FEATURE | All acceptance criteria verified by Product Owner in staging environment |
| ACCEPT-02 | L3 | TEAM-UX | UX review completed for user-facing changes |
| ACCEPT-03 | L3 | TEAM-ANALYTICS | Analytics event tracking implemented for new user actions |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion (placeholder for PO/Tech Lead additions) |

---

## Bug Fix

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers, including 1 from senior engineer or tech lead |
| CODE-02 | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub |
| CODE-03 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| CODE-05 | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10 per method |
| CODE-06 | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code |
| CODE-07 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code issues |
| CODE-08 | L2 | BUG-FIX-ROOT-CAUSE | Root cause documented in PR description or linked bug ticket |
| TEST-01 | L1 | QA-2.1-COV | JaCoCo reports ≥80% line coverage on all changed modules |
| TEST-02 | L1 | QA-2.1-COV | JaCoCo reports ≥75% branch coverage on all changed modules |
| TEST-03 | L1 | QA-2.1-COV | CI confirms no existing covered code has lost coverage |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present and passing for all new/changed business logic |
| TEST-05 | L2 | QA-2.2-INT | Integration tests present if bug was integration-related |
| TEST-06 | L2 | QA-2.2-E2E | E2E test present if bug was UI-related |
| TEST-07 | L2 | QA-2.3-REG, INC-003 | Regression test covering exact reproduction path from original bug report |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan reports 0 Critical or High severity findings |
| SEC-02 | L1 | SEC-3.1-SNYK | All Medium severity findings have tracked Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEP | mvn dependency:check reports 0 Critical CVE findings |
| SEC-05 | L1 | SEC-3.3-DEP | npm audit reports 0 Critical CVE findings |
| DOC-01 | L1 | L1-UNIVERSAL-DOC | Documentation updated where bug fix impacts user-facing behavior or operations |
| DOC-02 | L2 | BUG-FIX-CHANGELOG | CHANGELOG.md updated with entry under [Unreleased] → Fixed section |
| CI-01 | L1 | L1-UNIVERSAL-CI | All CI checks pass: lint, build, unit tests, integration tests, security scans |
| CI-02 | L3 | TEAM-KAFKA-HEALTH | If bug involves Kafka, integration test verifies event schema matches producer contract |
| CI-03 | L3 | TEAM-POSTGRESQL-MIGRATION | If bug involves database, Flyway migration script tested in staging |
| ACC-01 | L2 | BUG-FIX-REPRO | Bug reporter or QA confirms fix resolves original issue in staging |
| ACC-02 | L2 | BUG-FIX-NO-SIDE-EFFECTS | QA confirms no new side effects introduced in related features |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion (placeholder for PO/Tech Lead additions) |

---

## Tech Debt

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers, including 1 from senior engineer or tech lead |
| CODE-02 | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub |
| CODE-03 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format |
| CODE-04 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| CODE-05 | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10 per method |
| CODE-06 | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code |
| CODE-07 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code issues |
| CODE-08 | L2 | ENG-6.2-ADR | Architecture Decision Record (ADR) created for structural changes |
| TEST-01 | L1 | QA-2.1-COV | JaCoCo reports ≥80% line coverage on all changed modules |
| TEST-02 | L1 | QA-2.1-COV | JaCoCo reports ≥75% branch coverage on all changed modules |
| TEST-03 | L1 | QA-2.1-COV | CI confirms no existing covered code has lost coverage |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present and passing for all new/changed business logic |
| TEST-05 | L2 | QA-2.2-INT | Integration tests present if tech debt impacts cross-service contracts or data layer |
| TEST-06 | L3 | TEAM-TECHDEBT-KAFKA | If refactors Kafka logic, integration test verifies message serialization/deserialization |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan reports 0 Critical or High severity findings |
| SEC-02 | L1 | SEC-3.1-SNYK | All Medium severity findings have tracked Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEP | mvn dependency:check reports 0 Critical CVE findings |
| SEC-05 | L1 | SEC-3.3-DEP | npm audit reports 0 Critical CVE findings |
| DOC-01 | L1 | L1-UNIVERSAL-DOC | README.md updated if tech debt changes module structure, dependencies, or build/run instructions |
| DOC-02 | L2 | ENG-6.2-ADR | Architecture Guild review approval documented in PR if ADR was required |
| DOC-03 | L3 | TEAM-TECHDEBT-SONAR | If driven by SonarQube findings, PR description documents which issues are resolved |
| CI-01 | L1 | L1-UNIVERSAL-CI | All GitHub Actions CI checks pass: lint, build, unit tests, integration tests, security scans |
| CI-02 | L3 | TEAM-TECHDEBT-SONARQUBE | SonarQube quality gate status is "Passed" with 0 new code smells, bugs, vulnerabilities |
| CI-03 | L2 | TECHDEBT-WORKTYPE | No new technical debt introduced: SonarQube shows Technical Debt Ratio ≤5% |
| ACC-01 | L2 | TECHDEBT-WORKTYPE | Tech Lead has reviewed and approved the refactoring approach |
| ACC-02 | L3 | TEAM-TECHDEBT-POSTGRES | If includes database changes, DBA or Platform Engineering team has reviewed migration script |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion (placeholder for PO/Tech Lead additions) |

---

## API Change

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers, including 1 from senior engineer or tech lead |
| CODE-02 | L2 | ENG-4.1-SEC | Security-critical API changes include approval from designated Security Champion |
| CODE-03 | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub |
| CODE-04 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format |
| CODE-05 | L1 | ENG-4.2-MERGE | PR uses squash merge strategy |
| CODE-06 | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10 per method |
| CODE-07 | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code |
| CODE-08 | L1 | ENG-4.3-DEAD | SonarQube reports zero dead code issues |
| TEST-01 | L1 | QA-2.1-COV | JaCoCo reports ≥80% line coverage on all changed modules |
| TEST-02 | L1 | QA-2.1-COV | JaCoCo reports ≥75% branch coverage on all changed modules |
| TEST-03 | L1 | QA-2.1-COV | CI confirms no existing covered code has lost coverage |
| TEST-04 | L2 | QA-2.2-UNIT | Unit tests present and passing for all new/changed business logic |
| TEST-05 | L2 | QA-2.2-INT | Integration tests present and passing for API contract changes |
| TEST-06 | L2 | DEFECT-INC-002 | API contract tests include explicit tests for all nullable fields |
| TEST-07 | L2 | QA-2.4-PERF | k6 load test present for endpoints handling >1000 RPS |
| TEST-08 | L3 | TEAM-KAFKA | If API change affects Kafka event schemas, consumer-driven contract tests pass |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan reports 0 Critical or High severity findings |
| SEC-02 | L1 | SEC-3.1-SNYK | All Medium severity findings have tracked Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEP | mvn dependency:check reports 0 Critical CVE findings |
| SEC-05 | L1 | SEC-3.3-DEP | npm audit reports 0 Critical CVE findings |
| SEC-06 | L3 | TEAM-AUTH | If modifies auth/authz logic, security review performed by Security Champion |
| DOC-01 | L2 | ENG-6.1-API | OpenAPI specification file updated to reflect API changes |
| DOC-02 | L2 | ENG-6.1-API | CHANGELOG.md updated with entry under [Unreleased] |
| DOC-03 | L2 | ENG-6.1-API | API diff document generated and attached to PR |
| DOC-04 | L2 | ENG-6.2-ADR | If affects cross-service contracts or data model, ADR created |
| DOC-05 | L2 | ENG-6.2-ADR | If ADR required, Architecture Guild review approval documented |
| DOC-06 | L1 | L1-UNIVERSAL-DOC | API documentation updated where changes impact client integration |
| CI-01 | L1 | L1-UNIVERSAL-CI | All CI checks pass: lint, build, unit tests, integration tests, security scans |
| CI-02 | L3 | TEAM-POSTGRES | If includes database schema migrations, Flyway migration scripts present and tested |
| CI-03 | L3 | TEAM-BACKWARDS-COMPAT | If API is public-facing, backward compatibility verified |
| ACC-01 | L3 | TEAM-PO-REVIEW | If affects user-facing functionality, Product Owner review documented |
| ACC-02 | L3 | TEAM-API-CONSUMERS | If consumed by external teams, consumer teams notified |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion (placeholder for PO/Tech Lead additions) |

---

## Release

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers, including 1 from senior engineer or tech lead |
| CODE-02 | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub |
| CODE-03 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format |
| TEST-01 | L2 | QA-3.1-RELEASE | Full regression test suite passes in staging environment with 100% pass rate |
| TEST-02 | L2 | QA-3.1-RELEASE | Full regression test suite passes in pre-prod environment with 100% pass rate |
| TEST-03 | L2 | QA-3.1-RELEASE | Smoke test suite passes in production environment post-deploy with 100% pass rate |
| TEST-04 | L3 | TEAM-COMMERCE-PLATFORM | End-to-end order flow test passes in production |
| TEST-05 | L3 | TEAM-COMMERCE-PLATFORM | Kafka event publishing verified for all order state transitions |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan reports 0 Critical or High severity findings |
| SEC-02 | L1 | SEC-3.1-SNYK | All Medium severity findings have tracked Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected |
| SEC-04 | L1 | SEC-3.3-DEP | mvn dependency:check reports 0 Critical CVE findings |
| SEC-05 | L1 | SEC-3.3-DEP | npm audit reports 0 Critical CVE findings |
| DOC-01 | L2 | QA-3.1-RELEASE | Release notes prepared and approved by Engineering Manager |
| DOC-02 | L2 | QA-3.1-RELEASE | Runbook updated if operational procedures have changed |
| DOC-03 | L3 | TEAM-COMMERCE-PLATFORM | API changelog updated if any REST or GraphQL endpoints changed |
| DOC-04 | L3 | TEAM-COMMERCE-PLATFORM | Database migration scripts documented with rollback instructions |
| DEPLOY-01 | L2 | QA-3.1-RELEASE | Rollback plan documented and tested in staging environment |
| DEPLOY-02 | L3 | TEAM-COMMERCE-PLATFORM | Blue-green deployment configuration verified |
| DEPLOY-03 | L3 | TEAM-COMMERCE-PLATFORM | Kafka consumer lag verified <1000 messages before deployment |
| DEPLOY-04 | L3 | TEAM-COMMERCE-PLATFORM | Database connection pool settings verified for new traffic load |
| CI-01 | L1 | L1-UNIVERSAL-CI | All CI checks pass: lint, build, unit tests, integration tests, security scans |
| CI-02 | L3 | TEAM-COMMERCE-PLATFORM | SonarQube quality gate passes with 0 new code smells, bugs, vulnerabilities |
| CI-03 | L3 | TEAM-COMMERCE-PLATFORM | Docker image build completes successfully with size <500MB |
| ACCEPT-01 | L2 | QA-3.1-RELEASE | Engineering Manager approval documented in release PR |
| ACCEPT-02 | L3 | TEAM-COMMERCE-PLATFORM | Product Owner sign-off obtained if release includes customer-facing features or breaking changes |
| ACCEPT-03 | L3 | TEAM-COMMERCE-PLATFORM | On-call engineer notified and confirmed available during deployment window |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion (placeholder for PO/Tech Lead additions) |

---

## Infrastructure

| Criterion ID | Layer | Source Policy Ref | Criterion Text (Summary) |
|--------------|-------|-------------------|--------------------------|
| CODE-01 | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers, including 1 from senior engineer or tech lead |
| CODE-02 | L2 | ENG-4.1-SEC | PR includes approval from designated Security Champion (all infra changes security-critical) |
| CODE-03 | L1 | ENG-4.2 | All commits are signed with GPG or SSH key registered in GitHub |
| CODE-04 | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format |
| CODE-05 | L2 | SEC-4.1-TFPLAN | terraform plan output attached to PR showing no unintended resource deletions |
| CODE-06 | L2 | SEC-4.1-TFPLAN | Platform Engineering team approval documented in PR |
| CODE-07 | L2 | ENG-6.2-ADR | Architecture Decision Record (ADR) created for structural infrastructure changes |
| CODE-08 | L2 | ENG-6.2-ADR | Architecture Guild review approval documented in PR (if ADR created) |
| SEC-01 | L1 | SEC-3.1-SNYK | Snyk scan reports 0 Critical or High severity findings |
| SEC-02 | L1 | SEC-3.1-SNYK | All Medium severity findings have tracked Jira tickets |
| SEC-03 | L1 | SEC-3.2-SECRETS | Gitleaks scan passes with 0 secrets detected |
| SEC-04 | L2 | SEC-4.1-TFPLAN | tfsec scan passes with 0 HIGH or CRITICAL findings |
| SEC-05 | L2 | SEC-4.2-SECRETS-MGMT | All new secrets documented as stored in AWS Secrets Manager or GitHub Actions secrets |
| SEC-06 | L3 | TEAM-KAFKA | Kafka topic ACLs configured for new topics |
| TEST-01 | L2 | QA-2.2-INT | Integration tests present for infrastructure changes affecting service-to-service interactions |
| TEST-02 | L3 | TEAM-POSTGRES | Database migration tested with rollback verification |
| TEST-03 | L3 | TEAM-DR | Disaster recovery impact assessed and documented |
| DOC-01 | L1 | L1-UNIVERSAL-DOC | Documentation updated where infrastructure change impacts operational procedures |
| DOC-02 | L2 | QA-3.1-RELEASE | Runbook updated if operational procedures have changed |
| DOC-03 | L3 | TEAM-TERRAFORM | Terraform module README.md updated with input/output variable documentation |
| CI-01 | L1 | L1-UNIVERSAL-CI | All GitHub Actions CI checks pass: terraform validate, fmt, tfsec, Gitleaks, Snyk |
| CI-02 | L3 | TEAM-STAGING | Infrastructure change deployed to staging environment and validated |
| ACCEPT-01 | L2 | QA-3.1-RELEASE | Rollback plan documented and tested in staging environment |
| ACCEPT-02 | L3 | TEAM-EM-SIGNOFF | Engineering Manager sign-off documented for production-impacting infrastructure changes |
| SS-01 | L4 | PO-OR-TECH-LEAD | Story-specific criterion (placeholder for PO/Tech Lead additions) |

---

## Summary Statistics

| Work Type | Total Criteria | L1 Universal | L2 Work-Type | L3 Team | L4 Story | Escaped Defect Criteria |
|-----------|----------------|--------------|--------------|---------|----------|------------------------|
| feature_story | 33 | 16 | 11 | 5 | 1 | 1 (INC-001) |
| bug_fix | 28 | 15 | 11 | 2 | 1 | 1 (INC-003) |
| tech_debt | 28 | 15 | 10 | 3 | 1 | 0 |
| api_change | 33 | 16 | 11 | 5 | 1 | 1 (INC-002) |
| release | 27 | 9 | 8 | 9 | 1 | 0 |
| infrastructure | 25 | 7 | 10 | 7 | 1 | 0 |
| **TOTAL** | **174** | **78** | **61** | **31** | **6** | **3** |

---

## Policy Source References (Consolidated)

| Source Ref | Description | Referenced By (Work Types) |
|-----------|-------------|---------------------------|
| ENG-4.1 | PR approval requirements (2+ engineers, 1 senior/lead) | All work types |
| ENG-4.1-SEC | Security Champion approval for security-critical changes | feature_story, api_change, infrastructure |
| ENG-4.2 | Commit signing (GPG/SSH) | All work types |
| ENG-4.2-CONV | Conventional Commits format | All work types |
| ENG-4.2-MERGE | Squash merge strategy | feature_story, bug_fix, tech_debt, api_change |
| ENG-4.3-COMPLEXITY | Cyclomatic complexity ≤10 | feature_story, bug_fix, tech_debt, api_change |
| ENG-4.3-LOC | Method length ≤50 lines | feature_story, bug_fix, tech_debt, api_change |
| ENG-4.3-DEAD | Zero dead code | feature_story, bug_fix, tech_debt, api_change |
| ENG-6.1-API | API documentation requirements (OpenAPI, changelog, diff) | feature_story, api_change |
| ENG-6.2-ADR | Architecture Decision Records for structural changes | tech_debt, api_change, infrastructure |
| QA-2.1-COV | Code coverage thresholds (80% line, 75% branch) | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-UNIT | Unit testing requirements | feature_story, bug_fix, tech_debt, api_change |
| QA-2.2-INT | Integration testing requirements | feature_story, bug_fix, tech_debt, api_change, infrastructure |
| QA-2.2-E2E | End-to-end testing requirements | feature_story, bug_fix |
| QA-2.3-REG | Regression testing requirements | bug_fix |
| QA-2.4-PERF | Performance testing requirements (k6 load tests) | feature_story, api_change |
| QA-3.1-RELEASE | Release checklist requirements | release, infrastructure |
| QA-POLICY-FEATURE | Product Owner acceptance criteria verification | feature_story |
| SEC-3.1-SNYK | Snyk security scanning thresholds | All work types |
| SEC-3.2-SECRETS | Gitleaks secret detection | All work types |
| SEC-3.3-DEP | Dependency vulnerability scanning (Maven/npm) | All work types |
| SEC-4.1-TFPLAN | Terraform plan review and tfsec scanning | infrastructure |
| SEC-4.2-SECRETS-MGMT | Secrets management practices | feature_story, infrastructure |
| L1-UNIVERSAL-DOC | Universal documentation update requirements | All work types |
| L1-UNIVERSAL-CI | Universal CI check requirements | All work types |
| TEAM-SPRING-BOOT | Spring Boot startup verification | feature_story |
| TEAM-REACT | React build and lint requirements | feature_story |
| TEAM-UX | UX review requirements | feature_story |
| TEAM-ANALYTICS | Analytics event tracking | feature_story |
| TEAM-KAFKA | Kafka event schema validation | bug_fix, tech_debt, api_change, infrastructure |
| TEAM-KAFKA-HEALTH | Kafka health verification | bug_fix |
| TEAM-POSTGRESQL-MIGRATION | Database migration testing | bug_fix, api_change |
| TEAM-POSTGRES | PostgreSQL-specific requirements | tech_debt, api_change, infrastructure |
| TEAM-TECHDEBT-KAFKA | Tech debt Kafka refactoring tests | tech_debt |
| TEAM-TECHDEBT-SONAR | SonarQube issue tracking for tech debt | tech_debt |
| TEAM-TECHDEBT-SONARQUBE | SonarQube quality gate for tech debt | tech_debt |
| TEAM-TECHDEBT-POSTGRES | Database review for tech debt | tech_debt |
| TEAM-AUTH | Authentication/authorization review | api_change |
| TEAM-BACKWARDS-COMPAT | API backward compatibility | api_change |
| TEAM-PO-REVIEW | Product Owner review for API changes | api_change |
| TEAM-API-CONSUMERS | Consumer notification for API changes | api_change |
| TEAM-COMMERCE-PLATFORM | Commerce Platform team-specific requirements | release |
| TEAM-TERRAFORM | Terraform documentation requirements | infrastructure |
| TEAM-STAGING | Staging deployment validation | infrastructure |
| TEAM-DR | Disaster recovery assessment | infrastructure |
| TEAM-EM-SIGNOFF | Engineering Manager sign-off | infrastructure, release |
| BUG-FIX-ROOT-CAUSE | Root cause documentation | bug_fix |
| BUG-FIX-CHANGELOG | Bug fix changelog entry | bug_fix |
| BUG-FIX-REPRO | Bug reporter verification | bug_fix |
| BUG-FIX-NO-SIDE-EFFECTS | Side effect testing | bug_fix |
| TECHDEBT-WORKTYPE | Tech debt-specific requirements | tech_debt |
| DEFECT-INC-001 | Escaped defect INC-001 (SSO auth flow testing) | feature_story |
| DEFECT-INC-002 | Escaped defect INC-002 (nullable field contract tests) | api_change |
| DEFECT-INC-003 | Escaped defect INC-003 (regression test requirement) | bug_fix |
| PO-OR-TECH-LEAD | Story-specific criteria placeholder | All work types |

---

## Notes on Traceability

1. **L1 Universal Criteria**: 78 total instances across all work types (13 unique L1 criteria replicated across 6 work types).

2. **Escaped Defect Integration**: 3 unique escaped defects incorporated into DoD:
   -