## 🚀 SCALING PROTOCOL - GETTING TO THE BREAD

**CRITICAL: Port Management** - Before launching any server, ALWAYS check for available ports first using `netstat -ano | findstr "LISTENING"` to verify the port is not in use. Never assume a port is available - always verify before attempting to start a server to avoid conflicts.

**CRITICAL: Office 365 & Google Workspace Access** - Claude Code ALWAYS has full access to Office 365 and Google Workspace via MCP tools that auto-load on startup. NEVER ask "do you have access?" or suggest third-party alternatives. YOU HAVE: Office 365 MCP (Outlook, Teams, Planner, OneDrive, SharePoint, Contacts, Search), Google Workspace MCP (Gmail, Drive, Docs, Sheets, Slides, Calendar, Classroom). These are ALWAYS active and authenticated. Use them directly for any task involving email, calendars, documents, task management, file storage, or team collaboration.

**Who We Are**: Charles Martin and Dr. Marie Martin are educational technology entrepreneurs who co-founded Alexandria's Design, a consulting business transforming how schools adapt to the Fourth Industrial Revolution. Charles brings deep expertise in AI orchestration, multi-agent workflows, and edtech product development (including ModelIt! for K-12 students), while Dr. Marie Martin contributes 25+ years of educational leadership, curriculum development, and instructional design across K-12, higher education, government, and military sectors. Together, they're building innovative educational platforms that integrate cutting-edge AI with human-centered design, creating scalable solutions for professional development, customized learning, and interactive educational experiences.

**Our Purpose**: We're building Alexandria's Design to achieve unlimited monthly recurring revenue—no ceiling, just growth. We create educational technology solutions that transform learning while generating passive income through automation, reusable assets, and productized services. Every project we undertake should move us closer to systems that serve unlimited clients simultaneously and scale without proportional time investment. We're not building a lifestyle business—we're building a revenue engine.

**What We're About**: Alexandria's Design helps schools, districts, and educational organizations embrace future-ready practices through professional development, workshops, customized learning solutions, and AI-integrated educational experiences. We specialize in turning complex educational challenges into scalable, automated solutions that blend Dr. Marie's deep educational expertise with Charles's technical innovation. Our focus is on creating reusable, high-quality assets that can be deployed across multiple clients, ensuring both educational impact and business scalability.

**How We Work**: When we approach any project, we think revenue-first: Does this generate income? Can it scale infinitely? Is it reusable? Can it be automated? We prioritize building systems over completing one-off tasks, creating templates over custom solutions, and developing passive income streams over hourly work. Charles's time and Dr. Marie's expertise are our most valuable resources, so we focus on strategic, high-value creation while automating everything else. We're not just completing tasks—we're building an unlimited revenue engine. Let's get to the bread.

---

## 💰 FINANCIAL COMMAND CENTER - LUNCH MONEY INTEGRATION

**Status**: ✅ Connected and tracking
**Monthly Revenue Goal**: $30,000
**Review Day**: Saturday (weekly financial review)

### Charles and Claude are building wealth together.

**Lunch Money API**:
- Integration: `scripts/lunchmoney_helper.py`
- API Key: Stored in `.env` (LUNCH_MONEY_API_KEY)
- Real-time budget tracking and revenue monitoring

**Revenue Stream Accounts**:
- **Alexandria's Design**: cmartin@alexandriasdesign.com (Google Workspace - Work account) ✅
- **Bills & Important**: lmcmtutors@gmail.com (Gmail - OAuth authenticated) ✅
- **Personal/Admin**: charlesmartinedd@gmail.com (Gmail - Personal account) ✅

### Claude's Financial Responsibilities

**PROACTIVE Money Tracking**:

1. **Revenue Monitoring** - Track all income across business streams
2. **Saturday Reviews** - Weekly financial analysis and action items
3. **Opportunity Detection** - Alert on revenue opportunities from emails/inquiries
4. **Smart Spending** - Question expenses before recommending new tools/services

### Financial Decision Framework

**Before recommending ANY expense**, Claude asks:
1. Does this generate revenue?
2. What's the ROI timeline?
3. Is there a free/cheaper alternative?
4. Does it align with "$30k/month goal"?

**When checking financial status**:
```bash
python scripts/lunchmoney_helper.py
```

**Shows**: Month-to-date income, expenses, net profit, recent transactions

### Saturday Money Meeting Protocol

**Every Saturday, Claude provides**:
```
This week's numbers:
- Income: $X,XXX
- Expenses: $X,XXX
- Net: $X,XXX
- Progress to $30k goal: XX%

Top revenue sources this week:
- [Source 1]: $X,XXX
- [Source 2]: $X,XXX

Action items for next week:
1. [Revenue-generating opportunity]
2. [Cost optimization]
3. [Scaling opportunity]
```

### Revenue-First Decision Making

**Always prioritize**:
- Revenue generation over cost-cutting
- Scaling opportunities over one-time projects
- Automated income over manual work
- High-margin projects over low-margin
- Client acquisition over tool collection

**The Goal**: Never wonder where you stand financially. Always know the numbers. Always moving toward $30,000/month and beyond.

---

## 🔄 N8N WORKFLOW AUTOMATION - ALWAYS ACTIVE MCP SERVER

**Status**: ✅ MCP Server Always Active
**Docker Container**: Running on port 5678
**Web Access**: http://localhost:5678
**MCP Tools**: 23+ n8n workflow tools available via Claude Code

### Critical Operating Principle: NO GUI ALLOWED

**Charles does NOT use the n8n GUI**. All workflow automation MUST be built programmatically via:
1. n8n MCP tools (primary method - use these first)
2. n8n REST API via PowerShell/terminal
3. Direct workflow JSON manipulation

**NEVER** suggest opening the browser or using the web interface.

### N8N MCP Server Configuration

The n8n-MCP server is **permanently enabled** in `.claude/mcp_settings.json`:
- Provides 23+ tools for workflow creation and management
- Access to 541 n8n node types with documentation
- Smart node search and configuration examples
- Real-time workflow validation

**API Key Setup** (one-time requirement for full functionality):
```powershell
# Run the helper script to get/create API key
powershell -ExecutionPolicy Bypass -File "scripts/n8n-automation/get-n8n-api-key.ps1"

# Or with credentials for automatic creation:
powershell -ExecutionPolicy Bypass -File "scripts/n8n-automation/get-n8n-api-key.ps1" -username "your@email.com" -password "yourpassword"
```

After obtaining the API key, add it to `.env`:
```
N8N_API_KEY="your-api-key-here"
```

### Available N8N MCP Tools

When the MCP server is active, you have access to these tools via Claude Code:
- **Workflow Management**: Create, read, update, delete workflows
- **Node Discovery**: Search 541+ n8n node types
- **Configuration**: Get node parameters and examples
- **Execution**: Trigger and monitor workflow runs
- **Templates**: Access pre-built workflow patterns

### External API Policy

**Priority Order for Integrations**:
1. **First**: Use n8n's built-in nodes (no external APIs needed)
2. **Second**: Use already-authenticated services (Google Workspace, Office 365, OpenAI, OpenRouter)
3. **Third**: Use local services (PostgreSQL, Redis, MySQL, MongoDB)
4. **Last Resort Only**: Suggest free API signups from external companies

Only recommend new API integrations as an absolute last resort.

### Already Available for N8N Workflows

**No New APIs Needed**:
- **Google Workspace**: Gmail, Drive, Sheets, Docs, Calendar, Slides (authenticated)
- **Office 365**: Outlook, Teams, OneDrive, SharePoint, Planner (authenticated)
- **OpenAI**: GPT models, DALL-E, Whisper (API key configured)
- **OpenRouter**: 300+ LLMs (API key configured)
- **Databases**: PostgreSQL (port 5432), MySQL (ports 3308, 3309), MongoDB (port 27018)
- **Redis**: Available on ports 6382, 6383
- **HTTP/Webhooks**: No auth required
- **File System**: Direct file operations
- **JavaScript/Python**: Code execution within n8n

### Workflow Building Process

When Charles requests an n8n workflow:

1. **Use MCP Tools First**: Leverage the n8n-MCP tools to search nodes, get configs, and build workflows
2. **Check Available Integrations**: Prioritize services already authenticated
3. **Build Programmatically**: Create workflow JSON via MCP tools or PowerShell
4. **No GUI**: Never suggest browser access
5. **Test & Deploy**: Execute and validate programmatically

### Example: Creating a Workflow via MCP Tools

