# Policy Traceability Matrix
**Generated:** 2026-03-30  
**DoD Builder Version:** 1.0  
**Organisation:** Acme Engineering  
**Team:** Commerce Platform

## Purpose
This matrix provides complete traceability from source policy documents to individual Definition-of-Done criteria across all work types. Every criterion references at least one source policy, ensuring no arbitrary requirements exist in the DoD checklists.

## Matrix Structure
- **Criterion ID:** Unique identifier within each work type DoD
- **Work Type:** The DoD checklist containing this criterion
- **Layer:** L1-UNIVERSAL (all work), L2-WORKTYPE (type-specific), L3-TEAM (team-specific), L4-STORY (story-specific)
- **Source Policy Ref:** Reference ID from source policy documents
- **Criterion Text:** Brief summary of the criterion requirement
- **Escaped Defect:** Indicates if criterion originated from production incident analysis

---

## Feature Story

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text | Escaped Defect |
|---|---|---|---|---|---|
| CODE-01 | feature_story | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | No |
| CODE-02 | feature_story | L1 | ENG-4.2 | All commits are signed with GPG or SSH signing key registered in GitHub. | No |
| CODE-03 | feature_story | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | No |
| CODE-04 | feature_story | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy only; merge commits prohibited on main branch. | No |
| CODE-05 | feature_story | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | No |
| CODE-06 | feature_story | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). | No |
| CODE-07 | feature_story | L1 | ENG-4.3-DEAD | SonarQube reports 0 dead code violations (unreachable or commented-out code removed). | No |
| CODE-08 | feature_story | L2 | ENG-4.1-SEC | PR touching security-critical paths has approval from designated Security Champion. | No |
| TEST-01 | feature_story | L1 | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI build. | No |
| TEST-02 | feature_story | L1 | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI build. | No |
| TEST-03 | feature_story | L1 | QA-2.1-REGRESS | CI build verifies no coverage regression on existing covered code (JaCoCo diff check passes). | No |
| TEST-04 | feature_story | L2 | QA-2.2-FEATURE | Unit tests present and passing in CI (JUnit 5) for feature story. | No |
| TEST-05 | feature_story | L2 | QA-2.2-FEATURE | Integration tests present and passing in CI (JUnit 5) for feature story. | No |
| TEST-06 | feature_story | L2 | QA-2.2-FEATURE | E2E tests present covering happy path + minimum 1 error path (Playwright) for feature story. | No |
| TEST-07 | feature_story | L2 | QA-2.4 | k6 load test present in CI for endpoints expected to handle >1000 RPS, verifying P95 <500ms and P99 <2000ms. | No |
| TEST-08 | feature_story | L2 | INC-001 | Integration test verifies SSO login flow for all configured auth methods (JUnit 5) present in CI. | **Yes** |
| SEC-01 | feature_story | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings in CI before merge to main. | No |
| SEC-02 | feature_story | L1 | SEC-3.1 | All Medium severity findings from Snyk acknowledged with tracked Jira ticket referenced in PR. | No |
| SEC-03 | feature_story | L1 | SEC-3.2 | Gitleaks scan passes in CI with zero secrets detected before merge to main. | No |
| SEC-04 | feature_story | L1 | SEC-3.3-APPROVED | All third-party dependencies are listed in approved dependency registry (verified in CI). | No |
| SEC-05 | feature_story | L1 | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present (npm audit / mvn dependency:check passes). | No |
| SEC-06 | feature_story | L1 | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) run in CI and report 0 Critical findings. | No |
| SEC-07 | feature_story | L1 | SEC-4.2 | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified via code review). | No |
| DOC-01 | feature_story | L3 | TEAM-STANDARD | README.md updated if feature changes setup, configuration, or deployment procedures. | No |
| DOC-02 | feature_story | L3 | TEAM-STANDARD | Inline code comments added for complex business logic (cyclomatic complexity >5). | No |
| DOC-03 | feature_story | L3 | TEAM-STANDARD | Confluence page updated if feature changes user-facing behavior or adds new UI flows. | No |
| CI-01 | feature_story | L1 | UNIVERSAL | All GitHub Actions CI checks pass (lint, build, test, security scan, coverage). | No |
| CI-02 | feature_story | L3 | TEAM-STANDARD | Feature deployed to staging environment and smoke tested before PR merge. | No |
| ACC-01 | feature_story | L2 | FEATURE-STORY-STANDARD | All acceptance criteria defined in Jira ticket verified by Product Owner. | No |
| ACC-02 | feature_story | L2 | FEATURE-STORY-STANDARD | UX review approval documented if feature changes UI/UX. | No |
| ACC-03 | feature_story | L3 | TEAM-STANDARD | Analytics event tracking verified if feature adds user interaction. | No |
| SS-01 | feature_story | L4 | PO-OR-TECH-LEAD | Story-specific criterion added during grooming (if applicable). | No |

