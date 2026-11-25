# AURUM Money Services: Ledger System

> **Client project** · Built by [Rahimi Tech Solution](https://github.com/AbdulRahmanRahimi) · The source code is private to the client · Status: in development

A ledger system for **AURUM Afghanistan Mobile Money Services Company**. It replaces separate Excel workbooks for each depositor and currency with one auditable, **append-only ledger**.

## Design principles

- **Money is stored as whole minor units** (`BIGINT`), never as floating point
- **Balances are derived** from the ledger and never stored
- **Append-only**: entries are never edited or deleted, and corrections are reversals
- **Currencies never mix**: AFN and USD never appear in the same total
- Negative balances are allowed by design, because depositors can owe money

## Built so far

- Ledger core: schema, triggers, Row Level Security, posting functions and an automated test suite
- Planned modules: Excel importer, accounts, entry screens, MoneyGram, vouchers, cash count, reports and administration

## Tech stack

| Layer | Tools |
|---|---|
| Frontend | React, TypeScript, Vite |
| Backend | Supabase: PostgreSQL, triggers, RPC functions, Row Level Security |
| Testing | pgTAP / Vitest |
| Hosting | Vercel |

---

Designed and built by **Abdul Rahman Rahimi**.
