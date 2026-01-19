# ══════════════════════════════════════════════════════════════════════════════
#
#                    PROJECT COMMISSIONING BRIEF - ADDENDUM 001
#                              KITE TOKEN CAPTURE MODULE
#
# ══════════════════════════════════════════════════════════════════════════════
#
#              Document ID: BCI-ADDENDUM-001-TOKEN-CAPTURE
#              Classification: TIER 2 — GOVERNANCE (Binding)
#              Version: 1.0.0
#              Date Issued: January 17, 2026
#              Supplements: BCI-COMMISSION-BRIEF-001 v3.0 FINAL
#              Status: APPROVED
#
# ══════════════════════════════════════════════════════════════════════════════


                    ╔═══════════════════════════════════════╗
                    ║                                       ║
                    ║     "AUTHENTICATION IS THE GATE"      ║
                    ║                                       ║
                    ║   Before any system can ignite,       ║
                    ║   the operator must be authenticated  ║
                    ║   with absolute certainty.            ║
                    ║                                       ║
                    ╚═══════════════════════════════════════╝


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                         ADDENDUM PURPOSE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

This addendum establishes the **PHASE 0: KITE TOKEN CAPTURE MODULE** as a
MANDATORY prerequisite before any other MCI operations can commence.

RATIONALE:
─────────
• Kite Connect tokens expire DAILY at 6:00 AM IST
• No automated token refresh is possible (Zerodha security policy)
• User must manually authenticate each trading day
• MCI must capture this token BEFORE Pre-Ignition Scanner can run
• Failure to capture token = COMPLETE SYSTEM BLOCKADE

INSERTION POINT:
───────────────
This module is inserted as **PHASE 0** in the MCI operational sequence:

  ┌─────────────────────────────────────────────────────────────────────────┐
  │                                                                         │
  │  REVISED MCI OPERATIONAL PHASES                                        │
  │  ═══════════════════════════════                                       │
  │                                                                         │
  │  PHASE 0: TOKEN CAPTURE ◄──── NEW (This Addendum)                      │
  │           ↓                                                             │
  │  PHASE 1: PRE-IGNITION SCANNER (existing Section 2)                    │
  │           ↓                                                             │
  │  PHASE 2: MODEL SELECTION (existing Section 3)                         │
  │           ↓                                                             │
  │  PHASE 3: IGNITION SEQUENCE (existing Section 4)                       │
  │           ↓                                                             │
  │  PHASE 4: OPERATIONAL MONITORING (existing Section 5-6)                │
  │           ↓                                                             │
  │  PHASE 5: SHUTDOWN (existing Section 7)                                │
  │                                                                         │
  └─────────────────────────────────────────────────────────────────────────┘


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    SECTION A: TOKEN CAPTURE OVERVIEW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

A.1 KITE TOKEN LIFECYCLE
─────────────────────────

  ╔═══════════════════════════════════════════════════════════════════════════╗
  ║                                                                           ║
  ║                    KITE TOKEN DAILY LIFECYCLE                             ║
  ║                                                                           ║
  ║  ┌─────────────────────────────────────────────────────────────────────┐ ║
  ║  │                                                                     │ ║
  ║  │   6:00 AM IST                              6:00 AM IST (Next Day)  │ ║
  ║  │       │                                           │                │ ║
  ║  │       ▼                                           ▼                │ ║
  ║  │   ┌───────┐                                   ┌───────┐            │ ║
  ║  │   │ TOKEN │                                   │ TOKEN │            │ ║
  ║  │   │EXPIRES│                                   │EXPIRES│            │ ║
  ║  │   └───┬───┘                                   └───────┘            │ ║
  ║  │       │                                                            │ ║
  ║  │       │  ┌──────────────────────────────────────────────────────┐ │ ║
  ║  │       │  │                                                      │ │ ║
  ║  │       └─►│           TOKEN VALID (~24 HOURS)                   │ │ ║
  ║  │          │                                                      │ │ ║
  ║  │          │  User authenticates once per day, typically at      │ │ ║
  ║  │          │  market open (8:00 AM - 9:15 AM IST)                │ │ ║
  ║  │          │                                                      │ │ ║
  ║  │          └──────────────────────────────────────────────────────┘ │ ║
  ║  │                                                                     │ ║
  ║  └─────────────────────────────────────────────────────────────────────┘ ║
  ║                                                                           ║
  ╚═══════════════════════════════════════════════════════════════════════════╝