---

## Bug Fix

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text | Escaped Defect |
|---|---|---|---|---|---|
| CODE-01 | bug_fix | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | No |
| CODE-02 | bug_fix | L1 | ENG-4.2 | All commits are signed with GPG or SSH signing key registered in GitHub. | No |
| CODE-03 | bug_fix | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | No |
| CODE-04 | bug_fix | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy only; merge commits prohibited on main branch. | No |
| CODE-05 | bug_fix | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | No |
| CODE-06 | bug_fix | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). | No |
| CODE-07 | bug_fix | L1 | ENG-4.3-DEAD | SonarQube reports 0 dead code violations (unreachable or commented-out code removed). | No |
| CODE-08 | bug_fix | L2 | BUG-FIX-ROOT-CAUSE | Root cause analysis documented in PR description or linked Jira ticket. | No |
| TEST-01 | bug_fix | L1 | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI build. | No |
| TEST-02 | bug_fix | L1 | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI build. | No |
| TEST-03 | bug_fix | L1 | QA-2.1-REGRESS | CI build verifies no coverage regression on existing covered code (JaCoCo diff check passes). | No |
| TEST-04 | bug_fix | L2 | QA-2.2-BUG | Unit tests present and passing in CI (JUnit 5) for bug fix. | No |
| TEST-05 | bug_fix | L2 | QA-2.2-BUG | Integration tests present if bug is integration-related (JUnit 5). | No |
| TEST-06 | bug_fix | L2 | QA-2.2-BUG | E2E tests present if bug is UI-related (Playwright). | No |
| TEST-07 | bug_fix | L2 | QA-2.3, INC-003 | Regression test covering exact reproduction path from original bug report present in CI. | **Yes** |
| SEC-01 | bug_fix | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings in CI before merge to main. | No |
| SEC-02 | bug_fix | L1 | SEC-3.1 | All Medium severity findings from Snyk acknowledged with tracked Jira ticket referenced in PR. | No |
| SEC-03 | bug_fix | L1 | SEC-3.2 | Gitleaks scan passes in CI with zero secrets detected before merge to main. | No |
| SEC-04 | bug_fix | L1 | SEC-3.3-APPROVED | All third-party dependencies are listed in approved dependency registry (verified in CI). | No |
| SEC-05 | bug_fix | L1 | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present (npm audit / mvn dependency:check passes). | No |
| SEC-06 | bug_fix | L1 | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) run in CI and report 0 Critical findings. | No |
| SEC-07 | bug_fix | L1 | SEC-4.2 | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified via code review). | No |
| DOC-01 | bug_fix | L2 | TEAM-STANDARD | Jira ticket updated with fix details and verification steps. | No |
| DOC-02 | bug_fix | L3 | COMMERCE-PLATFORM | If bug affects payment processing or checkout flow, incident postmortem document updated. | No |
| CI-01 | bug_fix | L1 | UNIVERSAL | All GitHub Actions workflows pass (lint, build, test, security). | No |
| CI-02 | bug_fix | L2 | TEAM-STANDARD | Staging deployment successful and smoke test passed. | No |
| ACCEPT-01 | bug_fix | L2 | TEAM-STANDARD | Bug reporter or QA verifies fix resolves original issue in staging environment. | No |
| ACCEPT-02 | bug_fix | L2 | TEAM-STANDARD | Product Owner notified if bug fix affects user-facing functionality. | No |
| SS-01 | bug_fix | L4 | PO-OR-TECH-LEAD | Story-specific criterion added during grooming (if applicable). | No |

