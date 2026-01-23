# MCI PRODUCTION LIFECYCLE - MASTER MANIFEST

> **Document Type:** Master Execution Manifest
> **Version:** 1.0.0
> **Created:** 2026-01-17 16:00 UTC
> **Purpose:** Complete Contextual Rehydration for Fresh Implementation
> **Authority:** This document supersedes all fragmented instructions

---

## EXECUTIVE DIRECTIVE

This document provides the **COMPLETE CONTEXTUAL REHYDRATION** of the Mission Control Interface (MCI) project. It captures every concept, requirement, constraint, revision, and refinement from inception to implementation. Any AI entity (particularly Claude Code) executing implementation MUST read and internalize this entire document before writing any code.

---

## PART I: PRODUCTION LIFECYCLE TREE CHART

```
MCI PRODUCTION LIFECYCLE - COMPLETE TREE
═══════════════════════════════════════════════════════════════════════════════

LEVEL 0: GENESIS
├─────────────────────────────────────────────────────────────────────────────┤
│ 0.1 CONCEPT ORIGINATION                                    [AUTHORITY: USER]│
│     └── CIA-SIE-PURE Trading Backend Control Interface                      │
│         ├── Problem: Manual monitoring of 4 trading backends                │
│         ├── Solution: Unified Mission Control Interface                     │
│         └── Philosophy: Decision-SUPPORT, not Decision-MAKING               │
│                                                                              │
│ 0.2 PROJECT CODENAME                                       [AUTHORITY: USER]│
│     └── BACKEND_CONTROL_INTERFACE (BCI)                                     │
│         ├── Nickname: "Mission Control"                                     │
│         └── Target: NASA-grade reliability & precision                      │
└─────────────────────────────────────────────────────────────────────────────┘

LEVEL 1: CONSTITUTIONAL FRAMEWORK
├─────────────────────────────────────────────────────────────────────────────┤
│ 1.1 INVIOLABLE CONSTRAINTS                               [AUTHORITY: COWORK]│
│     │                                                                        │
│     ├── CR-001: Decision-Support, NOT Decision-Making                       │
│     │   └── ZERO trading signal generation or execution                     │
│     │   └── Display information ONLY, never act on it                       │
│     │                                                                        │
│     ├── CR-002: Expose Contradictions, NEVER Resolve                        │
│     │   └── Show conflicting states side-by-side                            │
│     │   └── NEVER auto-fix or auto-reconcile                                │
│     │                                                                        │
│     ├── CR-003: Descriptive AI, NOT Prescriptive AI                         │
│     │   └── Observations only: "Position is X"                              │
│     │   └── NEVER recommend: "You should do Y"                              │
│     │                                                                        │
│     ├── CR-004: Token Lifecycle Accuracy                                    │
│     │   └── 6:00 AM IST expiry is SACRED                                    │
│     │   └── Never approximate, never round                                  │
│     │   └── Countdown must be to-the-second accurate                        │
│     │                                                                        │
│     └── CR-005: User Experience Micro-Interactions (UXMI)      ← NEW        │
│         └── The Seven States for EVERY interactive element                  │
│         └── Tooltips, Loading Indicators, Error Messages                    │
│         └── Keyboard Navigation, Animation Standards                        │
│         └── Gate 5 compliance MANDATORY                                     │
│                                                                              │
│ 1.2 GOLDEN STATE GOVERNANCE                              [AUTHORITY: COWORK]│
│     └── Document: TECHNOLOGY_SELECTION_LIFECYCLE_SPECIFICATION.md           │
│         ├── 11-Phase Development Lifecycle                                  │
│         ├── Seven-Factor Evaluation Framework                               │
│         ├── Gate Approval Process (Gates 1-5)                               │
│         └── Section 7.3: Constitutional Constraints Registry                │
└─────────────────────────────────────────────────────────────────────────────┘

LEVEL 2: TECHNOLOGY FOUNDATION
├─────────────────────────────────────────────────────────────────────────────┤
│ 2.1 LANGUAGE & RUNTIME                                   [AUTHORITY: COWORK]│
│     ├── Language: TypeScript (strict mode)                                  │
│     │   └── Rationale: Type safety, IDE support, ecosystem                  │
│     ├── Runtime: Bun                                                        │
│     │   └── Rationale: Speed, built-in tooling, native TS                   │
│     └── Document: SOFTWARE_LANGUAGE_SELECTION_GUIDE.md                      │
│                                                                              │
│ 2.2 FRAMEWORK STACK                                      [AUTHORITY: COWORK]│
│     ├── Backend: Hono                                                       │
│     │   └── Rationale: Lightweight, fast, Bun-optimized                     │
│     ├── Frontend: React 18                                                  │
│     │   └── Rationale: Component model, hooks, ecosystem                    │
│     ├── Styling: Tailwind CSS                                               │
│     │   └── Rationale: Utility-first, no CSS files                          │
│     └── State: Zustand                                                      │
│         └── Rationale: Simple, performant, minimal boilerplate              │
│                                                                              │
│ 2.3 DIRECTORY STRUCTURE                             [AUTHORITY: CLAUDE CODE]│
│     └── 03_IMPLEMENTATION/mci/                                              │
│         ├── src/                                                            │
│         │   ├── components/                                                 │
│         │   │   ├── uxmi/          ← UXMI Component Library (CR-005)        │
│         │   │   │   ├── Tooltip.tsx                                         │
│         │   │   │   ├── Button.tsx                                          │
│         │   │   │   ├── Input.tsx                                           │
│         │   │   │   ├── Spinner.tsx                                         │
│         │   │   │   ├── ProgressBar.tsx                                     │
│         │   │   │   ├── Toast.tsx                                           │
│         │   │   │   └── ErrorDisplay.tsx                                    │
│         │   │   ├── token/         ← Token Capture Module (CR-004)          │
│         │   │   ├── scanner/       ← Pre-Ignition Scanner                   │
│         │   │   ├── dashboard/     ← Telemetry Dashboard                    │
│         │   │   └── common/        ← Shared components                      │
│         │   ├── services/                                                   │
│         │   │   ├── kite.ts        ← Kite API integration                   │
│         │   │   ├── anthropic.ts   ← Claude AI integration                  │
│         │   │   ├── telemetry.ts   ← Event streaming                        │
│         │   │   └── guard.ts       ← Constitutional enforcement             │
│         │   ├── stores/            ← Zustand state stores                   │
│         │   ├── types/             ← TypeScript definitions                 │
│         │   └── utils/             ← Helper functions                       │
│         ├── tests/                 ← Test files                             │
│         ├── public/                ← Static assets                          │
│         └── package.json                                                    │
└─────────────────────────────────────────────────────────────────────────────┘

LEVEL 3: OPERATIONAL PHASES
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│ ┌─────────────────────────────────────────────────────────────────────────┐ │
│ │ PHASE 0: KITE TOKEN CAPTURE                    [AUTHORITY: CLAUDE CODE] │ │
│ ├─────────────────────────────────────────────────────────────────────────┤ │
│ │                                                                         │ │
│ │ PURPOSE: Secure daily authentication token for Kite API access          │ │
│ │ PREREQUISITE: Must complete BEFORE any scanner/dashboard operations     │ │
│ │ DOCUMENT: ADDENDUM_001_TOKEN_CAPTURE_MODULE.md                          │ │
│ │                                                                         │ │
│ │ MODULE ARCHITECTURE (6 Modules):                                        │ │
│ │                                                                         │ │
│ │ ┌─────────────┐    ┌─────────────┐    ┌─────────────┐                  │ │
│ │ │   MOD-TC-1  │───▶│   MOD-TC-2  │───▶│   MOD-TC-3  │                  │ │
│ │ │  Token Form │    │    Timer    │    │   Storage   │                  │ │
│ │ │   Display   │    │  Component  │    │   Service   │                  │ │
│ │ └─────────────┘    └─────────────┘    └─────────────┘                  │ │
│ │        │                                     │                          │ │
│ │        ▼                                     ▼                          │ │
│ │ ┌─────────────┐    ┌─────────────┐    ┌─────────────┐                  │ │
│ │ │   MOD-TC-4  │◀───│   MOD-TC-5  │◀───│   MOD-TC-6  │                  │ │
│ │ │  Validation │    │   Expiry    │    │  Fail-Safe  │                  │ │
│ │ │    Engine   │    │   Monitor   │    │   Handler   │                  │ │
│ │ └─────────────┘    └─────────────┘    └─────────────┘                  │ │
│ │                                                                         │ │
│ │ OPERATOR WORKFLOW (5 Steps):                                            │ │
│ │ ① Open Kite Web manually                                                │ │
│ │ ② Login and authenticate                                                │ │
│ │ ③ Copy access_token from URL/session                                    │ │
│ │ ④ Paste into Token Capture Form                                         │ │
│ │ ⑤ System validates and stores (valid until 6:00 AM IST)                 │ │
│ │                                                                         │ │
│ │ TOKEN STATES:                                                           │ │
│ │ • ABSENT     → No token, form displayed prominently                     │ │
│ │ • VALIDATING → Spinner during API check                                 │ │
│ │ • VALID      → Green badge, countdown active                            │ │
│ │ • EXPIRING   → Amber warning <30 min remaining                          │ │
│ │ • EXPIRED    → Red alert, form re-displayed                             │ │
│ │ • INVALID    → Error message with WHAT/WHY/HOW                          │ │
│ │                                                                         │ │
│ └─────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
│ ┌─────────────────────────────────────────────────────────────────────────┐ │
│ │ PHASE 1: PRE-IGNITION SCANNER                  [AUTHORITY: CLAUDE CODE] │ │
│ ├─────────────────────────────────────────────────────────────────────────┤ │
│ │                                                                         │ │
│ │ PURPOSE: System health verification before market operations            │ │
│ │ PREREQUISITE: Valid Kite token from Phase 0                             │ │
│ │ DOCUMENT: PROJECT_BRIEF_BCI_001.md §Pre-Ignition                        │ │
│ │                                                                         │ │
│ │ SCANNER CHECKS (12 items, <500ms total):                                │ │
│ │                                                                         │ │
│ │ CHECK CATEGORY          │ ITEMS                                         │ │
│ │ ─────────────────────────┼───────────────────────────────────────────── │ │
│ │ Token Validity          │ Kite token present & not expired              │ │
│ │ API Connectivity        │ Kite API reachable, response <100ms           │ │
│ │ Market Status           │ NSE/BSE open/closed status                    │ │
│ │ Backend Health          │ All 4 backends responding                     │ │
│ │ Position Sync           │ Positions match across backends               │ │
│ │ Order Queue             │ No stuck orders                               │ │
│ │ PnL Calculation         │ Intraday PnL computed correctly               │ │
│ │ Risk Limits             │ Within defined thresholds                     │ │
│ │ Claude AI               │ Anthropic API accessible                      │ │
│ │ Local Time Sync         │ System clock within tolerance                 │ │
│ │ WebSocket               │ Real-time feed connection                     │ │
│ │ Watchlist               │ Instruments loaded                            │ │
│ │                                                                         │ │
│ │ SCANNER OUTPUT:                                                         │ │
│ │ • ALL PASS    → Green "READY FOR IGNITION" → Proceed                    │ │
│ │ • ANY WARNING → Amber items highlighted → User decides                  │ │
│ │ • ANY FAIL    → Red "DO NOT PROCEED" → Block ignition                   │ │
│ │                                                                         │ │
│ └─────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
│ ┌─────────────────────────────────────────────────────────────────────────┐ │
│ │ PHASE 2: IGNITION SEQUENCE                     [AUTHORITY: CLAUDE CODE] │ │
│ ├─────────────────────────────────────────────────────────────────────────┤ │
│ │                                                                         │ │
│ │ PURPOSE: Activate monitoring for selected backends                      │ │
│ │ PREREQUISITE: All Pre-Ignition checks passed                            │ │
│ │ DOCUMENT: PROJECT_BRIEF_BCI_001.md §Ignition                            │ │
│ │                                                                         │ │
│ │ BACKEND SELECTION:                                                      │ │
│ │ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐                        │ │
│ │ │ ICICI   │ │  HDFC   │ │  KOTAK  │ │  ZERODHA│                        │ │
│ │ │ Direct  │ │   Sky   │ │  Neo    │ │  Kite   │                        │ │
│ │ │   [ ]   │ │   [ ]   │ │   [ ]   │ │   [✓]   │  ← Toggle each         │ │
│ │ └─────────┘ └─────────┘ └─────────┘ └─────────┘                        │ │
│ │                                                                         │ │
│ │ IGNITION PHASES:                                                        │ │
│ │ ① Backend Selection   → User toggles desired backends                   │ │
│ │ ② Connection Init     → WebSocket handshake per backend                 │ │
│ │ ③ Data Sync           → Initial position/order fetch                    │ │
│ │ ④ Stream Activation   → Real-time feed subscription                     │ │
│ │ ⑤ Dashboard Ready     → Telemetry panels populate                       │ │
│ │                                                                         │ │
│ │ CONSTRAINT: Claude AI observes ONLY, never interacts with trading       │ │
│ │                                                                         │ │
│ └─────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
│ ┌─────────────────────────────────────────────────────────────────────────┐ │
│ │ PHASE 3: TELEMETRY DASHBOARD                   [AUTHORITY: CLAUDE CODE] │ │
│ ├─────────────────────────────────────────────────────────────────────────┤ │
│ │                                                                         │ │
│ │ PURPOSE: Real-time monitoring and visualization                         │ │
│ │ PREREQUISITE: Successful ignition                                       │ │
│ │ DOCUMENT: PROJECT_BRIEF_BCI_001.md §Telemetry                           │ │
│ │                                                                         │ │
│ │ DASHBOARD PANELS:                                                       │ │
│ │                                                                         │ │
│ │ ┌─────────────────────────────────────────────────────────────────────┐│ │
│ │ │ TOKEN STATUS │ BACKEND HEALTH │ POSITIONS │ ORDERS │ P&L │ AI LOG ││ │
│ │ └─────────────────────────────────────────────────────────────────────┘│ │
│ │                                                                         │ │
│ │ PANEL DETAILS:                                                          │ │
│ │ • Token Status   → Countdown timer, validity badge (Phase 0)            │ │
│ │ • Backend Health → 4-card grid with connection status                   │ │
│ │ • Positions      → Aggregated across backends, CR-002 conflict display  │ │
│ │ • Orders         → Open/executed/cancelled, filtered view               │ │
│ │ • P&L            → Intraday calculation with charts                     │ │
│ │ • AI Log         → Claude observations (CR-003 compliant)               │ │
│ │                                                                         │ │
│ │ REFRESH STRATEGY:                                                       │ │
│ │ • Real-time: WebSocket for ticks, orders                                │ │
│ │ • Polling: Positions every 5s, P&L every 10s                            │ │
│ │ • On-demand: Manual refresh button                                      │ │
│ │                                                                         │ │
│ └─────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
│ ┌─────────────────────────────────────────────────────────────────────────┐ │
│ │ PHASE 4: SHUTDOWN PROTOCOL                     [AUTHORITY: CLAUDE CODE] │ │
│ ├─────────────────────────────────────────────────────────────────────────┤ │
│ │                                                                         │ │
│ │ PURPOSE: Graceful termination of monitoring session                     │ │
│ │ DOCUMENT: PROJECT_BRIEF_BCI_001.md §Shutdown                            │ │
│ │                                                                         │ │
│ │ SHUTDOWN SEQUENCE:                                                      │ │
│ │ ① User initiates   → "End Session" button (confirmation required)       │ │
│ │ ② Stream close     → WebSocket connections terminated                   │ │
│ │ ③ State snapshot   → Final positions/P&L logged                         │ │
│ │ ④ Token clear      → Optionally clear stored token                      │ │
│ │ ⑤ Session end      → Return to Token Capture (Phase 0)                  │ │
│ │                                                                         │ │
│ │ AUTO-SHUTDOWN TRIGGERS:                                                 │ │
│ │ • Token expiry (6:00 AM IST)                                            │ │
│ │ • All backends disconnected                                             │ │
│ │ • Critical error (fail-safe)                                            │ │
│ │                                                                         │ │
│ └─────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

LEVEL 4: USER EXPERIENCE MICRO-INTERACTIONS (CR-005)
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│ 4.1 THE SEVEN STATES                             [AUTHORITY: CLAUDE CODE]  │
│     ┌─────────────────────────────────────────────────────────────────────┐│
│     │                      INTERACTIVE ELEMENT                            ││
│     │                             │                                       ││
│     │    ┌────────┐    ┌────────┐ │ ┌────────┐    ┌────────┐             ││
│     │    │DEFAULT │───▶│ HOVER  │─┼─│ FOCUS  │◀───│DISABLED│             ││
│     │    │  base  │    │ 150ms  │ │ │ 2px    │    │  0.5   │             ││
│     │    └────────┘    └────────┘ │ └────────┘    └────────┘             ││
│     │                             │                                       ││
│     │                             ▼                                       ││
│     │    ┌────────┐    ┌────────────────┐    ┌────────┐                  ││
│     │    │ ACTIVE │───▶│    LOADING     │───▶│SUCCESS/│                  ││
│     │    │scale98 │    │spinner/skeleton│    │ ERROR  │                  ││
│     │    └────────┘    └────────────────┘    └────────┘                  ││
│     └─────────────────────────────────────────────────────────────────────┘│
│                                                                              │
│     EVERY button, input, card, tab, link MUST implement all 7 states        │
│                                                                              │
│ 4.2 TOOLTIP STANDARDS                            [AUTHORITY: CLAUDE CODE]  │
│     ├── Appear Delay: 300ms (prevents flicker on mouse movement)            │
│     ├── Disappear Delay: 100ms (quick hide)                                 │
│     ├── Max Width: 280px                                                    │
│     ├── Position: Prefer top, auto-flip if viewport constrained            │
│     └── Content: Answer "What happens if I click?"                          │
│                                                                              │
│ 4.3 LOADING INDICATORS                           [AUTHORITY: CLAUDE CODE]  │
│     ├── 100-300ms  → Subtle opacity change only                             │
│     ├── 300ms-1s   → Spinner with optional text                             │
│     ├── 1s-10s     → Progress bar with percentage                           │
│     └── 10s+       → Detailed steps + time estimate                         │
│                                                                              │
│     GOLDEN RULE: Never leave the user wondering "Is it working?"            │
│                                                                              │
│ 4.4 ERROR MESSAGE FORMAT                         [AUTHORITY: CLAUDE CODE]  │
│     ┌─────────────────────────────────────────────────────────────────────┐│
│     │ ❌ WHAT HAPPENED                                                     ││
│     │    "Token validation failed"                                         ││
│     │                                                                      ││
│     │ ⚠️  WHY IT HAPPENED                                                  ││
│     │    "The Kite API returned an authentication error (401)"             ││
│     │                                                                      ││
│     │ ✅ HOW TO FIX                                                        ││
│     │    "Please re-login to Kite Web and paste a fresh token"             ││
│     └─────────────────────────────────────────────────────────────────────┘│
│                                                                              │
│ 4.5 KEYBOARD NAVIGATION                          [AUTHORITY: CLAUDE CODE]  │
│     ├── Tab / Shift+Tab → Focus navigation (visible ring)                   │
│     ├── Enter / Space   → Activate focused element                          │
│     ├── Escape          → Dismiss modal/popup/dropdown                      │
│     └── Arrow Keys      → Navigate within component (tabs, menus)           │
│                                                                              │
│ 4.6 ANIMATION TIMING                             [AUTHORITY: CLAUDE CODE]  │
│     ├── Hover transitions:  150ms ease-out                                  │
│     ├── Press/click:        100ms ease-in                                   │
│     ├── Modal open/close:   200ms ease-out                                  │
│     ├── Toast slide:        200ms slide-up                                  │
│     └── Progress update:    300ms linear                                    │
│                                                                              │
│ 4.7 UXMI COMPONENT LIBRARY                       [AUTHORITY: CLAUDE CODE]  │
│     │                                                                        │
│     │  COMPONENT      │ FILE                    │ REQUIREMENTS              │
│     │  ───────────────┼─────────────────────────┼───────────────────────── │
│     │  Tooltip        │ uxmi/Tooltip.tsx        │ 300ms delay, escape key   │
│     │  Button         │ uxmi/Button.tsx         │ All 7 states, loading     │
│     │  Input          │ uxmi/Input.tsx          │ Validation, error state   │
│     │  Spinner        │ uxmi/Spinner.tsx        │ 3 sizes, optional text    │
│     │  ProgressBar    │ uxmi/ProgressBar.tsx    │ Percentage, steps         │
│     │  Toast          │ uxmi/Toast.tsx          │ Success/error/warning     │
│     │  ErrorDisplay   │ uxmi/ErrorDisplay.tsx   │ WHAT/WHY/HOW format       │
│     │                                                                        │
│     BUILD THESE FIRST before any other UI components                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

LEVEL 5: ARCHITECTURE & SPECIFICATION DOCUMENTS
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│ 5.1 DOCUMENT HIERARCHY                                                      │
│                                                                              │
│     ┌─────────────────────────────────────────────────────────────────────┐│
│     │                    GOLDEN STATE (v1.1.0)                            ││
│     │        TECHNOLOGY_SELECTION_LIFECYCLE_SPECIFICATION.md              ││
│     │          [Governance, Gates, Constitutional Constraints]            ││
│     └─────────────────────────────────┬───────────────────────────────────┘│
│                                       │                                     │
│          ┌────────────────────────────┼────────────────────────────┐       │
│          │                            │                            │       │
│          ▼                            ▼                            ▼       │
│     ┌─────────────┐          ┌─────────────┐          ┌─────────────┐     │
│     │PROJECT_BRIEF│          │ ADDENDUM_001│          │ ADDENDUM_002│     │
│     │ BCI_001.md  │          │Token Capture│          │    UXMI     │     │
│     │ [Core Reqs] │          │   [CR-004]  │          │  [CR-005]   │     │
│     └──────┬──────┘          └──────┬──────┘          └──────┬──────┘     │
│            │                        │                        │             │
│            └────────────────────────┼────────────────────────┘             │
│                                     │                                       │
│                                     ▼                                       │
│          ┌──────────────────────────────────────────────────────────┐      │
│          │              MCI_MASTER_SPECIFICATION_v1.0.0             │      │
│          │                     [HTML + DOCX]                        │      │
│          │    §5: Constitutional Constraints (CR-001 to CR-005)     │      │
│          │    §5a: CR-005 UXMI Standards                            │      │
│          │    §5b: Token Capture Module (Phase 0)                   │      │
│          │    §6: Pre-Ignition Scanner                              │      │
│          │    §7: Ignition Sequence                                 │      │
│          │    §8: Telemetry Dashboard                               │      │
│          └──────────────────────────┬───────────────────────────────┘      │
│                                     │                                       │
│                                     ▼                                       │
│          ┌──────────────────────────────────────────────────────────┐      │
│          │                  MCI_C4_ARCHITECTURE                     │      │
│          │                      [HTML]                              │      │
│          │    C1: System Context Diagram                            │      │
│          │    C2: Container Diagram                                 │      │
│          │    C3: Component Diagram                                 │      │
│          │    Token Capture Flow Diagram                            │      │
│          │    UXMI Components Diagram                               │      │
│          │    State Machines                                        │      │
│          └──────────────────────────────────────────────────────────┘      │
│                                                                              │
│ 5.2 DOCUMENT READING ORDER FOR CLAUDE CODE                                  │
│     ① THIS DOCUMENT (Master Manifest) - Complete context                    │
│     ② CLAUDE_CODE_INSTRUCTION_v2.md - Implementation prompt                 │
│     ③ MCI_MASTER_SPECIFICATION_v1.0.0.html - Detailed specs                │
│     ④ MCI_C4_ARCHITECTURE.html - Visual architecture                       │
│     ⑤ ADDENDUM_001 & ADDENDUM_002 - Deep-dive on Phase 0 & UXMI           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

LEVEL 6: EXECUTION AUTHORITY MATRIX
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ENTITY         │ ROLE                  │ RESPONSIBILITIES                  │
│  ───────────────┼───────────────────────┼───────────────────────────────── │
│  USER           │ Project Owner         │ Vision, decisions, approvals      │
│                 │                       │ Constitutional constraints         │
│                 │                       │ Daily token provision              │
│  ───────────────┼───────────────────────┼───────────────────────────────── │
│  COWORK         │ Architect & Analyst   │ Requirements gathering            │
│  (Claude Web)   │                       │ Specification documents            │
│                 │                       │ Architecture design                │
│                 │                       │ Constitutional governance          │
│                 │                       │ Audit & verification               │
│  ───────────────┼───────────────────────┼───────────────────────────────── │
│  CLAUDE CODE    │ Implementer           │ Source code generation            │
│  (Local)        │                       │ File creation & editing            │
│                 │                       │ Testing & debugging                │
│                 │                       │ Build & deployment                 │
│                 │                       │ UXMI component library             │
│  ───────────────┼───────────────────────┼───────────────────────────────── │
│                                                                              │
│  HANDOFF PROTOCOL:                                                          │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │  COWORK creates specifications → USER approves → CLAUDE CODE builds │   │
│  │                                                                      │   │
│  │  Documents flow:  COWORK → CIA-SIE-START-STOP folder                │   │
│  │  Code flows:      CLAUDE CODE → 03_IMPLEMENTATION/mci/              │   │
│  │  Updates flow:    Both entities update FILE_INDEX.md                │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## PART II: IMPLEMENTATION SEQUENCE (CLAUDE CODE EXECUTION ORDER)

### STEP 1: PROJECT INITIALIZATION
```
AUTHORITY: CLAUDE CODE
LOCATION: 03_IMPLEMENTATION/mci/