A.2 OPERATOR DAILY WORKFLOW
────────────────────────────

  ╔═══════════════════════════════════════════════════════════════════════════╗
  ║                                                                           ║
  ║                    DAILY AUTHENTICATION WORKFLOW                          ║
  ║                    (Typical: 8:00 AM IST)                                 ║
  ║                                                                           ║
  ║  ┌─────────────────────────────────────────────────────────────────────┐ ║
  ║  │                                                                     │ ║
  ║  │  08:00 AM ─► Operator opens MCI in browser (localhost:8080)        │ ║
  ║  │      │                                                              │ ║
  ║  │      ▼                                                              │ ║
  ║  │  08:00:01 ─► MCI checks for valid Kite token                       │ ║
  ║  │      │                                                              │ ║
  ║  │      ├─► IF TOKEN VALID ─► Proceed to Pre-Ignition Scanner        │ ║
  ║  │      │                                                              │ ║
  ║  │      └─► IF TOKEN EXPIRED/MISSING ─► Show Token Capture Form      │ ║
  ║  │              │                                                      │ ║
  ║  │              ▼                                                      │ ║
  ║  │  08:00:05 ─► Operator copies Kite Login URL from MCI               │ ║
  ║  │      │                                                              │ ║
  ║  │      ▼                                                              │ ║
  ║  │  08:00:10 ─► Operator pastes URL in Chrome, logs in                │ ║
  ║  │      │                                                              │ ║
  ║  │      ▼                                                              │ ║
  ║  │  08:00:25 ─► Kite redirects to callback URL                        │ ║
  ║  │      │                                                              │ ║
  ║  │      ▼                                                              │ ║
  ║  │  08:00:30 ─► Operator copies callback URL from Chrome              │ ║
  ║  │      │                                                              │ ║
  ║  │      ▼                                                              │ ║
  ║  │  08:00:35 ─► Operator pastes URL into MCI Token Capture Form       │ ║
  ║  │      │                                                              │ ║
  ║  │      ▼                                                              │ ║
  ║  │  08:00:36 ─► MCI processes token (6-module sequence)               │ ║
  ║  │      │                                                              │ ║
  ║  │      ▼                                                              │ ║
  ║  │  08:00:38 ─► TOKEN AUTHENTICATED ─► Proceed to Pre-Ignition        │ ║
  ║  │                                                                     │ ║
  ║  │  TOTAL TIME: ~38 seconds                                           │ ║
  ║  │                                                                     │ ║
  ║  └─────────────────────────────────────────────────────────────────────┘ ║
  ║                                                                           ║
  ╚═══════════════════════════════════════════════════════════════════════════╝


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    SECTION B: TOKEN CAPTURE FORM SPECIFICATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

B.1 FORM VISUAL DESIGN
───────────────────────

  ╔═══════════════════════════════════════════════════════════════════════════╗
  ║                                                                           ║
  ║                    KITE TOKEN AUTHENTICATION                              ║
  ║                    ════════════════════════                               ║
  ║                                                                           ║
  ║  ┌─────────────────────────────────────────────────────────────────────┐ ║
  ║  │                                                                     │ ║
  ║  │  ⚠️  AUTHENTICATION REQUIRED                                        │ ║
  ║  │                                                                     │ ║
  ║  │  Your Kite token has expired or is not found.                      │ ║
  ║  │  Please follow these steps to authenticate:                        │ ║
  ║  │                                                                     │ ║
  ║  │  ═══════════════════════════════════════════════════════════════   │ ║
  ║  │                                                                     │ ║
  ║  │  STEP 1: Copy the Kite Login URL below                             │ ║
  ║  │  ───────────────────────────────────────────                       │ ║
  ║  │                                                                     │ ║
  ║  │  ┌───────────────────────────────────────────────────────────────┐ │ ║
  ║  │  │ https://kite.zerodha.com/connect/login?v=3&api_key=xxxxxxxx  │ │ ║
  ║  │  │                                                               │ │ ║
  ║  │  │                                        [📋 COPY TO CLIPBOARD] │ │ ║
  ║  │  └───────────────────────────────────────────────────────────────┘ │ ║
  ║  │                                                                     │ ║
  ║  │  STEP 2: Open Chrome and paste the URL                             │ ║
  ║  │  ───────────────────────────────────────────                       │ ║
  ║  │  Open a new Chrome tab, paste the URL, and press Enter.            │ ║
  ║  │                                                                     │ ║
  ║  │  STEP 3: Login with your Zerodha credentials                       │ ║
  ║  │  ───────────────────────────────────────────                       │ ║
  ║  │  Enter your Zerodha User ID, Password, and 2FA PIN.                │ ║
  ║  │                                                                     │ ║
  ║  │  STEP 4: Copy the FULL redirect URL from Chrome                    │ ║
  ║  │  ───────────────────────────────────────────                       │ ║
  ║  │  After login, Chrome will redirect to a URL that looks like:       │ ║
  ║  │  http://127.0.0.1:xxxx/?request_token=xxxxxxxx&action=login...     │ ║
  ║  │                                                                     │ ║
  ║  │  Copy the ENTIRE URL from Chrome's address bar.                    │ ║
  ║  │                                                                     │ ║
  ║  │  STEP 5: Paste the callback URL here                               │ ║
  ║  │  ───────────────────────────────────────────                       │ ║
  ║  │                                                                     │ ║
  ║  │  ┌───────────────────────────────────────────────────────────────┐ │ ║
  ║  │  │                                                               │ │ ║
  ║  │  │  Paste the callback URL here...                               │ │ ║
  ║  │  │                                                               │ │ ║
  ║  │  └───────────────────────────────────────────────────────────────┘ │ ║
  ║  │                                                                     │ ║
  ║  │                                                                     │ ║
  ║  │  ┌─────────────────────────────────────────────────────────────┐   │ ║
  ║  │  │                                                             │   │ ║
  ║  │  │                   🚀 AUTHENTICATE TOKEN                     │   │ ║
  ║  │  │                                                             │   │ ║
  ║  │  └─────────────────────────────────────────────────────────────┘   │ ║
  ║  │                                                                     │ ║
  ║  └─────────────────────────────────────────────────────────────────────┘ ║
  ║                                                                           ║
  ╚═══════════════════════════════════════════════════════════════════════════╝