---

## Tech Debt

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text | Escaped Defect |
|---|---|---|---|---|---|
| CODE-01 | tech_debt | L1-UNIVERSAL | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | No |
| CODE-02 | tech_debt | L1-UNIVERSAL | ENG-4.2 | All commits are signed with GPG or SSH signing key registered in GitHub. | No |
| CODE-03 | tech_debt | L1-UNIVERSAL | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | No |
| CODE-04 | tech_debt | L1-UNIVERSAL | ENG-4.2-MERGE | PR merged using squash merge strategy only; merge commits prohibited on main branch. | No |
| CODE-05 | tech_debt | L1-UNIVERSAL | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | No |
| CODE-06 | tech_debt | L1-UNIVERSAL | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). | No |
| CODE-07 | tech_debt | L1-UNIVERSAL | ENG-4.3-DEAD | SonarQube reports 0 dead code violations (unreachable or commented-out code removed). | No |
| CODE-08 | tech_debt | L2-WORKTYPE | ENG-6.2 | ADR document created in docs/adr/ for architecture, data model, or cross-service contract changes. | No |
| TEST-01 | tech_debt | L1-UNIVERSAL | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI build. | No |
| TEST-02 | tech_debt | L1-UNIVERSAL | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI build. | No |
| TEST-03 | tech_debt | L1-UNIVERSAL | QA-2.1-REGRESS | CI build verifies no coverage regression on existing covered code (JaCoCo diff check passes). | No |
| TEST-04 | tech_debt | L2-WORKTYPE | QA-2.2-DEBT | Unit tests present and passing in CI (JUnit 5) for tech debt work. | No |
| TEST-05 | tech_debt | L2-WORKTYPE | QA-2.2-DEBT | Integration tests present and passing in CI (JUnit 5) for tech debt work. | No |
| TEST-06 | tech_debt | L3-TEAM | TEAM-SPRING-BOOT | Spring Boot integration tests verify application context loads successfully after refactor. | No |
| SEC-01 | tech_debt | L1-UNIVERSAL | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings in CI before merge to main. | No |
| SEC-02 | tech_debt | L1-UNIVERSAL | SEC-3.1 | All Medium severity findings from Snyk acknowledged with tracked Jira ticket referenced in PR. | No |
| SEC-03 | tech_debt | L1-UNIVERSAL | SEC-3.2 | Gitleaks scan passes in CI with zero secrets detected before merge to main. | No |
| SEC-04 | tech_debt | L1-UNIVERSAL | SEC-3.3-APPROVED | All third-party dependencies are listed in approved dependency registry (verified in CI). | No |
| SEC-05 | tech_debt | L1-UNIVERSAL | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present (npm audit / mvn dependency:check passes). | No |
| SEC-06 | tech_debt | L1-UNIVERSAL | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) run in CI and report 0 Critical findings. | No |
| SEC-07 | tech_debt | L1-UNIVERSAL | SEC-4.2 | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified via code review). | No |
| SEC-08 | tech_debt | L3-TEAM | TEAM-KAFKA | Kafka consumer/producer configurations reviewed for security settings (SASL, SSL, ACLs). | No |
| DOC-01 | tech_debt | L2-WORKTYPE | ENG-6.2 | Architecture Guild review approval documented in PR (comment or approval from guild member). | No |
| DOC-02 | tech_debt | L3-TEAM | TEAM-POSTGRESQL | Database schema changes documented in docs/schema/ with migration script rationale. | No |
| DOC-03 | tech_debt | L3-TEAM | TEAM-SONARQUBE | If SonarQube technical debt ratio decreased by >5%, CHANGELOG.md updated with achievement note. | No |
| CI-01 | tech_debt | L1-UNIVERSAL | CI-GATE | All GitHub Actions CI checks pass (lint, build, test, security scan, coverage). | No |
| CI-02 | tech_debt | L1-UNIVERSAL | SONARQUBE-GATE | SonarQube quality gate status = PASSED for PR branch. | No |
| CI-03 | tech_debt | L3-TEAM | TEAM-SPRING-BOOT-BUILD | Maven build produces executable JAR artifact with embedded Tomcat (verified by CI). | No |
| CI-04 | tech_debt | L3-TEAM | TEAM-REACT-BUILD | React production build completes with 0 warnings and build/static/ directory generated. | No |
| ACCEPT-01 | tech_debt | L2-WORKTYPE | TECH-DEBT-REVIEW | Tech Lead confirms technical debt metric improved or neutral (SonarQube technical debt ratio). | No |
| ACCEPT-02 | tech_debt | L2-WORKTYPE | TECH-DEBT-SONARQUBE | SonarQube shows 0 new code smells introduced in changed modules. | No |
| ACCEPT-03 | tech_debt | L3-TEAM | TEAM-PERFORMANCE | If refactor touches performance-critical path: k6 smoke test shows no P95 latency regression. | No |
| SS-01 | tech_debt | L4-STORY | PO-OR-TECH-LEAD | Story-specific criterion added during grooming (if applicable). | No |

