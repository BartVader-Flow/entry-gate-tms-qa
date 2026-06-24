# Entry Gate Slides — Speaker Notes (Draft)

**Audience:** QA Leads (Emre, Irem, Fadil, James, …)  
**Purpose:** Collect feedback before wider rollout (Confluence / other stakeholders)  
**Files:** `entry-gate-slides-draft.html` (3 screens: cover + EG-1 + EG-2)  
**Standalone:** No external strategy deck required — everything needed is in this file.

---

## Cover

**Say (short):** Two-slide draft for us — EG-1 roles/RACI, EG-2 gates. Left panel = problem; right panel = what’s inside.

**Ask leads:** Does the “Why we need this” list match your squads?

---

## RACI — explain in plain language (use on EG-1)

If someone is unsure what RACI means, use this:

| Letter | Word | Plain English |
|--------|------|----------------|
| **R** | Responsible | **Does the work** — executes the task (can be shared). |
| **A** | Accountable | **Owns the outcome** — one role answers if it goes wrong; approves when done. |
| **C** | Consulted | **Ask before acting** — two-way input (e.g. BA asks QA about testability). |
| **I** | Informed | **Tell after** — one-way update, no decision needed. |

**Example for the room:**  
“BA is **R** for writing positive test cases. PO is **A** for the story being ready for sprint. QA is **R** for running tests and **C** while BA drafts cases. Dev is **I** when test results affect their fix.”

**Common confusion:**  
- **A** is not “the boss who does everything” — it is **one neck to choke** for that deliverable.  
- **R** and **A** can sit on different roles (BA does the writing, PO owns sprint readiness).

---

## EG-1 — Feature lifecycle: who owns what

### Key message

- Step 2 (Test) is where QA is strongest — but steps 1 and prerequisites are owned elsewhere.
- The problem is not “QA refuses to test” — it is “work enters step 2 without step 1 being done.”

### Walk through RACI table

| Row | Discussion point for leads |
|-----|---------------------------|
| Story & AC | Where do we still see QA doing BA work? Which Jira states would enforce BA R? |
| Positive cases | Target: BA R for happy path, QA R for negative/edge. Realistic in your modules? |
| Unit / API | What is actually enforced in CI today vs aspirational? |
| Playwright | Squad QA extends existing suites — confirm this matches New track expectations |
| Golden Data | Is TO/Core clearly engaged before sprint commitment? |

### As-is → Target (stakeholder data)

**As-is:** QA chases missing specs and business rules.  
**Target:** BA delivers; QA validates at Gate 0; incomplete stories go back to BA (not absorbed by QA).

**Ask leads:**

1. Is “return to BA” workable in your squads, or do we need a softer “conditional start” first?
2. What minimum checklist for Gate 0 can you sign off per module (5–8 bullets)?

---

## EG-2 — When QA starts: entry gates

**Layout:** 2×2 grid — each gate has a **central checklist** (large rows, not tiny tags).

**Gate 0 (6 items — ask leads which are mandatory):**
- Jira story in sprint & linked epic
- AC complete · Spec linked · BA happy-path
- Module, env, provisioner known

**Gate 1:** negative & edge cases, error messages, …  
**Gate 2:** Dev unit tests passing, feature deployed to SD-TEST, …  
**Gate 3 added:** Golden Data updated, defects triaged

**Ask leads:** Which Gate 0 rows are must-have vs nice-to-have for your modules?

---

## Feedback we need from QA Leads

Please reply with:

1. **RACI:** Is the 4-letter explainer on EG-1 clear enough, or do we need a separate cheat-sheet slide?
2. **EG-1:** Anything wrong or missing in the RACI rows?
3. **Gate 0:** Your proposed 5–8 bullet checklist (module-specific examples welcome).
4. **Reject workflow:** Jira status / who clicks “return to BA”?
5. **Core vs Squad:** Confirm Golden Data team exempt from squad allocation.
6. **Wording:** Any term that will confuse Dev/BA/PO if we show this upward later?

---

## Optional next artifacts (out of scope for this draft)

- Gate 0 Jira checklist (custom field or template)
- Module game plan one-pager
- Confluence page under QA space