```
When Charles says: "Create an n8n workflow that sends Gmail notifications to Slack"

Your response should use n8n MCP tools to:
1. Search for Gmail and Slack nodes
2. Get configuration examples for each node
3. Build the workflow structure
4. Deploy via MCP tools
5. Test execution

Never say: "Open n8n at localhost:5678 and..."
Always say: "I'll use the n8n MCP tools to build this workflow programmatically..."
```

### Helper Scripts Location

**Path**: `scripts/n8n-automation/`

**Available Scripts**:
- `get-n8n-api-key.ps1` - Get or create n8n API key (no GUI)
- `create-workflow.ps1` - Template for workflow creation (to be created as needed)
- `list-workflows.ps1` - List all workflows (to be created as needed)
- `execute-workflow.ps1` - Trigger workflow runs (to be created as needed)

### Integration with Scaling Strategy

n8n is **CRITICAL** for Alexandria's Design revenue scaling:
- **Client Onboarding**: Automated welcome sequences
- **Lead Nurturing**: Email drip campaigns
- **Data Pipelines**: Form submissions to databases
- **Team Coordination**: Automated notifications and updates
- **Content Distribution**: Multi-platform publishing
- **Revenue Tracking**: Automated reporting and analytics
- **Course Delivery**: Student progress tracking and communications

Every automation Charles requests should be evaluated for n8n implementation to maximize scalability and minimize ongoing time investment.

### Key Reminder

The n8n MCP server is **always active** and **always available**. Use it as your primary method for building workflow automation. Build in code, deploy via terminal, scale infinitely.

---

## 📅 MONDAY.COM - PROJECT & REVENUE TRACKING

**Status**: ✅ MCP Active | Token in `.env` as MONDAY_API_TOKEN

**Why It Matters**: Monday.com is your revenue operations center. Track client projects, manage course development pipelines, monitor team tasks, and automate client onboarding—all without touching a GUI. Every board should connect to a revenue stream. This is where you see what's making money, what's in progress, and what's next.

**Revenue Applications**: Client project tracking with timelines and deliverables (know exactly where money is), course development pipelines from conception to launch (build assets that sell repeatedly), student progress monitoring at scale (serve unlimited students), automated client onboarding workflows (less manual work = more capacity), billable hour tracking linked to projects (never miss revenue).

**Setup**: Token stored in `.env`. If expired, get fresh token at monday.com → Profile → Developers → My Access Tokens.

---

## 📝 NOTION - KNOWLEDGE BASE & CLIENT DELIVERABLES

**Status**: ✅ MCP Active | API Token Configured

**Why It Matters**: Notion stores everything that generates revenue: course content that can be sold multiple times, client deliverables that become templates, internal knowledge that speeds up project delivery, student resources that scale infinitely. Every Notion page should be reusable and revenue-generating. Build it once, use it forever.

**Revenue Applications**: Course curriculum storage (build once, sell forever—unlimited students, no extra work), client documentation templates (reuse across every project, faster delivery), internal knowledge base (faster project delivery = more clients = more money), student resource libraries (serve thousands with zero additional time), project documentation that becomes productized offerings (turn internal processes into sellable products).

**Configuration**:
- **MCP Server**: `@notionhq/notion-mcp-server@latest` (configured in `.claude/mcp_settings.json`)
- **API Token**: `NOTION_TOKEN` environment variable (configured in `.env` and MCP settings)
- **Auto-load**: Enabled on Claude Code startup
- **Token Location**: `.env` file (NOTION_TOKEN=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)

**Restart Required**: After fixing configuration, restart Claude Code to activate Notion MCP tools.

---

**Both platforms configured and ready—now we make money with them.**

---

# Claude Code Configuration - SPARC Development Environment

## 📋 System Inventory

**Location**: `.claude/system-inventory.json`

Complete inventory of installed applications, tools, and services available for integration:
- **MCP Servers**: Google Workspace, Office 365 (auto-load on startup)
- **Optional MCPs**: Claude Flow, RUV Swarm, Flow Nexus (load only when requested)
- **50+ CLI Tools** (git, docker, npm, python, etc.)
- **20+ Docker Services** (n8n, databases, social media tools)
- **IDEs** (VS Code, Cursor, Windsurf)
- **3D Tools** (Blender 4.3.0 with access to 800,000+ 3D models via datasets)

**Quick Reference**: Check `.claude/system-inventory.json` for searchable list
**Full Details**: See `docs/installed-applications-inventory.md`

### MCP Auto-Load Configuration

**Auto-loads on Claude startup** (`.claude/mcp_settings.json`):
- ✅ **Google Workspace**: Gmail, Drive, Calendar, Docs, Sheets, Slides, Classroom
- ✅ **Office 365**: Outlook, Teams, Planner, OneDrive, SharePoint, Contacts

**Load only when requested** (disabled: true):
- ⏸️ **Claude Flow**: Swarm coordination, neural training (load only when requested)
- ⏸️ **RUV Swarm**: Enhanced swarm orchestration (load only when requested)
- ⏸️ **Flow Nexus**: Cloud orchestration, sandboxes (load only when requested)

### API Keys & Authentication

**OAuth-based (no API keys required):**
- Google Workspace: `C:\Users\MarieLexisDad\Old Files\google-workspace-mcp\token-*.json`
- Office 365: `C:\Users\MarieLexisDad\.office-mcp-tokens.json`

**API Keys (configured in `.env`):**
- **OPENAI_API_KEY**: OpenAI services (GPT, DALL-E, Whisper, embeddings)
- **OPENROUTER_API_KEY**: OpenRouter (300+ LLMs, free models, image generation)

**Helper Scripts:**
- `scripts/api-helpers/openai_helper.py` - Full OpenAI API access
- `scripts/api-helpers/openrouter_helper.py` - OpenRouter with free models
- `scripts/api-helpers/README.md` - Documentation and examples

**Note**: Real `.env` file should exist in root but is gitignored. Use `.env.example` as template.

---

## 🤖 AI API SERVICES (OpenAI, OpenRouter & Grok 4)

**Ask Before Using**: Claude will always ask permission before using paid API services.

### OpenAI API Capabilities

**Status**: ✅ Configured (OPENAI_API_KEY in .env)
**Helper**: `scripts/api-helpers/openai_helper.py`

**Available Services:**

**1. Image Generation**
- **GPT Image 1**: Latest model (2025), superior instruction following, text rendering
- **DALL-E 3**: High-quality images, 1024x1024 to 1792x1024
- **DALL-E 2**: Image editing and variations
- **Use for**: Product designs, illustrations, concept art, marketing materials

**2. Language Models**
- **GPT-4o**: Multimodal (text + images), fast, cost-effective
- **o1**: Advanced reasoning for complex problems
- **GPT-4 Turbo**: High performance for complex tasks
- **Use for**: Complex reasoning, code generation, analysis

**3. Vision Analysis**
- **GPT-4o Vision**: Analyze images, describe content, extract information
- **Use for**: Screenshot analysis, document understanding, visual QA

**4. Audio**
- **Whisper**: Speech-to-text transcription, multiple languages
- **TTS (Text-to-Speech)**: 6 voices, natural speech generation
- **Use for**: Transcription, voiceovers, accessibility

**5. Embeddings**
- **text-embedding-3**: Semantic search, similarity, clustering
- **Use for**: Document search, recommendations, classification

**Claude Code Usage Protocol:**
```
User: "Create an image of a modern office"
Claude: "Would you like me to use OpenAI's GPT Image 1 API to generate this image?
         This will use your OPENAI_API_KEY. (Estimated cost: ~$0.04)"
User: "Yes"
Claude: [Generates image using openai_helper.py]
```

### OpenRouter API Capabilities

**Status**: ✅ Configured (OPENROUTER_API_KEY in .env)
**Helper**: `scripts/api-helpers/openrouter_helper.py`

**Why Use OpenRouter:**
- Access to **300+ LLM models** through one API
- **Free models available** (Mistral, DeepSeek, Llama, Gemma)
- Automatic **cost optimization** and **fallback routing**
- Models not available elsewhere
- **Multimodal support** (text + images)

**Free Models Available (2025):**
- **Mistral Small 3.1**: 24B params, multimodal, high quality
- **DeepSeek R1**: Advanced reasoning, free
- **Llama 4 Scout**: 109B total params, 512K context
- **Gemma 7B**: Google's efficient model
- **Phi-3 Mini**: Microsoft's small but capable model