---

## API Change

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text | Escaped Defect |
|---|---|---|---|---|---|
| CODE-01 | api_change | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | No |
| CODE-02 | api_change | L2 | ENG-4.1-SEC | PR touching security-critical paths has approval from designated Security Champion. | No |
| CODE-03 | api_change | L1 | ENG-4.2 | All commits are signed with GPG or SSH signing key registered in GitHub. | No |
| CODE-04 | api_change | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | No |
| CODE-05 | api_change | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy only; merge commits prohibited on main branch. | No |
| CODE-06 | api_change | L1 | ENG-4.3-COMPLEXITY | SonarQube quality gate passes with cyclomatic complexity ≤10 per method. | No |
| CODE-07 | api_change | L1 | ENG-4.3-LOC | No method exceeds 50 lines of code (verified by SonarQube). | No |
| CODE-08 | api_change | L1 | ENG-4.3-DEAD | SonarQube reports 0 dead code violations (unreachable or commented-out code removed). | No |
| TEST-01 | api_change | L1 | QA-2.1-LINE | JaCoCo reports ≥80% line coverage on all changed modules in CI build. | No |
| TEST-02 | api_change | L1 | QA-2.1-BRANCH | JaCoCo reports ≥75% branch coverage on all changed modules in CI build. | No |
| TEST-03 | api_change | L1 | QA-2.1-REGRESS | CI build verifies no coverage regression on existing covered code (JaCoCo diff check passes). | No |
| TEST-04 | api_change | L2 | QA-2.2-API | Unit tests present and passing in CI (JUnit 5) for API change. | No |
| TEST-05 | api_change | L2 | QA-2.2-API | Integration tests present and passing in CI (JUnit 5) for API change. | No |
| TEST-06 | api_change | L2 | INC-002 | API contract test includes all nullable fields documented in OpenAPI spec (JUnit 5) present in CI. | **Yes** |
| TEST-07 | api_change | L2 | QA-2.4 | k6 load test present in CI for endpoints expected to handle >1000 RPS, verifying P95 <500ms and P99 <2000ms. | No |
| TEST-08 | api_change | L3 | TEAM-API-CONTRACT | Consumer-driven contract tests pass for all known API consumers (Spring Cloud Contract or Pact). | No |
| SEC-01 | api_change | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings in CI before merge to main. | No |
| SEC-02 | api_change | L1 | SEC-3.1 | All Medium severity findings from Snyk acknowledged with tracked Jira ticket referenced in PR. | No |
| SEC-03 | api_change | L1 | SEC-3.2 | Gitleaks scan passes in CI with zero secrets detected before merge to main. | No |
| SEC-04 | api_change | L1 | SEC-3.3-APPROVED | All third-party dependencies are listed in approved dependency registry (verified in CI). | No |
| SEC-05 | api_change | L1 | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present (npm audit / mvn dependency:check passes). | No |
| SEC-06 | api_change | L1 | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) run in CI and report 0 Critical findings. | No |
| SEC-07 | api_change | L1 | SEC-4.2 | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified via code review). | No |
| DOC-01 | api_change | L2 | ENG-6.1 | OpenAPI specification file (api/openapi.yaml) updated to reflect all API endpoint changes. | No |
| DOC-02 | api_change | L2 | ENG-6.1 | CHANGELOG.md updated with entry under [Unreleased] section describing API changes. | No |
| DOC-03 | api_change | L2 | ENG-6.1 | API diff generated and attached to pull request as artifact or comment. | No |
| DOC-04 | api_change | L3 | TEAM-API-MIGRATION | If breaking change, API migration guide published in docs/api-migrations/ with version number and upgrade instructions. | No |
| CI-01 | api_change | L1 | CI-GATE | All GitHub Actions CI checks pass (lint, build, unit tests, integration tests, security scans, coverage checks). | No |
| CI-02 | api_change | L3 | TEAM-KAFKA-SCHEMA | If API change affects Kafka event schemas, Confluent Schema Registry compatibility check passes in CI. | No |
| ACC-01 | api_change | L2 | API-CHANGE-REVIEW | API changes reviewed and approved by Product Owner and 1 consumer team representative (if known consumers exist). | No |
| SS-01 | api_change | L4 | PO-OR-TECH-LEAD | Story-specific criterion added during grooming (if applicable). | No |