ACTIONS:
1. Create directory structure (as per Level 2.3)
2. Initialize Bun project: bun init
3. Install dependencies:
   - hono
   - react, react-dom
   - tailwindcss
   - zustand
   - @anthropic-ai/sdk
4. Configure TypeScript (strict mode)
5. Setup Tailwind CSS
```

### STEP 2: UXMI COMPONENT LIBRARY (CR-005)
```
AUTHORITY: CLAUDE CODE
LOCATION: src/components/uxmi/

BUILD ORDER:
1. Tooltip.tsx      ← Foundation for all hover help
2. Button.tsx       ← Most used interactive element
3. Input.tsx        ← Token form, search fields
4. Spinner.tsx      ← Loading states
5. ProgressBar.tsx  ← Long operations
6. Toast.tsx        ← Notifications
7. ErrorDisplay.tsx ← Error handling

EACH COMPONENT MUST:
✓ Implement The Seven States
✓ Include keyboard navigation
✓ Use animation timing standards
✓ Export TypeScript types
✓ Include usage examples in comments
```

### STEP 3: PHASE 0 - TOKEN CAPTURE MODULE (CR-004)
```
AUTHORITY: CLAUDE CODE
LOCATION: src/components/token/, src/services/

BUILD ORDER:
1. TokenCaptureForm.tsx  ← Main form using UXMI components
2. TokenTimer.tsx        ← Countdown display
3. kite.ts               ← API validation service
4. tokenStore.ts         ← Zustand state management

