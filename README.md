## 🌐 Product Vision

### 1. **TeamPulse**

A SaaS platform for **remote and distributed teams** to measure and improve **employee well-being and productivity** through lightweight check-ins, dashboards, and actionable recommendations.

---

### 2. **Core Mission**

Help employees, managers, and organizations **stay healthy and productive in a remote-first world** by:

- Giving **employees** tools for reflection and self-awareness.
- Giving **managers** data-driven insights on team morale and productivity.
- Giving **organizations** anonymized trends to reduce burnout and improve retention.

---

### 3. **Primary Users & Needs**

1. **Employees (individual contributors)**
   - Need: A private, simple way to track mood, stress, and productivity.
   - Value: Gain self-awareness and personal progress insights.
2. **Managers / Team Leads**
   - Need: Visibility into team well-being and performance trends without micromanaging.
   - Value: Spot early burnout or disengagement signals and act quickly.
3. **HR / Admins**
   - Need: Anonymized organizational data to inform well-being programs.
   - Value: Drive retention and productivity at scale.

---

### 4. **Core Features (MVP Scope)**

#### For Employees

- Daily/weekly pulse surveys (mood, stress, productivity).
- Personal dashboard with historical trends (mood, stress, focus, productivity).
- Optional focus timer or productivity tracker to log deep work sessions.
- Private data control — employees see their own data, only anonymized data is shared upward.

#### For Managers

- Team dashboard with aggregated and anonymized scores.
- Trend analysis (stress/productivity over time, participation rates).
- Alerts when team metrics dip below thresholds or show burnout signals.
- Actionable recommendations (AI-powered or template-based) for improving well-being and productivity.

#### For Admins / SaaS Layer

- Multi-tenant org structure with separate organizations.
- Role-based access (employee, manager, admin).
- Org-level insights (company-wide anonymized trends).
- Program impact measurement (see if wellness initiatives correlate with improvements).
- Subscription tiers (free vs premium with advanced analytics and recommendations).

## 🏗️ **Tech Stack**

| Tech                  | Purpose                        |
| --------------------- | ------------------------------ |
| Nextjs                | Framework, Caching             |
| Tailwindcss           | CSS styling                    |
| Shadcn                | Ui library                     |
| Zustand               | State-management               |
| Zod                   | Data validator                 |
| Postgres              | Database                       |
| Prisma                | Database orm                   |
| Stripe                | Billing                        |
| OpenAi                | Ai recommendation integration  |
| Log                   | Winston                        |
| Sentry (on Glitchtip) | Error tracking                 |
| Playwright            | Unit test / end-to-end testing |
| NextAuth.js           | Authentication + RBAC          |

## 📂 Directory Structure

```
team-pulse/
│
├── app/                              # Next.js app directory
│   ├── api/                          # Route handlers (Edge/Node)
│   ├── favicon.ico                   # Site favicon
│   ├── global-error.tsx              # Global error boundary UI
│   ├── globals.css                   # Global styles (TailwindCSS)
│   ├── layout.tsx                    # Root layout for the app
│   └── page.tsx                      # Home page
│
├── commitlint.config.ts              # Conventional commit lint rules
├── components.json                   # shadcn/ui generator config
├── eslint.config.mjs                 # ESLint configuration
├── instrumentation-client.ts         # Client-side Sentry/Next instrumentation
├── instrumentation.ts                # Server/edge instrumentation entry
├── lib/
│   └── utils.ts                      # Shared utilities (e.g., className helpers)
├── next-env.d.ts                     # Next.js TypeScript ambient types
├── next.config.ts                    # Next.js configuration
├── node_modules/                     # Installed dependencies
├── package-lock.json                 # Exact dependency lockfile (npm)
├── package.json                      # Project metadata, scripts, deps
├── playwright.config.ts              # Playwright test configuration
├── postcss.config.mjs                # PostCSS/Tailwind pipeline config
├── README.md                         # Project documentation
├── sentry.edge.config.ts             # Sentry config for Edge runtime
├── sentry.server.config.ts           # Sentry config for Node/server runtime
├── tests/                            # Automated tests
└── tsconfig.json                     # TypeScript compiler options
```
