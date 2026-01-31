# MCI TERMINAL - PROJECT TAXONOMY & CANONICAL STRUCTURE

## FOR AI/CURSOR INGESTION

This document provides a complete map of the MCI Terminal project structure following the Universal Taxonomy from The Holy Grail of Folder Rehydration Protocol.

---

## PROJECT IDENTITY

| Attribute | Value |
|-----------|-------|
| **Project Name** | MCI Terminal (Mission Control Interface) |
| **Location** | `/Users/nevillemehta/Downloads/001_MCI_TERMINAL_EXTRACTION/` |
| **Total Files** | 24,392 |
| **Primary Language** | TypeScript/React (Frontend), Node.js (Backend) |
| **GitHub** | https://github.com/Nevillemehta-Claude/001_MCI_TERMINAL_EXTRACTION |

---

## UNIVERSAL TAXONOMY STRUCTURE

```
001_MCI_TERMINAL_EXTRACTION/
│
├── GOVERNANCE/                    [13 files] - Authority & Control Documents
├── PROJECTS/                      [24,351 files] - Main Project Code & Docs
├── DOCUMENTATION/                 [19 files] - Technical Documentation
├── ASSETS/                        [3 catalogs] - Media & Resource Catalogs
├── DATA/                          [1 catalog] - Data File Catalogs
├── ARCHIVES/                      [empty] - Compressed/Backup Files
├── EXECUTABLES/                   [1 catalog] - Scripts & Binaries
├── COMMUNICATIONS/                [2 files] - Transcripts & Records
├── RESEARCH/                      [empty] - Research Materials
├── TEMPLATES/                     [empty] - Template Files
├── UNCLASSIFIED/                  [1 file] - Uncategorized Items
│
├── MASTER_INDEX.md                - Complete repository overview
├── GOVERNANCE_INDEX.md            - Governance document catalog
├── MIGRATION_LOG.md               - Rehydration audit trail
└── ASSET_MANIFEST.csv             - Reversibility registry
```

---

## DETAILED FOLDER BREAKDOWN

### 1. GOVERNANCE/ (Authority Documents)

Purpose: High-level directives, principles, and governance frameworks that control project behavior.

```
GOVERNANCE/
├── 01_Directives/         - Authority statements, position papers
├── 02_Principles/         - Invariants, constraints, boundaries
├── 03_Protocols/          - Procedures, extraction reports
├── 04_Standards/          - Conformance maps, error standards
├── 05_Frameworks/         - Circuit diagrams, traceability matrices
├── 06_Meta/               - (empty)
└── 07_Archive/            - (empty)
```

**Key Files:**
- Constitutional constraints and boundaries
- Program director directives
- Gold standard benchmark matrices
- State transition authority tables

---

### 2. PROJECTS/MCI_Terminal/ (Main Project)

Purpose: Complete application source code with internal organization.

```
PROJECTS/MCI_Terminal/
│
├── .git/                          - Git repository
├── .github/workflows/             - CI/CD pipelines
│
├── 00_GOVERNANCE/                 [80 files] - Project-internal governance
│   ├── Attestations, certifications
│   ├── Gate approvals
│   ├── Forensic reviews
│   └── Leap consolidated attestations
│
├── 01_DECISIONS/                  [3 files] - Architecture decisions
│
├── 02_ARCHITECTURE/               [32 files] - System architecture
│   ├── PHASE_0_TOKEN_CAPTURE/
│   ├── PHASE_1_PRE_IGNITION/
│   ├── PHASE_2_IGNITION/
│   ├── PHASE_3_TELEMETRY/
│   ├── PHASE_4_SHUTDOWN/
│   ├── UXMI/                      - UI component library specs
│   └── FLOWCHARTS/                - System flow diagrams
│
├── 03_SPECIFICATIONS/             [8 files] - Feature specifications
│
├── 04_IMPLEMENTATION/             [7 files] - Implementation patterns
│   ├── PATTERNS/
│   └── CODE_SNIPPETS/
│
├── 05_PROBLEMS_SOLVED/            [4 files] - Bug fixes & solutions
│
├── 06_ACTION_ITEMS/               [1 file] - TODOs
│
├── 07_KNOWLEDGE_BASE/             [14 files] - Documentation & references
│   ├── MASTER_INDEX.md
│   ├── GLOSSARY.md
│   ├── CROSS_REFERENCE.md
│   └── Session narratives
│
├── 08_CERTIFICATION/              [3 files] - Extraction certificates
│
├── 09_IMPLEMENTATION_ROADMAP/     [41 files] - Roadmaps & guides
│   ├── PHASE_ARTIFACTS/
│   │   ├── PHASE_I/               - Mission charter, stakeholders
│   │   ├── PHASE_II/              - Requirements, acceptance criteria
│   │   ├── PHASE_III/             - C4 architecture diagrams
│   │   └── PHASE_3.5/             - UXMI component catalog
│   └── Interactive HTML roadmaps
│
├── 10_QA_EXCHANGES/               [2 files] - QA chronicles
│
├── 11_MCI_FORENSIC_AUDIT.../      [2 files] - Annotated audit docs
│
├── 12_APPLICATION_CODE/           [23,308 files] - MAIN CODEBASE
│   ├── src/
│   │   ├── client/                - React frontend
│   │   │   ├── components/
│   │   │   │   ├── phase0/        - Token capture UI
│   │   │   │   ├── phase1/        - Pre-ignition scanner
│   │   │   │   ├── phase2/        - Ignition controls
│   │   │   │   ├── phase3/        - Telemetry dashboard
│   │   │   │   ├── phase4/        - Shutdown panel
│   │   │   │   ├── uxmi/          - UI component library
│   │   │   │   └── cockpit/       - Mission control cockpit
│   │   │   ├── stores/            - Zustand state stores
│   │   │   ├── hooks/             - React hooks
│   │   │   └── lib/               - Utilities
│   │   │
│   │   ├── server/                - Node.js backend
│   │   │   ├── routes/            - API endpoints
│   │   │   ├── services/          - Business logic
│   │   │   └── lib/               - Server utilities
│   │   │
│   │   ├── shared/                - Shared code
│   │   │   ├── types.ts           - TypeScript types
│   │   │   ├── validation/        - Input validation
│   │   │   ├── resilience/        - Circuit breakers, retry logic
│   │   │   ├── activation/        - Kill switch, rollback
│   │   │   ├── verification/      - Gate 7 verification
│   │   │   ├── live/              - Live trading phases
│   │   │   └── integration/       - Integration adapters
│   │   │
│   │   └── test/                  - Test utilities
│   │
│   ├── e2e/                       - Playwright E2E tests
│   ├── scripts/                   - Shell scripts (start, stop, status)
│   ├── .github/workflows/         - CI/CD workflows
│   │
│   ├── package.json               - Dependencies
│   ├── vite.config.ts             - Vite bundler config
│   ├── tailwind.config.js         - Tailwind CSS config
│   ├── tsconfig.json              - TypeScript config
│   └── vitest.config.ts           - Test config
│
├── 99_INDEPENDENT_VERIFICATION/   [20 files] - Verification reports
│
└── CIA_SIE_PURE_FRONTEND_PROTOTYPE/ [3 files] - Frontend prototype
```

