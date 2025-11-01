## 🚀 SCALING PROTOCOL - GETTING TO THE BREAD

**CRITICAL: Port Management** - Before launching any server, ALWAYS check for available ports first using `netstat -ano | findstr "LISTENING"` to verify the port is not in use. Never assume a port is available - always verify before attempting to start a server to avoid conflicts.

**CRITICAL: Office 365 & Google Workspace Access** - Claude Code ALWAYS has full access to Office 365 and Google Workspace via MCP tools that auto-load on startup. NEVER ask "do you have access?" or suggest third-party alternatives. YOU HAVE: Office 365 MCP (Outlook, Teams, Planner, OneDrive, SharePoint, Contacts, Search), Google Workspace MCP (Gmail, Drive, Docs, Sheets, Slides, Calendar, Classroom). These are ALWAYS active and authenticated. Use them directly for any task involving email, calendars, documents, task management, file storage, or team collaboration.

**Who We Are**: Charles Martin and Dr. Marie Martin are educational technology entrepreneurs who co-founded Alexandria's Design, a consulting business transforming how schools adapt to the Fourth Industrial Revolution. Charles brings deep expertise in AI orchestration, multi-agent workflows, and edtech product development (including ModelIt! for K-12 students), while Dr. Marie Martin contributes 25+ years of educational leadership, curriculum development, and instructional design across K-12, higher education, government, and military sectors. Together, they're building innovative educational platforms that integrate cutting-edge AI with human-centered design, creating scalable solutions for professional development, customized learning, and interactive educational experiences.

**Our Purpose**: We're building Alexandria's Design to achieve unlimited monthly recurring revenue—no ceiling, just growth. We create educational technology solutions that transform learning while generating passive income through automation, reusable assets, and productized services. Every project we undertake should move us closer to systems that serve unlimited clients simultaneously and scale without proportional time investment. We're not building a lifestyle business—we're building a revenue engine.

**What We're About**: Alexandria's Design helps schools, districts, and educational organizations embrace future-ready practices through professional development, workshops, customized learning solutions, and AI-integrated educational experiences. We specialize in turning complex educational challenges into scalable, automated solutions that blend Dr. Marie's deep educational expertise with Charles's technical innovation. Our focus is on creating reusable, high-quality assets that can be deployed across multiple clients, ensuring both educational impact and business scalability.

**How We Work**: When we approach any project, we think revenue-first: Does this generate income? Can it scale infinitely? Is it reusable? Can it be automated? We prioritize building systems over completing one-off tasks, creating templates over custom solutions, and developing passive income streams over hourly work. Charles's time and Dr. Marie's expertise are our most valuable resources, so we focus on strategic, high-value creation while automating everything else. We're not just completing tasks—we're building an unlimited revenue engine. Let's get to the bread.

---

## 🚀 QUICK AGENT REFERENCE

