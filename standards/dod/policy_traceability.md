# Policy Traceability Matrix
Generated: 2026-03-04

This matrix provides complete traceability from each DoD criterion back to its source policy document or escaped defect incident. Every criterion in the DoD is traceable to at least one authoritative source.

## Matrix Structure
- **Criterion ID**: Unique identifier within work type (e.g., CODE-01, TEST-05)
- **Work Type**: Type of work item this criterion applies to
- **Layer**: L1 (Universal), L2 (Work Type), L3 (Team), or L4 (Story)
- **Source Policy Ref**: Reference to source policy document or incident
- **Criterion Text**: Full text of the DoD criterion

---

## Feature Story DoD Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | feature_story | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | feature_story | L1 | ENG-4.1-SEC | If PR touches authentication, authorization, payment processing, or PII handling, Security Champion approval is documented in PR review comments. |
| CODE-03 | feature_story | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | feature_story | L1 | ENG-4.2 | All commit messages follow Conventional Commits format (type(scope): description). |
| CODE-05 | feature_story | L1 | ENG-4.2 | PR is configured for squash merge (merge commits prohibited). |
| CODE-06 | feature_story | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | feature_story | L1 | ENG-4.3 | SonarQube reports zero methods exceeding 50 lines of code. |
| CODE-08 | feature_story | L1 | ENG-4.3 | SonarQube reports zero dead code (unreachable or commented-out code). |
| TEST-01 | feature_story | L1 | QA-2.1 | JaCoCo reports ≥ 80% line coverage on all changed modules in CI. |
| TEST-02 | feature_story | L1 | QA-2.1 | JaCoCo reports ≥ 75% branch coverage on all changed modules in CI. |
| TEST-03 | feature_story | L1 | QA-2.1 | CI build confirms zero coverage regression on existing covered code. |
| TEST-04 | feature_story | L2 | QA-2.2-FEATURE | Unit tests present covering all changed business logic (JUnit 5). |
| TEST-05 | feature_story | L2 | QA-2.2-FEATURE | Integration tests present covering API contracts and database interactions. |
| TEST-06 | feature_story | L2 | QA-2.2-FEATURE | E2E test present covering happy path user flow (Playwright). |
| TEST-07 | feature_story | L2 | QA-2.2-FEATURE | E2E test present covering at least 1 error path scenario (Playwright). |
| TEST-08 | feature_story | L2 | QA-2.4 | If feature includes API endpoint expected to handle > 1000 RPS, k6 load test present in CI. |
| PERF-01 | feature_story | L2 | QA-2.4 | If k6 load test present, k6 test report shows P95 response time < 500ms under normal load. |
| PERF-02 | feature_story | L2 | QA-2.4 | If k6 load test present, k6 test report shows P99 response time < 2000ms under normal load. |
| SEC-01 | feature_story | L1 | SEC-3.1 | Snyk security scan reports 0 Critical severity findings in CI. |
| SEC-02 | feature_story | L1 | SEC-3.1 | Snyk security scan reports 0 High severity findings in CI. |
| SEC-03 | feature_story | L1 | SEC-3.1 | All Medium severity Snyk findings acknowledged with tracked Jira ticket reference in PR description. |
| SEC-04 | feature_story | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan passes in CI with 0 secrets detected. |
| SEC-05 | feature_story | L1 | SEC-4.2 | All application secrets stored in AWS Secrets Manager or GitHub Actions secrets (documented in PR description). |
| SEC-06 | feature_story | L1 | SEC-3.3 | All new dependencies present in approved dependency registry (referenced in PR description). |
| SEC-07 | feature_story | L1 | SEC-3.3 | Maven dependency:check reports 0 Critical CVE findings in CI. |
| SEC-08 | feature_story | L2 | INC-001 | Integration test: SSO login flow verified for all configured auth methods before merge. |
| CI-01 | feature_story | L1 | ENG-4.1 | All GitHub Actions required checks pass (lint, build, test, security). |
| CI-02 | feature_story | L3 | TEAM-TECH-STACK | Spring Boot application builds successfully with ./mvnw clean package. |
| CI-03 | feature_story | L3 | TEAM-TECH-STACK | React frontend builds successfully with npm run build (production mode). |
| CI-04 | feature_story | L3 | TEAM-TECH-STACK | PostgreSQL integration tests run against Docker container with schema migrations applied. |
| DOC-01 | feature_story | L2 | ENG-6.1 | If feature modifies public API endpoints, OpenAPI specification file (api/openapi.yaml) updated to reflect changes. |
| DOC-02 | feature_story | L2 | ENG-6.1 | If feature modifies public API endpoints, CHANGELOG.md updated with entry under [Unreleased] section. |
| DOC-03 | feature_story | L2 | ENG-6.1 | If feature modifies public API endpoints, API diff document generated and attached to PR. |
| DOC-04 | feature_story | L3 | TEAM-TECH-STACK | If feature adds new Kafka topics or changes event schema, event catalog documentation updated (docs/events/). |
| DOC-05 | feature_story | L3 | TEAM-TECH-STACK | If feature changes user-facing behavior, README.md or user documentation updated. |
| ACC-01 | feature_story | L2 | QA-2.2-FEATURE | All acceptance criteria defined in user story verified by Product Owner. |
| ACC-02 | feature_story | L3 | TEAM-PROCESS | If feature includes UI changes, UX review completed and design approval documented. |
| ACC-03 | feature_story | L3 | TEAM-PROCESS | If feature is user-facing, analytics events instrumented and verified in staging. |
| SS-01 | feature_story | L4 | PO-OR-TECH-LEAD | (Add story-specific criterion here during grooming if needed) |

