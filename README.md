# Shafikul Islam (Shafik Tanbir)

**Backend, Platform & Cloud Infrastructure Engineer** · Node.js · TypeScript · Go · PostgreSQL · Kubernetes · HIPAA/PIPEDA  
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

## Merged Upstream Open-Source Pull Requests (6 Merged)

External engineering teams at US and European developer-tool companies reviewed, tested, and merged these bug fixes into their production repositories:

| Repository | PR | Scope Reviewed & Merged Upstream |
| :--- | :--- | :--- |
| `checkly/checkly-cli` | [#1574](https://github.com/checkly/checkly-cli/pull/1574) | Prevented empty inline `-c=` / `--config=` CLI flag from consuming positional arguments (reviewed by `@sorccu`) |
| `checkly/checkly-cli` | [#1566](https://github.com/checkly/checkly-cli/pull/1566) | Included retry counts for unfinished checks on `--max-failures` reporter exits (reviewed by `@sorccu`) |
| `restatedev/sdk-typescript` | [#810](https://github.com/restatedev/sdk-typescript/pull/810) | Preserved `RestateError.code` across `RetryableError.from()` & `PauseError.from()` (approved by `@slinkydeveloper`) |
| `openstatusHQ/openstatus` | [#3003](https://github.com/openstatusHQ/openstatus/pull/3003) | Ordered status page incident reports by latest update in `getLight` + Vitest suite (reviewed by `@mxkaske`) |
| `openstatusHQ/openstatus` | [#2988](https://github.com/openstatusHQ/openstatus/pull/2988) | Sorted synthetic timing phases chronologically in `mapTimingPhases` + Vitest coverage (reviewed by `@mxkaske`) |
| `jitsucom/jitsu` | [#1592](https://github.com/jitsucom/jitsu/pull/1592) | Accepted `objectMappings` cleanly in `prepareSource` RETL mirror preflight (approved by `@absorbb`) |

*(Also open & CLA-signed in active review: `restatedev/sdk-typescript#814`, `SigNoz/signoz#13255`, `Infisical/infisical#8881`, `calcom/cal.diy#30401`.)*

---

## Public Systems & Concurrency Repositories

| Repository | What It Solves (Plain English) | Technical Architecture & Verified Checks |
| :--- | :--- | :--- |
| **[`K8s-Infra-Hardening`](https://github.com/shafiktanbir/K8s-Infra-Hardening)** | Rolls out new releases gradually and blocks misconfigured workloads before downtime | Helm, Argo Rollouts canary + `AnalysisTemplate`, Kyverno policies, Go Pod Hygiene CLI (`go test` + `helm lint` CI green) |
| **[`Sneaker-Drop-System`](https://github.com/shafiktanbir/Sneaker-Drop-System)** | Prevents two customers from buying the exact same item/slot during flash-sale spikes | Go gateway, atomic Redis Lua (`EVALSHA` 60s TTL), WebSocket fan-out (`go test -race` + 2k-VU k6 suite) |
| **[`rust-ecommerce-backend`](https://github.com/shafiktanbir/rust-ecommerce-backend)** | Processes high-volume orders and stock updates safely without double-selling | Rust, Axum 0.7, Tokio, SQLx `FOR UPDATE` locking, multi-stage `cargo-chef` Docker (**4,665 RPS / 28.4ms P95** across 307k 4-node Hetzner requests) |
| **[`rabbitmq-event-driven-architecture`](https://github.com/shafiktanbir/rabbitmq-event-driven-architecture)** | Guarantees background emails/webhooks retry reliably and never drop silently | Node.js/TypeScript, RabbitMQ progressive DLX retries (`10s -> 60s -> DLQ`), publisher confirms, LRU dedup (`26/26` tests) |
| **[`node-microservices-blueprint`](https://github.com/shafiktanbir/node-microservices-blueprint)** | Keeps independent user, task & notification services isolated during restarts | TypeScript, Node.js, RabbitMQ Event-Carried State Transfer, Zod validation, isolated MongoDBs (`48/48` Jest tests) |

---

## Core Technical Stack & Certifications

- **Languages & Runtimes:** Node.js, TypeScript, Go (Golang), Python (FastAPI / Django), Rust (Axum / Tokio)
- **Databases & Caching:** PostgreSQL (`Row-Level Security (RLS)`, `EXPLAIN (ANALYZE, BUFFERS)`, Composite/Partial B-Tree Indexes, `PgBouncer`, `TOAST`), Redis (`Cache-Aside`, Lua `EVALSHA`, Pub/Sub), MongoDB, RabbitMQ
- **Security, Privacy & Compliance:** HIPAA & PIPEDA Controls, SOC 2 / GDPR-Ready Multi-Tenant Isolation, SHA-256 Immutable Audit Logs, HL7 v3 eClaims, FusionAuth SSO, OAuth2/JWT (`HttpOnly`), Dynamic RBAC, Kyverno, Kubernetes NetworkPolicies, Trivy, WireGuard
- **Cloud, Containers & GitOps:** Docker, Kubernetes (`K3s` / `EKS`), Helm, ArgoCD GitOps, Argo Rollouts, Ansible, Ubuntu Server, AWS, GitHub Actions
- **Verified 2026 Credentials:** Canonical Ubuntu Linux · Docker Foundations · PagerDuty DevOps ([Verify on shafiktanbir.com](https://shafiktanbir.com/?tab=experience))