B.2 FORM FIELD SPECIFICATIONS
──────────────────────────────

  ┌────────────────────────────────────────────────────────────────────────────┐
  │ ELEMENT                    │ SPECIFICATION                                 │
  ├────────────────────────────┼───────────────────────────────────────────────┤
  │ Kite Login URL Display     │ • Read-only text field                        │
  │                            │ • Monospace font for clarity                  │
  │                            │ • "Copy to Clipboard" button adjacent         │
  │                            │ • URL constructed from KITE_API_KEY env var   │
  │                            │ • Format: https://kite.zerodha.com/connect/   │
  │                            │   login?v=3&api_key={KITE_API_KEY}            │
  ├────────────────────────────┼───────────────────────────────────────────────┤
  │ Callback URL Input         │ • Single-line text input                      │
  │                            │ • Placeholder: "Paste the callback URL here"  │
  │                            │ • Auto-trim whitespace on paste               │
  │                            │ • Validate URL format on input                │
  │                            │ • Highlight in red if invalid format          │
  │                            │ • Highlight in green if valid format          │
  ├────────────────────────────┼───────────────────────────────────────────────┤
  │ Authenticate Button        │ • Disabled until valid URL detected           │
  │                            │ • Primary action color (cyan/blue)            │
  │                            │ • Transforms to progress indicator on click   │
  │                            │ • Displays "AUTHENTICATING..." during process │
  ├────────────────────────────┼───────────────────────────────────────────────┤
  │ Step Instructions          │ • Numbered steps 1-5                          │
  │                            │ • Clear, concise language                     │
  │                            │ • Always visible (hardcoded, not collapsible) │
  │                            │ • Monospace for URLs/technical terms          │
  └────────────────────────────────────────────────────────────────────────────┘


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    SECTION C: 6-MODULE PROCESSING ARCHITECTURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

C.1 MODULE OVERVIEW
────────────────────

  ╔═══════════════════════════════════════════════════════════════════════════╗
  ║                                                                           ║
  ║                    TOKEN AUTHENTICATION MODULES                           ║
  ║                    ═════════════════════════════                          ║
  ║                                                                           ║
  ║  ┌─────────┐   ┌─────────┐   ┌─────────┐   ┌─────────┐   ┌─────────┐   ║
  ║  │MODULE 1 │──►│MODULE 2 │──►│MODULE 3 │──►│MODULE 4 │──►│MODULE 5 │   ║
  ║  │ STATUS  │   │  FORM   │   │VALIDATE │   │EXCHANGE │   │ STORE   │   ║
  ║  │ CHECK   │   │ DISPLAY │   │   URL   │   │ TOKEN   │   │ TOKEN   │   ║
  ║  └─────────┘   └─────────┘   └─────────┘   └─────────┘   └─────────┘   ║
  ║                                                   │                       ║
  ║                                                   ▼                       ║
  ║                                            ┌─────────┐                   ║
  ║                                            │MODULE 6 │                   ║
  ║                                            │ VERIFY  │                   ║
  ║                                            │ TOKEN   │                   ║
  ║                                            └─────────┘                   ║
  ║                                                   │                       ║
  ║                                                   ▼                       ║
  ║                                            ┌─────────┐                   ║
  ║                                            │ SUCCESS │                   ║
  ║                                            │   ──►   │                   ║
  ║                                            │PRE-IGN. │                   ║
  ║                                            └─────────┘                   ║
  ║                                                                           ║
  ╚═══════════════════════════════════════════════════════════════════════════╝


C.2 MODULE SPECIFICATIONS
──────────────────────────

