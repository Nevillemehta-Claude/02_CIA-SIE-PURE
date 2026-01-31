# CIA-SIE-PURE - PROJECT TAXONOMY & CANONICAL STRUCTURE

## FOR AI/CURSOR INGESTION

This document provides a complete map of the CIA-SIE-PURE project structure following the Universal Taxonomy from The Holy Grail of Folder Rehydration Protocol.

---

## PROJECT IDENTITY

| Attribute | Value |
|-----------|-------|
| **Project Name** | CIA-SIE-PURE (Competitive Intelligence & Analysis - Signal Intelligence Engine) |
| **Location** | `/Users/nevillemehta/Downloads/02_CIA-SIE-PURE/` |
| **Total Files** | 9,459 |
| **Primary Language** | Python |
| **Framework** | FastAPI |
| **GitHub** | https://github.com/Nevillemehta-Claude/02_CIA-SIE-PURE |

---

## UNIVERSAL TAXONOMY STRUCTURE

```
02_CIA-SIE-PURE/
│
├── GOVERNANCE/                    [6 files] - Authority & Control Documents
├── PROJECTS/                      [9,443 files] - Main Project Code & Docs
├── DOCUMENTATION/                 [5 files] - Technical Documentation
├── ASSETS/                        [catalog] - Diagram Catalogs
├── DATA/                          [catalog] - Database Catalogs
├── ARCHIVES/                      [empty] - Compressed/Backup Files
├── EXECUTABLES/                   [catalog] - Script Catalogs
├── COMMUNICATIONS/                [empty] - Transcripts & Records
├── RESEARCH/                      [empty] - Research Materials
├── TEMPLATES/                     [catalog] - Template Catalogs
├── UNCLASSIFIED/                  [empty] - Uncategorized Items
│
├── MASTER_INDEX.md                - Complete repository overview
├── GOVERNANCE_INDEX.md            - Governance document catalog
├── MIGRATION_LOG.md               - Rehydration audit trail
└── ASSET_MANIFEST.csv             - Reversibility registry
```

---

## DETAILED FOLDER BREAKDOWN

### 1. GOVERNANCE/ (Authority Documents)

Purpose: High-level directives, principles, and governance frameworks.

```
GOVERNANCE/
├── 01_Directives/         - Master ecosystem synthesis
├── 02_Principles/         - Constitutional principles (CR-001+)
├── 04_Standards/          - Gold standard conformance, failure taxonomy
└── 05_Frameworks/         - State transitions, reconstruction blueprint
```

**Key Files:**
- Constitutional rules and principles
- Gold standard conformance charts
- State transition authority tables
- Failure taxonomy standards

---

### 2. PROJECTS/CIA_SIE_PURE/ (Main Project)

Purpose: Complete Python backend application.

