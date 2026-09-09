# Vandelay Industries: Archstone DMS Renewal

**Workshop folder for "Architect Your AI Work: A Bring Your Own Harness Session" (RLLB 2026)**

Everything in this folder is fictional. Vandelay Industries, Archstone Software, Hooli, Pied Piper, Northstar, and every person, price, invoice, and survey response were invented for this workshop. Character names are used with affection. Nothing here describes a real company, product, or contract.

## The situation

You lead legal operations at Vandelay Industries, a 22,000-employee industrial company with a 230-person Legal Department headquartered in New York, with people in six US cities and in London, Dublin, Singapore, and Mexico City.

Your document management system, Archstone DMS, is coming to the end of a three-year term on **February 28, 2027**. You thought you had until the end of the year to decide what to do. Last week your legal technology manager found the current notice provision buried in the second amendment: it is 120 days, not the 60 everyone remembered. Notice of non-renewal has to be delivered by **October 31, 2026**. Today is **September 9**. You have 52 days.

Archstone's renewal proposal arrived two weeks ago: an 18 percent price increase, "AI included," and a loyalty-pricing deadline of October 15. Finance wants the legal technology budget flat. IT is pushing every department onto the Hooli Workspace suite. The paralegals live in this system and the General Counsel has said not to break litigation.

You need to pull every fact Vandelay has about this relationship into one place, fast, and decide: renew as proposed, renegotiate from documented leverage, or open a rapid RFI and make Archstone earn it. This folder is everything Vandelay knows about the last three years.

There is no single right answer. Someone who weights price will reach a different conclusion from someone who weights adoption, risk, service, or enterprise strategy. All of those conclusions are supportable from these files. The point of the session is how you get to yours.

## What is in the folder

```
01_Contracts/        The paper. Master agreement (2018) and three amendments (2021, 2024, 2025).
                     Amendments override the master. Read the newest first.
02_Standards/        Vandelay's Software Renewal Review Standards (LO-STD-014 v3.1): twelve
                     provisions and the position Vandelay expects on each, with a scorecard.
03_Vendor/           What Archstone sent you: the renewal proposal with Order Form No. 4 and the
                     Insight AI terms (Schedule C); the Q2 2026 Customer Success Review; the most
                     recent SOC 2 bridge letter (Feb 2025); the ISO 27001 certificate (expired).
04_Finance/          30 monthly invoices (Mar 2024 to Aug 2026) and the license export (240 seats).
05_Usage_and_Adoption/  Per-user monthly usage telemetry (30 months), the LMS training export
                     since the 2024 relaunch, and the anonymous July 2026 pulse survey (158 responses).
06_Service/          1,508 support tickets with response and resolution times, monthly availability
                     as measured by Vandelay, and the incident log.
07_Market/           Northstar market brief (Q3 2026), the 60-department peer poll, and overviews
                     from Hooli Docs and Pied Piper Vault.
08_Internal/         The department roster (join key for everything), the integration inventory,
                     the 2018 selection memo (what Archstone promised), and the September 4 kickoff
                     notes (what Finance, IT, Procurement, Privacy, Security, and the GC each want).
09_Templates/        Procurement's rapid RFI template, for Option B.
PROMPTS.md           Every prompt used in the session, by module, ready to paste.
```

Structured data is provided as `.xlsx` (with summary sheets and notes) and, where large, as `.csv` for convenience. Documents are PDF.

## How the files connect

- `employee_id` (VL-1001 and up) links the roster to the license export, the usage telemetry, the training export, and the support tickets.
- `cohort_key` (practice group and level band) links all of those to the anonymous survey, which carries no individual identifiers.
- The survey's `tenure_band` (Under 2 years, 2 to 5, 5 to 10, 10+) is not a roster column; derive it from `hire_date` as of July 2026 if you want to compare.
- Cohorts with fewer than five survey responses are noise; the survey notes say so. Only about ten practice-group-by-level cohorts clear that bar, so roll up to level band or tenure band for a second cut.
- Former employees' licenses carry legacy `VL-0xxx` identifiers from the pre-2019 HR system, which is why they are not on the roster.
- Contract dates, seat counts, and rates in the invoices match the amendments. If they do not appear to, look again; that is the exercise.

## A few things to know

The files are realistic, which means imperfect. Invoices bill seats that belong to people who have left. The vendor's availability figure and Vandelay's do not agree, and both are "correct" under their own definitions. A professional services charge has no statement of work behind it. The survey is anonymous, so some joins only work at the cohort level. Real renewal folders look like this.

The documents are deliberately short for a workshop: the master agreement is 13 pages where a real one might be 40, and the exhibits are one page each. The architecture you build to work with them is identical to the one you would use on the real thing; only the token bill changes.

When your harness reads a PDF, ask it to preserve table layout (for example `pdftotext -layout`); plain extraction de-columnizes the tables in several of these documents.

If you would rather work against your own material in the second half of the session, use non-privileged or sanitized documents only. This is a conference room.

## Setup check

Point your harness at this folder and ask: *"How many files are in this folder, what types are they, and which one is the most recent amendment to the Archstone agreement?"* If you get a sensible answer, you are ready.

*Prepared by Harbor for RLLB 2026. Draft v1, September 9, 2026.*