┌──────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  MODULE 1: TOKEN STATUS CHECK                                                │
│  ════════════════════════════                                                │
│                                                                              │
│  PURPOSE:    Determine if valid Kite token exists                           │
│  TRIGGER:    MCI application start                                          │
│  EXECUTION:  Automatic, no user interaction                                  │
│                                                                              │
│  PROCESS:                                                                    │
│  ─────────                                                                   │
│  1. Check if token file exists (~/.mci/kite_token.json)                     │
│  2. If exists, read token and expiry timestamp                              │
│  3. Calculate current time vs expiry (6:00 AM IST)                          │
│  4. Determine token state: VALID / EXPIRED / MISSING                        │
│                                                                              │
│  OUTPUTS:                                                                    │
│  ─────────                                                                   │
│  • TOKEN_VALID: Proceed to Pre-Ignition Scanner                             │
│  • TOKEN_EXPIRED: Display Token Capture Form (Module 2)                     │
│  • TOKEN_MISSING: Display Token Capture Form (Module 2)                     │
│                                                                              │
│  TIMING: < 10ms                                                              │
│                                                                              │
│  FAIL-SAFE:                                                                  │
│  ───────────                                                                 │
│  • If file read error → Treat as MISSING, show form                         │
│  • If JSON parse error → Treat as CORRUPTED, show form with warning         │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  MODULE 2: FORM DISPLAY                                                      │
│  ══════════════════════                                                      │
│                                                                              │
│  PURPOSE:    Present Token Capture Form to operator                         │
│  TRIGGER:    Module 1 returns EXPIRED or MISSING                            │
│  EXECUTION:  Render form, wait for user input                               │
│                                                                              │
│  PROCESS:                                                                    │
│  ─────────                                                                   │
│  1. Construct Kite Login URL using KITE_API_KEY                             │
│  2. Render form with 5-step instructions                                    │
│  3. Enable "Copy to Clipboard" functionality                                │
│  4. Monitor callback URL input field for changes                            │
│  5. Enable "Authenticate" button when valid URL detected                    │
│                                                                              │
│  OUTPUTS:                                                                    │
│  ─────────                                                                   │
│  • User clicks "Authenticate" → Proceed to Module 3                         │
│  • User closes form → MCI remains in TOKEN_REQUIRED state                   │
│                                                                              │
│  TIMING: User-dependent (typically 20-30 seconds)                           │
│                                                                              │
│  FAIL-SAFE:                                                                  │
│  ───────────                                                                 │
│  • If KITE_API_KEY not set → Show configuration error with instructions     │
│  • Form always visible with hardcoded steps (never auto-hidden)             │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  MODULE 3: URL VALIDATION                                                    │
│  ═════════════════════════                                                   │
│                                                                              │
│  PURPOSE:    Validate pasted callback URL and extract request_token         │
│  TRIGGER:    User clicks "Authenticate" button                              │
│  EXECUTION:  Automatic validation sequence                                   │
│                                                                              │
│  PROCESS:                                                                    │
│  ─────────                                                                   │
│  1. Trim whitespace from input                                              │
│  2. Parse URL format                                                         │
│  3. Check for required parameter: request_token                             │
│  4. Extract request_token value                                              │
│  5. Validate request_token format (alphanumeric, expected length)           │
│                                                                              │
│  OUTPUTS:                                                                    │
│  ─────────                                                                   │
│  • VALID: request_token extracted → Proceed to Module 4                     │
│  • INVALID: Validation error → Show error, return to Module 2               │
│                                                                              │
│  TIMING: < 50ms                                                              │
│                                                                              │
│  FAIL-SAFE:                                                                  │
│  ───────────                                                                 │
│  • Invalid URL format → "The URL format is incorrect. Please copy the       │
│    FULL URL from Chrome's address bar after login."                         │
│  • Missing request_token → "The URL does not contain a request token.       │
│    Please ensure you copied the URL AFTER completing the Kite login."       │
│  • Invalid token format → "The request token appears corrupted.             │
│    Please try logging in again and copy the fresh URL."                     │
│                                                                              │
│  PROGRESS INDICATOR: [████░░░░░░] 20%                                       │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  MODULE 4: TOKEN EXCHANGE                                                    │
│  ═════════════════════════                                                   │
│                                                                              │
│  PURPOSE:    Exchange request_token for access_token via Kite API           │
│  TRIGGER:    Module 3 returns VALID                                         │
│  EXECUTION:  API call to Kite Connect                                       │
│                                                                              │
│  PROCESS:                                                                    │
│  ─────────                                                                   │
│  1. Construct API request:                                                   │
│     POST https://api.kite.trade/session/token                               │
│     Body: {                                                                  │
│       api_key: KITE_API_KEY,                                                │
│       request_token: {extracted_token},                                     │
│       checksum: SHA256(KITE_API_KEY + request_token + KITE_API_SECRET)     │
│     }                                                                        │
│  2. Execute API call with 10-second timeout                                  │
│  3. Parse response for access_token                                          │
│  4. Extract additional data: user_id, user_name, etc.                       │
│                                                                              │
│  OUTPUTS:                                                                    │
│  ─────────                                                                   │
│  • SUCCESS: access_token received → Proceed to Module 5                     │
│  • FAILURE: API error → Show error, offer retry from Module 2               │
│                                                                              │
│  TIMING: 500ms - 3000ms (network dependent)                                 │
│                                                                              │
│  FAIL-SAFE:                                                                  │
│  ───────────                                                                 │
│  • Network timeout → "Unable to reach Kite servers. Please check your       │
│    internet connection and try again."                                       │
│  • Token expired → "The request token has expired. Request tokens are       │
│    valid for only 60 seconds. Please login again quickly."                  │
│  • Invalid checksum → "Authentication checksum failed. Please contact       │
│    support if this persists."                                                │
│  • API rate limit → "Too many authentication attempts. Please wait          │
│    {X} seconds before trying again."                                         │
│                                                                              │
│  PROGRESS INDICATOR: [████████░░] 60%                                       │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  MODULE 5: TOKEN STORAGE                                                     │
│  ═════════════════════════                                                   │
│                                                                              │
│  PURPOSE:    Securely store access_token for session use                    │
│  TRIGGER:    Module 4 returns SUCCESS                                       │
│  EXECUTION:  File system write operation                                    │
│                                                                              │
│  PROCESS:                                                                    │
│  ─────────                                                                   │
│  1. Create token storage directory if not exists (~/.mci/)                  │
│  2. Construct token object:                                                  │
│     {                                                                        │
│       access_token: "xxxxxxxx",                                             │
│       token_type: "Bearer",                                                 │
│       user_id: "AB1234",                                                    │
│       user_name: "NEVILLE MEHTA",                                           │
│       issued_at: "2026-01-17T08:00:36Z",                                   │
│       expires_at: "2026-01-18T06:00:00+05:30",                             │
│       expires_at_timestamp: 1737183000000                                   │
│     }                                                                        │
│  3. Write to ~/.mci/kite_token.json with restricted permissions (600)       │
│  4. Verify file written successfully                                         │
│  5. Update in-memory token cache                                             │
│                                                                              │
│  OUTPUTS:                                                                    │
│  ─────────                                                                   │
│  • SUCCESS: Token stored → Proceed to Module 6                              │
│  • FAILURE: Storage error → Show error, token held in memory only           │
│                                                                              │
│  TIMING: < 50ms                                                              │
│                                                                              │
│  FAIL-SAFE:                                                                  │
│  ───────────                                                                 │
│  • Directory creation fails → Warn user, continue with in-memory token      │
│  • File write fails → Warn user, continue with in-memory token              │
│  • Permission error → "Unable to save token securely. Token will be         │
│    valid for this session only. Please check folder permissions."           │
│                                                                              │
│  PROGRESS INDICATOR: [██████████] 80%                                       │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  MODULE 6: TOKEN VERIFICATION                                                │
│  ═════════════════════════════                                               │
│                                                                              │
│  PURPOSE:    Verify token works by making test API call                     │
│  TRIGGER:    Module 5 returns SUCCESS                                       │
│  EXECUTION:  API call to Kite Connect                                       │
│                                                                              │
│  PROCESS:                                                                    │
│  ─────────                                                                   │
│  1. Call Kite profile endpoint:                                              │
│     GET https://api.kite.trade/user/profile                                 │
│     Headers: Authorization: token KITE_API_KEY:access_token                 │
│  2. Verify HTTP 200 response                                                 │
│  3. Parse user profile data                                                  │
│  4. Confirm user_id matches stored token                                    │
│  5. Mark token as VERIFIED                                                   │
│                                                                              │
│  OUTPUTS:                                                                    │
│  ─────────                                                                   │
│  • SUCCESS: Token verified → PROCEED TO PRE-IGNITION SCANNER               │
│  • FAILURE: Verification failed → Show error, restart from Module 2        │
│                                                                              │
│  TIMING: 200ms - 1000ms (network dependent)                                 │
│                                                                              │
│  FAIL-SAFE:                                                                  │
│  ───────────                                                                 │
│  • Profile call fails → "Token verification failed. The token may have     │
│    been invalidated. Please authenticate again."                             │
│  • User mismatch → "Token belongs to different user. Please login with      │
│    the correct Zerodha account."                                             │
│                                                                              │
│  PROGRESS INDICATOR: [██████████] 100% ✓ COMPLETE                           │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    SECTION D: PROGRESS INDICATOR SPECIFICATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

