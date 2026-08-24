---
framework_version: 1.1.1
---

# Candidate Profile

## Identity
- **Name:** Sawan Dasari
- **Location:** New York City, NY
- **Phone:** 513-689-0708
- **Email:** sawan.dasari@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/sawan-dasari/
- **GitHub:** https://github.com/sa1dasari
- **Portfolio:** https://sa1dasari.github.io/
- **Status:** Employed (Software Engineer II, JPMorgan Chase), open to new opportunities
- **Work Authorization:** H-1B (transfer-eligible, no lottery required)
- **Constraints:** Open to relocation, remote, or hybrid — no location constraint

### Languages
<!-- Every language you can work in professionally, with your honest level. Used by the
Language Gate in 04-job-evaluation.md and by job-scraper/search-queries.md's query-language
generation. Omit any language you don't actually work in - an undeclared language is treated as
a hard no, not a gap to smooth over. -->

| Language | Level | Notes |
|----------|-------|-------|
| English | Fluent | |

## Education

| Degree | Period | Institution | Key Topics |
|--------|--------|-------------|------------|
| M.S., Information Technology | 2022-2023 | University of Cincinnati, Cincinnati, OH | Machine Learning & Data Mining, System Design, Principles of Cybersecurity, Advanced Storage Technologies, Advanced Algorithms (GPA 3.968) |
| B.Tech, Computer Science | 2017-2021 | BV Raju Institute of Technology (BVRIT) | |

## Professional Experience

### Software Engineer II - JPMorgan Chase (Jul 2025 - Present)
New York, NY
- Architected and deployed a cloud-native data platform from scratch on AWS (Step Functions, Glue, Athena, ECS) with Terraform, processing 10M+ records/day with 99.9% reliability and automated, self-healing failure recovery
- Implemented a real-time change-data-capture pipeline using CockroachDB changefeeds to stream row-level mutations into a data lake and Snowflake with exactly-once delivery and minimal OLTP impact
- Developed Python/PySpark ETL jobs on AWS Glue for TB-scale processing, with schema validation, data-quality checks, and partition optimization feeding Snowflake tables for downstream analytics
- Designed RESTful APIs and microservices with Spring Boot and Java, reducing downstream data-access latency by 60%
- Automated weekly and monthly billing report generation with scheduled AWS Glue jobs and Step Functions orchestration, replacing manual reporting
- Built automated CI/CD pipelines (Jenkins, Docker) across DEV/UAT/PROD, cutting deployment time by 70%
- Built end-to-end monitoring and observability (CloudWatch custom metrics, PagerDuty alerting), reducing mean time to detect issues by 45%

### Software Engineer - State Street (Jan 2024 - Jun 2025)
Boston, MA
- Developed Spring Boot microservices for credit-decisioning workflows serving 5M+ requests/day against PostgreSQL and Cassandra
- Built real-time event pipelines with Kafka and Flink for cross-system data synchronization with sub-second latency and exactly-once delivery
- Reduced processing latency by 40% through query tuning, caching, and parallelism improvements under production load
- Deployed to Kubernetes (EKS) via Spinnaker with auto-scaling and zero-downtime releases; served in on-call rotation with root-cause analysis on production incidents
- Implemented a comprehensive automated testing strategy (JUnit, Mockito, integration and performance tests), achieving 95%+ coverage

### Teaching Assistant - University of Cincinnati (Jun 2022 - Aug 2023)
Cincinnati, OH
- Assisted in delivering Machine Learning & Data Mining coursework: grading, hands-on student support, and guidance on regression, classification, and clustering techniques
- Helped students implement ML solutions in Python notebooks, developing practical skills in applied machine learning

### Software Engineer - State Street (Jun 2020 - Dec 2021)
Hyderabad, India
- Built Java microservices and PostgreSQL schemas for investment-data reconciliation and reporting over 100M+ records
- Introduced Kafka-based event-driven data propagation between services and AWS Lambda serverless batch jobs, cutting infrastructure cost about 30% vs. EC2
- Implemented Spring Security (OAuth2/JWT) with role-based access control to meet GDPR and SOX requirements

## Independent Projects
<!-- Projects outside of employment: freelance, open source, personal -->
- **WordForge** (wordlegames.co, live): Solo-designed, built, and operates a real-time multiplayer word-game platform (solo, duel, party, daily modes) end-to-end — vanilla JS PWA frontend, Node.js/Socket.io backend on Railway, Supabase for auth/leaderboards/streaks. Iterates directly against live user behavior post-launch with no QA/ops team.
- **Paper-to-Prototype Agent** (github.com/sa1dasari): Self-correcting agent pipeline that converts ML research PDFs into runnable Jupyter notebooks, auto-detecting and repairing failed cells/missing dependencies, with an SSIM-based automated eval comparing generated figures to the source paper's originals.
- **NYC Running Events Finder Agent** (github.com/sa1dasari): Autonomous agent (Anthropic Managed Agents + Gmail MCP) that integrates four independent external event sources (RunSignUp, NYRR, RaceRaves, Eventbrite), deduplicates results, and emails a formatted HTML digest on a GitHub Actions cron with no manual intervention.
- **fullpicture** (Android, github.com/sa1dasari/fullpicture): Android app combining the Claude API with Accessibility Service and MediaProjection to deliver real-time, on-device contextual analysis of on-screen content for misinformation detection.
- **Personal Finance Coaching Agent** (github.com/sa1dasari): Full conversational Java application built on the Anthropic API from scratch, including multi-turn state management, architected independently end-to-end.
- **Applied ML Research: Retraining Policies Under Drift** (github.com/sa1dasari): Designed and ran a 3,933-run factorial study comparing four model retraining policies across three datasets and drift types under budget/latency constraints; built the evaluation harness; prepared for IEEE submission.

## Technical Skills

### Programming & ML
- **Languages:** Java, Python, JavaScript/Node.js, SQL, CQL
- **AI/Agents:** Anthropic Claude API, Model Context Protocol (MCP), agentic system design, tool use/function calling, prompt engineering, RAG concepts, self-correcting agent loops, eval design & automated scoring
- **Data Engineering:** PySpark, ETL/ELT pipeline design, Snowflake, data lakes, CDC ingestion, data modeling, schema validation, data-quality checks
- **Streaming & Backend:** Apache Kafka, Apache Flink, Spring Boot, REST APIs, microservices, event-driven architecture

### Domain Expertise
- Fintech / investment banking (credit decisioning, investment-data reconciliation, billing/reporting platforms)
- Cloud-native data platforms and CDC-based ingestion pipelines

### Software & Tools
- **Cloud & Infra:** AWS (Glue, Athena, Step Functions, Lambda, S3, ECS, EKS, EventBridge), Kubernetes, Docker, Terraform
- **Databases:** Snowflake, CockroachDB, PostgreSQL, Cassandra, MongoDB
- **DevOps & Quality:** Jenkins, Spinnaker, Datadog, Grafana, CloudWatch, Splunk, JUnit, Mockito, Git

## Certifications
- Java (Intermediate) Certificate
- Programming Essentials in Python
- Problem Solving (Basic) Certificate

## Publications
<!-- List peer-reviewed publications, if any -->
None yet. "Applied ML Research: Retraining Policies Under Drift" (see Independent Projects) is prepared for IEEE submission but not yet published — do not cite as a publication until accepted.

## Awards
None on record.

## References
Available upon request — not yet collected in this profile.