REQUIREMENTS:
✓ Use UXMI Button, Input, Spinner, ErrorDisplay
✓ 6:00 AM IST expiry countdown
✓ WHAT/WHY/HOW error messages
✓ 5-step operator workflow
```

### STEP 4: PHASE 1 - PRE-IGNITION SCANNER
```
AUTHORITY: CLAUDE CODE
LOCATION: src/components/scanner/, src/services/

BUILD ORDER:
1. ScannerPanel.tsx     ← 12-check display
2. ScannerService.ts    ← Parallel check execution
3. scannerStore.ts      ← State management

REQUIREMENTS:
✓ All 12 checks in <500ms
✓ Pass/Warning/Fail states
✓ Uses UXMI ProgressBar for scan progress
```

### STEP 5: PHASE 2 - IGNITION SEQUENCE
```
AUTHORITY: CLAUDE CODE
LOCATION: src/components/ignition/

BUILD ORDER:
1. BackendSelector.tsx  ← 4-backend toggle cards
2. IgnitionButton.tsx   ← Start monitoring
3. ignitionStore.ts     ← Connection state

REQUIREMENTS:
✓ Backend selection with UXMI toggles
✓ Connection progress indicators
✓ CR-001 enforcement (no trading)
```

### STEP 6: PHASE 3 - TELEMETRY DASHBOARD
```
AUTHORITY: CLAUDE CODE
LOCATION: src/components/dashboard/