D.1 VISUAL PROGRESS DISPLAY
────────────────────────────

  ╔═══════════════════════════════════════════════════════════════════════════╗
  ║                                                                           ║
  ║                    TOKEN AUTHENTICATION IN PROGRESS                       ║
  ║                                                                           ║
  ║  ┌─────────────────────────────────────────────────────────────────────┐ ║
  ║  │                                                                     │ ║
  ║  │  AUTHENTICATION SEQUENCE                                           │ ║
  ║  │  ═══════════════════════════════════════════════════════════════   │ ║
  ║  │                                                                     │ ║
  ║  │  ✅ Module 1: Status Check ────────────────────────── COMPLETE     │ ║
  ║  │     └── Token expired, authentication required                     │ ║
  ║  │                                                                     │ ║
  ║  │  ✅ Module 2: Form Submitted ──────────────────────── COMPLETE     │ ║
  ║  │     └── Callback URL received                                      │ ║
  ║  │                                                                     │ ║
  ║  │  ✅ Module 3: URL Validated ───────────────────────── COMPLETE     │ ║
  ║  │     └── Request token extracted: abc123...                        │ ║
  ║  │                                                                     │ ║
  ║  │  🔄 Module 4: Token Exchange ──────────────────────── IN PROGRESS  │ ║
  ║  │     └── Contacting Kite API...                                    │ ║
  ║  │                                                                     │ ║
  ║  │  ⏳ Module 5: Token Storage ───────────────────────── PENDING      │ ║
  ║  │                                                                     │ ║
  ║  │  ⏳ Module 6: Verification ────────────────────────── PENDING      │ ║
  ║  │                                                                     │ ║
  ║  │  ═══════════════════════════════════════════════════════════════   │ ║
  ║  │                                                                     │ ║
  ║  │  PROGRESS: [████████████████████░░░░░░░░░░░░░░░░░░░░] 55%         │ ║
  ║  │                                                                     │ ║
  ║  │  Elapsed: 1.2s                                                     │ ║
  ║  │                                                                     │ ║
  ║  └─────────────────────────────────────────────────────────────────────┘ ║
  ║                                                                           ║
  ╚═══════════════════════════════════════════════════════════════════════════╝


