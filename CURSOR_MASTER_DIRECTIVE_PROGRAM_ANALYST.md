# CURSOR MASTER DIRECTIVE

## PROGRAM ANALYST & MISSION CONTROL OPERATING PROTOCOL

**Classification:** OPERATIONAL DIRECTIVE
**Authority Level:** NASA Program Analyst Grade
**Effective Date:** 2026-01-31
**Scope:** All Cursor AI Operations Within This Workspace

---

# SECTION 1: DIRECTIVE AUTHORITY

## 1.1 Purpose

This directive establishes the canonical operating protocol for Cursor AI when working within the MCI Terminal and CIA-SIE-PURE ecosystem. You are hereby instructed to **ingest, internalize, and operationalize** the folder taxonomy and project structure defined herein.

## 1.2 Binding Authority

This document supersedes all prior assumptions about project structure. When in doubt about file locations, architectural decisions, or operational procedures, **THIS DIRECTIVE IS YOUR SOURCE OF TRUTH**.

## 1.3 Compliance Requirement

You MUST:
- Study this document completely before commencing any task
- Reference this structure in ALL file operations
- Use the canonical paths defined herein
- Maintain consistency with the Universal Taxonomy
- Cite specific file locations when discussing code or documentation

---

# SECTION 2: WORKSPACE TOPOLOGY

## 2.1 Primary Repositories

| Repository | Local Path | GitHub URL | Purpose |
|------------|------------|------------|---------|
| **MCI Terminal** | `/Users/nevillemehta/Downloads/001_MCI_TERMINAL_EXTRACTION/` | `https://github.com/Nevillemehta-Claude/001_MCI_TERMINAL_EXTRACTION` | Frontend Mission Control Interface |
| **CIA-SIE-PURE** | `/Users/nevillemehta/Downloads/02_CIA-SIE-PURE/` | `https://github.com/Nevillemehta-Claude/02_CIA-SIE-PURE` | Backend Intelligence Engine |

## 2.2 Universal Taxonomy Structure

Both repositories follow the **Holy Grail of Folder Rehydration** Universal Taxonomy:

```
[REPOSITORY_ROOT]/
│
├── GOVERNANCE/              → Authority documents, directives, principles
├── PROJECTS/                → Main application code and project docs
├── DOCUMENTATION/           → Technical documentation and reports
├── ASSETS/                  → Media files and resource catalogs
├── DATA/                    → Data files and database catalogs
├── ARCHIVES/                → Compressed and backup files
├── EXECUTABLES/             → Scripts and binary catalogs
├── COMMUNICATIONS/          → Transcripts and correspondence
├── RESEARCH/                → Research materials
├── TEMPLATES/               → Template files
├── UNCLASSIFIED/            → Uncategorized items
│
├── MASTER_INDEX.md          → Repository overview
├── GOVERNANCE_INDEX.md      → Governance catalog
├── MIGRATION_LOG.md         → Rehydration audit trail
└── ASSET_MANIFEST.csv       → Reversibility registry
```

---

# SECTION 3: MCI TERMINAL - COMPLETE FILE MAP

## 3.1 Identity Matrix

| Attribute | Value |
|-----------|-------|
| **Codename** | MCI Terminal (Mission Control Interface) |
| **Total Files** | 24,392 |
| **Primary Stack** | TypeScript, React, Node.js, Vite |
| **State Management** | Zustand |
| **Styling** | Tailwind CSS |
| **Testing** | Vitest, Playwright |
| **CI/CD** | GitHub Actions |

## 3.2 Critical Path Navigation

### 3.2.1 Source Code Locations