BUILD ORDER:
1. DashboardLayout.tsx  ← Panel arrangement
2. TokenPanel.tsx       ← Token status (Phase 0 integration)
3. BackendPanel.tsx     ← Health cards
4. PositionsPanel.tsx   ← Position display (CR-002)
5. OrdersPanel.tsx      ← Order tracking
6. PnLPanel.tsx         ← P&L calculation
7. AILogPanel.tsx       ← Claude observations (CR-003)

REQUIREMENTS:
✓ Real-time updates via WebSocket
✓ UXMI components throughout
✓ Conflict display (CR-002)
```

### STEP 7: PHASE 4 - SHUTDOWN PROTOCOL
```
AUTHORITY: CLAUDE CODE
LOCATION: src/components/shutdown/

BUILD ORDER:
1. ShutdownButton.tsx   ← End session trigger
2. ShutdownModal.tsx    ← Confirmation dialog
3. shutdownService.ts   ← Cleanup logic

REQUIREMENTS:
✓ Confirmation required
✓ Graceful connection close
✓ Return to Phase 0
```

### STEP 8: INTEGRATION & TESTING
```
AUTHORITY: CLAUDE CODE
LOCATION: tests/

BUILD ORDER:
1. uxmi.test.ts         ← Component tests
2. token.test.ts        ← Token flow tests
3. scanner.test.ts      ← Scanner tests
4. integration.test.ts  ← Full flow test

