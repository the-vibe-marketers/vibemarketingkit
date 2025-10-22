
## 🔧 General Format for All `.md` Templates

At the **top of each file**, add this reusable system header:

```markdown
# 🧩 How to Use This Template

### 📍 Purpose
This file is a **reusable system template** for the MCP-powered research workflow inside Cursor.  
It’s meant to be copied into each client or project folder, where Claude Code + MCPs will fill it automatically.

---

### ⚙️ Steps to Use in Cursor

1. **Copy this file** from `/templates` into your project folder  
   Example:  
```

/projects/acme/market-gap-analysis.md

```

2. **Replace placeholders** like `[your-site.com]` or `[Gap Name]` if running manually  
OR  
**Run the automation prompt** in Cursor chat:
```

Copy all templates from /templates to /projects/[project-name].
Replace placeholders with project name and Firecrawl audit data.

```

3. **Reference this doc in a prompt** to Claude or the MCP:
```

Reference market-gap-analysis.md.
Fill it with 5–7 competitor gaps, each with a unique angle + content ideas.

```

4. Claude Code will automatically:
- Read this file as context
- Write results in Markdown structure
- Save the completed version back to your project folder

---

### 🪄 Pro Tip
If you’re using this repeatedly:
- Keep a clean `/templates` folder  
- Use a consistent naming format (`site-exec-summary.md`, `market-gap-analysis.md`, `priority-content-plan.md`, etc.)  
- Create a `generate-project.mcp` or `new-client.mcp` that automates copying templates and running Firecrawl + Perplexity for you
```

---

Then below that header, you include your existing **content template** (for example, your Priority Content Plan template).

Here’s how that looks together 👇

---

### ✅ Example: Final `priority-content-plan.md` Template

```markdown
# 🧩 How to Use This Template

### 📍 Purpose
This file helps you **prioritize content opportunities** identified in your Market Gap Analysis.  
Claude Code or the Cursor Agent will fill this file automatically by grouping ideas into “Today”, “This Week”, and “Later”.

---

### ⚙️ Steps to Use in Cursor

1. Copy this file from `/templates` into your client folder:  
```

/projects/acme/priority-content-plan.md

```

2. Run this prompt in Cursor Agent:
```

Reference Site-Executive-Summary.md and Market-Gap-Analysis.md.
Create a Priority Content Plan.md grouping ideas into Today, This Week, and Later,
with 2–3 actions per section.

```

3. Claude Code will:
- Analyze ICP + Gaps  
- Generate prioritized topics  
- Auto-fill this Markdown structure

---

# Priority Content Plan (Template)

## 🚀 Today (Low-effort / High-impact)
- **[Gap Name 1]:**
- [Idea 1]
- [Idea 2]
- **[Gap Name 2]:**
- [Idea 1]
- [Idea 2]

## 📅 This Week
- Expand [Series Name or Campaign]  
- Draft [Post Type or Guide]  
- Collect [UGC / Testimonials / Data]  

## 📈 Later
- Build [Long-form or Challenge Concept]  
- Launch [New Series / Strategy Name]  
- Expand into [Channel or Format Type]

---

### 📌 Prompt to Regenerate Automatically
```

Reference Site-Executive-Summary.md and Market-Gap-Analysis.md.
Prioritize 3–5 low-effort, high-impact content topics.
Group them under "Today", "This Week", and "Later".
Output a concise plan with 2–3 action items per category.

```
```

---

## 💡 What You’d Do for Each `.md` File

* Add that same **header block** (“🧩 How to Use This Template”)
* Adjust the **steps + prompts** for that specific file:

  * `site-exec-summary.md` → explains using Firecrawl MCP
  * `market-gap-analysis.md` → explains using Perplexity MCP
  * `priority-content-plan.md` → as above
  * `first-post-draft.md` → explains using Cursor Agent + references content plan
  * `mcp_research_setup.md` → stays as your root setup guide

