# Shafikul Islam (Shafik Tanbir)

**Backend, Platform & Cloud Infrastructure Engineer** · Node.js · TypeScript · Go · Rust · PostgreSQL · Kubernetes · HIPAA/PIPEDA  
Dhaka, Bangladesh (`UTC+6` · Full EU/UK/APAC overlap · Daily US East overlap through `12:00 PM ET` · Deel / Remote.com EOR or Direct B2B)

> I build and operate the backend APIs, multi-tenant databases, and HIPAA/PIPEDA privacy-compliant cloud infrastructure behind live commercial platforms — keeping customer data strictly isolated, billing/booking flows race-free, and deployments rollback-safe.

[**Portfolio & Live Case Studies**](https://shafiktanbir.com) · [**1-Page Resume (PDF)**](https://shafiktanbir.com/resume.pdf) · [**LinkedIn**](https://www.linkedin.com/in/shafiktanbir/) · [**Book Intro Call**](https://shafiktanbir.com/?tab=book)

---

## Live Commercial Systems & Impact

| Platform | Plain-English Outcome | Engineering Ownership & Proof |
| :--- | :--- | :--- |
| **[emmai.ca](https://emmai.ca)** *(Cansoft Technologies)* | Kept daily clinic booking and multi-payer billing online with zero downtime and strict patient-record isolation | HIPAA/PIPEDA multi-tenant architecture (`*.emmai.ca`), PostgreSQL Row-Level Security (RLS), FusionAuth SSO, SHA-256 immutable SOAP sealing, HL7 v3 eClaims, streaming Jane App `TOAST` migrations (72h rollbacks), & K3s/ArgoCD GitOps |
| **[ridebustang.com](https://ridebustang.com)** *(Digital Gregg · Contract)* | Cut real-time bus rider API wait times by **45%** across Colorado's intercity transit network | Engineered REST & GTFS-Realtime / WebSocket vehicle telemetry endpoints; fixed N+1 queries via PostgreSQL composite indexing, Redis caching, & GitHub Actions Docker pipelines |

---

## Merged Upstream Open-Source Pull Requests (12 Code PRs · 6 US/EU Teams)

External engineering teams across **TypeScript, Python, and Rust** production SDKs and developer tools reviewed, tested, and merged these bug and security fixes upstream:

| Repository | Stack | PR | Scope Reviewed & Merged Upstream |
| :--- | :--- | :--- | :--- |
| `upstash/qstash-js` | TypeScript | [#296](https://github.com/upstash/qstash-js/pull/296) | Rejected empty request URLs and missing body claims during JWT webhook signature verification (merged by `@CahidArda`) |
| `upstash/qstash-py` | Python | [#61](https://github.com/upstash/qstash-py/pull/61) | Rejected empty URLs and non-string body claims in QStash signature verification (merged by `@CahidArda`) |
| `upstash/vector-js` | TypeScript | [#76](https://github.com/upstash/vector-js/pull/76) | Prevented mutating caller `fetch` options when reading vector namespace headers (merged by `@CahidArda`) |
| `upstash/vector-py` | Python | [#53](https://github.com/upstash/vector-py/pull/53) | Rejected mixed vector and data queries regardless of batch order (merged by `@CahidArda`) |
| `resend/resend-rust` | Rust | [#148](https://github.com/resend/resend-rust/pull/148) | Percent-encoded event identifiers safely in request paths (merged by `@AntoniosBarotsis`) |
| `restatedev/sdk-typescript` | TypeScript | [#814](https://github.com/restatedev/sdk-typescript/pull/814) | Forwarded per-call headers in `doWorkflowHandleCall` across durable ingress calls (merged by `@slinkydeveloper`) |
| `restatedev/sdk-typescript` | TypeScript | [#810](https://github.com/restatedev/sdk-typescript/pull/810) | Preserved `RestateError.code` across `RetryableError.from()` & `PauseError.from()` (approved by `@slinkydeveloper`) |
| `checkly/checkly-cli` | TypeScript | [#1574](https://github.com/checkly/checkly-cli/pull/1574) | Prevented empty inline `-c=` / `--config=` CLI flag from consuming positional arguments (reviewed by `@sorccu`) |
| `checkly/checkly-cli` | TypeScript | [#1566](https://github.com/checkly/checkly-cli/pull/1566) | Included retry counts for unfinished checks on `--max-failures` reporter exits (reviewed by `@sorccu`) |
| `openstatusHQ/openstatus` | TypeScript | [#3003](https://github.com/openstatusHQ/openstatus/pull/3003) | Ordered status page incident reports by latest update in `getLight` + Vitest suite (reviewed by `@mxkaske`) |
| `openstatusHQ/openstatus` | TypeScript | [#2988](https://github.com/openstatusHQ/openstatus/pull/2988) | Sorted synthetic timing phases chronologically in `mapTimingPhases` + Vitest coverage (reviewed by `@mxkaske`) |
| `jitsucom/jitsu` | TypeScript | [#1592](https://github.com/jitsucom/jitsu/pull/1592) | Accepted `objectMappings` cleanly in `prepareSource` RETL mirror preflight (approved by `@absorbb`) |

*(Plus 67 open Cloud & Go PRs in active review across `grafana/dskit#1181`, `ClickHouse/ch-go#1245`, `temporalio/sdk-go#2923`, `livekit/sip#1004`, `netbirdio/kubernetes-operator#540`, `tailscale/tailscale#22593`, `aquasecurity/trivy#11719`, and `SigNoz/signoz#13255`.)*

---

## Public Systems & Concurrency Repositories

| Repository | What It Solves (Plain English) | Technical Architecture & Live CI |
| :--- | :--- | :--- |
| **[`Sneaker-Drop-System`](https://github.com/shafiktanbir/Sneaker-Drop-System)** | Prevents two customers from buying the exact same item/slot during flash-sale spikes | Go gateway, atomic Redis Lua (`EVALSHA` 60s TTL), WebSockets · [![Go Engine CI](https://github.com/shafiktanbir/Sneaker-Drop-System/actions/workflows/ci.yml/badge.svg)](https://github.com/shafiktanbir/Sneaker-Drop-System/actions/workflows/ci.yml) |
| **[`rust-ecommerce-backend`](https://github.com/shafiktanbir/rust-ecommerce-backend)** | Processes high-volume orders and stock updates safely without double-selling | Rust, Axum 0.7, Tokio, SQLx `FOR UPDATE`, `cargo-chef` (**4,665 RPS / 28.4ms P95** on Hetzner) · [![Rust CI](https://github.com/shafiktanbir/rust-ecommerce-backend/actions/workflows/ci.yml/badge.svg)](https://github.com/shafiktanbir/rust-ecommerce-backend/actions/workflows/ci.yml) |
| **[`K8s-Infra-Hardening`](https://github.com/shafiktanbir/K8s-Infra-Hardening)** | Rolls out new releases gradually and blocks misconfigured workloads before downtime | Helm, Argo Rollouts canary, Kyverno non-root policies, Trivy, Go Pod CLI · [![K8s Hardening CI](https://github.com/shafiktanbir/K8s-Infra-Hardening/actions/workflows/ci-cd-k8s.yml/badge.svg)](https://github.com/shafiktanbir/K8s-Infra-Hardening/actions/workflows/ci-cd-k8s.yml) |
| **[`rabbitmq-event-driven-architecture`](https://github.com/shafiktanbir/rabbitmq-event-driven-architecture)** | Guarantees background emails/webhooks retry reliably and never drop silently | Node.js/TypeScript, RabbitMQ DLX (`10s -> 60s -> DLQ`), confirms, LRU (`26/26` tests) · [![RabbitMQ CI](https://github.com/shafiktanbir/rabbitmq-event-driven-architecture/actions/workflows/ci.yml/badge.svg)](https://github.com/shafiktanbir/rabbitmq-event-driven-architecture/actions/workflows/ci.yml) |
| **[`node-microservices-blueprint`](https://github.com/shafiktanbir/node-microservices-blueprint)** | Keeps independent user, task & notification services isolated during restarts | TypeScript, Node.js, RabbitMQ ECST, Zod, isolated MongoDBs (`48/48` tests) · [![Microservices CI](https://github.com/shafiktanbir/node-microservices-blueprint/actions/workflows/ci.yml/badge.svg)](https://github.com/shafiktanbir/node-microservices-blueprint/actions/workflows/ci.yml) |

---

## Core Technical Stack & Certifications

- **Languages & Runtimes:** Node.js, TypeScript, Go (Golang), Python (FastAPI / Django), Rust (Axum / Tokio)
- **Databases & Caching:** PostgreSQL (`Row-Level Security (RLS)`, `EXPLAIN (ANALYZE, BUFFERS)`, Composite/Partial B-Tree Indexes, `PgBouncer`, `TOAST`), Redis (`Cache-Aside`, Lua `EVALSHA`, Pub/Sub), MongoDB, RabbitMQ
- **Security, Privacy & Compliance:** HIPAA & PIPEDA Controls, SOC 2 / GDPR-Ready Multi-Tenant Isolation, SHA-256 Immutable Audit Logs, HL7 v3 eClaims, FusionAuth SSO, OAuth2/JWT (`HttpOnly`), Dynamic RBAC, Kyverno, Kubernetes NetworkPolicies, Trivy, WireGuard
- **Cloud, Containers & GitOps:** Docker, Kubernetes (`K3s` / `EKS`), Helm, ArgoCD GitOps, Argo Rollouts, Ansible, Ubuntu Server, AWS, GitHub Actions
- **Verified 2026 Credentials:** Canonical Ubuntu Linux · Docker Foundations · PagerDuty DevOps ([Verify on shafiktanbir.com](https://shafiktanbir.com/?tab=experience))

---

## Work With Me — Remote Teams & Startup Founders

- **Full-Time Remote Engineering Roles:** Backend, Software (`Node.js` / `Go`), Platform, DevOps & Infrastructure roles (including HealthTech, FinTech, and regulated SaaS) via Deel / Remote.com EOR or direct B2B.
- **Non-Technical & Startup Founders (Direct B2B):** Building a SaaS product or fixing slow/failing production infrastructure without an in-house CTO? Reach out in plain English via [`shafiktanbir.com/book`](https://shafiktanbir.com/book) or `shafiktanbir@gmail.com`.