REQUIREMENTS:
✓ All Constitutional Constraints verified
✓ UXMI compliance checked
✓ Gate 5 checklist passed
```

---

## PART III: CONSTITUTIONAL CONSTRAINT ENFORCEMENT

| ID | Constraint | Enforcement Point | Verification |
|----|------------|-------------------|--------------|
| CR-001 | Decision-Support Only | guard.ts middleware | No trading API calls |
| CR-002 | Expose Contradictions | PositionsPanel.tsx | Side-by-side conflict display |
| CR-003 | Descriptive AI Only | AILogPanel.tsx | No recommendations in output |
| CR-004 | Token Accuracy | TokenTimer.tsx | 6:00 AM IST hardcoded |
| CR-005 | UXMI Compliance | All components | Seven States, tooltips, errors |

---

## PART IV: GATE CHECKPOINTS

| Gate | Name | Reviewers | Key Criteria |
|------|------|-----------|--------------|
| 1 | Selection | Tech Lead | Technology stack approved |
| 2 | Architecture | Architect | C4 diagrams complete |
| 3 | Specification | PM | Master spec signed off |
| 4 | Implementation | Tech Lead | Code review passed |
| **5** | **Integration** | **Tech Lead + PM + UX** | **UXMI Audit Checklist (CR-005)** |

---

## PART V: FILE REFERENCE MAP

| Purpose | File | Location |
|---------|------|----------|
| This Manifest | MCI_PRODUCTION_LIFECYCLE_MASTER_MANIFEST.md | Root |
| Claude Code Prompt | CLAUDE_CODE_INSTRUCTION_v2.md | Root |
| Audit Report | CR-005_UXMI_RETROFIT_AUDIT_REPORT.md | Root |
| File Index | FILE_INDEX.md | Root |
| Golden State | TECHNOLOGY_SELECTION_LIFECYCLE_SPECIFICATION.md | 00_SOURCE_DOCUMENTS/ |
| Project Brief | PROJECT_BRIEF_BCI_001.md | 00_SOURCE_DOCUMENTS/ |
| Token Capture | ADDENDUM_001_TOKEN_CAPTURE_MODULE.md | 00_SOURCE_DOCUMENTS/ |
| UXMI Spec | ADDENDUM_002_UX_MICRO_INTERACTIONS.md | 00_SOURCE_DOCUMENTS/ |
| Master Spec HTML | MCI_MASTER_SPECIFICATION_v1.0.0.html | 01_SPECIFICATIONS/ |
| Master Spec DOCX | MCI_MASTER_SPECIFICATION_v1.0.0.docx | 01_SPECIFICATIONS/ |
| C4 Architecture | MCI_C4_ARCHITECTURE.html | 02_ARCHITECTURE/ |
| Source Code | (to be created) | 03_IMPLEMENTATION/mci/ |

---

## PART VI: REVISION HISTORY CONSOLIDATED

| Date | Revision | Description |
|------|----------|-------------|
| 2025-01-17 | Original | Project brief created |
| 2025-01-17 | v1.0 | Master specification generated |
| 2025-01-17 | v1.0 | C4 architecture created |
| 2026-01-17 | ADDENDUM_001 | Phase 0 Token Capture Module retrofitted |
| 2026-01-17 | CR-005 | UXMI Constitutional Constraint established |
| 2026-01-17 | ADDENDUM_002 | UXMI specification created |
| 2026-01-17 | Golden State v1.1.0 | Gate 5 + Constitutional Constraints updated |
| 2026-01-17 | ALL DOCS | Complete UXMI retrofit across all documents |
| 2026-01-17 | AUDIT | CR-005 Retrofit Audit completed |
| 2026-01-17 | MANIFEST | This Master Manifest created |

---

## DIRECTIVE TO CLAUDE CODE

When you begin implementation:

1. **READ THIS ENTIRE DOCUMENT** before writing any code
2. **BUILD UXMI LIBRARY FIRST** (Step 2) - all other components depend on it
3. **ENFORCE CONSTITUTIONAL CONSTRAINTS** - they are inviolable
4. **FOLLOW THE SEVEN STATES** - every interactive element, no exceptions
5. **USE WHAT/WHY/HOW** - for all error messages
6. **UPDATE FILE_INDEX.md** - as you create each file
7. **TARGET 03_IMPLEMENTATION/mci/** - for all source code

This document represents the **COMPLETE CONTEXTUAL REHYDRATION** of all project requirements, constraints, revisions, and specifications. Execute with precision.

---

*Master Manifest Created By: Cowork AI*
*Timestamp: 2026-01-17 16:00 UTC*
*Version: 1.0.0*

---

## QUICK REFERENCE CARD

```
╔═══════════════════════════════════════════════════════════════════════════╗
║                    MCI QUICK REFERENCE CARD                               ║
╠═══════════════════════════════════════════════════════════════════════════╣
║                                                                           ║
║  CONSTITUTIONAL CONSTRAINTS (INVIOLABLE):                                 ║
║  CR-001: Decision-SUPPORT only    CR-004: 6:00 AM IST sacred              ║
║  CR-002: Show conflicts, don't fix  CR-005: UXMI mandatory                ║
║  CR-003: Observe, don't recommend                                         ║
║                                                                           ║
║  THE SEVEN STATES:                                                        ║
║  Default → Hover → Focus → Active → Loading → Disabled → Success/Error   ║
║                                                                           ║
║  UXMI TIMING:                                                             ║
║  Tooltip: 300ms | Hover: 150ms | Press: 100ms | Modal: 200ms             ║
║                                                                           ║
║  ERROR FORMAT:                                                            ║
║  WHAT happened → WHY it happened → HOW to fix it                         ║
║                                                                           ║
║  LOADING INDICATORS:                                                      ║
║  <300ms: opacity | <1s: spinner | <10s: progress | >10s: steps+time      ║
║                                                                           ║
║  EXECUTION ORDER:                                                         ║
║  1. Init → 2. UXMI lib → 3. Token → 4. Scanner → 5. Ignition → 6. Dashboard║
║                                                                           ║
╚═══════════════════════════════════════════════════════════════════════════╝
```