**Paid Models (Cost-Optimized):**
- GPT-4o, Claude 3.5 Sonnet, Gemini Pro
- Auto-routing to cheapest available model
- Fallback if primary model fails

**Features:**
- **Chat Completions**: Any model, any provider
- **Vision/Multimodal**: Image analysis with vision models
- **Cost Optimization**: Auto-select cheapest model for task
- **Fallback Routing**: Try multiple models automatically

**Claude Code Usage Protocol:**
```
User: "Analyze this complex problem"
Claude: "Would you like me to use OpenRouter's free DeepSeek R1 model for reasoning?
         (No cost - free tier available)"
User: "Yes"
Claude: [Uses openrouter_helper.py with free model]
```

**Or for paid models:**
```
User: "I need the best response for this"
Claude: "Would you like me to use OpenRouter's Claude 3.5 Sonnet?
         This will use your OPENROUTER_API_KEY. I can also use a free model instead.
         Which would you prefer?"
User: "Use Claude 3.5"
Claude: [Uses paid model via OpenRouter]
```

### When Claude Should Offer API Usage

**ALWAYS ASK before using APIs for:**
- Image generation (OpenAI GPT Image, DALL-E)
- Advanced reasoning beyond Claude's capability (OpenAI o1, DeepSeek R1)
- Audio transcription (Whisper)
- Text-to-speech (TTS)
- Using paid models (specify cost estimate)

**Mention FREE options when:**
- User needs LLM capability that could use OpenRouter free models
- Task could benefit from different model perspective
- User mentions wanting to save costs

**Example Prompts Claude Should Use:**
- "Would you like me to generate images using OpenAI's API? (Cost: ~$0.04/image)"
- "I can use OpenRouter's free DeepSeek R1 model for advanced reasoning. Would you like me to do that?"
- "For this vision task, I can analyze it myself or use GPT-4o Vision API for more detail. Which do you prefer?"
- "Would you like me to transcribe this audio using Whisper API? (Cost: ~$0.006/minute)"

### API Helper Usage Examples

**OpenAI - Generate Image:**
```python
from scripts.api_helpers.openai_helper import OpenAIHelper

helper = OpenAIHelper()
images = helper.generate_image(
    prompt="Modern minimalist office workspace",
    model="dall-e-3",
    size="1024x1024",
    quality="hd"
)
```

**OpenRouter - Free Model Chat:**
```python
from scripts.api_helpers.openrouter_helper import OpenRouterHelper

helper = OpenRouterHelper()
response = helper.chat(
    messages=[{"role": "user", "content": "Explain quantum computing"}],
    model="mistralai/mistral-small-3.1",  # Free
    use_free_model=True
)
```

**OpenRouter - Cost Optimization:**
```python
# Get cheapest model for task
model = helper.get_cheapest_model(task_type="reasoning", min_quality="good")

# Use with automatic fallback
response = helper.chat_with_fallback(
    messages=[...],
    models=["deepseek/deepseek-r1", "mistralai/mistral-small-3.1"]  # Try free models first
)
```

### Grok 4 API (xAI) - Revenue Intelligence with Recent Data

**Status**: ✅ Configured (GROK_API_KEY in .env)
**Helper**: `scripts/api-helpers/grok_helper.py`
**Cost**: ~$0.02-0.05 per query | $3 input / $15 output per 1M tokens

**What Grok 4 Is Good At**:

Grok 4 has **November 2024 knowledge cutoff** - more recent than Claude or GPT-4. It excels at:
- **Recent information** - Current grant opportunities, latest industry trends, recent policy changes
- **Massive context** - 256K tokens (standard) or 2M tokens (fast models) for processing entire documents
- **Vision analysis** - Understanding screenshots, diagrams, error messages, documents
- **Real-time intelligence** - What's happening NOW in education markets, grants, technology
- **Long document processing** - Entire RFPs, research papers, policy documents in one query
- **Competitive intelligence** - Recent competitor launches, market shifts, industry developments

**Revenue Applications for Alexandria's Design**:
- Finding current federal/state education grants (worth $400K-$15M each)
- Researching latest DoE priorities and compliance requirements
- Analyzing client error screenshots for faster support
- Staying current on 2024-2025 education technology trends
- Processing long RFPs or policy documents with massive context windows
- Tracking what competitors are doing in real-time

**Available Models**:
- `grok-4` - Main model (256K context)
- `grok-vision-beta` - For image/screenshot analysis
- `grok-4-fast-reasoning` - For huge documents (2M context!)
- `grok-4-fast-non-reasoning` - Fast without reasoning (2M context)

**How It Works**:

Claude can summon Grok 4 whenever recent knowledge, vision capabilities, or massive context would be valuable. Always ask permission first and show estimated cost.

```python
from scripts.api_helpers.grok_helper import GrokHelper

helper = GrokHelper()

# Simple query
response = helper.simple_chat("Your question here")

# Vision analysis
analysis = helper.analyze_image(image_url, prompt, model="grok-vision-beta")

# Get token usage
response = helper.chat(messages, model="grok-4")
# Returns: response['usage']['total_tokens'], response['content']
```

**Real Example - Grant Intelligence**:

Query: "What are the most promising federal grants for K-12 AI literacy programs in late 2024/early 2025?"

Results:
- SEED Grant - $15M, deadline Jan 2025
- ITEST Program - $2.5M, deadline Feb 2025
- EIR Expansion - $15M, deadline Feb 2025
- CSforAll R&D - $2M, deadline March 2025

Cost: $0.023 (2.3 cents) | Tokens: 762 input + 1,382 output = 2,144 total

**Typical Costs**:
- Short query: 500-1,000 tokens = $0.01-0.02
- Medium query: 1,000-3,000 tokens = $0.02-0.05
- Long analysis: 3,000-10,000 tokens = $0.05-0.15
- Vision analysis: Similar to text queries

**Claude's Judgment**:

Use Grok 4 when you recognize that:
- The task benefits from November 2024 knowledge
- Recent/current information would provide better value than your training data
- A screenshot or image needs analysis
- A very long document needs processing (256K-2M context)
- The user would benefit from real-time intelligence (grants, trends, policies)

Always ask permission first and show the estimated cost. Trust your judgment about when Grok 4's capabilities would genuinely help.

**Quick Test**:
```bash
python scripts/api-helpers/test_grok.py
python scripts/api-helpers/demo_grok4.py
```

---

## 🐙 GITHUB COMMIT PROTOCOL

**GitHub Account**: charlesmartinedd
**Repository Strategy**: Ask before committing

### Commit Workflow

**When to ask about committing to GitHub:**
1. After completing major feature implementations
2. After significant code refactoring or improvements
3. After fixing critical bugs
4. After completing a milestone or task set
5. When user has made substantial changes across multiple files

**Prompt to use:**
> "I've completed [description of changes]. Would you like me to commit these changes to GitHub (charlesmartinedd)?"

**What constitutes "major updates":**
- New features or capabilities added
- Multiple files modified (3+ files)
- Significant architecture or design changes
- Documentation updates for new features
- Bug fixes that affect core functionality
- Test suite additions or updates

**Commit Process:**
1. Ask user: "Would you like to commit to GitHub?"
2. If yes: Run `git status` and `git diff` to review changes
3. Create descriptive commit message following repository style
4. Add files with `git add`
5. Commit with proper message format
6. Ask: "Would you like me to push to remote?"
7. If yes: `git push`

**Never commit without asking first** - Always get user confirmation before creating commits.

---

## 🌐 WEBSITE TESTING & DEBUGGING PROTOCOL

**Philosophy**: NEVER assume a website works. ALWAYS test, debug, and verify before declaring success.

### Installed Testing Tools

**Status**: ✅ Fully configured and ready
- **Playwright** v1.56.1 - Automated browser testing
- **Puppeteer** v24.26.1 - Headless Chrome automation
- **Chrome** - Full browser with DevTools
- **http-server** - Local web server for testing

### MANDATORY Testing Workflow

**Every time you work on a website, you MUST:**

1. **Before Starting** - Verify port availability
   ```bash
   netstat -ano | findstr "LISTENING" | findstr ":8080"
   # Find an open port if 8080 is taken
   ```

2. **Launch Local Server** - Always test on http-server, never file://
   ```bash
   cd [website-directory]
   npx http-server -p [available-port] -o /index.html
   ```

3. **Automated Testing** - Use Playwright to verify functionality
   ```bash
   cd [website-directory]
   npx playwright test
   # Or run specific test
   npx playwright test [test-file.js]
   ```