---

## Bug Fix DoD Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | bug_fix | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | bug_fix | L1 | ENG-4.1-SEC | If PR touches security-critical code paths, approval from designated Security Champion is documented in review comments. |
| CODE-03 | bug_fix | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | bug_fix | L1 | ENG-4.2 | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | bug_fix | L1 | ENG-4.2 | PR is configured for squash merge (merge commits prohibited). |
| CODE-06 | bug_fix | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | bug_fix | L1 | ENG-4.3 | SonarQube reports zero methods exceeding 50 lines of code. |
| CODE-08 | bug_fix | L1 | ENG-4.3 | SonarQube reports zero dead code (unreachable or commented-out code blocks). |
| TEST-01 | bug_fix | L1 | QA-2.1 | JaCoCo reports ≥ 80% line coverage on all changed modules in CI. |
| TEST-02 | bug_fix | L1 | QA-2.1 | JaCoCo reports ≥ 75% branch coverage on all changed modules in CI. |
| TEST-03 | bug_fix | L1 | QA-2.1 | CI build confirms zero coverage regression on existing covered code. |
| TEST-04 | bug_fix | L2 | QA-2.2-BUGFIX | Unit tests present covering fixed code path (JUnit 5). |
| TEST-05 | bug_fix | L2 | QA-2.2-BUGFIX | Integration tests present if bug originated in API contract or database interaction. |
| TEST-06 | bug_fix | L2 | QA-2.2-BUGFIX | E2E test present if bug manifested in UI (Playwright). |
| TEST-07 | bug_fix | L2 | QA-2.3, INC-003 | Regression test covering exact bug reproduction path present in CI. |
| TEST-08 | bug_fix | L2 | QA-2.3 | PR description documents that regression test fails on pre-fix commit and passes on fixed commit. |
| SEC-01 | bug_fix | L1 | SEC-3.1 | Snyk security scan reports 0 Critical severity findings in CI. |
| SEC-02 | bug_fix | L1 | SEC-3.1 | Snyk security scan reports 0 High severity findings in CI. |
| SEC-03 | bug_fix | L1 | SEC-3.1 | All Medium severity Snyk findings acknowledged with tracked Jira ticket reference in PR description. |
| SEC-04 | bug_fix | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan passes in CI with 0 secrets detected. |
| SEC-05 | bug_fix | L1 | SEC-4.2 | All application secrets stored in AWS Secrets Manager or GitHub Actions secrets (documented in PR description). |
| SEC-06 | bug_fix | L1 | SEC-3.3 | Dependency vulnerability scan (mvn dependency:check) reports 0 Critical CVE findings in CI. |
| SEC-07 | bug_fix | L3 | COMMERCE-PLATFORM-SEC | If bug fix touches payment processing, PCI-DSS code review checklist completed and attached to PR. |
| DOC-01 | bug_fix | L2 | ENG-HANDBOOK-BUGFIX | Bug ticket includes root cause analysis section documenting why defect occurred. |
| DOC-02 | bug_fix | L2 | ENG-HANDBOOK-BUGFIX | PR description includes "Reproduction Steps" section documenting exact steps to reproduce original bug. |
| DOC-03 | bug_fix | L2 | ENG-HANDBOOK-BUGFIX | PR description includes "Fix Summary" section explaining technical approach to fix. |
| DOC-04 | bug_fix | L3 | COMMERCE-PLATFORM-DOC | If bug impacts external API contracts, CHANGELOG.md updated with [Bugfix] entry under [Unreleased]. |
| CI-01 | bug_fix | L1 | ENG-HANDBOOK-CI | All GitHub Actions checks pass (build, lint, test, security). |
| CI-02 | bug_fix | L2 | COMMERCE-PLATFORM-CI | If bug was environment-specific, fix verified in staging environment before merge. |
| CI-03 | bug_fix | L3 | COMMERCE-PLATFORM-KAFKA | If bug involved Kafka message handling, manual verification performed with sample messages in dev environment. |
| ACC-01 | bug_fix | L2 | QA-POLICY-BUGFIX | Bug reporter or QA engineer confirms fix resolves original issue in staging environment. |
| ACC-02 | bug_fix | L2 | PRODUCT-POLICY | If bug impacts customer-facing functionality, Product Owner approval documented in PR. |
| SS-01 | bug_fix | L4 | PO-OR-TECH-LEAD | Story-specific criterion added during grooming (if applicable). |