| Component | Canonical Path |
|-----------|----------------|
| **React App Entry** | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/client/main.tsx` |
| **Server Entry** | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/server/index.ts` |
| **Shared Types** | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/shared/types.ts` |
| **Package Config** | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/package.json` |
| **Vite Config** | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/vite.config.ts` |
| **TypeScript Config** | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/tsconfig.json` |
| **Tailwind Config** | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/tailwind.config.js` |

### 3.2.2 Component Hierarchy

```
PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/client/components/
│
├── phase0/                  → Token Capture Phase
│   ├── TokenCaptureForm.tsx
│   ├── TokenTimer.tsx
│   ├── CredentialsHelper.tsx
│   └── index.ts
│
├── phase1/                  → Pre-Ignition Scanner Phase
│   ├── PreIgnitionScanner.tsx
│   ├── ScanCheckItem.tsx
│   └── index.ts
│
├── phase2/                  → Ignition Phase
│   ├── IgnitionButton.tsx
│   ├── BackendSelector.tsx
│   └── index.ts
│
├── phase3/                  → Telemetry Phase
│   ├── TelemetryDashboard.tsx
│   ├── SystemHealthPanel.tsx
│   ├── ActivityLogPanel.tsx
│   ├── MarketDataPanel.tsx
│   ├── OrdersPanel.tsx
│   ├── PositionsPanel.tsx
│   ├── AccountPanel.tsx
│   └── index.ts
│
├── phase4/                  → Shutdown Phase
│   ├── ShutdownPanel.tsx
│   └── index.ts
│
├── uxmi/                    → UI Component Library
│   ├── Button.tsx
│   ├── Input.tsx
│   ├── Spinner.tsx
│   ├── Toast.tsx
│   ├── Tooltip.tsx
│   ├── ProgressBar.tsx
│   ├── ErrorDisplay.tsx
│   └── index.ts
│
└── cockpit/                 → Mission Control Cockpit
    ├── EngineStatusIndicator.tsx
    ├── SimulationBadge.tsx
    ├── StatusBar.tsx
    └── index.ts
```

### 3.2.3 State Stores

```
PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/client/stores/
│
├── index.ts                 → Store exports
├── tokenStore.ts            → OAuth token management
├── scannerStore.ts          → Pre-ignition scan state
├── ignitionStore.ts         → Ignition state
├── telemetryStore.ts        → Telemetry data state
├── shutdownStore.ts         → Shutdown state
└── ciaSieHealthStore.ts     → CIA-SIE backend health
```

### 3.2.4 Server Routes

```
PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/server/routes/
│
├── index.ts                 → Route aggregation
├── auth.ts                  → Authentication routes
├── scan.ts                  → Scanner routes
├── ignition.ts              → Ignition routes
├── telemetry.ts             → Telemetry routes
└── shutdown.ts              → Shutdown routes
```

### 3.2.5 Shared Modules

```
PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/shared/
│
├── types.ts                 → TypeScript type definitions
├── validation/              → Input validation & sanitization
├── resilience/              → Circuit breakers, retry, timeout
├── activation/              → Kill switch, rollback, governance
├── verification/            → Gate 7 verification, contracts
├── live/                    → Live trading phase orchestration
├── integration/             → Integration adapters, guards
└── errors/                  → Error handling & translation
```

### 3.2.6 CI/CD Workflows

```
PROJECTS/MCI_Terminal/12_APPLICATION_CODE/.github/workflows/
│
├── ci.yml                   → Main CI pipeline
├── pr-checks.yml            → Pull request checks
├── deploy.yml               → Deployment workflow
├── pad-gh1-integration.yml  → PAD-GH1 integration tests
├── pad-gh1-mci-independent.yml
├── pad-gh1-cia-sie-independent.yml
├── pad-gh1-stress.yml
├── pad-gh2-integration.yml  → PAD-GH2 integration tests
├── pad-gh2-mci-independent.yml
└── pad-gh2-stress.yml
```

### 3.2.7 Governance Documents

```
GOVERNANCE/                  → Top-level governance
│
├── 01_Directives/
├── 02_Principles/
├── 03_Protocols/
├── 04_Standards/
└── 05_Frameworks/

PROJECTS/MCI_Terminal/00_GOVERNANCE/  → Project-internal governance
│
├── Attestations/
├── Forensic Reviews/
├── Gate approvals
├── Leap attestations
└── Certification reports
```

### 3.2.8 Architecture Documentation

```
PROJECTS/MCI_Terminal/02_ARCHITECTURE/
│
├── PHASE_0_TOKEN_CAPTURE/DESIGN.md
├── PHASE_1_PRE_IGNITION/DESIGN.md
├── PHASE_2_IGNITION/DESIGN.md
├── PHASE_3_TELEMETRY/DESIGN.md
├── PHASE_4_SHUTDOWN/DESIGN.md
├── UXMI/
│   ├── COMPONENT_LIBRARY.md
│   └── VERBATIM_STATES.md
└── FLOWCHARTS/
    ├── 2.1_TOKEN_FLOW.md
    ├── 2.2_SCANNER_LOGIC.md
    ├── 2.3_IGNITION_SEQUENCE.md
    ├── 2.4_TELEMETRY_PIPELINE.md
    ├── 2.5_SHUTDOWN_SEQUENCE.md
    └── ... more flowcharts