---

## Release

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text | Escaped Defect |
|---|---|---|---|---|---|
| CODE-01 | release | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | No |
| CODE-02 | release | L1 | ENG-4.2 | All commits are signed with GPG or SSH signing key registered in GitHub. | No |
| CODE-03 | release | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | No |
| CODE-04 | release | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy only; merge commits prohibited on main branch. | No |
| TEST-01 | release | L2 | QA-3.1-REGRESSION | Full regression test suite passes in staging and pre-prod environments before release. | No |
| TEST-02 | release | L2 | QA-3.1-SMOKE | Smoke test suite passes in production environment post-deployment. | No |
| TEST-03 | release | L3 | TEAM-KAFKA-01 | Kafka consumer lag monitoring confirms all consumers are caught up (lag <100 messages) post-deployment. | No |
| TEST-04 | release | L3 | TEAM-DB-01 | PostgreSQL database migration scripts tested successfully in pre-prod with rollback verification. | No |
| SEC-01 | release | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings in CI before merge to main. | No |
| SEC-02 | release | L1 | SEC-3.1 | All Medium severity findings from Snyk acknowledged with tracked Jira ticket referenced in PR. | No |
| SEC-03 | release | L1 | SEC-3.2 | Gitleaks scan passes in CI with zero secrets detected before merge to main. | No |
| SEC-04 | release | L1 | SEC-3.3-APPROVED | All third-party dependencies are listed in approved dependency registry. | No |
| SEC-05 | release | L1 | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present. | No |
| SEC-06 | release | L1 | SEC-3.3-AUDIT | npm audit (for React) and mvn dependency:check (for Java) run in CI and report 0 Critical findings. | No |
| DOC-01 | release | L2 | QA-3.1-NOTES | Release notes prepared in CHANGELOG.md and approved by Engineering Manager. | No |
| DOC-02 | release | L2 | QA-3.1-ROLLBACK | Rollback plan documented in runbook and tested successfully in staging environment. | No |
| DOC-03 | release | L2 | QA-3.1-RUNBOOK | Runbook updated if operational procedures changed. | No |
| DOC-04 | release | L3 | TEAM-COMM-01 | Release announcement posted in #engineering-releases Slack channel with deployment window and on-call engineer tagged. | No |
| CI-01 | release | L1 | ENG-4.1 | GitHub Actions workflows pass: lint, build, unit tests, integration tests, security scans. | No |
| CI-02 | release | L3 | TEAM-BUILD-01 | Docker images built and pushed to ECR with semantic version tags (vX.Y.Z) and "latest" tag. | No |
| CI-03 | release | L3 | TEAM-DEPLOY-01 | Staging deployment completed successfully with zero failed pods for 10 minutes post-deploy. | No |
| ACCEPT-01 | release | L2 | QA-3.1-NOTES | Engineering Manager sign-off documented in release PR or release issue. | No |
| ACCEPT-02 | release | L3 | TEAM-PO-01 | Product Owner verification completed for all user-facing changes included in release. | No |
| ACCEPT-03 | release | L3 | TEAM-ONCALL-01 | On-call engineer confirmed available for 2 hours post-deployment and has access to rollback procedure. | No |
| SS-01 | release | L4 | PO-OR-TECH-LEAD | Release-specific criterion added during release planning (if applicable). | No |