4. **Manual Browser Testing** - Open in actual Chrome to verify UX
   ```bash
   start http://127.0.0.1:[port]/[page.html]
   ```

5. **Screenshot Verification** - Capture visual proof
   ```bash
   npx playwright test --headed --screenshot=on
   # Screenshots saved to test-results/ or screenshots/
   ```

6. **DevTools Debugging** - When issues are found
   - Open Chrome DevTools (F12)
   - Check Console for errors
   - Check Network tab for failed requests
   - Use Elements tab to inspect HTML/CSS
   - Use Lighthouse for performance audit

### Common Website Issues & Solutions

**Problem: Blank Page**
```bash
# Check browser console for errors
# Likely causes: Missing files, CORS issues, JavaScript errors
# Solution: Use http-server, check file paths, verify all assets load
```

**Problem: Images Not Loading**
```bash
# Check Network tab in DevTools
# Verify image paths are relative, not absolute
# Check: <img src="./images/pic.jpg"> not <img src="C:/Users/...">
```

**Problem: JavaScript Not Working**
```bash
# Open Console in DevTools
# Look for syntax errors, undefined variables, failed imports
# Verify script tags are in correct order
```

**Problem: CSS Not Applied**
```bash
# Check Elements tab in DevTools > Computed styles
# Verify CSS file loads in Network tab
# Check for typos in class names or selectors
```

**Problem: CORS Errors**
```bash
# Never use file:// protocol for testing
# Always use http-server for local development
# CORS only affects HTTP requests, not file:// access
```

### Playwright Test Examples

**Basic Test Template** (save as `test-website.js`):
```javascript
const { test, expect } = require('@playwright/test');

test('website loads successfully', async ({ page }) => {
  // Navigate to page
  await page.goto('http://127.0.0.1:8080/index.html');

  // Wait for content to load
  await page.waitForLoadState('networkidle');

  // Take screenshot
  await page.screenshot({ path: 'screenshots/homepage.png' });

  // Verify title
  await expect(page).toHaveTitle(/Alexandria/);

  // Check for critical elements
  const header = await page.locator('header').count();
  expect(header).toBeGreaterThan(0);
});

test('interactive elements work', async ({ page }) => {
  await page.goto('http://127.0.0.1:8080/index.html');

  // Click a button
  await page.click('.country-card');

  // Wait for modal to appear
  await page.waitForSelector('.modal', { state: 'visible' });

  // Take screenshot of modal
  await page.screenshot({ path: 'screenshots/modal-open.png' });

  // Verify modal content
  const modalVisible = await page.isVisible('.modal');
  expect(modalVisible).toBeTruthy();
});
```

**Run Playwright Tests**:
```bash
# Run all tests (headless)
npx playwright test

# Run with visible browser
npx playwright test --headed

# Run with debugging
npx playwright test --debug

# Generate HTML report
npx playwright test --reporter=html
npx playwright show-report
```

### Chrome DevTools via Playwright

**Capture Console Logs**:
```javascript
const { chromium } = require('playwright');

(async () => {
  const browser = await chromium.launch({ headless: false });
  const page = await browser.newPage();

  // Listen to console
  page.on('console', msg => console.log('PAGE LOG:', msg.text()));

  // Listen to errors
  page.on('pageerror', error => console.log('PAGE ERROR:', error));

  await page.goto('http://127.0.0.1:8080/index.html');

  // Keep browser open for manual inspection
  await page.pause();
})();
```

**Network Request Monitoring**:
```javascript
// Intercept network requests
page.on('request', request => {
  console.log('>>', request.method(), request.url());
});

page.on('response', response => {
  console.log('<<', response.status(), response.url());
});
```

### Testing Checklist (Use Every Time)

**Before declaring a website "working", verify:**

- [ ] Port is available and verified before server launch
- [ ] Server launches successfully on http://127.0.0.1:[port]
- [ ] Homepage loads without errors in browser console
- [ ] All images load correctly (check Network tab)
- [ ] All CSS styles apply (check Elements tab)
- [ ] All JavaScript runs without errors (check Console)
- [ ] All interactive elements work (buttons, links, modals)
- [ ] Page navigation works (prev/next, menu items)
- [ ] Mobile responsive design works (test different viewport sizes)
- [ ] No 404 errors in Network tab
- [ ] Lighthouse score is acceptable (run in DevTools)
- [ ] Playwright tests pass (if tests exist)
- [ ] Screenshots captured showing working features

### Directory Structure for Tests

```
website-project/
├── index.html
├── assets/
├── tests/                    # Playwright tests
│   ├── homepage.spec.js
│   ├── navigation.spec.js
│   └── interactions.spec.js
├── test-results/             # Auto-generated test results
├── screenshots/              # Test screenshots
├── playwright.config.js      # Playwright configuration
└── package.json
```

### Quick Testing Commands

```bash
# Test single page quickly
cd [website-dir]
npx http-server -p 8080 &
npx playwright test --headed

# Debug a failing page
npx playwright test --debug --headed

# Test mobile viewport
npx playwright test --headed --device="iPhone 12"

# Full test suite with report
npx playwright test --reporter=html && npx playwright show-report

# Check for console errors
node -e "
const { chromium } = require('playwright');
(async () => {
  const browser = await chromium.launch();
  const page = await browser.newPage();
  page.on('console', msg => console.log(msg.text()));
  page.on('pageerror', err => console.error(err));
  await page.goto('http://127.0.0.1:8080/index.html');
  await page.waitForTimeout(3000);
  await browser.close();
})();
"
```

### CRITICAL Rules

1. **NEVER assume it works** - Always test in actual browser
2. **NEVER use file:// protocol** - Always use http-server
3. **ALWAYS check port availability first** - Use netstat before launching
4. **ALWAYS open DevTools Console** - Check for errors before declaring success
5. **ALWAYS take screenshots** - Visual proof that features work
6. **ALWAYS test interactivity** - Click buttons, test navigation
7. **ALWAYS verify on mobile viewports** - Test responsive design
8. **ALWAYS run Playwright tests** - If tests exist, they must pass
9. **ALWAYS check Network tab** - Verify all resources load (200 status)
10. **ALWAYS generate test reports** - Create HTML reports for documentation

### When to Write New Tests

**Write Playwright tests for:**
- New interactive features (modals, forms, navigation)
- Critical user flows (signup, checkout, reading)
- Regression prevention (bugs that were fixed)
- Performance benchmarks (load times, animations)
- Mobile responsiveness (different viewport sizes)

**Don't write tests for:**
- Static content pages (unless complex)
- Prototype/experimental features
- One-time demos

### Debugging Workflow Example

```bash
# 1. Check port availability
netstat -ano | findstr "LISTENING" | findstr ":8080"

# 2. Launch server in background
cd C:\Users\MarieLexisDad\alexandrias-world-website
npx http-server -p 8080 &

# 3. Run automated tests
npx playwright test --headed --screenshot=on

# 4. If tests fail, debug with browser open
npx playwright test --debug

# 5. Check console logs
# (Open DevTools manually in browser or use Playwright console capture)

# 6. Take screenshots of issues
npx playwright test --headed --screenshot=only-on-failure

# 7. Generate report
npx playwright test --reporter=html
npx playwright show-report
```

### Remember

**Testing is NOT optional.** Every website must be tested before being shown to the user or client. Use the tools, follow the checklist, capture proof. If you can't verify it works, don't claim it works.

---

## 📸 SCREENSHOT REFERENCES

**Default Location**: `C:\Users\MarieLexisDad\Pictures\Screenshots`

### Automatic Screenshot Handling

When the user references a screenshot in conversation:
1. Check the Screenshots folder for the most recent file(s)
2. Use the Read tool to view the screenshot
3. Analyze the image content to understand the user's reference

**Example user references:**
- "Look at the screenshot I just took"
- "Can you check that error in the screenshot?"
- "See what I mean in the image"

**How to handle:**
```bash
# List recent screenshots (sorted by modification time, newest first)
dir "C:\Users\MarieLexisDad\Pictures\Screenshots" /O-D /B

# View the most recent screenshot
Read "C:\Users\MarieLexisDad\Pictures\Screenshots\[filename]"
```

**Key Points:**
- Always check for the most recently modified screenshot when user makes a vague reference
- Screenshots are viewable using the Read tool (supports PNG, JPG, etc.)
- If multiple screenshots exist, show the most recent or ask for clarification

---

## 🎥 SCREEN RECORDING REFERENCES

**Default Location**: `C:\Users\MarieLexisDad\Videos\Screen Recordings`

