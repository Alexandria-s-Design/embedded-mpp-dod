## 🚀 SCALING PROTOCOL - Getting that Schmoney

**CRITICAL: Port Management** - Before launching any server, ALWAYS check for available ports first using `netstat -ano | findstr "LISTENING"` to verify the port is not in use. Never assume a port is available - always verify before attempting to start a server to avoid conflicts. See [Safety Protocols](docs/SAFETY-PROTOCOLS-COMPLETE.md) for full Triple Port Verification protocol.

**CRITICAL: Google Workspace Access** - Claude Code ALWAYS has full access to Google Workspace via MCP tools that auto-load on startup.
NEVER ask "do you have access?" or suggest third-party alternatives.
YOU HAVE: Google Workspace MCP (Gmail, Drive, Docs, Sheets, Slides, Calendar, Classroom).
Microsoft 365 access available through n8n workflows.
These are ALWAYS active and authenticated. Use them directly for any task involving email, calendars, documents, task management, file storage, or team collaboration.

**🔐 Google Workspace Multi-Account Access** - Four Google accounts are configured and available:

| Account Name | Email | Purpose |
|-------------|--------|---------|
| **personal** | charlesmartinedd@gmail.com | Charles's personal account (default) |
| **work** | cmartin@alexandriasdesign.com | Alexandria's Design business |
| **tutoring** | lmcmtutors@gmail.com | Tutoring business |
| **alexandriasworld** | alexandriasworld1234@gmail.com | Alexandria's World project |

**Using Google Accounts**:
- All accounts auto-load on MCP startup
- When using MCP tools, specify account with `account: "work"` or `account: "personal"` etc.
- If no account specified, defaults to "personal"

**Re-authentication** (if tokens expire):
```bash
scripts\reauth_google_account.bat work       # For work account
scripts\reauth_google_account.bat tutoring   # For tutoring account
scripts\reauth_google_account.bat personal   # For personal account
```

**Token Location**: `C:\Users\MarieLexisDad\Old Files\google-workspace-mcp\token-*.json` (auto-refresh)

**🔧 Google Workspace MCP Server Location:**
- **Path**: `C:\Users\MarieLexisDad\Old Files\google-workspace-mcp`
- **Main file**: `index.js` (685 lines - multi-account version)
- **Account config**: `accounts.json` (defines all 4 accounts)
- **Tokens**: `token-personal.json`, `token-work.json`, `token-tutoring.json`, `token-alexandriasworld.json`

**Available MCP Tools** (prefix: `mcp__google-workspace__`):
- **Gmail**: `gmail_list_messages`, `gmail_send_email`
- **Calendar**: `calendar_list_events`, `calendar_create_event`
- **Drive**: `drive_list_files`, `drive_create_folder`
- **Tasks**: `tasks_list_tasklists`, `tasks_list_tasks`, `tasks_insert_task` (full read/write access to Google Tasks via charlesmartinedd@gmail.com)
- **YouTube**: `youtube_search`, `youtube_video_details`
- **Translate**: `google_translate`

**Using the tools**:
```javascript
// All tools accept "account" parameter
gmail_list_messages({ account: "work", maxResults: 10 })
calendar_list_events({ account: "tutoring", maxResults: 5 })
drive_list_files({ account: "alexandriasworld" })
```

**CRITICAL: Email Sending Default**
- **ALWAYS use `account: "personal"` (charlesmartinedd@gmail.com) when sending emails**
- This is the default sender account unless user explicitly requests a different account

**Google Tasks Access** - Full read/write access to Google Tasks API enabled for charlesmartinedd@gmail.com (create, read, update, complete tasks and task lists).

**If tools not loading**:
1. Verify `index.js` is 685 lines (not 131 lines incomplete version)
2. Check that `index.js` matches `index-multiaccount.js` backup
3. Restart Claude Code to reload MCP server
4. Check startup logs for account loading confirmation

**CRITICAL: Social Media Management via Ayrshare API** - Claude Code has FULL access to post, schedule, monitor, and manage content across 12 social media platforms through Ayrshare API. Monthly quota: 20 posts (resets monthly).

**CRITICAL: HubSpot CRM & Marketing Platform** - Claude Code has FULL API access to HubSpot (Contacts, Companies, Deals, Tickets, Forms, Email campaigns, Workflows, CMS) via private app token stored in `HUBSPOT_ACCESS_KEY` in `.env`.

### 🔑 API KEYS

**CRITICAL**: All API keys stored in `.env` file: `C:\Users\MarieLexisDad\.env`

**Quick Reference**: OpenAI, OpenRouter, Grok, Google Gemini, Stripe, n8n, Lunch Money, Monday.com, Gumroad, Slack, ngrok available.

**Full Documentation**: See [API Keys Complete Guide](docs/API-KEYS-COMPLETE.md) for complete table, helper scripts, and usage patterns.