D.2 PROGRESS INDICATOR REQUIREMENTS
────────────────────────────────────

  ┌────────────────────────────────────────────────────────────────────────────┐
  │ REQUIREMENT                              │ SPECIFICATION                   │
  ├──────────────────────────────────────────┼─────────────────────────────────┤
  │ Update frequency                         │ 60fps minimum (16.67ms)         │
  ├──────────────────────────────────────────┼─────────────────────────────────┤
  │ Module status icons                      │ ⏳ Pending, 🔄 In Progress,     │
  │                                          │ ✅ Complete, ❌ Failed           │
  ├──────────────────────────────────────────┼─────────────────────────────────┤
  │ Progress bar                             │ Smooth animation, no jumps      │
  ├──────────────────────────────────────────┼─────────────────────────────────┤
  │ Elapsed time display                     │ Updates every 100ms             │
  ├──────────────────────────────────────────┼─────────────────────────────────┤
  │ Status messages                          │ Real-time, descriptive          │
  ├──────────────────────────────────────────┼─────────────────────────────────┤
  │ Color scheme                             │ Cyan for progress, Green for    │
  │                                          │ success, Red for failure        │
  └────────────────────────────────────────────────────────────────────────────┘


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    SECTION E: FAIL-SAFE MECHANISM
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

E.1 FAIL-SAFE PHILOSOPHY
─────────────────────────

  ╔═══════════════════════════════════════════════════════════════════════════╗
  ║                                                                           ║
  ║                    ROCKET RE-ENTRY PRINCIPLE                              ║
  ║                    ═════════════════════════                              ║
  ║                                                                           ║
  ║  "A rocket re-entering Earth's atmosphere has ONE correct angle.          ║
  ║   Too shallow = bounce off. Too steep = burn up.                          ║
  ║   There is NO partial success. Only SUCCESS or ABORT."                    ║
  ║                                                                           ║
  ║  APPLIED TO TOKEN CAPTURE:                                                ║
  ║  ─────────────────────────                                                ║
  ║                                                                           ║
  ║  • Every module has exactly TWO outcomes: SUCCESS or FAILURE              ║
  ║  • There is NO partial success                                            ║
  ║  • FAILURE triggers immediate, clear guidance                             ║
  ║  • User is NEVER left in an ambiguous state                              ║
  ║  • Retry is ALWAYS available                                              ║
  ║  • System NEVER proceeds without confirmed success                        ║
  ║                                                                           ║
  ╚═══════════════════════════════════════════════════════════════════════════╝


E.2 ERROR MESSAGE SPECIFICATIONS
─────────────────────────────────

  ╔═══════════════════════════════════════════════════════════════════════════╗
  ║                                                                           ║
  ║  ⚠️  AUTHENTICATION FAILED                                                 ║
  ║  ═══════════════════════════                                              ║
  ║                                                                           ║
  ║  ┌─────────────────────────────────────────────────────────────────────┐ ║
  ║  │                                                                     │ ║
  ║  │  WHAT HAPPENED:                                                    │ ║
  ║  │  ───────────────                                                   │ ║
  ║  │  The request token could not be exchanged for an access token.     │ ║
  ║  │                                                                     │ ║
  ║  │  LIKELY CAUSE:                                                     │ ║
  ║  │  ──────────────                                                    │ ║
  ║  │  Request tokens expire within 60 seconds of generation.            │ ║
  ║  │  You may have taken too long between login and pasting the URL.    │ ║
  ║  │                                                                     │ ║
  ║  │  HOW TO FIX:                                                       │ ║
  ║  │  ────────────                                                      │ ║
  ║  │  1. Click "Try Again" below                                        │ ║
  ║  │  2. Copy the login URL                                             │ ║
  ║  │  3. Login quickly in Chrome (within 30 seconds)                    │ ║
  ║  │  4. Copy and paste the callback URL immediately                    │ ║
  ║  │                                                                     │ ║
  ║  │  ┌─────────────────┐            ┌─────────────────┐               │ ║
  ║  │  │   ↩️ TRY AGAIN   │            │   ❌ CANCEL      │               │ ║
  ║  │  └─────────────────┘            └─────────────────┘               │ ║
  ║  │                                                                     │ ║
  ║  └─────────────────────────────────────────────────────────────────────┘ ║
  ║                                                                           ║
  ╚═══════════════════════════════════════════════════════════════════════════╝