---

### 3. DOCUMENTATION/ (Technical Docs)

```
DOCUMENTATION/
├── Technical/                     [18 files]
│   ├── Certificates
│   ├── Attestations
│   ├── Determinism reports
│   └── Readiness reports
├── Operational/                   [empty]
├── Reference/                     [empty]
├── Instructional/                 [empty]
└── DOCUMENTATION_CATALOG.md
```

---

### 4. ASSETS/ (Media Catalogs)

```
ASSETS/
├── Images/IMAGE_CATALOG.md        - 9 images cataloged
├── SourceMaps/SOURCE_MAP_CATALOG.md - 4,833 .map files cataloged
├── Fonts/FONT_CATALOG.md          - 2 fonts cataloged
├── Screenshots/                   [empty]
├── Diagrams/                      [empty]
├── Videos/                        [empty]
└── Audio/                         [empty]
```

---

### 5. DATA/ (Data File Catalogs)

```
DATA/
├── Serialized/DATA_FILE_CATALOG.md - JSON, YAML, CSV files cataloged
├── Spreadsheets/                  [empty]
├── Tabular/                       [empty]
└── Persistent/                    [empty]
```

---

### 6. EXECUTABLES/ (Scripts Catalog)

```
EXECUTABLES/
├── Binaries/EXECUTABLE_CATALOG.md - Shell scripts cataloged
├── Installers/                    [empty]
└── Packages/                      [empty]
```

---

### 7. COMMUNICATIONS/ (Transcripts)

```
COMMUNICATIONS/
├── Transcripts/AGENT_SESSION_TRANSCRIPT_2026-01-29.txt
├── COMMUNICATIONS_CATALOG.md
├── Correspondence/                [empty]
└── Records/                       [empty]
```

---

## KEY FILE TYPES & LOCATIONS

| File Type | Count | Primary Location |
|-----------|-------|------------------|
| `.ts/.tsx` | 6,224 | PROJECTS/.../src/ |
| `.js` | 8,695 | PROJECTS/.../node_modules, dist |
| `.map` | 4,833 | PROJECTS/.../node_modules, dist |
| `.md` | 905+ | GOVERNANCE, DOCUMENTATION, PROJECTS |
| `.json` | 692 | PROJECTS/.../configs, node_modules |
| `.yml` | 82 | PROJECTS/.../.github/workflows |

---

## APPLICATION ARCHITECTURE

### Frontend (React + TypeScript)
- **State Management:** Zustand stores
- **Styling:** Tailwind CSS
- **Build:** Vite
- **Testing:** Vitest + Playwright

### Backend (Node.js)
- **Framework:** Express
- **API:** RESTful routes
- **Integration:** Kite API, CIA-SIE-PURE backend

### Phase Lifecycle
1. **Phase 0:** Token Capture - OAuth flow with Kite
2. **Phase 1:** Pre-Ignition - System health checks
3. **Phase 2:** Ignition - Backend connection
4. **Phase 3:** Telemetry - Live market data
5. **Phase 4:** Shutdown - Graceful termination

---

## NAVIGATION QUICK REFERENCE

| Looking for... | Go to... |
|----------------|----------|
| React components | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/client/components/` |
| API routes | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/server/routes/` |
| State stores | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/client/stores/` |
| Type definitions | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/shared/types.ts` |
| Tests | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/**/*.test.ts` |
| CI/CD workflows | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/.github/workflows/` |
| Governance docs | `GOVERNANCE/` or `PROJECTS/MCI_Terminal/00_GOVERNANCE/` |
| Architecture | `PROJECTS/MCI_Terminal/02_ARCHITECTURE/` |

---

## IMPORTANT CONVENTIONS

1. **Phase-based organization:** Components are organized by lifecycle phase (0-4)
2. **UXMI:** Unified UI component library with consistent styling
3. **Governance-first:** All changes require attestation/certification
4. **Dual governance:** Top-level GOVERNANCE/ + project-internal 00_GOVERNANCE/
5. **Resilience patterns:** Circuit breakers, retry logic, kill switches built-in

---

*Generated for Cursor AI ingestion - 2026-01-31*
*Protocol: The Holy Grail of Folder Rehydration*