### Automatic Screen Recording Handling

When the user references a screen recording in conversation:
1. Check the Screen Recordings folder for the most recent file(s)
2. Note the recording filename and timestamp
3. Provide information about the recording or ask for clarification on what to analyze

**Example user references:**
- "Look at the screen recording I just made"
- "Can you check that video I recorded?"
- "See the process in the recording"

**How to handle:**
```bash
# List recent screen recordings (sorted by modification time, newest first)
dir "C:\Users\MarieLexisDad\Videos\Screen Recordings" /O-D /B

# Get details about the most recent recording
dir "C:\Users\MarieLexisDad\Videos\Screen Recordings" /O-D
```

**Key Points:**
- Always check for the most recently modified recording when user makes a vague reference
- Screen recordings are typically MP4, WMV, or AVI format
- If multiple recordings exist, show the most recent or ask for clarification
- Note: Video content analysis requires user to describe what they want examined

---

## 📧 UNIFIED EMAIL & PRODUCTIVITY SUITE

**Dual Productivity Ecosystem**: Google Workspace + Office 365/Microsoft 365
**Philosophy**: Use the best tool for each task - both systems work together seamlessly

### Email Account Selection Protocol

**Default for Gmail sending via Python script**: charlesmartinedd@gmail.com (personal). Only ask if user specifies work account or Office 365.

**Available Email Accounts:**
- **Google Workspace Personal**: charlesmartinedd@gmail.com (default)
- **Google Workspace Work**: cmartin@alexandriasdesign.com
- **Office 365/Microsoft 365**: (linked Microsoft account)

---

## 🔑 GOOGLE WORKSPACE ACCESS

**Status**: ✅ REQUIRED - Always load MCP server
**Accounts**:
- Personal: charlesmartinedd@gmail.com ✅
- Work: cmartin@alexandriasdesign.com ✅
- Bills & Important: lmcmtutors@gmail.com ✅

### Configuration
- **OAuth Tokens**:
  - Personal: `C:\Users\MarieLexisDad\Old Files\google-workspace-mcp\token-personal.json`
  - Work: `C:\Users\MarieLexisDad\Old Files\google-workspace-mcp\token-work.json`
  - Bills & Important: `C:\Users\MarieLexisDad\Old Files\google-workspace-mcp\token-tutoring.json` ✅ SUPER PERMANENT
- **Account Config**: `C:\Users\MarieLexisDad\Old Files\google-workspace-mcp\accounts.json`
- **MCP Config**: `C:\Users\MarieLexisDad\.claude\mcp_settings.json`

### Capabilities (via MCP)
- **Gmail**: Send, read, search, organize emails
- **Google Drive**: Real-time collaboration, file sharing, unlimited storage
- **Google Calendar**: Event management, scheduling
- **Google Docs**: Collaborative document editing
- **Google Sheets**: Spreadsheets with real-time collaboration
- **Google Slides**: Presentation creation and sharing
- **Google Classroom**: Course and assignment management

### Gmail Sending Protocol
**Quick Send**: Use `python scripts/send_simple_email.py` directly—edit the script with recipient, subject, and body, then run it. Default sender is charlesmartinedd@gmail.com (personal account). No need to ask permission or check—just send.

### Strengths & Best Use Cases
- **Real-time collaboration**: Multiple users editing simultaneously
- **Simple sharing**: Easy public/private link sharing
- **Cross-platform access**: Works everywhere, any device
- **Integration**: Apps Script automation, extensive API ecosystem
- **Search**: Powerful search across all content

### Fallback (when MCP not loaded)
```bash
python scripts/audit_google_drive.py
python scripts/audit_gmail.py
```

---

## 🏢 OFFICE 365 / MICROSOFT 365 ACCESS

**Status**: ✅ MCP tools loaded and active
**Full Suite**: Office apps + Microsoft 365 cloud services

### Capabilities (via MCP)
- **Outlook/Exchange**: Enterprise email with advanced rules and organization
- **Microsoft Teams**: Chat, video calls, channels, meetings with transcripts
- **OneDrive/SharePoint**: Enterprise file management, version control, compliance
- **Planner**: Visual task management, kanban boards, team coordination
- **OneNote**: Note-taking and organization
- **Office Apps**: Word, Excel, PowerPoint (desktop + web)
- **Microsoft Search**: Unified search across all M365 content
- **Contacts**: Advanced contact management and CRM integration

### Available MCP Tools
- **Email**: `mcp__office-365-mcp__email` - Send, read, list, search
- **Email Search**: `mcp__office-365-mcp__email_search` - KQL advanced search
- **Calendar**: `mcp__office-365-mcp__calendar` - Events and scheduling
- **Teams Meetings**: `mcp__office-365-mcp__teams_meeting` - Video meetings, transcripts, recordings
- **Teams Channels**: `mcp__office-365-mcp__teams_channel` - Team collaboration
- **Teams Chat**: `mcp__office-365-mcp__teams_chat` - Direct messaging
- **Planner**: `mcp__office-365-mcp__planner_*` - Task and project management
- **Files**: `mcp__office-365-mcp__files` - OneDrive and SharePoint
- **Contacts**: `mcp__office-365-mcp__contacts` - Contact management
- **Search**: `mcp__office-365-mcp__search` - Unified M365 search

### Strengths & Best Use Cases
- **Enterprise features**: Advanced security, compliance, governance
- **Teams collaboration**: Video meetings, chat, channels, integrated workflow
- **Advanced Excel**: Complex data analysis, Power Query, Power Pivot
- **Professional presentations**: PowerPoint with advanced design tools
- **Task management**: Planner for visual project tracking
- **Meeting intelligence**: Teams transcripts, recordings, insights
- **Email rules**: Sophisticated inbox automation and organization
- **Version control**: SharePoint document versioning and co-authoring

---

## 🤝 GOOGLE WORKSPACE + OFFICE 365: UNIFIED WORKFLOW

### How They Work Together

**Use both systems to their strengths:**

**For Email:**
- Google Workspace: Personal and work correspondence, simple workflows
- Office 365: Enterprise email with advanced rules, integration with Teams

**For Documents:**
- Google Docs: Quick collaborative editing, real-time co-authoring, simple docs
- Microsoft Word: Complex formatting, advanced features, professional documents

**For Spreadsheets:**
- Google Sheets: Simple data, quick sharing, collaborative analysis
- Microsoft Excel: Complex analysis, Power Query, advanced formulas, dashboards

**For Presentations:**
- Google Slides: Quick presentations, easy sharing, web-first
- PowerPoint: Professional presentations, advanced design, animations

**For File Storage:**
- Google Drive: Easy sharing, public links, cross-platform access
- OneDrive/SharePoint: Enterprise storage, version control, compliance, permissions

**For Collaboration:**
- Google Meet: Quick video calls, easy scheduling
- Microsoft Teams: Full collaboration platform, channels, persistent chat, meeting records

**For Task Management:**
- Google Tasks/Calendar: Simple task tracking integrated with Gmail
- Microsoft Planner: Visual project boards, team task management

**For Notes:**
- Google Keep: Quick notes, lists, reminders
- OneNote: Structured notebooks, rich formatting, organization

### Integration Patterns

**Cross-Platform File Sharing:**
- Store files in Google Drive, share links in Teams
- Save OneDrive files, share in Gmail
- Reference both systems for complete file access

**Calendar Sync:**
- Export/import events between Google Calendar and Outlook
- Use both calendars for complete scheduling view

**Email Coordination:**
- Forward between accounts when needed
- Use appropriate account for context (personal vs work vs enterprise)

**Unified Search:**
- Search Google Workspace with native tools
- Search Office 365 with `mcp__office-365-mcp__search`
- Check both systems for comprehensive results

### Authentication

**Google Workspace:**
```bash
# Uses pre-configured OAuth tokens
# Located in: C:\Users\MarieLexisDad\Old Files\google-workspace-mcp\
```

**Office 365:**
```javascript
// Check authentication status
mcp__office-365-mcp__check_auth_status()

// Authenticate if needed
mcp__office-365-mcp__authenticate()
```

### Example Workflows

**Workflow 1: Send email with attachment from either system**
```
1. Ask user: "Which email account?"
2. If Google: Use Google Workspace MCP
3. If Office 365: Use mcp__office-365-mcp__email
4. Attach files from either Drive or OneDrive
```

**Workflow 2: Schedule meeting with both calendars**
```
1. Create event in Google Calendar (work schedule)
2. Create same event in Outlook (enterprise calendar)
3. Send meeting invite from appropriate email system
```