```

---

# SECTION 4: CIA-SIE-PURE - COMPLETE FILE MAP

## 4.1 Identity Matrix

| Attribute | Value |
|-----------|-------|
| **Codename** | CIA-SIE-PURE (Competitive Intelligence & Analysis - Signal Intelligence Engine) |
| **Total Files** | 9,459 |
| **Primary Stack** | Python, FastAPI, SQLAlchemy |
| **AI Integration** | Anthropic Claude API |
| **Database** | SQLite (Alembic migrations) |
| **Testing** | pytest |
| **CI/CD** | GitHub Actions |

## 4.2 Critical Path Navigation

### 4.2.1 Source Code Locations

| Component | Canonical Path |
|-----------|----------------|
| **FastAPI Entry** | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/main.py` |
| **Alembic Config** | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/alembic.ini` |
| **Project Config** | `PROJECTS/CIA_SIE_PURE/pyproject.toml` |
| **Requirements** | `PROJECTS/CIA_SIE_PURE/requirements.txt` |

### 4.2.2 Python Package Structure

```
PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/
│
├── __init__.py
├── main.py                  → FastAPI application entry
│
├── api/                     → REST API Layer
│   ├── __init__.py
│   └── routes/
│       ├── narratives.py    → Narrative generation endpoints
│       └── relationships.py → Relationship analysis endpoints
│
├── ai/                      → AI/LLM Integration
│   └── __init__.py
│   (claude_client, prompt_builder, response_validator)
│
├── bridge/                  → External Platform Integrations
│   └── __init__.py
│   (kite_adapter, tradingview_adapter)
│
├── core/                    → Core Business Logic
│   └── __init__.py
│
├── dal/                     → Data Access Layer
│   └── __init__.py
│   (repositories, models, database)
│
├── exposure/                → Signal Exposure Detection
│   ├── __init__.py
│   ├── confirmation_detector.py
│   └── contradiction_detector.py
│
├── ingestion/               → Signal Ingestion Pipeline
│   ├── __init__.py
│   └── signal_normalizer.py
│
└── platforms/               → Platform-Specific Adapters
    └── __init__.py
```

### 4.2.3 Database Migrations

```
PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/alembic/
│
├── env.py
├── script.py.mako
└── versions/
    ├── 20251230_0001_initial_schema.py
    └── 20251231_1004_add_ai_tables_conversations_ai_usage.py
```

### 4.2.4 Test Suite

```
PROJECTS/CIA_SIE_PURE/07_TESTING/tests/
│
├── unit/                    [28 test files]
│   ├── test_response_validator.py
│   ├── test_constitutional_compliance.py
│   ├── test_relationship_exposer.py
│   ├── test_exposure.py
│   ├── test_kite_adapter.py
│   ├── test_usage_tracker.py
│   ├── test_dal_repositories.py
│   ├── test_tradingview_adapter.py
│   ├── test_signal_normalizer.py
│   ├── test_confirmation_detector.py
│   ├── test_contradiction_detector.py
│   ├── test_narrative_generator.py
│   ├── test_prompt_builder.py
│   ├── test_claude_client.py
│   ├── test_models.py
│   ├── test_main.py
│   └── ... more unit tests
│
├── integration/             [3 test files]
├── constitutional/          [5 test files]
├── backend/                 [8 test files]
├── e2e/                     [3 test files]
└── chaos/                   [3 test files]
```

### 4.2.5 Architecture Diagrams (PlantUML)

```
PROJECTS/CIA_SIE_PURE/04_DOCUMENTATION/02_ARCHITECTURE/diagrams/
│
├── system_architecture.puml
├── constitutional_rules.puml
├── ai_narrative_flow.puml
├── entity_relationship.puml
├── signal_ingestion_flow.puml
├── api_endpoints.puml
├── contradiction_detection.puml
├── user_journey.puml
├── kite_oauth_flow.puml
└── README.md
```

### 4.2.6 AI Prompts & Configuration

```
PROJECTS/CIA_SIE_PURE/04_DOCUMENTATION/04_AI_HANDOFF/prompts/
│
├── CURSOR_PROMPT.md
├── PROJECT_CONFIGURATION.md
└── V0_COMPONENT_PROMPTS.md
```

---

# SECTION 5: OPERATIONAL DIRECTIVES

## 5.1 File Location Protocol

When you need to locate a file, follow this decision tree:

```
START
  │
  ├─► Is it source code?
  │     ├─► TypeScript/React → PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/
  │     └─► Python → PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/
  │
  ├─► Is it a test file?
  │     ├─► MCI tests → PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/**/*.test.ts
  │     └─► CIA tests → PROJECTS/CIA_SIE_PURE/07_TESTING/tests/
  │
  ├─► Is it a workflow/CI file?
  │     ├─► MCI workflows → PROJECTS/MCI_Terminal/12_APPLICATION_CODE/.github/workflows/
  │     └─► CIA workflows → PROJECTS/CIA_SIE_PURE/.github/workflows/
  │
  ├─► Is it a governance document?
  │     ├─► High-level → GOVERNANCE/
  │     ├─► MCI project → PROJECTS/MCI_Terminal/00_GOVERNANCE/
  │     └─► CIA project → PROJECTS/CIA_SIE_PURE/00_GOVERNANCE/
  │
  ├─► Is it architecture documentation?
  │     ├─► MCI → PROJECTS/MCI_Terminal/02_ARCHITECTURE/
  │     └─► CIA → PROJECTS/CIA_SIE_PURE/04_DOCUMENTATION/02_ARCHITECTURE/
  │
  └─► Is it a configuration file?
        ├─► MCI → PROJECTS/MCI_Terminal/12_APPLICATION_CODE/[config files]
        └─► CIA → PROJECTS/CIA_SIE_PURE/[config files]