---

## Tech Debt DoD Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | tech_debt | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | tech_debt | L1 | ENG-4.1-SEC | If PR touches authentication, authorization, payment processing, or PII handling code, Security Champion approval documented in PR review comments. |
| CODE-03 | tech_debt | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | tech_debt | L1 | ENG-4.2 | All commit messages follow Conventional Commits format: type(scope): description. |
| CODE-05 | tech_debt | L1 | ENG-4.2 | PR is configured for squash merge (merge commit option disabled in GitHub branch protection). |
| CODE-06 | tech_debt | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | tech_debt | L1 | ENG-4.3 | SonarQube reports zero methods exceeding 50 lines of code. |
| CODE-08 | tech_debt | L1 | ENG-4.3 | SonarQube reports zero dead code (unreachable or commented-out code blocks). |
| TEST-01 | tech_debt | L1 | QA-2.1 | JaCoCo reports ≥ 80% line coverage on all changed modules in CI. |
| TEST-02 | tech_debt | L1 | QA-2.1 | JaCoCo reports ≥ 75% branch coverage on all changed modules in CI. |
| TEST-03 | tech_debt | L1 | QA-2.1 | CI build confirms zero coverage regression on existing covered code (no previously covered lines lost coverage). |
| TEST-04 | tech_debt | L2 | QA-2.2-TECHDEBT | Unit tests present covering all refactored code paths (JUnit 5). |
| TEST-05 | tech_debt | L2 | QA-2.2-TECHDEBT | Integration tests present if tech debt impacts service boundaries, API contracts, or data layer interactions. |
| TEST-06 | tech_debt | L3 | TEAM-TECHDEBT-01 | No new technical debt introduced: SonarQube "New Code" gate shows 0 new code smells, 0 new bugs, 0 new vulnerabilities. |
| SEC-01 | tech_debt | L1 | SEC-3.1 | Snyk security scan reports 0 Critical severity findings in CI. |
| SEC-02 | tech_debt | L1 | SEC-3.1 | Snyk security scan reports 0 High severity findings in CI. |
| SEC-03 | tech_debt | L1 | SEC-3.1 | All Medium severity Snyk findings acknowledged with tracked Jira ticket reference in PR description. |
| SEC-04 | tech_debt | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan passes with 0 secrets detected; all application secrets stored in AWS Secrets Manager or GitHub Actions secrets (documented in PR description if secrets configuration changed). |
| SEC-05 | tech_debt | L1 | SEC-3.3 | All new third-party dependencies added to pom.xml are listed in PR description and present in approved dependency registry (docs/approved-dependencies.md). |
| SEC-06 | tech_debt | L1 | SEC-3.3 | Dependency vulnerability scan (mvn dependency:check) reports 0 Critical CVE findings in CI. |
| DOC-01 | tech_debt | L2 | ENG-6.2 | If tech debt involves architectural change (e.g., module restructuring, design pattern introduction, data model change), Architecture Decision Record (ADR) created in docs/adr/ documenting rationale, alternatives considered, and decision. |
| DOC-02 | tech_debt | L2 | ENG-6.2 | If ADR created, PR has approval from Architecture Guild member documented in review comments. |
| DOC-03 | tech_debt | L3 | TEAM-DOC-01 | If refactoring changes public API surface (Spring @RestController endpoints, method signatures), inline Javadoc updated on changed methods documenting parameters, return types, and exceptions. |
| DOC-04 | tech_debt | L3 | TEAM-DOC-02 | README.md in changed module updated if refactoring impacts module purpose, dependencies, or usage examples. |
| CI-01 | tech_debt | L1 | ENG-4.2 | GitHub Actions CI workflow completes successfully: all jobs (lint, build, unit-test, integration-test, sonarqube, snyk, gitleaks) show green checkmarks. |
| CI-02 | tech_debt | L3 | TEAM-CI-01 | Spring Boot application starts successfully in CI environment: Spring context loads without errors, all @Component beans instantiate, health check endpoint /actuator/health returns UP. |
| ACC-01 | tech_debt | L2 | TEAM-TECHDEBT-02 | Tech Lead or Staff Engineer confirms refactoring achieves stated technical objective documented in tech debt ticket (e.g., "reduce cyclomatic complexity in OrderService", "eliminate duplicate code in payment processing"). |
| ACC-02 | tech_debt | L3 | TEAM-TECHDEBT-03 | If refactoring touches Kafka event producers/consumers, event schema validation passes: Kafka integration test verifies events produced match schema registry, events consumed deserialize correctly. |
| SS-01 | tech_debt | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (e.g., "Database migration script tested in staging environment", "Performance benchmark shows 20% reduction in query time"). |