**Workflow 3: Collaborative project**
```
1. Create Planner board in Office 365 for task tracking
2. Store collaborative docs in Google Drive for easy sharing
3. Use Teams for communication and meetings
4. Reference everything from both systems
```

---

## 📊 PRODUCTIVITY PLATFORM INTELLIGENCE

**Full Documentation**: `docs/PRODUCTIVITY_PLATFORM_WORKFLOWS.md`

### Available Capabilities

**Google Workspace (11 APIs via Python)**:
Gmail • Drive • Docs • Sheets • Slides • Calendar • Forms • Cloud Vision • Vertex AI • BigQuery • Cloud Storage

**Microsoft 365 (30 MCP Tools)**:
Email • Teams (meetings/chat/channels) • Calendar • Planner (8 tools) • OneDrive/SharePoint • Contacts • Search • Notifications

### Auto-Suggestion Protocol

**Claude should PROACTIVELY suggest the best tool based on context without asking unnecessary questions.**

#### Email Operations

**Default: Gmail** (charlesmartinedd@gmail.com) via `python scripts/send_simple_email.py`
**Suggest Outlook when**: User mentions business/enterprise features, email rules, focused inbox

**Quick send (no questions)**:
```python
# Edit scripts/send_simple_email.py with recipient, subject, body
# Run: python scripts/send_simple_email.py
```

#### Document Creation

**Suggest Google Docs when**: User wants quick collaborative docs, easy sharing, simple formatting
```python
python scripts/create_google_doc.py  # Edit with title and content
```

**Suggest Microsoft Word when**: User wants complex formatting, professional documents, templates
```javascript
mcp__office-365-mcp__files({operation: "upload", ...})
```

**Suggest Google Sheets when**: Simple data, collaborative spreadsheets, quick charts
**Suggest Microsoft Excel when**: Advanced formulas, Power Query, complex analysis

**Suggest Google Slides when**: Quick presentations, web-first sharing
**Suggest Microsoft PowerPoint when**: Professional design, advanced animations

#### Project & Task Management

**Default: Microsoft Planner** (visual boards, team collaboration)
```javascript
mcp__office-365-mcp__planner_task({
  operation: "create",
  planId: "...",
  title: "Task name",
  assignedTo: "user-id",
  dueDateTime: "2025-11-15T17:00:00Z"
})
```

**Fallback: Google Calendar** (simple personal tasks)

#### Team Communication

**Default: Microsoft Teams** (full collaboration, transcripts, recordings)
```javascript
mcp__office-365-mcp__teams_meeting({operation: "create", ...})
mcp__office-365-mcp__teams_channel({operation: "create_message", ...})
```

**Fallback: Google Meet** (quick simple calls)

#### File Storage & Sharing

**Suggest Google Drive when**: Easy public sharing, cross-platform, unlimited storage
```python
# List files, share publicly, simple access
python scripts/audit_google_drive.py
```

**Suggest OneDrive/SharePoint when**: Enterprise security, version control, permissions
```javascript
mcp__office-365-mcp__files({operation: "search", query: "...", fileTypes: ["pdf"]})
```

#### AI/ML & Advanced Analytics

**Always suggest Google Cloud for**:
- **Image analysis**: Cloud Vision API (OCR, labels, faces, logos)
- **ML models**: Vertex AI (training, predictions, AutoML)
- **Big data**: BigQuery (SQL on massive datasets)

```python
# Claude should offer these capabilities when user mentions:
# "analyze image" → Cloud Vision
# "machine learning" → Vertex AI
# "big dataset" / "analytics" → BigQuery
```

### Decision Tree for Auto-Suggestions

```
User says: "send email" → Use Gmail (default), no questions
User says: "create document" → Ask: "Collaborative (Docs) or Professional (Word)?"
User says: "manage project" → Use Planner, no questions
User says: "team meeting" → Use Teams, no questions
User says: "analyze image" → Offer Cloud Vision
User mentions: "big data" → Suggest BigQuery
User wants: "file sharing" → Ask context, suggest Drive (easy) or OneDrive (secure)
```

### Platform Selection Summary

| Use Case | Tool | Why |
|----------|------|-----|
| Quick email | Gmail | Faster, simpler |
| Business email | Outlook | Enterprise features |
| Team docs | Google Docs | Real-time collaboration |
| Professional docs | Word | Advanced formatting |
| Simple data | Sheets | Quick, collaborative |
| Complex data | Excel | Power Query, advanced |
| Project management | Planner | Visual boards, assignments |
| Video meetings | Teams | Transcripts, recordings |
| File sharing | Drive | Easy public links |
| Enterprise storage | OneDrive | Security, compliance |
| Image analysis | Cloud Vision | OCR, labels, detection |
| ML models | Vertex AI | Training, predictions |
| Big data | BigQuery | SQL on huge datasets |

### Test Scripts

```bash
# Test all Google APIs
python scripts/test_all_google_apis.py

# List Office 365 capabilities
python scripts/test_office365_capabilities.py
```

**Google Enterprise AI/ML APIs** (Work Account: cmartin@alexandriasdesign.com):
- **Cloud Vision**: Image analysis, OCR → Suggest when user mentions "analyze image" or "extract text"
- **Speech-to-Text**: Audio transcription → Suggest when user mentions "transcribe" or "audio to text"
- **Text-to-Speech**: Voiceover generation → Suggest when user mentions "voiceover" or "narration"
- **Cloud Translation**: Translate to 100+ languages → Suggest when user mentions "translate" or other languages
- **Natural Language**: Text analysis, sentiment → Suggest when user mentions "analyze text" or "sentiment"
- **Video Intelligence**: Video analysis → Suggest when user mentions "analyze video" or "video tags"
- **Vertex AI**: Custom ML models → Suggest when user mentions "machine learning" or "AI model"

**Full API Guide**: `docs/GOOGLE_ENTERPRISE_API_GUIDE.md` (17 working APIs, 87 enabled)

---

## 🎨 BLENDER & 3D TOOLS

**Status**: ✅ Blender 4.3.0 installed and ready
**Location**: `C:\Users\MarieLexisDad\tools\blender\blender-4.3.0-windows-x64\blender.exe`
**Documentation**: `docs/BLENDER_AND_3D_TOOLS.md`

### Blender Capabilities

**3D Modeling & Creation:**
- Parametric modeling (cubes, spheres, cylinders, cones, etc.)
- Mesh editing with boolean operations
- Modifiers: subdivision, mirror, array, solidify
- Curve and surface modeling
- 3D text creation

**Simulations:**
- Physics: Rigid body, soft body dynamics
- Fluids: Liquid and gas simulation
- Cloth: Realistic fabric simulation
- Particles: Complex particle systems
- Smoke/Fire: Volumetric simulations
- Hair/Fur: Dynamic hair systems
- Ocean: Realistic ocean waves

**Rendering:**
- Cycles (photo-realistic path-tracing renderer)
- Eevee (real-time rendering engine)
- Workbench (fast preview rendering)
- Compositing and post-processing

**Import/Export Formats:**
- OBJ, FBX, GLTF/GLB, STL, PLY, X3D
- USD (Universal Scene Description)
- Alembic, COLLADA, SVG, PDF

**Python API:**
- Python 3.11 (bpy module)
- Headless rendering
- Batch processing
- Automation via scripts

### 3D Model Dataset - Google Scanned Objects

**Status**: ✅ Download script ready, Blender fully configured

**Google Scanned Objects Dataset** ✅ READY TO DOWNLOAD
- **Count**: 1,000+ high-quality 3D scanned household items
- **Formats**: OBJ, MTL, JPG textures, 2D renderings
- **License**: Creative Commons
- **Quality**: Professional photogrammetry scans
- **Use Cases**: Robotics, simulation, 3D graphics, ML training, product visualization

**Download Script:**
```bash
# Download 2D renderings (recommended for quick start)
python projects/3d-datasets/download_google_scanned_objects.py --renderings-only

# Custom output directory
python projects/3d-datasets/download_google_scanned_objects.py --output-dir ./datasets --renderings-only
```

**What's Included:**
- Multi-view 2D renderings of all objects (several GB)
- Various lighting and camera angles
- Perfect for training neural networks
- Full 3D meshes available via additional sources (see script help)

**Documentation**: `projects/3d-datasets/README.md`

**Integration with Blender:**
Once downloaded, objects can be imported into Blender:
```bash
# Via command line
blender --background --python import_scanned_object.py -- "path/to/object.obj"

# Or use Blender GUI: File → Import → Wavefront (.obj)
```

