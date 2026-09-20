# Arthur Mulunda

Software engineer in Nairobi, Kenya. Third-year Computer Science diploma student graduating November 2027. I'm aiming for backend and AI engineering roles.

I like to understand how a system works before I write code: schema design, data flow, and what happens when something fails.

---

## Projects

### Job Card System (completed)

A full-stack field service management platform, built solo during my internship at Copycat Group to replace paper-based job tracking for technician dispatch.

- Job lifecycle from assignment to completion, with priorities, completion reports, customer signature capture, and PDF reports
- Role-based access for supervisors and technicians, with JWT in HTTP-only cookies
- Payments through M-Pesa STK Push (Daraja API) and Paystack hosted checkout, with payment status tracked per job
- Email notifications and customer invoices with payment links (Nodemailer)
- Separate Python/FastAPI monitoring service that streams Docker container health, host CPU, memory and disk, backend response times, and an activity feed over WebSockets
- I learned Python by building that monitoring service

**Stack:** React, Vite, Tailwind CSS, Node.js, Express, PostgreSQL, Python, FastAPI, Docker, Nginx
**Repo:** [JobCardSystem](https://github.com/arthurmchege/JobCardSystem)

### Nexus (completed)

An uptime and health monitoring platform. I built it because my own projects kept crashing and I only found out after the fact.

- Scheduler claims due monitors with PostgreSQL row locking, so multiple instances don't double-schedule
- Redis-backed job queue with workers and bounded retries
- Check results stored in time-partitioned PostgreSQL tables
- Incident detection with consecutive-failure thresholds, deduplicated webhook alerts, and at-least-once delivery
- Multi-user auth (bcrypt, JWT in httpOnly cookies) and Redis rate limiting that fails closed
- Structured JSON logs, request ID propagation, and a health metrics endpoint
- Read-only public demo mode
- The README documents its scope limits, including that DB claim and Redis enqueue are not one atomic transaction

**Stack:** FastAPI, SQLAlchemy 2.0, PostgreSQL 16, Redis 7, Next.js 14, Docker Compose, Caddy
**Repo:** [Nexus](https://github.com/arthurmchege/nexus)

### AttachIQ (MVP complete, full build in progress)

An AI-agent platform for industrial attachment assessment at Kenyan TVET institutions under the CBET framework. Workplace supervisors are asked to rate students against competency criteria they have usually never seen, and the rating step is not tied to the evidence the student submitted. AttachIQ adds an agent that walks the supervisor through it.

**Working in the MVP**
- SupervisorIQ, an agent built on Google ADK and Gemini that calls tools against the real PostgreSQL database
- It pulls the student's profile, pending competency units, and submitted evidence, asks targeted follow-up questions, drafts a score and comments, and writes the assessment once the supervisor confirms
- Responses streamed over SSE with a manual fetch and ReadableStream, so the JWT stays out of the URL
- JWT auth with a role gate on the agent endpoint, student evidence upload, and a 7-table schema seeded with demo data

**In progress**
- Reworking the schema and role model for production
- Institution registration and admin approval flow

**Planned:** StudentIQ, CoordIQ, an orchestrator agent, coordinator and admin portals, cloud file storage, refresh token rotation, an automated test suite, CI/CD, and deployment.

A working demo is targeted for KINAP's 6th International Research Conference in October 2026.

**Stack:** Next.js, TypeScript, Tailwind CSS, shadcn/ui, FastAPI, async SQLAlchemy, PostgreSQL, Google ADK, Gemini API
**Repo:** [AttachIQ](https://github.com/arthurmchege/AttachIQ)


---

## Tech

**Languages:** TypeScript, JavaScript, Python, SQL
**Backend:** Node.js, Express, FastAPI, SQLAlchemy 2.0, Pydantic
**Frontend:** React, Next.js, Tailwind CSS, shadcn/ui
**Data and messaging:** PostgreSQL, Redis, BullMQ, WebSockets
**AI:** Google Agent Development Kit, Gemini API
**Infrastructure:** Docker, Docker Compose, Nginx, Caddy
**Integrations:** M-Pesa Daraja API, Paystack
**Tools:** Git, Postman, Linux

---

## Contact
**Arthur Mulunda**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](http://www.linkedin.com/in/arthur-chege-b4a216375)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/arthurmchege)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:arthurmulunda941@gmail.com)