---

## API Change DoD Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | api_change | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | api_change | L1 | ENG-4.1-SEC | Security-critical PRs have approval from designated Security Champion in addition to standard approvals. |
| CODE-03 | api_change | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | api_change | L1 | ENG-4.2 | All commit messages follow Conventional Commits format (type(scope): description). |
| CODE-05 | api_change | L1 | ENG-4.2 | PR is configured for squash merge (merge commits prohibited). |
| CODE-06 | api_change | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | api_change | L1 | ENG-4.3 | SonarQube reports zero methods exceeding 50 lines of code. |
| CODE-08 | api_change | L1 | ENG-4.3 | SonarQube reports zero dead code (unreachable or commented-out code). |
| TEST-01 | api_change | L1 | QA-2.1 | JaCoCo reports ≥ 80% line coverage on all changed modules in CI. |
| TEST-02 | api_change | L1 | QA-2.1 | JaCoCo reports ≥ 75% branch coverage on all changed modules in CI. |
| TEST-03 | api_change | L1 | QA-2.1 | CI build confirms zero coverage regression on existing covered code (no previously covered lines lost coverage). |
| TEST-04 | api_change | L2 | QA-2.2-API | Unit tests present covering API endpoint logic (JUnit 5). |
| TEST-05 | api_change | L2 | QA-2.2-API | Integration tests present covering API contract and response formats. |
| TEST-06 | api_change | L2 | INC-002 | API contract test must include all nullable fields documented in the OpenAPI spec. |
| TEST-07 | api_change | L2 | QA-2.4 | k6 load test present in CI for API endpoints expected to handle > 1000 RPS. |
| TEST-08 | api_change | L2 | QA-2.4 | k6 test report shows P95 response time < 500ms under normal load. |
| SEC-01 | api_change | L1 | SEC-3.1 | Snyk security scan reports 0 Critical severity findings in CI. |
| SEC-02 | api_change | L1 | SEC-3.1 | Snyk security scan reports 0 High severity findings in CI. |
| SEC-03 | api_change | L1 | SEC-3.1 | All Medium severity Snyk findings acknowledged with tracked Jira ticket reference in PR description. |
| SEC-04 | api_change | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan passes in CI with 0 secrets detected; all application secrets stored in AWS Secrets Manager or GitHub Actions secrets (documented in PR description). |
| SEC-05 | api_change | L1 | SEC-3.3 | All new dependencies present in approved dependency registry (referenced in PR description). |
| SEC-06 | api_change | L1 | SEC-3.3 | Dependency vulnerability scan (mvn dependency:check) reports 0 Critical CVE findings in CI. |
| DOC-01 | api_change | L2 | ENG-6.1 | OpenAPI specification file (api/openapi.yaml) updated to reflect all API endpoint changes. |
| DOC-02 | api_change | L2 | ENG-6.1 | CHANGELOG.md updated with entry under [Unreleased] section describing API changes. |
| DOC-03 | api_change | L2 | ENG-6.1 | API diff document generated and attached to PR showing before/after comparison. |
| DOC-04 | api_change | L2 | ENG-6.2 | Architecture Decision Record (ADR) created in docs/adr/ documenting architectural change rationale if API change impacts system architecture, data model, or cross-service contracts. |
| DOC-05 | api_change | L2 | ENG-6.2 | PR has approval from Architecture Guild member documented in review comments if ADR is required. |
| DOC-06 | api_change | L3 | TEAM-KAFKA | If API change involves publishing or consuming Kafka events, event schema is documented in docs/event-schemas/ with Avro schema file. |
| CI-01 | api_change | L1 | CI-GATE | All GitHub Actions workflows pass with green status (build, test, security, lint). |
| CI-02 | api_change | L2 | QA-2.4 | k6 test report shows P99 response time < 2000ms under normal load for high-traffic endpoints. |
| ACC-01 | api_change | L3 | TEAM-API-REVIEW | API change reviewed in team API Design Review meeting if introducing new public endpoint or breaking change. |
| SS-01 | api_change | L4 | PO-OR-TECH-LEAD | [Add story-specific criterion here if applicable] |