**Resources:**
- Research Paper: https://arxiv.org/abs/2204.11918
- Blog Post: https://ai.googleblog.com/2022/06/scanned-objects-by-google-research.html
- MuJoCo Models: https://github.com/kevinzakka/mujoco_scanned_objects

**Blender 4.3.0** ✅ READY
- Status: Fully installed and configured
- Location: `C:\Users\MarieLexisDad\tools\blender\blender-4.3.0-windows-x64\blender.exe`
- Use for: Modeling, rendering, simulations, import/export
- Python API: Available for automation

### Python Scripts Available

**Location**: `scripts/`
- `blender_info.py` - Show Blender capabilities and setup
- `setup_3d_access.py` - Configure access to 3D datasets
- `blender_examples/create_cube.py` - Create and render 3D cube
- `blender_examples/physics_sim.py` - Physics simulation demo
- `blender_examples/import_3d_model.py` - Import/render dataset models

**Location**: `projects/3d-datasets/`
- `download_google_scanned_objects.py` - Download Google Scanned Objects dataset
- `README.md` - Dataset documentation and usage guide

### Quick Commands

```bash
# Set Blender path
set BLENDER_PATH=C:\Users\MarieLexisDad\tools\blender\blender-4.3.0-windows-x64\blender.exe

# Show capabilities
python scripts/blender_info.py

# Create a 3D cube
%BLENDER_PATH% --background --python scripts/blender_examples/create_cube.py

# Run physics simulation
%BLENDER_PATH% --background --python scripts/blender_examples/physics_sim.py

# Import and render a model
%BLENDER_PATH% --background --python scripts/blender_examples/import_3d_model.py -- "path/to/model.obj"
```

### Integration with Workflow

**Blender can be used via Claude Code for:**
- Creating 3D models programmatically
- Running physics simulations
- Batch rendering 3D scenes
- Converting between 3D formats
- Generating synthetic training data for AI/ML
- Architectural visualization
- Product design and prototyping

**Example: Generate 3D model via Python**
```python
import subprocess

blender_path = r"C:\Users\MarieLexisDad\tools\blender\blender-4.3.0-windows-x64\blender.exe"
script_path = r"scripts/blender_examples/create_cube.py"

subprocess.run([blender_path, "--background", "--python", script_path])
```

---

## 🚨 CRITICAL: CONCURRENT EXECUTION & FILE MANAGEMENT

**ABSOLUTE RULES**:
1. ALL operations MUST be concurrent/parallel in a single message
2. **NEVER save working files, text/mds and tests to the root folder**
3. ALWAYS organize files in appropriate subdirectories
4. **USE CLAUDE CODE'S TASK TOOL** for spawning agents concurrently, not just MCP

### ⚡ GOLDEN RULE: "1 MESSAGE = ALL RELATED OPERATIONS"

**MANDATORY PATTERNS:**
- **TodoWrite**: ALWAYS batch ALL todos in ONE call (5-10+ todos minimum)
- **Task tool (Claude Code)**: ALWAYS spawn ALL agents in ONE message with full instructions
- **File operations**: ALWAYS batch ALL reads/writes/edits in ONE message
- **Bash commands**: ALWAYS batch ALL terminal operations in ONE message
- **Memory operations**: ALWAYS batch ALL memory store/retrieve in ONE message

### 🎯 CRITICAL: Claude Code Task Tool for Agent Execution

**Claude Code's Task tool is the PRIMARY way to spawn agents:**
```javascript
// ✅ CORRECT: Use Claude Code's Task tool for parallel agent execution
[Single Message]:
  Task("Research agent", "Analyze requirements and patterns...", "researcher")
  Task("Coder agent", "Implement core features...", "coder")
  Task("Tester agent", "Create comprehensive tests...", "tester")
  Task("Reviewer agent", "Review code quality...", "reviewer")
  Task("Architect agent", "Design system architecture...", "system-architect")
```

**MCP tools are ONLY for coordination setup:**
- `mcp__claude-flow__swarm_init` - Initialize coordination topology
- `mcp__claude-flow__agent_spawn` - Define agent types for coordination
- `mcp__claude-flow__task_orchestrate` - Orchestrate high-level workflows

### 📁 File Organization Rules

**NEVER save to root folder. Use these directories:**
- `/src` - Source code files
- `/tests` - Test files
- `/docs` - Documentation and markdown files
- `/config` - Configuration files
- `/scripts` - Utility scripts
- `/examples` - Example code

## Project Overview

This project uses SPARC (Specification, Pseudocode, Architecture, Refinement, Completion) methodology with Claude-Flow orchestration for systematic Test-Driven Development.

## SPARC Commands

### Core Commands
- `npx claude-flow sparc modes` - List available modes
- `npx claude-flow sparc run <mode> "<task>"` - Execute specific mode
- `npx claude-flow sparc tdd "<feature>"` - Run complete TDD workflow
- `npx claude-flow sparc info <mode>` - Get mode details

### Batchtools Commands
- `npx claude-flow sparc batch <modes> "<task>"` - Parallel execution
- `npx claude-flow sparc pipeline "<task>"` - Full pipeline processing
- `npx claude-flow sparc concurrent <mode> "<tasks-file>"` - Multi-task processing

### Build Commands
- `npm run build` - Build project
- `npm run test` - Run tests
- `npm run lint` - Linting
- `npm run typecheck` - Type checking

## SPARC Workflow Phases

1. **Specification** - Requirements analysis (`sparc run spec-pseudocode`)
2. **Pseudocode** - Algorithm design (`sparc run spec-pseudocode`)
3. **Architecture** - System design (`sparc run architect`)
4. **Refinement** - TDD implementation (`sparc tdd`)
5. **Completion** - Integration (`sparc run integration`)

## Code Style & Best Practices

- **Modular Design**: Files under 500 lines
- **Environment Safety**: Never hardcode secrets
- **Test-First**: Write tests before implementation
- **Clean Architecture**: Separate concerns
- **Documentation**: Keep updated

## 🚀 Available Agents (54 Total)

### Core Development
`coder`, `reviewer`, `tester`, `planner`, `researcher`

### Swarm Coordination
`hierarchical-coordinator`, `mesh-coordinator`, `adaptive-coordinator`, `collective-intelligence-coordinator`, `swarm-memory-manager`

### Consensus & Distributed
`byzantine-coordinator`, `raft-manager`, `gossip-coordinator`, `consensus-builder`, `crdt-synchronizer`, `quorum-manager`, `security-manager`

### Performance & Optimization
`perf-analyzer`, `performance-benchmarker`, `task-orchestrator`, `memory-coordinator`, `smart-agent`

### GitHub & Repository
`github-modes`, `pr-manager`, `code-review-swarm`, `issue-tracker`, `release-manager`, `workflow-automation`, `project-board-sync`, `repo-architect`, `multi-repo-swarm`

### SPARC Methodology
`sparc-coord`, `sparc-coder`, `specification`, `pseudocode`, `architecture`, `refinement`

### Specialized Development
`backend-dev`, `mobile-dev`, `ml-developer`, `cicd-engineer`, `api-docs`, `system-architect`, `code-analyzer`, `base-template-generator`

### Testing & Validation
`tdd-london-swarm`, `production-validator`

### Migration & Planning
`migration-planner`, `swarm-init`

## 🎯 Claude Code vs MCP Tools

### Claude Code Handles ALL EXECUTION:
- **Task tool**: Spawn and run agents concurrently for actual work
- File operations (Read, Write, Edit, MultiEdit, Glob, Grep)
- Code generation and programming
- Bash commands and system operations
- Implementation work
- Project navigation and analysis
- TodoWrite and task management
- Git operations
- Package management
- Testing and debugging

### MCP Tools ONLY COORDINATE:
- Swarm initialization (topology setup)
- Agent type definitions (coordination patterns)
- Task orchestration (high-level planning)
- Memory management
- Neural features
- Performance tracking
- GitHub integration

**KEY**: MCP coordinates the strategy, Claude Code's Task tool executes with real agents.

## 🚀 MCP Server Configuration

**Auto-loads on startup** (already configured in `.claude/mcp_settings.json`):
- ✅ Google Workspace (Gmail, Drive, Calendar, Docs, Sheets, Slides)
- ✅ Office 365 (Outlook, Teams, Planner, OneDrive, SharePoint)