```

## 5.2 Test Writing Protocol for GitHub Actions

When writing tests that will run on GitHub Actions:

### 5.2.1 MCI Terminal Tests

**Location:** `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/`

**Naming Convention:** `*.test.ts` or `*.test.tsx`

**Test Structure:**
```typescript
// File: src/client/components/[phase]/[Component].test.tsx
import { describe, it, expect, vi } from 'vitest';
import { render, screen } from '@testing-library/react';
import { ComponentName } from './ComponentName';

describe('ComponentName', () => {
  it('should render correctly', () => {
    // test implementation
  });
});
```

**GitHub Workflow Reference:** `.github/workflows/ci.yml`

### 5.2.2 CIA-SIE-PURE Tests

**Location:** `PROJECTS/CIA_SIE_PURE/07_TESTING/tests/`

**Naming Convention:** `test_*.py`

**Test Structure:**
```python
# File: tests/unit/test_module_name.py
import pytest
from cia_sie.module import function_to_test

class TestModuleName:
    def test_function_behavior(self):
        # test implementation
        assert result == expected
```

**GitHub Workflow Reference:** `.github/workflows/ci.yml`

## 5.3 GitHub Actions Integration

### 5.3.1 Workflow Triggers

| Event | MCI Terminal | CIA-SIE-PURE |
|-------|--------------|--------------|
| Push to main | ci.yml | ci.yml |
| Pull Request | pr-checks.yml | pr-checks.yml |
| Manual Dispatch | pad-gh*.yml | pad-gh*.yml |

### 5.3.2 Test Execution Commands

**MCI Terminal (in workflow):**
```yaml
- run: npm ci
- run: npm run lint
- run: npm run type-check
- run: npm run test
- run: npm run build
```

**CIA-SIE-PURE (in workflow):**
```yaml
- run: pip install -r requirements.txt
- run: pytest tests/ -v --tb=short
- run: python -m mypy src/
```

## 5.4 Cross-Repository Integration

MCI Terminal communicates with CIA-SIE-PURE via REST API:

```
┌─────────────────────┐         ┌─────────────────────┐
│    MCI Terminal     │   HTTP  │   CIA-SIE-PURE      │
│    (Frontend)       │ ──────► │   (Backend)         │
│                     │         │                     │
│ • React Components  │         │ • FastAPI Routes    │
│ • Zustand Stores    │         │ • AI Integration    │
│ • UI/UX Layer       │         │ • Signal Processing │
└─────────────────────┘         └─────────────────────┘
```

**Integration Points:**
- Health checks: MCI → CIA `/health` endpoint
- Narratives: MCI → CIA `/api/narratives` endpoint
- Relationships: MCI → CIA `/api/relationships` endpoint

---

# SECTION 6: MANDATORY OPERATIONAL BEHAVIORS

## 6.1 When Asked to Create/Modify Files

1. **ALWAYS** use the canonical paths defined in this directive
2. **VERIFY** the file location exists before creating new files
3. **MAINTAIN** the taxonomy structure - never create files outside the defined folders
4. **UPDATE** relevant index files if creating new significant artifacts

## 6.2 When Asked to Write Tests

1. **IDENTIFY** which repository the test belongs to (MCI or CIA)
2. **USE** the correct test framework (Vitest for MCI, pytest for CIA)
3. **FOLLOW** the naming conventions defined in Section 5.2
4. **ENSURE** tests will pass in GitHub Actions environment
5. **REFERENCE** existing tests as patterns

## 6.3 When Asked to Debug Issues

1. **CONSULT** the architecture documentation first
2. **TRACE** through the file structure using Section 3/4 maps
3. **CHECK** governance documents for constraints
4. **REVIEW** CI/CD logs if GitHub Actions related

## 6.4 When Discussing the Codebase

1. **CITE** specific file paths using the canonical format
2. **REFERENCE** this directive when explaining structure
3. **USE** the correct terminology (phases, taxonomy folders, etc.)
4. **ACKNOWLEDGE** the dual-governance model (top-level + project-internal)

---

# SECTION 7: QUICK REFERENCE TABLES

## 7.1 MCI Terminal - Most Used Paths

| Purpose | Path |
|---------|------|
| Add new component | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/client/components/[phase]/` |
| Add new store | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/client/stores/` |
| Add new route | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/server/routes/` |
| Add new hook | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/client/hooks/` |
| Add shared type | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/shared/types.ts` |
| Add unit test | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/[module]/*.test.ts` |
| Add E2E test | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/e2e/` |
| Add workflow | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/.github/workflows/` |

## 7.2 CIA-SIE-PURE - Most Used Paths

| Purpose | Path |
|---------|------|
| Add new endpoint | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/api/routes/` |
| Add new service | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/core/` |
| Add DAL model | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/dal/` |
| Add migration | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/alembic/versions/` |
| Add unit test | `PROJECTS/CIA_SIE_PURE/07_TESTING/tests/unit/` |
| Add integration test | `PROJECTS/CIA_SIE_PURE/07_TESTING/tests/integration/` |
| Add workflow | `PROJECTS/CIA_SIE_PURE/.github/workflows/` |

## 7.3 File Type Quick Lookup

| Extension | MCI Terminal Location | CIA-SIE-PURE Location |
|-----------|----------------------|----------------------|
| `.ts/.tsx` | `PROJECTS/MCI_Terminal/12_APPLICATION_CODE/src/` | N/A |
| `.py` | N/A | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/` |
| `.test.ts` | Same directory as source | N/A |
| `test_*.py` | N/A | `PROJECTS/CIA_SIE_PURE/07_TESTING/tests/` |
| `.yml` (CI) | `.github/workflows/` | `.github/workflows/` |
| `.md` (docs) | `PROJECTS/MCI_Terminal/02_ARCHITECTURE/` | `PROJECTS/CIA_SIE_PURE/04_DOCUMENTATION/` |
| `.puml` | N/A | `04_DOCUMENTATION/02_ARCHITECTURE/diagrams/` |

---

# SECTION 8: CONSTITUTIONAL COMPLIANCE

## 8.1 Governance Hierarchy

```
LEVEL 1: Universal Taxonomy (Holy Grail Protocol)
    │
LEVEL 2: Top-Level GOVERNANCE/ folder
    │
LEVEL 3: Project-Internal 00_GOVERNANCE/ folder
    │
LEVEL 4: Application-Level Constraints (types, validation)
```

## 8.2 Change Authorization

| Change Type | Required Authorization |
|-------------|----------------------|
| New file in taxonomy folder | None (follow structure) |
| New taxonomy folder | Requires justification |
| Modify governance doc | Requires attestation |
| Modify CI workflow | Requires verification |
| Delete any file | Requires confirmation |

---

# SECTION 9: EXECUTION CONFIRMATION

## 9.1 Acknowledgment Protocol

Upon ingesting this directive, you MUST:

1. ✅ Acknowledge understanding of the Universal Taxonomy
2. ✅ Confirm awareness of both repository structures
3. ✅ Recognize the canonical file paths
4. ✅ Understand the test writing protocols
5. ✅ Accept the GitHub Actions integration requirements

## 9.2 Operational Readiness

You are now authorized to:
- Navigate the codebase using canonical paths
- Create files in appropriate taxonomy locations
- Write tests following established patterns
- Reference governance documents for constraints
- Support GitHub Actions CI/CD operations

---

# SECTION 10: AMENDMENTS LOG

| Date | Amendment | Authority |
|------|-----------|-----------|
| 2026-01-31 | Initial directive creation | Program Analyst |

---

**END OF DIRECTIVE**

*This document constitutes the authoritative operating protocol for Cursor AI within the MCI Terminal and CIA-SIE-PURE ecosystem. Compliance is mandatory.*

---

**Document Metadata:**
- Version: 1.0
- Classification: OPERATIONAL
- Distribution: Cursor AI Context
- Generated: 2026-01-31
- Protocol: The Holy Grail of Folder Rehydration