**When to invoke specialized agents** (use Claude Code's Task tool):

| When User Says... | Invoke Agent | File Location | Why |
|-------------------|--------------|---------------|-----|
| "Saturday review" / "check finances" / "should I buy..." | **Big Baller** | `.claude/agents/big-baller.md` | Financial tracking, expense decisions |
| "Create workflow" / "automate this" / "n8n" | **Workflow Wizard** | `.claude/agents/workflow-wizard.md` | n8n automation (NO GUI!) |
| "Find grants" / "analyze screenshot" / "recent trends" | **Grok Keeps it Real** | `.claude/agents/grok-keeps-it-real.md` | Nov 2024 knowledge + vision |
| "Generate 100..." / "bulk content" / "cheap generation" | **GLM Is Not Claude Code** | `.claude/agents/glm-is-not-claude-code.md` | Cost-efficient generation (must verify!) |
| "Test website" / "debug this" / "why isn't it working?" | **The Validator** | `.claude/agents/the-validator.md` | QA, testing, debugging |
| "Send email" / "Google Doc" / "Drive" / "Sheets" | **Getting to the Google** | `.claude/agents/getting-to-the-google.md` | Google Workspace + Cloud AI |
| "Teams meeting" / "Planner" / "Outlook" / "SharePoint" | **Money Making Microsoft** | `.claude/agents/money-making-microsoft.md` | M365 enterprise features |
| "Create image" / "3D model" / "course cover" | **Bob Ross Image 3D Makers** | `.claude/agents/bob-ross-image-3d-makers.md` | Visual content creation |

**Invocation syntax**: `Task("Agent Name", "your task description", "agent-slug")`

**Default behaviors (no agent needed)**:
- **Email**: Defaults to Gmail (charlesmartinedd@gmail.com) via `python scripts/send_simple_email.py`
- **Quick tasks**: Claude Code handles directly (file operations, simple questions, general conversation)
- **Simple questions**: No specialized agent needed

---

## 🤔 AGENT DECISION TREE

```
User request → Evaluate domain → Invoke appropriate agent

Financial decision? → Big Baller
Automation/workflow? → Workflow Wizard
Recent info/grants/screenshots? → Grok Keeps it Real
Bulk generation (cost-sensitive)? → GLM Is Not Claude Code
Testing/debugging/validation? → The Validator
Google ecosystem? → Getting to the Google
Microsoft 365? → Money Making Microsoft
Visual content (images/3D)? → Bob Ross Image 3D Makers
Simple task? → Claude Code handles directly (no agent)
```

**Use agents when**:
- Task requires specialized domain knowledge
- Multiple steps in specialized domain
- Revenue/financial decisions needed
- Testing/validation required
- Platform-specific operations (Google, Microsoft, n8n)
- Cost-optimization important (Grok vs GLM)

**DON'T use agents for**:
- Simple one-off questions
- Quick file operations (Read, Write, Edit)
- General conversation
- Tasks Claude Code handles directly

---

## 💰 FINANCIAL COMMAND CENTER

**Big Baller Agent**: For financial tracking, Saturday reviews, expense decisions, and revenue analysis, use the `big-baller` agent (`.claude/agents/big-baller.md`). Monthly goal: $30k. Revenue-first decisions only. Track via `scripts/lunchmoney_helper.py`. Invoke with: `Task("Big Baller", "your financial query", "big-baller")`

**Auto-invoke when user says**:
- "Saturday review" / "It's Saturday" / "Weekly financial review"
- "Check finances" / "How are we doing financially?"
- "Should I buy..." / "Should I subscribe to..."
- "Is this expense worth it?" / "ROI on this tool?"
- "Track revenue" / "Income this week" / "Progress to $30k"

---

## 🔄 N8N WORKFLOW AUTOMATION

**Status**: ✅ Running on port 5678 | API Key configured
**API Key**: `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIzN2NkZGI4Ny1kNDk4LTQxZTUtYTVjMi0yNWNmZmY1MDZhZWEiLCJpc3MiOiJuOG4iLCJhdWQiOiJwdWJsaWMtYXBpIiwiaWF0IjoxNzYyMDAzODg3fQ.cWnwy9w0m9cn3i4wazqadJq-qRFl5KIR3e70ta8Rufc`

**Workflow Wizard Agent**: For n8n automation, workflow building, and integration tasks, use the `workflow-wizard` agent (`.claude/agents/workflow-wizard.md`). **CRITICAL**: NO GUI ever—build programmatically via n8n MCP tools. Docker on port 5678. Scripts: `scripts/n8n-automation/`. Invoke with: `Task("Workflow Wizard", "your automation task", "workflow-wizard")`

**Auto-invoke when user says**:
- "Create an n8n workflow" / "Build a workflow" / "Automate this process"
- "Connect Gmail to..." / "When email arrives, do..."
- "Schedule automated..." / "Run this daily/weekly"
- "Webhook trigger" / "API integration"
- **NEVER**: "Open n8n" / "Use the GUI" (forbidden!)

---

## 📅 MONDAY.COM - PROJECT & REVENUE TRACKING

**Status**: ✅ MCP Active | Token in `.env` as MONDAY_API_TOKEN

**Why It Matters**: Monday.com is your revenue operations center. Track client projects, manage course development pipelines, monitor team tasks, and automate client onboarding—all without touching a GUI. Every board should connect to a revenue stream. This is where you see what's making money, what's in progress, and what's next.

**Revenue Applications**: Client project tracking with timelines and deliverables (know exactly where money is), course development pipelines from conception to launch (build assets that sell repeatedly), student progress monitoring at scale (serve unlimited students), automated client onboarding workflows (less manual work = more capacity), billable hour tracking linked to projects (never miss revenue).

**Setup**: Token stored in `.env`. If expired, get fresh token at monday.com → Profile → Developers → My Access Tokens.

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

## 🤖 AI API SERVICES (OpenAI, OpenRouter, Grok 4 & GLM-4.6)

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

### Grok 4 API - Recent Intelligence & Vision

**Grok Keeps it Real Agent**: For recent knowledge (Nov 2024), grant research, screenshot analysis, massive documents (2M context), and market intelligence, use the `grok-keeps-it-real` agent (`.claude/agents/grok-keeps-it-real.md`). Cost: ~$0.02-0.05/query. Helper: `scripts/api-helpers/grok_helper.py`. Invoke with: `Task("Grok Keeps it Real", "your research query", "grok-keeps-it-real")`

**Auto-invoke when user mentions**:
- "Find grants" / "Grant opportunities" / "DoE funding"
- "Analyze this screenshot" / "What's wrong in this image?"
- "Recent trends in..." / "Latest developments in..." / "2024-2025 market"
- "Analyze this RFP" / "Read this 50-page document"
- "Competitor analysis" / "What are competitors doing?"

### GLM-4.6 API - Cheap Code & Content Generation

**GLM Is Not Claude Code Agent**: For cost-efficient code generation and bulk content creation, use the `glm-is-not-claude-code` agent (`.claude/agents/glm-is-not-claude-code.md`). **CRITICAL**: GLM generates only—Claude Code must verify and execute. 5x cheaper than Grok. Helper: `scripts/api-helpers/glm_helper.py`. Invoke with: `Task("GLM Is Not Claude Code", "generate [description]", "glm-is-not-claude-code")`

**Auto-invoke when user says**:
- "Generate 50..." / "Generate 100..." / "Bulk create..."
- "Create lesson plans at scale" / "Mass quiz generation"
- "Cheap code generation" / "Cost-efficient generation"
- **CRITICAL**: Always verify and execute with Claude Code after generation!

---

## 🐙 GITHUB VERSION CONTROL

**Git Guardian Agent**: For all git operations (commits, pushes, PRs, branching), use the `git-guardian` agent (`.claude/agents/git-guardian.md`). **CRITICAL**: Never commit without user permission. Quality commits with descriptive messages. Safety-first with version control. Invoke with: `Task("Git Guardian", "commit these changes", "git-guardian")`

**Auto-invoke when user says**:
- "Commit this" / "Push to GitHub" / "Create commit"
- "Make a PR" / "Pull request" / "Create branch"
- "Git add" / "Git push" / User explicitly requests version control

**GitHub Account**: charlesmartinedd | **Never commit without asking first**

---

## 🌐 WEBSITE TESTING & DEBUGGING PROTOCOL

**The Validator Agent**: For website validation, debugging, and quality assurance, use the `the-validator` agent (`.claude/agents/the-validator.md`). **MANDATORY**: Full testing protocol with Playwright, Chrome DevTools, screenshots. Can use OpenRouter premium models (ChatGPT-5) for complex debugging. NEVER declare "it works" without proof. Invoke with: `Task("The Validator", "validate [website/code]", "the-validator")`

**Auto-invoke when user says**:
- "Test this website" / "Is this working?" / "Does it work?"
- "Debug this" / "Why isn't this working?" / "Fix this error"
- "Blank page" / "Not loading" / "Console errors"
- "Validate before deployment" / "QA check"
- **Philosophy**: NEVER assume it works without proof!

### 🚨 MANDATORY WEBSITE LAUNCH PROTOCOL

**Every single time you launch, modify, or work on ANY website, you MUST follow this exact sequence without exception:**

First, verify the port is available using `netstat -ano | findstr "LISTENING"` and find an open port (8080, 8000, 3000, etc.). Then launch http-server in the website's directory on that verified port in the background. Immediately after the server starts, open the website in Chrome browser using `start http://127.0.0.1:[port]/index.html`. While the browser is loading, run Playwright tests using `npx playwright test --headed --screenshot=on` to capture automated verification. Once the browser opens, manually press F12 to open Chrome DevTools and check three critical tabs: Console (must show zero red errors), Network (all resources must return 200 status, no 404s), and Elements (verify HTML structure and CSS is applied). Take screenshots of the working website using Playwright's screenshot feature and save them to the screenshots folder with descriptive names. If ANY errors appear in Console or Network tabs, stop and debug immediately using DevTools - do not proceed until all errors are resolved. Only after ALL checks pass (automated tests green, console clean, network clean, screenshots captured) can you declare the website working. Document what was tested in a brief summary and ask the user if they want to see the test results. This is NOT optional - this protocol must be executed completely for every website interaction, every time, without shortcuts or assumptions.

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

**Getting to the Google Agent**: For all Google Workspace and Cloud operations (Gmail, Drive, Docs, Sheets, Slides, Calendar, Classroom, Cloud AI APIs), use the `getting-to-the-google` agent (`.claude/agents/getting-to-the-google.md`). Manages 3 accounts seamlessly, 11 APIs, revenue-generating Cloud services. Invoke with: `Task("Getting to the Google", "your Google task", "getting-to-the-google")`

**Auto-invoke when user says**:
- "Send email" / "Gmail" / "Create Google Doc"
- "Share in Drive" / "Google Sheets" / "Slides presentation"
- "Schedule meeting" / "Google Calendar"
- "OCR this image" / "Translate to Spanish" / "Transcribe audio" (Cloud AI)
- "Google Classroom" / "Course delivery"

**Accounts**: charlesmartinedd@gmail.com (personal), cmartin@alexandriasdesign.com (work), lmcmtutors@gmail.com (bills) ✅

**OAuth Tokens**: `C:\Users\MarieLexisDad\Old Files\google-workspace-mcp\token-*.json`
**Full details**: See Getting to the Google agent file

---

## 🏢 OFFICE 365 / MICROSOFT 365 ACCESS

**Money Making Microsoft Agent**: For all Microsoft 365 operations (Outlook, Teams, Planner, OneDrive, SharePoint, Contacts, Calendar), use the `money-making-microsoft` agent (`.claude/agents/money-making-microsoft.md`). 30 MCP tools, Teams transcripts, Planner boards (8 tools!), enterprise features. Invoke with: `Task("Money Making Microsoft", "your M365 task", "money-making-microsoft")`

**Auto-invoke when user says**:
- "Teams meeting" / "Schedule Teams call" / "Meeting transcript"
- "Planner board" / "Create tasks" / "Project management"
- "Outlook" / "Enterprise email" / "Email rules"
- "SharePoint" / "OneDrive" / "Version control"
- "Meeting intelligence" / "AI summary" / "Action items"

**Status**: ✅ MCP tools loaded and active (30 tools total)

**Tokens**: `C:\Users\MarieLexisDad\.office-mcp-tokens.json`
**Full details**: See Money Making Microsoft agent file

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

## 🎨 IMAGE & 3D CREATION

**Bob Ross Image 3D Makers Agent**: For AI image generation (OpenAI, OpenRouter) and 3D modeling (Blender, Google Scanned Objects), use the `bob-ross-image-3d-makers` agent (`.claude/agents/bob-ross-image-3d-makers.md`). Course covers, marketing materials, 3D models, simulations. "No mistakes, just happy little visuals." Invoke with: `Task("Bob Ross Image 3D Makers", "create [description]", "bob-ross-image-3d-makers")`

**Auto-invoke when user says**:
- "Create course cover" / "Design image" / "Marketing graphic"
- "Generate 20 images" / "Batch image creation"
- "3D model" / "Blender" / "Physics simulation"
- "Render 3D" / "Create visual assets"
- "DALL-E" / "AI image" / "Happy little visuals"

**Tools**: Blender 4.3.0, OpenAI DALL-E, OpenRouter, Google 3D dataset | **Docs**: `docs/BLENDER_AND_3D_TOOLS.md`

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

## 🚀 Available Agents (59 Total)

### Specialized Domain Agents (New! - 9 Total)
`big-baller` (financial tracking), `workflow-wizard` (n8n automation), `grok-keeps-it-real` (recent intelligence), `glm-is-not-claude-code` (cheap generation), `the-validator` (debugging & QA), `getting-to-the-google` (Google Workspace/Cloud), `money-making-microsoft` (M365 enterprise), `bob-ross-image-3d-makers` (visual creation), `git-guardian` (version control)

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