---

## Release DoD Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | release | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | release | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-03 | release | L1 | ENG-4.2 | All commit messages follow Conventional Commits format (type(scope): description). |
| CODE-04 | release | L1 | ENG-4.2 | PR is configured for squash merge (merge commits prohibited). |
| CODE-05 | release | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-06 | release | L1 | ENG-4.3 | SonarQube reports zero methods exceeding 50 lines of code. |
| CODE-07 | release | L1 | ENG-4.3 | SonarQube reports zero dead code (unreachable or commented-out code). |
| TEST-01 | release | L1 | QA-2.1 | JaCoCo reports ≥ 80% line coverage on all changed modules in CI. |
| TEST-02 | release | L1 | QA-2.1 | JaCoCo reports ≥ 75% branch coverage on all changed modules in CI. |
| TEST-03 | release | L1 | QA-2.1 | CI build confirms zero coverage regression on existing covered code (no previously covered lines lost coverage). |
| TEST-04 | release | L2 | QA-3.1 | Full regression test suite passes in staging and pre-prod environments. |
| TEST-05 | release | L2 | QA-3.1 | Smoke test suite passes in production environment post-deployment. |
| SEC-01 | release | L1 | SEC-3.1 | Snyk security scan reports 0 Critical severity findings in CI. |
| SEC-02 | release | L1 | SEC-3.1 | Snyk security scan reports 0 High severity findings in CI. |
| SEC-03 | release | L1 | SEC-3.1 | All Medium severity Snyk findings acknowledged with tracked Jira ticket reference in PR description. |
| SEC-04 | release | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan passes in CI with 0 secrets detected. |
| SEC-05 | release | L1 | SEC-3.3 | All new dependencies present in approved dependency registry (referenced in PR description). |
| SEC-06 | release | L1 | SEC-3.3 | Dependency vulnerability scan (mvn dependency:check) reports 0 Critical CVE findings in CI. |
| SEC-07 | release | L1 | SEC-4.2 | All application secrets stored in AWS Secrets Manager or GitHub Actions secrets (documented in PR description). |
| DOC-01 | release | L2 | QA-3.1 | Release notes prepared and approved by Engineering Manager (documented in PR or release ticket). |
| DOC-02 | release | L2 | QA-3.1 | Runbook updated to reflect any changed operational procedures. |
| DOC-03 | release | L3 | TEAM-COMMERCE | CHANGELOG.md updated with all feature, bugfix, and infrastructure changes under [Unreleased] section. |
| DEPLOY-01 | release | L2 | QA-3.1 | Rollback plan documented and tested successfully in staging environment. |
| DEPLOY-02 | release | L3 | TEAM-COMMERCE | Database migration scripts reviewed and have explicit rollback statements. |
| DEPLOY-03 | release | L3 | TEAM-COMMERCE | Kafka topic compatibility verified if event schema changes included. |
| CI-01 | release | L1 | ENG-4.1, QA-2.1, SEC-3.1 | All GitHub Actions CI checks pass (lint, build, test, coverage, security scan). |
| CI-02 | release | L3 | TEAM-COMMERCE | Production deployment approval obtained from on-call engineer via GitHub deployment protection rule. |
| ACCEPT-01 | release | L2 | QA-3.1 | Engineering Manager sign-off documented in release ticket or GitHub release. |
| ACCEPT-02 | release | L3 | TEAM-COMMERCE | Product Owner confirms acceptance of all user-facing changes in release. |
| ACCEPT-03 | release | L3 | TEAM-COMMERCE | Customer Success team notified of release 24 hours before deployment with summary of changes. |
| SS-01 | release | L4 | PO-OR-TECH-LEAD | Add story-specific criterion here if applicable (e.g., compliance audit requirements, customer-specific validation, regulatory filing). |

