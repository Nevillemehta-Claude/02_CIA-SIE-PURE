# PAD-GHΩ — GITHUB RECERTIFICATION DIRECTIVE

**Execution-Focused · Adaptive · Outcome-Driven**

---

## CLASSIFICATION

| Attribute | Value |
|-----------|-------|
| **Directive Type** | Execution with Adaptive Authority |
| **Goal** | Recertification through demonstrated correctness |
| **Environment** | GitHub Actions (primary), with practical flexibility |
| **Evidence** | Required, format flexible |

---

## 1. OBJECTIVE

Achieve verified recertification across three scopes:

| Scope | Repository | Purpose |
|-------|------------|---------|
| **CIA-SIE-PURE** | `02_CIA-SIE-PURE` | Backend verification |
| **MCI Terminal** | `001_MCI_TERMINAL_EXTRACTION` | Frontend verification |
| **Integrated System** | Both | End-to-end verification |

**Success = Repeatable correctness with documented evidence.**

---

## 2. REPOSITORY REFERENCE

### CIA-SIE-PURE
```
/Users/nevillemehta/Downloads/02_CIA-SIE-PURE/
├── PROJECTS/CIA_SIE_PURE/
│   ├── .github/workflows/           ← Workflows
│   ├── 06_SOURCE_CODE/src/cia_sie/  ← Python source
│   ├── 07_TESTING/tests/            ← Tests
│   └── 00_GOVERNANCE/               ← Reports go here
└── GOVERNANCE/                      ← High-level attestations
```
**GitHub:** https://github.com/Nevillemehta-Claude/02_CIA-SIE-PURE

### MCI Terminal
```
/Users/nevillemehta/Downloads/001_MCI_TERMINAL_EXTRACTION/
├── PROJECTS/MCI_Terminal/
│   ├── 12_APPLICATION_CODE/
│   │   ├── .github/workflows/       ← Workflows
│   │   └── src/                     ← TypeScript source
│   └── 00_GOVERNANCE/               ← Reports go here
└── GOVERNANCE/                      ← High-level attestations
```
**GitHub:** https://github.com/Nevillemehta-Claude/001_MCI_TERMINAL_EXTRACTION

---

## 3. EXECUTION APPROACH

### Phase Sequencing — FLEXIBLE

| Approach | When to Use |
|----------|-------------|
| **Sequential (CIA → MCI → Integrated)** | Default safe approach |
| **Parallel (CIA + MCI simultaneously)** | When time matters and resources allow |
| **Integrated-first** | When integration is the primary concern |

**Cursor discretion:** Choose the approach that best serves the recertification goal. Document your reasoning.

---

### PHASE I — CIA-SIE-PURE

**Workflow:** `pad-gh2-cia-sie-independent.yml`

**Cycle Guidance:**
| Situation | Recommended Cycles |
|-----------|-------------------|
| Variance stabilizes quickly | 5-10 cycles sufficient |
| Variance fluctuating | Continue until stable (up to 20) |
| Known flaky tests | Investigate root cause, then cycle |
| All green consistently | 3 consecutive clean runs = confidence |

**What matters:** Demonstrated stability, not arbitrary cycle counts.

**Artifacts:** Generate certification report documenting:
- Tests executed
- Pass rate
- Variance observed
- Confidence assessment

**Location:** `PROJECTS/CIA_SIE_PURE/00_GOVERNANCE/`

---

### PHASE II — MCI TERMINAL

**Workflow:** `pad-gh2-mci-independent.yml`

**Cycle Guidance:** Same adaptive approach as Phase I.

**Verification Targets:**
- Unit tests (Vitest)
- Type checking
- Lint
- Build

**Artifacts:** Certification report with same structure.

**Location:** `PROJECTS/MCI_Terminal/00_GOVERNANCE/`

---

### PHASE III — INTEGRATED SYSTEM

**Workflows:**
1. `pad-gh2-integration.yml`
2. `pad-gh2-stress.yml`

**Stress Dimensions — PRIORITIZED:**

| Priority | Dimension | Rationale |
|----------|-----------|-----------|
| **Critical** | Abort dominance | Safety-critical |
| **Critical** | Rollback verification | Data integrity |
| **Critical** | Cold start | User experience |
| **Important** | Health degradation | Graceful failure |
| **Important** | Warm restart | Operational continuity |
| **Valuable** | Latency injection | Edge case handling |
| **Valuable** | Mid-operation restart | Robustness |