---

## Infrastructure

| Criterion ID | Work Type | Layer | Source Policy Ref | Criterion Text | Escaped Defect |
|---|---|---|---|---|---|
| CODE-01 | infrastructure | L1 | ENG-4.1 | PR has minimum 2 approvals from engineers other than the author, including 1 from a senior engineer or tech lead. | No |
| CODE-02 | infrastructure | L2 | ENG-4.1-SEC | PR touching security-critical infrastructure has approval from designated Security Champion. | No |
| CODE-03 | infrastructure | L1 | ENG-4.2 | All commits are signed with GPG or SSH signing key registered in GitHub. | No |
| CODE-04 | infrastructure | L1 | ENG-4.2-CONV | All commit messages follow Conventional Commits format: type(scope): description. | No |
| CODE-05 | infrastructure | L1 | ENG-4.2-MERGE | PR merged using squash merge strategy only; merge commits prohibited on main branch. | No |
| CODE-06 | infrastructure | L2 | ENG-6.2 | ADR document created in docs/adr/ for architecture, data model, or cross-service contract changes. | No |
| CODE-07 | infrastructure | L2 | ENG-6.2 | Architecture Guild review approval documented in PR (comment or approval from guild member). | No |
| CODE-08 | infrastructure | L3 | TEAM-INFRA-01 | Terraform fmt passes with zero formatting violations. | No |
| TEST-01 | infrastructure | L2 | INFRA-TEST-01 | Infrastructure validation tests present and passing in CI (Terraform validate + plan). | No |
| TEST-02 | infrastructure | L3 | TEAM-INFRA-02 | Infrastructure smoke tests verify connectivity to PostgreSQL, Kafka, and critical AWS services post-apply. | No |
| SEC-01 | infrastructure | L1 | SEC-3.1 | Snyk scan shows 0 Critical or High severity findings in CI before merge to main. | No |
| SEC-02 | infrastructure | L1 | SEC-3.1 | All Medium severity findings from Snyk acknowledged with tracked Jira ticket referenced in PR. | No |
| SEC-03 | infrastructure | L1 | SEC-3.2 | Gitleaks scan passes in CI with zero secrets detected before merge to main. | No |
| SEC-04 | infrastructure | L1 | SEC-3.3-APPROVED | All third-party dependencies are listed in approved dependency registry (verified in CI). | No |
| SEC-05 | infrastructure | L1 | SEC-3.3-CVE | No dependencies with Critical CVEs older than 5 business days present. | No |
| SEC-06 | infrastructure | L1 | SEC-4.2 | All secrets stored in AWS Secrets Manager or GitHub Actions secrets (verified via code review). | No |
| SEC-07 | infrastructure | L2 | SEC-4.1-PLAN | terraform plan executed and produces clean plan with no unintended resource deletions (plan output attached to PR). | No |
| SEC-08 | infrastructure | L2 | SEC-4.1-PLAN | Platform Engineering team review approval documented in PR. | No |
| SEC-IAC-01 | infrastructure | L2 | SEC-4.1-PLAN | tfsec scan passes with 0 HIGH or CRITICAL findings in CI. | No |
| DOC-01 | infrastructure | L2 | INFRA-DOC-01 | Runbook updated if operational procedures changed (docs/runbooks/ or wiki entry modified). | No |
| DOC-02 | infrastructure | L3 | TEAM-INFRA-03 | Terraform module README.md updated with usage examples and variable descriptions for any new or modified modules. | No |
| DOC-03