---

## Infrastructure DoD Criteria

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text |
|---|---|---|---|---|
| CODE-01 | infrastructure | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. |
| CODE-02 | infrastructure | L1 | ENG-4.1-SEC | Security-critical PRs have approval from designated Security Champion in addition to standard approvals. |
| CODE-03 | infrastructure | L1 | ENG-4.2 | All commits in PR are signed with GPG or SSH key registered in GitHub. |
| CODE-04 | infrastructure | L1 | ENG-4.2 | All commit messages follow Conventional Commits format (type(scope): description). |
| CODE-05 | infrastructure | L1 | ENG-4.2 | PR is configured for squash merge (merge commits prohibited). |
| CODE-06 | infrastructure | L1 | ENG-4.3 | SonarQube quality gate passes with cyclomatic complexity ≤ 10 per method. |
| CODE-07 | infrastructure | L1 | ENG-4.3 | SonarQube reports zero methods exceeding 50 lines of code. |
| CODE-08 | infrastructure | L1 | ENG-4.3 | SonarQube reports zero dead code (unreachable or commented-out code). |
| TEST-01 | infrastructure | L1 | QA-2.1 | JaCoCo reports ≥ 80% line coverage on all changed modules in CI. |
| TEST-02 | infrastructure | L1 | QA-2.1 | JaCoCo reports ≥ 75% branch coverage on all changed modules in CI. |
| TEST-03 | infrastructure | L1 | QA-2.1 | CI build confirms zero coverage regression on existing covered code (no previously covered lines lost coverage). |
| TEST-04 | infrastructure | L3 | TEAM-INFRA-01 | Terraform configuration validated using terraform validate in CI. |
| TEST-05 | infrastructure | L3 | TEAM-INFRA-02 | Infrastructure tests present for critical resources (networking, data persistence, security groups). |
| SEC-01 | infrastructure | L1 | SEC-3.1 | Snyk security scan reports 0 Critical severity findings in CI. |
| SEC-02 | infrastructure | L1 | SEC-3.1 | Snyk security scan reports 0 High severity findings in CI. |
| SEC-03 | infrastructure | L1 | SEC-3.1 | All Medium severity Snyk findings acknowledged with tracked Jira ticket reference in PR description. |
| SEC-04 | infrastructure | L1 | SEC-3.2, SEC-4.2 | Gitleaks scan passes in CI with 0 secrets detected. |
| SEC-05 | infrastructure | L1 | SEC-4.2 | All application secrets stored in AWS