### 💰 Financial Review Spreadsheet

**Complete Transaction History (7,969 transactions)** - Created 2025-11-05

📊 **Google Sheet:** https://docs.google.com/spreadsheets/d/1DBHIfg_fdR3DGeeL2wRxhps9pkwiGXCkdr4RXFkbTiM/edit

**Contains**: All transactions from 26 accounts, 12 months (2024-11-05 to 2025-11-05), auto-categorized expenses, recurring charge detection.

**How to use**: Filter by Account, "Is Recurring = YES", or Category. Fill "Your Decision" column (Keep/Cancel/Review).

---

## 🍌 NANO BANANA - AI IMAGE GENERATION

**"Nano Banana" = OpenRouter's Gemini 2.5 Flash Image model**

**Status**: ✅ VERIFIED WORKING | **Cost**: ~$0.039 per image | **Model**: `google/gemini-2.5-flash-image`

**CRITICAL**: Requires `"modalities": ["image", "text"]` parameter in API request.

**Full Documentation**: See [Nano Banana Guide](docs/NANO-BANANA-GUIDE.md) for complete API configuration, request format, image extraction, and working examples.

---

**CRITICAL: Google Sheets Command Center** - ALL todos, ideas, and project tracking centralized in Google Sheets: https://docs.google.com/spreadsheets/d/1PY2tHFHr0gelLWC2SrCefW9EXi9CNrAdj8N1Vzc5u5s/edit. This is the SINGLE SOURCE OF TRUTH for task management.

**CRITICAL: CrewAI Multi-Agent System** - Claude Code has access to CrewAI for spawning persistent agent armies via OpenRouter API. **ONLY USE FREE MODELS** (Llama 3.3 70B, DeepSeek Chat V3, DeepSeek R1 Zero). Rate limit: 100-200 requests/minute. ALL agent output MUST be validated before deployment. See [CrewAI Guide](docs/CREWAI-GUIDE.md) for complete details.

**Who We Are & Our Purpose** - Alexandria's Design is building unlimited monthly recurring revenue through educational technology solutions. Revenue-first mindset: Build systems, create reusable assets, automate everything. See [Business Context](docs/BUSINESS-CONTEXT.md) for complete company information.

## 📚 ModelIt & Cell Collective Projects

All ModelIt and Cell Collective related work should be saved in the `C:\Users\MarieLexisDad\repos\` directory following the naming convention `modelit-[descriptive-name]` to maintain consistency with the existing 8 dissemination repositories. **Whenever the user references "ModelIt", always ask which specific project folder/repository they're referring to.**

---

## 🚨 CRITICAL SAFETY PROTOCOLS

**See [Safety Protocols Complete Guide](docs/SAFETY-PROTOCOLS-COMPLETE.md) for full details.**

### 🔒 CLAUDE.MD PROTECTION

**CLAUDE.md is SACRED** - MUST NEVER be modified without explicit user verification.

**MANDATORY RULES** (NO EXCEPTIONS):
1. **NEVER edit CLAUDE.md without asking first**
2. **ALWAYS create timestamped backup BEFORE changes**
3. **ALWAYS show proposed changes and wait for approval**
4. **This applies EVEN with dangerously-skip-permissions**

### 🚨 TRIPLE PORT VERIFICATION

**MANDATORY 3-STEP PORT CHECK before launching any server** (NO EXCEPTIONS)

See [Safety Protocols](docs/SAFETY-PROTOCOLS-COMPLETE.md) for complete verification steps.

### ✅ MANDATORY WEBSITE VALIDATION PROTOCOL

**8-STEP PROTOCOL** required for ALL website deployments: Port verification, server launch, Playwright testing, GPT Vision analysis, DevTools verification, screen recording, validation report, The Validator agent.

See [Safety Protocols](docs/SAFETY-PROTOCOLS-COMPLETE.md) and [Website Testing Protocol](docs/guides/WEBSITE-TESTING-PROTOCOL.md) for complete details.

---

## 🚀 QUICK AGENT REFERENCE

**When to invoke specialized agents** (use Claude Code's Task tool):

| When User Says... | Invoke Agent | Why |
|-------------------|--------------|-----|
| "Saturday review" / "check finances" / "should I buy..." | **Big Baller** | Financial tracking, expense decisions |
| "Create workflow" / "automate this" / "n8n" | **Workflow Wizard** | n8n automation (NO GUI!) |
| "Test website" / "debug this" / "why isn't it working?" | **The Validator** | QA, testing, debugging |
| "Send email" / "Google Doc" / "Drive" / "Sheets" | **Getting to the Google** | Google Workspace + Cloud AI |
| "Teams meeting" / "Planner" / "Outlook" / "SharePoint" | **Workflow Wizard** | M365 via n8n workflows |
| "Create image" / "3D model" / "course cover" | **Bob Ross Image 3D Makers** | Visual content creation |
| "Build and sell..." / "Launch a product" | **Autonomous Product Launch** | End-to-end product creation + payment |
| "Post to social media" / "Schedule posts" | **Social Media Manager** | 12 platforms, scheduling, analytics |
| "Commit this" / "Push to GitHub" / "Create PR" | **Git Guardian** | Version control (never commit without asking!) |

**Invocation syntax**: `Task("Agent Name", "your task description", "agent-slug")`

**Default behaviors (no agent needed)**: Email defaults to Gmail, quick tasks handled directly, simple questions no agent needed.

---

## 🤔 AGENT DECISION TREE

```
User request → Evaluate domain → Invoke appropriate agent