E.3 ERROR RECOVERY MATRIX
──────────────────────────

  ┌────────────────────────────────────────────────────────────────────────────┐
  │ ERROR TYPE                   │ RECOVERY ACTION                             │
  ├──────────────────────────────┼─────────────────────────────────────────────┤
  │ Invalid URL format           │ Return to form, highlight input field       │
  ├──────────────────────────────┼─────────────────────────────────────────────┤
  │ Missing request_token        │ Return to form, explain what to copy        │
  ├──────────────────────────────┼─────────────────────────────────────────────┤
  │ Token expired (60s limit)    │ Return to form, emphasize speed             │
  ├──────────────────────────────┼─────────────────────────────────────────────┤
  │ Network error                │ Show retry button, check connection         │
  ├──────────────────────────────┼─────────────────────────────────────────────┤
  │ API rate limit               │ Show countdown timer, auto-retry            │
  ├──────────────────────────────┼─────────────────────────────────────────────┤
  │ Invalid credentials          │ Return to form, verify Kite account         │
  ├──────────────────────────────┼─────────────────────────────────────────────┤
  │ Storage permission error     │ Warn but continue with in-memory token      │
  ├──────────────────────────────┼─────────────────────────────────────────────┤
  │ Verification failed          │ Restart entire sequence                      │
  └────────────────────────────────────────────────────────────────────────────┘


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    SECTION F: INTEGRATION WITH MCI PHASES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