**Cursor discretion:**
- Critical dimensions = mandatory
- Important dimensions = strongly recommended
- Valuable dimensions = include if time/resources permit

**Artifacts:** Integration and stress reports.

---

## 4. FAILURE HANDLING — INTELLIGENT

### Failure Classification

| Type | Response | Example |
|------|----------|---------|
| **Blocking** | Halt, investigate, report | Test logic failure, integration break |
| **Recoverable** | Fix if obvious, document, continue | Typo in test, missing import |
| **Environmental** | Retry, escalate if persistent | Network timeout, runner issue |
| **Flaky** | Identify root cause, stabilize, then proceed | Race condition, timing issue |

### Auto-Repair Authorization

| Scenario | Authorized? |
|----------|-------------|
| Fix obvious typo causing failure | ✅ Yes — document the fix |
| Add missing import | ✅ Yes — document the fix |
| Adjust test timeout for slow runner | ✅ Yes — document rationale |
| Change test logic to make it pass | ❌ No — investigate why it fails |
| Skip failing test | ❌ No — must understand cause |
| Modify production code to pass test | ❌ No — requires explicit approval |

**Principle:** Fix what's clearly broken. Investigate what's unclear. Never mask problems.

---

## 5. AUTHORIZATION SCOPE — EXPANDED

### Fully Authorized (proceed without asking):
- Execute any workflow
- Re-run failed jobs
- Retry on environmental failures
- Fix obvious test infrastructure issues
- Generate reports in any reasonable format
- Choose execution order based on judgment
- Adjust cycle counts based on variance behavior
- Download and analyze artifacts
- Create attestation documents

### Authorized with Documentation:
- Minor fixes to test code (document what and why)
- Timeout/retry adjustments (document rationale)
- Skip non-critical stress dimensions (document reason)
- Parallel execution (document approach)

### Requires Explicit Approval:
- Changes to production source code
- Changes to architectural constraints
- Skipping critical stress dimensions
- Marking something as passed despite failures

---

## 6. EVIDENCE REQUIREMENTS — PRACTICAL

**What constitutes valid evidence:**

| Evidence Type | Acceptable Forms |
|---------------|------------------|
| Test results | GitHub Actions logs, downloaded artifacts, screenshots |
| Cycle counts | Workflow run history, summary in report |
| Variance data | Calculated from results, presented in report |
| Pass/fail status | Clear statement with supporting data |

**Format flexibility:** Reports can be:
- Markdown (preferred)
- Structured text
- Tables
- Whatever clearly communicates the results

**What matters:** Clarity, accuracy, traceability — not rigid format.

---

## 7. FINAL ATTESTATION — OUTCOME-FOCUSED

After sufficient verification, produce:

**File:** `GITHUB_PAD_GH_OMEGA_RECERTIFICATION_ATTESTATION.md`

**Location:** `GOVERNANCE/` (top-level)

**Must Include:**
1. Status of each scope (CIA, MCI, Integrated)
2. Evidence summary (tests run, cycles, variance)
3. Confidence assessment
4. Any caveats or known limitations
5. Clear YES/NO on operational readiness

**May Include:**
- Recommendations for future improvement
- Observations about system behavior
- Notes on any fixes made during verification

**Tone:** Direct and factual. Confidence where earned, caveats where warranted.

---

## 8. WORKFLOW COMMANDS

```bash
# Trigger workflows
gh workflow run [WORKFLOW].yml --repo Nevillemehta-Claude/[REPO]

# Monitor
gh run list --repo [REPO]
gh run watch [RUN_ID] --repo [REPO]

# Download artifacts
gh run download [RUN_ID] --repo [REPO]
```

---

## 9. DECISION FRAMEWORK

When facing a choice, ask:

1. **Does this serve the recertification goal?**
2. **Am I masking a problem or solving it?**
3. **Can I document and justify this decision?**
4. **Would this give false confidence or true confidence?**

If answers are: Yes, Solving, Yes, True — proceed with confidence.

---

## 10. COMMUNICATION

**During Execution:**
- Report phase completions
- Flag blocking issues immediately
- Share key metrics as they emerge
- Ask clarifying questions when genuinely stuck

**After Execution:**
- Provide summary of what was verified
- Highlight any concerns or observations
- Deliver attestation with confidence assessment

---

## 11. BEGIN

You have broad authority to achieve recertification intelligently.

Use your judgment. Document your decisions. Deliver confidence.

**Execute.**