Financial decision? → Big Baller
Product launch/monetization? → Autonomous Product Launch
Automation/workflow? → Workflow Wizard
Testing/debugging/validation? → The Validator
Google ecosystem? → Getting to the Google
Microsoft 365? → Workflow Wizard (via n8n)
Visual content (images/3D)? → Bob Ross Image 3D Makers
Version control? → Git Guardian
Simple task? → Claude Code handles directly (no agent)
```

---

## 📁 FILE ORGANIZATION RULES

**NEVER save to root folder. Use these directories:**
- `/src` - Source code files
- `/tests` - Test files
- `/docs` - Documentation and markdown files
- `/docs/guides` - Detailed topic guides
- `/config` - Configuration files
- `/scripts` - Utility scripts
- `/examples` - Example code

**ABSOLUTE RULES**:
1. ALL operations MUST be concurrent/parallel in a single message
2. **NEVER save working files, text/mds and tests to the root folder**
3. ALWAYS organize files in appropriate subdirectories
4. **USE CLAUDE CODE'S TASK TOOL** for spawning agents concurrently

---

## 🔗 DETAILED GUIDES

**Complete guide index**: See [All Guides](docs/ALL-GUIDES.md)

**Key guides**:
- Financial: [Big Baller Guide](docs/guides/BIG-BALLER-GUIDE.md)
- Automation: [Workflow Wizard Guide](docs/guides/WORKFLOW-WIZARD-GUIDE.md)
- Product Launch: [Autonomous Product Launch](docs/AUTONOMOUS-PRODUCT-LAUNCH-GUIDE.md)
- Testing: [Website Testing Protocol](docs/guides/WEBSITE-TESTING-PROTOCOL.md)
- Google Workspace: [Google Workspace Guide](docs/guides/GOOGLE-WORKSPACE-GUIDE.md)
- Microsoft 365: [Microsoft 365 Guide](docs/guides/MICROSOFT-365-GUIDE.md)
- Visual Content: [Image & 3D Creation Guide](docs/BLENDER_AND_3D_TOOLS.md)

---

## ⚡ CRITICAL EXECUTION RULES

**CRITICAL: Zapier MCP Credit Usage** - ALWAYS ask user for explicit approval before using any Zapier MCP tools (mcp__zapier__*). Exception: Only proceed without asking if user explicitly requests "use Zapier" in current message.

### GOLDEN RULE: "1 MESSAGE = ALL RELATED OPERATIONS"

**MANDATORY PATTERNS:**
- **TodoWrite**: ALWAYS batch ALL todos in ONE call (5-10+ todos minimum)
- **Task tool (Claude Code)**: ALWAYS spawn ALL agents in ONE message with full instructions
- **File operations**: ALWAYS batch ALL reads/writes/edits in ONE message
- **Bash commands**: ALWAYS batch ALL terminal operations in ONE message

**Claude Code's Task tool is the PRIMARY way to spawn agents** - Use for parallel agent execution

**MCP tools are ONLY for coordination setup** (optional, advanced use cases)

---

## 🚨 IMPORTANT INSTRUCTION REMINDERS

**Do what has been asked; nothing more, nothing less.**

**CRITICAL: Attempt Complex Solutions First** - ALWAYS attempt difficult/complex approach FIRST. Don't default to simple alternatives. Only suggest simpler alternatives AFTER attempting complex approach and encountering genuine blockers. Goal is scalable, production-ready solutions.

**File Creation Rules**:
- NEVER create files unless absolutely necessary
- ALWAYS prefer editing existing file to creating new one
- NEVER proactively create documentation files (*.md) or README files
- Never save working files, text/mds and tests to root folder
- ALWAYS organize files in appropriate subdirectories

**MCP Server Access**: Google Workspace MCP server auto-loads on startup. ALWAYS available. Microsoft 365 accessed via n8n. Never ask "do you have access?"

**Revenue-First Mindset**: Every action should move toward unlimited monthly recurring revenue. Build systems, not one-offs. Create reusable assets. Automate everything possible. Let's get to the bread.
