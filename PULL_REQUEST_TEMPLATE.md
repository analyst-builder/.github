# Part A: Overview (for everyone)

## 1. Summary (required)
<!-- Explain it so someone outside the team understands it in 30 seconds. -->
**What changed:**
**Why:** <!-- the user problem or business reason -->
**Who is affected:** <!-- e.g. all premium users, admins only, no user-visible change -->
**GitHub issue:** <!-- e.g. "Closes #123", which closes the issue when this PR merges -->
**Related issues:** <!-- e.g. #124, #125; other repo: analyst-builder/<repo>#45 -->
**Design doc:** <!-- link, or "none" -->

**Type of change:**
- [ ] New feature
- [ ] Change to existing feature
- [ ] Bug fix
- [ ] Refactor (no behaviour change)
- [ ] Documentation update
- [ ] Chore
- [ ] Other (please specify):

## 2. Where to see it (required)
- **Apps affected:** <!-- front / admin / api -->
- **Preview URL(s):**
- **Branch:**
- **Figma:** <!-- link to the exact frame, or "none" -->
- **Feature flag / config needed:** <!-- name and how to turn it on, or "none" -->
- **Depends on:** <!-- other PRs that must be merged first (e.g. API PR), or "none" -->

---

# Part B: Technical details (for code reviewers)

## 3. How it works (required)
<!-- A short explanation of the approach. Point reviewers to the files that matter most. -->
- **Approach:**
- **Key files to review:**
- **Alternatives considered and why not:** <!-- optional -->

## 4. API and data changes (if any)
| Method | Endpoint | Who can call it | Main status codes | New or changed? |
|---|---|---|---|---|
| | | | | |

- **Database changes:** <!-- tables/fields added or changed, migrations, backfills -->
- **New environment variables or secrets:**
- **New dependencies:** <!-- package and why it was needed -->

## 5. Breaking changes and compatibility
- [ ] No breaking changes
- [ ] Breaking change: <!-- what breaks, for whom (frontend, admin, mobile, integrations), and the migration path -->

## 6. Security, performance and accessibility notes
<!-- Anything a reviewer should look at closely. Write "none" if nothing applies. -->
- **Security:** <!-- auth/permission checks, user input handling, file uploads, data exposure -->
- **Performance:** <!-- new queries, large lists, heavy components, caching -->
- **Accessibility:** <!-- keyboard use, labels, contrast -->

---

# Part C: Behaviour and testing (for QA)

## 7. Who can do what (required)
<!-- Fill every row. "Same as before" is a valid answer. QA tests every role, so a missing row becomes a guess. -->
| Role | Can see it? | Can use it? | Limits or differences |
|---|---|---|---|
| Logged out | | | |
| Free member | | | |
| Premium | | | |
| Admin | | | |

## 8. Expected behaviour (required)
<!-- The most important section for QA. One line per behaviour, written so a tester can check it.
     Include what happens on success AND when something goes wrong.
     Example: "Given a premium user with 5 notebooks, when they create a 6th, then it is created and shown first in the list."
     Example: "Given a free user, when they open Notes, then they see the upgrade prompt and cannot create a notebook." -->
1. Given … when … then …
2.
3.

## 9. Rules and limits (required if the feature has inputs, quotas or lists)
<!-- These become boundary tests. Exact numbers, please. -->
- **Fields and validation:** <!-- field: required? min/max length, allowed characters/format, default value -->
- **Exact error / success messages:** <!-- copy the strings, or point to the i18n keys -->
- **Quotas per tier:** <!-- e.g. free: 3 per day, premium: unlimited; when does the counter reset? -->
- **Lists:** <!-- sort order, page size, what the empty state says -->
- **Files:** <!-- allowed types, max size, checked on the server or only in the browser? -->

## 10. Out of scope and known gaps (required)
<!-- What is NOT done yet, or deliberately left out. Nobody will report these as bugs. -->
-

## 11. Test data and side effects
- **Test data needed:** <!-- e.g. "user with at least 1 completed course"; how to create it on staging -->
- **Can it be undone or deleted?** <!-- how QA can clean up what tests create -->
- **Side effects:** <!-- emails, notifications, payments, AI credits, third-party calls -->

## 12. Risk and regression
- **Other pages or features that share this code:**
- **Anything you're unsure about:**

## 13. How to try it
<!-- Shortest path to see the feature working. -->
1.

---

# Part D: Release

## 14. Deployment and rollback
- **Deploy order or steps:** <!-- e.g. API before frontend, run migration first, turn on flag after deploy -->
- **How to roll back:** <!-- revert is enough / flag off / migration needs reversing -->
- **Monitoring:** <!-- logs, alerts or metrics to watch after release -->

## 15. Author checklist
- [ ] Locally tested
- [ ] Tested on the preview
- [ ] Unit / integration tests added or updated
- [ ] Interactive elements have accessible names (button text, `aria-label`, or a `<label>`)
- [ ] Repeated items (cards, rows, list entries) have a `data-testid`, e.g. `data-testid="experience-card"`
- [ ] Loading and error states are visible in the UI
- [ ] No secrets, test accounts or debug code left in
- [ ] Docs or help text updated, if needed
- [ ] Ready for QA
