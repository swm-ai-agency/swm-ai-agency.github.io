<!-- BEGIN SWM SHARED ENGINEERING -->
<!-- Generated from swm-ai-agency/swm-ai-native-marketing-agency docs/ENGINEERING-BASELINE.md; edit the source, then regenerate. -->
<!-- Source SHA-256: 23d673b6b165a901489c3e240ec39894c78eb57edda740d845c38bc2519693d7 -->

# Shared engineering baseline

This is SWM's shared engineering guidance. Repository-specific architecture,
data, approval and deployment rules still apply. A conflict is a reason to
identify the conflicting sources and resolve it before dependent work.

- **Fix the cause.** Trace a reported failure from its trigger through the
  authoritative state and execution path. Separate verified facts from guesses.
  Reproduce it with a safe failing case before changing behavior when feasible;
  otherwise state the missing evidence. A disappearing symptom is insufficient.
- **Choose the smallest durable change.** Compare repairing the existing path,
  simplifying it and replacing it. Prefer one clear owner and source of truth.
  Avoid another fallback, retry layer, cache or service unless a demonstrated
  failure requires it. Do not turn every bug into a redesign.
- **Keep one coherent path.** Find other callers and competing implementations.
  Reuse the canonical contract rather than copying business rules. When a
  migration needs two paths, name the active path, cutover, rollback and old-path
  removal condition; never imply that both may own the same work.
- **Design recovery with execution.** Where relevant, verify partial failure,
  duplicate delivery, concurrency, timeout, restart and uncertain outcomes.
  Persist responsibility before irreversible work; a timeout does not prove
  external work stopped. Bound retries and resource use without replaying an
  uncertain action. Preserve authorization and tenant boundaries.
- **Make the next failure diagnosable.** Use existing logs, metrics and traces
  to show which stage failed, when useful work last completed, and what recovery
  is safe. Add the smallest missing signal at the failing boundary. A running
  process or successful request is not proof that the business job completed.
  Keep sensitive content out of telemetry; avoid unbounded labels and alerts.
- **Prove the outcome.** Exercise the real affected path with synthetic or
  otherwise permitted data. Add a regression that would detect the original
  failure and relevant recovery errors. Run focused checks before the applicable
  repository gates. Distinguish source, tested, merged, deployed and activated.
- **Spend verification resources deliberately.** Run focused local checks first
  when the machine and dependencies can support them. Combine related changes
  into one reviewable candidate before full hosted CI where repository gates
  permit; avoid repeating full suites for every intermediate edit. Documentation
  changes need the applicable documentation checks, not unrelated application
  suites. Cancel redundant runs only when replacement coverage preserves the
  required checks. Rerun for changed behavior, failures or unresolved risks;
  budget savings never justify omitting required tests, review or release gates.
- **Keep agent context small.** Root instructions contain invariants, commands
  and a task-to-source map; load relevant sections, not whole linked documents
  or archives. Use descriptive headings and one authoritative home per rule.
  Target at most 600 words for this shared block and 2,000 for each root entry
  including it; keep handoffs to current state, evidence, next step and limits.
  Split growing detail into linked task guides or records. These are maintenance
  targets, never permission to omit applicable safety rules or silently truncate
  required context. Name an overrun and its next simplification instead.
- **Leave less to maintain.** Remove superseded code and instructions within
  the verified scope, preserve unrelated work, and update the authoritative
  explanation when behavior changes. State remaining limitations and the next
  concrete step. A new warning or dashboard alone does not repair a backend
  failure.
<!-- END SWM SHARED ENGINEERING -->

# Repository scope

This is SWM's static public policy site. Start with index.html for navigation,
privacy.html and terms.html for the published policy pages, and style.css for
shared styling. Preserve .nojekyll. This is separate from the agency marketing
website in swm-website and from Creator Ops and its employee portal.

There is no application backend or package build in this repository. For page
changes, inspect HTML, local links and the affected desktop and phone layouts.
Do not run deployment commands or submit live forms as a verification step.

Keep private company policy, customer data, credentials and internal evidence
out of this public repository. A code or documentation edit does not authorize
a policy commitment, domain/hosting change, production publication, new service
or message. Preserve unrelated work and report source checks separately from
the state of the public website.