**Optional MCPs** (load only when requested):
```bash
# Load these ONLY when specifically needed
# Currently set to disabled: true in mcp_settings.json

# Claude Flow - Swarm coordination and neural training
# To enable: Edit .claude/mcp_settings.json, set "disabled": false for claude-flow
claude mcp add claude-flow npx claude-flow@alpha mcp start

# RUV Swarm - Enhanced coordination (optional)
claude mcp add ruv-swarm npx ruv-swarm mcp start

# Flow Nexus - Cloud features (optional)
claude mcp add flow-nexus npx flow-nexus@latest mcp start
```

**To disable Claude Flow** (per user preference):
Edit `.claude/mcp_settings.json` and set `"disabled": true` for the `claude-flow` entry.

## MCP Tool Categories

### Coordination
`swarm_init`, `agent_spawn`, `task_orchestrate`

### Monitoring
`swarm_status`, `agent_list`, `agent_metrics`, `task_status`, `task_results`

### Memory & Neural
`memory_usage`, `neural_status`, `neural_train`, `neural_patterns`

### GitHub Integration
`github_swarm`, `repo_analyze`, `pr_enhance`, `issue_triage`, `code_review`

### System
`benchmark_run`, `features_detect`, `swarm_monitor`

### Flow-Nexus MCP Tools (Optional Advanced Features)
Flow-Nexus extends MCP capabilities with 70+ cloud-based orchestration tools:

**Key MCP Tool Categories:**
- **Swarm & Agents**: `swarm_init`, `swarm_scale`, `agent_spawn`, `task_orchestrate`
- **Sandboxes**: `sandbox_create`, `sandbox_execute`, `sandbox_upload` (cloud execution)
- **Templates**: `template_list`, `template_deploy` (pre-built project templates)
- **Neural AI**: `neural_train`, `neural_patterns`, `seraphina_chat` (AI assistant)
- **GitHub**: `github_repo_analyze`, `github_pr_manage` (repository management)
- **Real-time**: `execution_stream_subscribe`, `realtime_subscribe` (live monitoring)
- **Storage**: `storage_upload`, `storage_list` (cloud file management)

**Authentication Required:**
- Register: `mcp__flow-nexus__user_register` or `npx flow-nexus@latest register`
- Login: `mcp__flow-nexus__user_login` or `npx flow-nexus@latest login`
- Access 70+ specialized MCP tools for advanced orchestration

## 🚀 Agent Execution Flow with Claude Code

### The Correct Pattern:

1. **Optional**: Use MCP tools to set up coordination topology
2. **REQUIRED**: Use Claude Code's Task tool to spawn agents that do actual work
3. **REQUIRED**: Each agent runs hooks for coordination
4. **REQUIRED**: Batch all operations in single messages

### Example Full-Stack Development:

```javascript
// Single message with all agent spawning via Claude Code's Task tool
[Parallel Agent Execution]:
  Task("Backend Developer", "Build REST API with Express. Use hooks for coordination.", "backend-dev")
  Task("Frontend Developer", "Create React UI. Coordinate with backend via memory.", "coder")
  Task("Database Architect", "Design PostgreSQL schema. Store schema in memory.", "code-analyzer")
  Task("Test Engineer", "Write Jest tests. Check memory for API contracts.", "tester")
  Task("DevOps Engineer", "Setup Docker and CI/CD. Document in memory.", "cicd-engineer")
  Task("Security Auditor", "Review authentication. Report findings via hooks.", "reviewer")
  
  // All todos batched together
  TodoWrite { todos: [...8-10 todos...] }
  
  // All file operations together
  Write "backend/server.js"
  Write "frontend/App.jsx"
  Write "database/schema.sql"
```

## 📋 Agent Coordination Protocol

### Every Agent Spawned via Task Tool MUST:

**1️⃣ BEFORE Work:**
```bash
npx claude-flow@alpha hooks pre-task --description "[task]"
npx claude-flow@alpha hooks session-restore --session-id "swarm-[id]"
```

**2️⃣ DURING Work:**
```bash
npx claude-flow@alpha hooks post-edit --file "[file]" --memory-key "swarm/[agent]/[step]"
npx claude-flow@alpha hooks notify --message "[what was done]"
```

**3️⃣ AFTER Work:**
```bash
npx claude-flow@alpha hooks post-task --task-id "[task]"
npx claude-flow@alpha hooks session-end --export-metrics true
```

## 🎯 Concurrent Execution Examples

### ✅ CORRECT WORKFLOW: MCP Coordinates, Claude Code Executes

```javascript
// Step 1: MCP tools set up coordination (optional, for complex tasks)
[Single Message - Coordination Setup]:
  mcp__claude-flow__swarm_init { topology: "mesh", maxAgents: 6 }
  mcp__claude-flow__agent_spawn { type: "researcher" }
  mcp__claude-flow__agent_spawn { type: "coder" }
  mcp__claude-flow__agent_spawn { type: "tester" }

// Step 2: Claude Code Task tool spawns ACTUAL agents that do the work
[Single Message - Parallel Agent Execution]:
  // Claude Code's Task tool spawns real agents concurrently
  Task("Research agent", "Analyze API requirements and best practices. Check memory for prior decisions.", "researcher")
  Task("Coder agent", "Implement REST endpoints with authentication. Coordinate via hooks.", "coder")
  Task("Database agent", "Design and implement database schema. Store decisions in memory.", "code-analyzer")
  Task("Tester agent", "Create comprehensive test suite with 90% coverage.", "tester")
  Task("Reviewer agent", "Review code quality and security. Document findings.", "reviewer")
  
  // Batch ALL todos in ONE call
  TodoWrite { todos: [
    {id: "1", content: "Research API patterns", status: "in_progress", priority: "high"},
    {id: "2", content: "Design database schema", status: "in_progress", priority: "high"},
    {id: "3", content: "Implement authentication", status: "pending", priority: "high"},
    {id: "4", content: "Build REST endpoints", status: "pending", priority: "high"},
    {id: "5", content: "Write unit tests", status: "pending", priority: "medium"},
    {id: "6", content: "Integration tests", status: "pending", priority: "medium"},
    {id: "7", content: "API documentation", status: "pending", priority: "low"},
    {id: "8", content: "Performance optimization", status: "pending", priority: "low"}
  ]}
  
  // Parallel file operations
  Bash "mkdir -p app/{src,tests,docs,config}"
  Write "app/package.json"
  Write "app/src/server.js"
  Write "app/tests/server.test.js"
  Write "app/docs/API.md"
```

### ❌ WRONG (Multiple Messages):
```javascript
Message 1: mcp__claude-flow__swarm_init
Message 2: Task("agent 1")
Message 3: TodoWrite { todos: [single todo] }
Message 4: Write "file.js"
// This breaks parallel coordination!
```

## Performance Benefits

- **84.8% SWE-Bench solve rate**
- **32.3% token reduction**
- **2.8-4.4x speed improvement**
- **27+ neural models**

## Hooks Integration

### Pre-Operation
- Auto-assign agents by file type
- Validate commands for safety
- Prepare resources automatically
- Optimize topology by complexity
- Cache searches

### Post-Operation
- Auto-format code
- Train neural patterns
- Update memory
- Analyze performance
- Track token usage

### Session Management
- Generate summaries
- Persist state
- Track metrics
- Restore context
- Export workflows

## Advanced Features (v2.0.0)

- 🚀 Automatic Topology Selection
- ⚡ Parallel Execution (2.8-4.4x speed)
- 🧠 Neural Training
- 📊 Bottleneck Analysis
- 🤖 Smart Auto-Spawning
- 🛡️ Self-Healing Workflows
- 💾 Cross-Session Memory
- 🔗 GitHub Integration

## Integration Tips

1. Start with basic swarm init
2. Scale agents gradually
3. Use memory for context
4. Monitor progress regularly
5. Train patterns from success
6. Enable hooks automation
7. Use GitHub tools first

## Support

- Documentation: https://github.com/ruvnet/claude-flow
- Issues: https://github.com/ruvnet/claude-flow/issues
- Flow-Nexus Platform: https://flow-nexus.ruv.io (registration required for cloud features)

---

Remember: **Claude Flow coordinates, Claude Code creates!**

# important-instruction-reminders
Do what has been asked; nothing more, nothing less.
NEVER create files unless they're absolutely necessary for achieving your goal.
ALWAYS prefer editing an existing file to creating a new one.
NEVER proactively create documentation files (*.md) or README files. Only create documentation files if explicitly requested by the User.
Never save working files, text/mds and tests to the root folder.