F.1 COMPLETE MCI OPERATIONAL FLOW
──────────────────────────────────

  ╔═══════════════════════════════════════════════════════════════════════════╗
  ║                                                                           ║
  ║                    MCI COMPLETE OPERATIONAL FLOW                          ║
  ║                    ═════════════════════════════                          ║
  ║                                                                           ║
  ║  ┌─────────────────────────────────────────────────────────────────────┐ ║
  ║  │                                                                     │ ║
  ║  │                         MCI STARTUP                                │ ║
  ║  │                              │                                     │ ║
  ║  │                              ▼                                     │ ║
  ║  │  ┌──────────────────────────────────────────────────────────────┐ │ ║
  ║  │  │ PHASE 0: TOKEN CAPTURE                                       │ │ ║
  ║  │  │ ══════════════════════                                       │ │ ║
  ║  │  │ • Check for valid Kite token                                 │ │ ║
  ║  │  │ • If expired/missing → Token Capture Form                    │ │ ║
  ║  │  │ • 6-module authentication sequence                           │ │ ║
  ║  │  │ • SUCCESS required to proceed                                │ │ ║
  ║  │  └──────────────────────────────────────────────────────────────┘ │ ║
  ║  │                              │                                     │ ║
  ║  │                              ▼                                     │ ║
  ║  │  ┌──────────────────────────────────────────────────────────────┐ │ ║
  ║  │  │ PHASE 1: PRE-IGNITION SCANNER                                │ │ ║
  ║  │  │ ═════════════════════════════                                │ │ ║
  ║  │  │ • 12 system verification checks                              │ │ ║
  ║  │  │ • Kite token check (#4) now GUARANTEED valid                 │ │ ║
  ║  │  │ • < 500ms total execution                                    │ │ ║
  ║  │  │ • ALL GREEN required to proceed                              │ │ ║
  ║  │  └──────────────────────────────────────────────────────────────┘ │ ║
  ║  │                              │                                     │ ║
  ║  │                              ▼                                     │ ║
  ║  │  ┌──────────────────────────────────────────────────────────────┐ │ ║
  ║  │  │ PHASE 2: MODEL SELECTION                                     │ │ ║
  ║  │  │ ════════════════════════                                     │ │ ║
  ║  │  │ • Select Anthropic Claude model                              │ │ ║
  ║  │  │ • View budget status                                         │ │ ║
  ║  │  │ • Model selection required to proceed                        │ │ ║
  ║  │  └──────────────────────────────────────────────────────────────┘ │ ║
  ║  │                              │                                     │ ║
  ║  │                              ▼                                     │ ║
  ║  │  ┌──────────────────────────────────────────────────────────────┐ │ ║
  ║  │  │ PHASE 3: IGNITION SEQUENCE                                   │ │ ║
  ║  │  │ ══════════════════════════                                   │ │ ║
  ║  │  │ • 3-second countdown                                         │ │ ║
  ║  │  │ • Sequential subsystem startup                               │ │ ║
  ║  │  │ • Progress bars for each component                           │ │ ║
  ║  │  └──────────────────────────────────────────────────────────────┘ │ ║
  ║  │                              │                                     │ ║
  ║  │                              ▼                                     │ ║
  ║  │  ┌──────────────────────────────────────────────────────────────┐ │ ║
  ║  │  │ PHASE 4: OPERATIONAL MONITORING                              │ │ ║
  ║  │  │ ═══════════════════════════════                              │ │ ║
  ║  │  │ • Real-time telemetry dashboard                              │ │ ║
  ║  │  │ • Token countdown timer                                      │ │ ║
  ║  │  │ • System health indicators                                   │ │ ║
  ║  │  └──────────────────────────────────────────────────────────────┘ │ ║
  ║  │                              │                                     │ ║
  ║  │                              ▼                                     │ ║
  ║  │  ┌──────────────────────────────────────────────────────────────┐ │ ║
  ║  │  │ PHASE 5: SHUTDOWN                                            │ │ ║
  ║  │  │ ═════════════════                                            │ │ ║
  ║  │  │ • Graceful or Emergency shutdown                             │ │ ║
  ║  │  │ • Resource cleanup                                           │ │ ║
  ║  │  │ • Session logging                                            │ │ ║
  ║  │  └──────────────────────────────────────────────────────────────┘ │ ║
  ║  │                                                                     │ ║
  ║  └─────────────────────────────────────────────────────────────────────┘ ║
  ║                                                                           ║
  ╚═══════════════════════════════════════════════════════════════════════════╝


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    SECTION G: TECHNICAL IMPLEMENTATION REFERENCE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

G.1 FILE STRUCTURE
───────────────────

  ┌────────────────────────────────────────────────────────────────────────────┐
  │                                                                            │
  │  03_IMPLEMENTATION/mci/src/                                               │
  │  │                                                                         │
  │  ├── server/                                                               │
  │  │   ├── services/                                                        │
  │  │   │   └── kite.ts              ◄── Token Capture Module (Backend)     │
  │  │   │       ├── checkTokenStatus()     - Module 1                       │
  │  │   │       ├── generateLoginURL()     - Module 2 support               │
  │  │   │       ├── validateCallbackURL()  - Module 3                       │
  │  │   │       ├── exchangeToken()        - Module 4                       │
  │  │   │       ├── storeToken()           - Module 5                       │
  │  │   │       └── verifyToken()          - Module 6                       │
  │  │   │                                                                    │
  │  │   └── routes/                                                          │
  │  │       └── auth.ts              ◄── Token Capture API Routes           │
  │  │           ├── GET /api/auth/status                                    │
  │  │           ├── GET /api/auth/login-url                                 │
  │  │           └── POST /api/auth/capture-token                            │
  │  │                                                                         │
  │  └── client/                                                               │
  │      └── components/                                                      │
  │          └── TokenCaptureForm.tsx  ◄── Token Capture UI Component        │
  │              ├── StepInstructions                                        │
  │              ├── LoginURLDisplay                                         │
  │              ├── CallbackURLInput                                        │
  │              ├── AuthenticateButton                                      │
  │              └── ProgressIndicator                                       │
  │                                                                            │
  └────────────────────────────────────────────────────────────────────────────┘


G.2 ENVIRONMENT VARIABLES REQUIRED
───────────────────────────────────

  ┌────────────────────────────────────────────────────────────────────────────┐
  │ VARIABLE              │ PURPOSE                          │ EXAMPLE         │
  ├───────────────────────┼──────────────────────────────────┼─────────────────┤
  │ KITE_API_KEY          │ Kite Connect API Key             │ xxxxxxxxxx      │
  ├───────────────────────┼──────────────────────────────────┼─────────────────┤
  │ KITE_API_SECRET       │ Kite Connect API Secret          │ xxxxxxxxxx      │
  ├───────────────────────┼──────────────────────────────────┼─────────────────┤
  │ MCI_TOKEN_STORAGE_PATH│ Token storage directory          │ ~/.mci/         │
  └────────────────────────────────────────────────────────────────────────────┘


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    DOCUMENT CONTROL
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

VERSION HISTORY
────────────────

  ┌────────────────────────────────────────────────────────────────────────────┐
  │ Version │ Date       │ Author     │ Changes                               │
  ├─────────┼────────────┼────────────┼───────────────────────────────────────┤
  │ 1.0.0   │ 2026-01-17 │ Cowork AI  │ Initial release - Token Capture       │
  │         │            │            │ Module specification                  │
  └────────────────────────────────────────────────────────────────────────────┘


APPROVAL
─────────

  ┌────────────────────────────────────────────────────────────────────────────┐
  │                                                                            │
  │  DOCUMENT APPROVAL                                                        │
  │                                                                            │
  │  Technical Authority: ________________________  Date: 2026-01-17          │
  │                                                                            │
  │  Project Owner:       ________________________  Date: ____________        │
  │                                                                            │
  └────────────────────────────────────────────────────────────────────────────┘


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

                              END OF ADDENDUM 001

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