```
PROJECTS/CIA_SIE_PURE/
│
├── .git/                          - Git repository
├── .github/workflows/             - CI/CD pipelines
├── .venv/                         [8,095 files] - Python virtual environment
│
├── 00_GOVERNANCE/                 - Project-internal governance
│   ├── Certifications
│   ├── Attestations
│   └── Standards documents
│
├── 02_CRITICAL_DOCUMENTS/         - Essential architecture specs
│
├── 04_DOCUMENTATION/              [287 files] - Comprehensive docs
│   ├── 01_GOVERNANCE/
│   │   ├── GOLD_STANDARD_FRAMEWORK.md
│   │   ├── FINANCIAL_SERVICES_ADAPTER.md
│   │   ├── CROSS_CUTTING_CONCERNS.md
│   │   └── decisions/             - ADR documents
│   │       ├── ADR-001_Data_Repository_Model.md
│   │       ├── ADR-002_Self_Contained_Workspace.md
│   │       └── ADR-003_AI_Model_Selection.md
│   │
│   ├── 02_ARCHITECTURE/
│   │   ├── BACKEND_ARCHITECTURE.md
│   │   ├── FRONTEND_DATA_FLOW.md
│   │   ├── INTEGRATION_ARCHITECTURE.md
│   │   ├── BACKEND_FLOWCHARTS.md
│   │   ├── DATA_TYPES_REFERENCE.md
│   │   └── diagrams/              [14 PlantUML files]
│   │       ├── system_architecture.puml
│   │       ├── constitutional_rules.puml
│   │       ├── ai_narrative_flow.puml
│   │       ├── entity_relationship.puml
│   │       ├── signal_ingestion_flow.puml
│   │       ├── api_endpoints.puml
│   │       ├── contradiction_detection.puml
│   │       ├── user_journey.puml
│   │       └── kite_oauth_flow.puml
│   │
│   ├── 03_SPECIFICATIONS/
│   │   ├── FRONTEND_TECH_SPEC.md
│   │   ├── ICD_FRONTEND_BUILD.md
│   │   ├── ICD_VERIFICATION_REPORT.md
│   │   └── design/
│   │       ├── CIA-SIE_REMEDIATION_PROTOCOL_v3.0.md
│   │       ├── CIA-SIE_REMEDIATION_PROTOCOL_v4.0_HITL.md
│   │       └── CIA-SIE_MISSION_CONTROL_CONSOLE_SPECIFICATION_v1_0.md
│   │
│   ├── 04_AI_HANDOFF/
│   │   └── prompts/
│   │       ├── CURSOR_PROMPT.md
│   │       ├── PROJECT_CONFIGURATION.md
│   │       └── V0_COMPONENT_PROMPTS.md
│   │
│   ├── 06_AUDITS/
│   │   ├── PROJECT_MATURITY_AUDIT.md
│   │   ├── handoff_audit/
│   │   └── migration/
│   │
│   ├── 07_TESTING/                - Test documentation
│   ├── 08_OPERATIONS/             - Operational guides
│   │
│   ├── mission-control/
│   │   ├── MCC_GENESIS_BUILD_SPECIFICATION.md
│   │   ├── MCC_HITL_APPROVAL_GATES.md
│   │   ├── MCC_GUI_MOCKUP_REQUIREMENTS.md
│   │   └── CURSOR_HANDOFF_PROTOCOL.md
│   │
│   └── QA_KNOWLEDGE_BASE/         - Q&A documentation
│
├── 06_SOURCE_CODE/                - MAIN PYTHON CODEBASE
│   ├── alembic/                   - Database migrations
│   │   ├── env.py
│   │   ├── script.py.mako
│   │   └── versions/
│   │       ├── 20251230_0001_initial_schema.py
│   │       └── 20251231_1004_add_ai_tables.py
│   │
│   ├── src/cia_sie/               - Main Python package
│   │   ├── __init__.py
│   │   ├── main.py                - FastAPI application entry
│   │   │
│   │   ├── api/                   - API layer
│   │   │   ├── __init__.py
│   │   │   └── routes/
│   │   │       ├── narratives.py
│   │   │       └── relationships.py
│   │   │
│   │   ├── ai/                    - AI integration
│   │   │   └── __init__.py
│   │   │
│   │   ├── bridge/                - External integrations
│   │   │   └── __init__.py
│   │   │
│   │   ├── core/                  - Core business logic
│   │   │   └── __init__.py
│   │   │
│   │   ├── dal/                   - Data Access Layer
│   │   │   └── __init__.py
│   │   │
│   │   ├── exposure/              - Signal exposure detection
│   │   │   ├── __init__.py
│   │   │   ├── confirmation_detector.py
│   │   │   └── contradiction_detector.py
│   │   │
│   │   ├── ingestion/             - Signal ingestion
│   │   │   ├── __init__.py
│   │   │   └── signal_normalizer.py
│   │   │
│   │   └── platforms/             - Platform adapters
│   │       └── __init__.py
│   │
│   ├── scripts/                   - Utility scripts
│   │   ├── launcher/              [5 shell scripts]
│   │   └── *.py                   - Python utilities
│   │
│   └── alembic.ini                - Alembic config
│
├── 07_TESTING/                    [1,016 tests] - Test Suite
│   ├── tests/
│   │   ├── unit/                  [28 test files]
│   │   │   ├── test_response_validator.py
│   │   │   ├── test_constitutional_compliance.py
│   │   │   ├── test_relationship_exposer.py
│   │   │   ├── test_exposure.py
│   │   │   ├── test_kite_adapter.py
│   │   │   ├── test_usage_tracker.py
│   │   │   ├── test_dal_repositories.py
│   │   │   ├── test_tradingview_adapter.py
│   │   │   ├── test_signal_normalizer.py
│   │   │   ├── test_confirmation_detector.py
│   │   │   ├── test_contradiction_detector.py
│   │   │   ├── test_narrative_generator.py
│   │   │   ├── test_prompt_builder.py
│   │   │   ├── test_claude_client.py
│   │   │   └── ... more unit tests
│   │   │
│   │   ├── integration/           [3 test files]
│   │   │   ├── conftest.py
│   │   │   └── __init__.py
│   │   │
│   │   ├── constitutional/        [5 test files]
│   │   ├── backend/               [8 test files]
│   │   ├── e2e/                   [3 test files]
│   │   └── chaos/                 [3 test files]
│   │
│   └── pytest.ini / conftest.py
│
├── 08_DATA/                       - Data storage
│   └── data/                      [4 SQLite databases]
│
├── 09_LOGS_AND_HISTORY/           - Session logs
│
├── 10_UTILITIES/                  [3 files] - Utility scripts
│   ├── generate_chronicle.py
│   ├── seed_sample_data.py
│   └── extract_chat_history.py
│
├── 99_ARCHIVE/                    - Archived configurations
│
├── .gitignore
├── .remediation-baseline
├── .remediation-env
├── pyproject.toml                 - Python project config
└── requirements.txt               - Python dependencies
```

