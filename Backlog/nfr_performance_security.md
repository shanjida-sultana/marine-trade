\# Product Backlog: Non-Functional Requirements (NFR)



This backlog documents the official Non-Functional Requirements (NFR) and their exact acceptance criteria for the MarineTrade application.



\---



\## \[NFR-01] Page Load Time

\* \*\*Description:\*\* All pages must fully load within 3 seconds under normal network conditions (>=10 Mbps).

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should load pages within 3 seconds on a standard connection.

&#x20; \* The system should load pages within 6 seconds on a 3G connection.

&#x20; \* The system should maintain a Lighthouse performance score of 80 or higher.



\## \[NFR-02] API Response Time

\* \*\*Description:\*\* All API endpoints must respond within 500ms for read operations and 1000ms for write operations.

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should keep P95 read latency below 500ms.

&#x20; \* The system should keep P95 write latency below 1 second.

&#x20; \* The system should monitor latency metrics through an APM tool.



\## \[NFR-03] Concurrent Users

\* \*\*Description:\*\* The platform must support at least 5,000 simultaneous users without degradation in response time.

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should handle 5,000 concurrent users successfully during load testing.

&#x20; \* The system should keep CPU utilization below 70% at peak load.

&#x20; \* The system should ensure that timeout errors do not occur during stress testing.



\## \[NFR-04] Document Generation Speed

\* \*\*Description:\*\* Trade documents (invoices, permits, BoL) must be generated and available for download within 5 seconds.

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should generate PDF files within 5 seconds.

&#x20; \* The system should not permit partial PDF generation.

&#x20; \* The system should display an error message if PDF generation exceeds 10 seconds.



\## \[NFR-05] Horizontal Scalability

\* \*\*Description:\*\* The system architecture must support adding server instances to handle traffic spikes during peak trade seasons.

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should activate auto-scaling when CPU usage reaches 70%.

&#x20; \* The system should ensure new server instances become available within 2 minutes.

&#x20; \* The system should ensure zero downtime during scale-out operations.



\## \[NFR-06] Database Scalability

\* \*\*Description:\*\* The database must handle growth beyond 10 million records without performance degradation.

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should keep query execution time below 200ms with 10 million database rows.

&#x20; \* The system should support read replicas in the database architecture.

&#x20; \* The system should maintain a documented sharding strategy.



\## \[NFR-07] File Storage Scalability

\* \*\*Description:\*\* Document and image storage must scale to accommodate growing volumes of trade documents and product photos.

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should automatically expand storage capacity when required.

&#x20; \* The system should handle file delivery through a CDN.

&#x20; \* The system should not impose storage limits below 10TB.



\## \[NFR-08] Data Encryption

\* \*\*Description:\*\* All sensitive data — credentials, payment info, trade documents — must be encrypted at rest (AES-256) and in transit (TLS 1.2+).

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should enforce TLS 1.2 or higher across all endpoints.

&#x20; \* The system should verify database encryption during security audits.

&#x20; \* The system should ensure that plain-text secrets do not appear in application logs.



\## \[NFR-09] Role-Based Access Control (RBAC)

\* \*\*Description:\*\* Each user role must access only permitted features; cross-role data must never be exposed.

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should enforce RBAC at the API layer.

&#x20; \* The system should ensure that privilege escalation vulnerabilities do not exist according to penetration testing.

&#x20; \* The system should maintain a properly documented access control matrix.



\## \[NFR-10] OTP \& Email Verification

\* \*\*Description:\*\* All registrations and password resets must require OTP or email link verification.

\* \*\*Acceptance Criteria:\*\*

&#x20; \* The system should set OTP validity to expire after 10 minutes.

&#x20; \* The system should limit OTP resend attempts to three.

&#x20; \* The system should keep unverified accounts inactive until verification is completed.



\---

\*\*Document Status:\*\* Approved \& Merged into Backlog

\*\*Assigned Owner:\*\* Sharmin Akter Aziza

