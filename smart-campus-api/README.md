# Enterprise Smart Campus REST API

An enterprise-grade, high-performance RESTful API engineered using **Java 17**, **JAX-RS (Jersey)**, and **Maven**. The platform provides a decentralized tracking architecture for monitoring real-time campus assets, hardware sensors, and time-series environmental readings.

The core engine is architected around robust multi-threaded synchronization patterns, advanced sub-resource navigation models, and custom interceptor pipelines to simulate industrial IoT workloads without framework overhead.

## 🛠️ Tech Stack & Advanced Topologies
* **Backend Core:** Java 17+ / JAX-RS (Jersey Core Framework) / Embedded Grizzly Server
* **Engineering Standards:** Arbitrary-Precision Thread Synchronization, Advanced Sub-Resource Routing Locators, Dynamic HATEOAS Micro-Gateways

## 📈 Core Business Value & Engineering Impact
* **Thread-Safe State Monitoring:** Bypasses framework configuration bottlenecks by maintaining state isolation using high-performance concurrent collections (`ConcurrentHashMap`), entirely eliminating multi-thread race conditions under intensive client workloads.
* **Fingerprint & Exploitation Defense:** Implements localized global `ExceptionMappers` to intercept runtime validation breaks. Suppresses native Java stack traces, layout structures, and dependency package fingerprints at the server boundary to enforce high-security data compliance.
* **Semantic Data Ingestion Pipelines:** Optimizes content routing protocols by combining early `@Consumes(MediaType.APPLICATION_JSON)` negotiation filters with diagnostic `422 Unprocessable Entity` status triggers to prevent relational data corruption.

## 📁 Core Relational Resource Contract

| Http Method | URI Pattern | Semantic Response | Operational Target |
| :--- | :--- | :--- | :--- |
| **GET** | `/api/v1` | `200 OK` | Self-Documenting Gateway Root (HATEOAS) |
| **POST** | `/api/v1/rooms` | `201 Created` | Ingests New Campus Facility Boundary |
| **GET** | `/api/v1/sensors` | `200 OK` | Queries Sensors (Supports optional `?type=` filters) |
| **POST** | `/api/v1/sensors` | `201 Created` / `422` | Provisions Sensor Resource to a Verified Facility |
| **POST** | `/api/v1/sensors/{id}/readings` | `201 Created` | Commits Time-Series Data Metric to Target Sensor |
| **DELETE**| `/api/v1/rooms/{id}` | `204 No Content` | Idempotent Facility Removal Sequence |

## 🌐 Live Interactive Demo
* To see the comprehensive application codebase, complete structural specifications, and execute local integration cURL scripts, explore the central standalone repository here: **[Smart Campus REST API Base Repository](https://github.com/SoheibKaddouri/smart-campus-api)**