---

### 3. DOCUMENTATION/ (Technical Docs)

```
DOCUMENTATION/
└── Technical/                     [5 files]
    ├── Certification reports
    ├── Determinism reports
    └── Readiness reports
```

---

### 4. ASSETS/ (Diagram Catalogs)

```
ASSETS/
└── Diagrams/DIAGRAM_CATALOG.md    - 14 PlantUML diagrams cataloged
```

---

### 5. DATA/ (Database Catalogs)

```
DATA/
└── Serialized/DATABASE_CATALOG.md - 4 SQLite databases cataloged
```

---

### 6. EXECUTABLES/ (Script Catalogs)

```
EXECUTABLES/
└── Binaries/SCRIPT_CATALOG.md     - 10 shell scripts cataloged
```

---

### 7. TEMPLATES/ (Template Catalogs)

```
TEMPLATES/
└── TEMPLATE_CATALOG.md            - 13 Mako templates cataloged
```

---

## KEY FILE TYPES & LOCATIONS

| File Type | Count | Primary Location |
|-----------|-------|------------------|
| `.py` | 200+ | PROJECTS/.../06_SOURCE_CODE, 07_TESTING |
| `.md` | 287 | GOVERNANCE, DOCUMENTATION, PROJECTS |
| `.puml` | 14 | PROJECTS/.../04_DOCUMENTATION/02_ARCHITECTURE/diagrams |
| `.db/.sqlite` | 4 | PROJECTS/.../08_DATA/data |
| `.sh` | 10 | PROJECTS/.../06_SOURCE_CODE/scripts |
| `.mako` | 13 | PROJECTS/.../alembic |

---

## APPLICATION ARCHITECTURE

### Backend (Python + FastAPI)
- **Framework:** FastAPI
- **ORM:** SQLAlchemy
- **Migrations:** Alembic
- **AI Integration:** Claude/Anthropic API
- **Testing:** pytest

### Core Modules

1. **api/** - REST API endpoints
   - Narratives generation
   - Relationship mapping

2. **ai/** - AI/LLM integration
   - Claude client
   - Prompt building
   - Response validation

3. **exposure/** - Signal analysis
   - Confirmation detection
   - Contradiction detection

4. **ingestion/** - Data ingestion
   - Signal normalization
   - Platform adapters

5. **dal/** - Data Access Layer
   - Repository pattern
   - SQLAlchemy models

6. **bridge/** - External integrations
   - Kite API adapter
   - TradingView adapter

### Constitutional Rules (CR)
- CR-001+: Core principles governing AI behavior
- All responses must comply with constitutional constraints
- Validation layer enforces compliance

---

## NAVIGATION QUICK REFERENCE

| Looking for... | Go to... |
|----------------|----------|
| FastAPI app | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/main.py` |
| API routes | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/api/routes/` |
| AI integration | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/ai/` |
| Signal processing | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/exposure/` |
| Database models | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/src/cia_sie/dal/` |
| Unit tests | `PROJECTS/CIA_SIE_PURE/07_TESTING/tests/unit/` |
| Migrations | `PROJECTS/CIA_SIE_PURE/06_SOURCE_CODE/alembic/versions/` |
| Architecture diagrams | `PROJECTS/CIA_SIE_PURE/04_DOCUMENTATION/02_ARCHITECTURE/diagrams/` |
| Governance docs | `GOVERNANCE/` or `PROJECTS/CIA_SIE_PURE/00_GOVERNANCE/` |
| AI prompts | `PROJECTS/CIA_SIE_PURE/04_DOCUMENTATION/04_AI_HANDOFF/prompts/` |

---

## IMPORTANT CONVENTIONS

1. **Constitutional compliance:** All AI outputs validated against CR rules
2. **Repository pattern:** Data access through DAL repositories
3. **Signal flow:** Ingestion → Normalization → Exposure → Narrative
4. **Governance-first:** All changes require attestation/certification
5. **Dual governance:** Top-level GOVERNANCE/ + project-internal 00_GOVERNANCE/
6. **HITL gates:** Human-in-the-loop approval gates for critical operations

---

## INTEGRATION WITH MCI TERMINAL

CIA-SIE-PURE serves as the **backend intelligence engine** for MCI Terminal:

| MCI Terminal (Frontend) | CIA-SIE-PURE (Backend) |
|-------------------------|------------------------|
| React UI | FastAPI REST API |
| User interactions | Signal processing |
| Display narratives | Generate narratives |
| Show relationships | Analyze relationships |
| Telemetry dashboard | Market data ingestion |

**Communication:** REST API calls from MCI Terminal to CIA-SIE-PURE endpoints.

---

*Generated for Cursor AI ingestion - 2026-01-31*
*Protocol: The Holy Grail of Folder Rehydration*
