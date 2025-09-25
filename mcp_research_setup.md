# MCP Research Workflow Setup Guide

This guide shows you how to replicate the **0→1 research workflow** from the transcript using Cursor, Firecrawl MCP, and Perplexity MCP.

---

## 1. Cursor + Claude Code

**What It Is:**  
Cursor is the coding + research IDE. It has two “modes”:
- **Cursor Agent** (chat panel) → general tasks, MCP calls
- **Claude Code** (terminal assistant) → deeper context, step-by-step coding

**Setup Steps:**
1. [Download Cursor](https://cursor.sh) and sign in with GitHub/Google.  
2. In **Settings → Models**, enable **Claude Code** (choose Claude Sonnet/Opus for bigger context).  
3. Open a new project folder. Cursor will auto-detect your terminal + repo.  
4. Verify you can open:  
   - **Agent panel** (chat on the right)  
   - **Claude Code terminal** (bottom)  

**Pro Tip:** Use Claude Code for structured, multi-file projects; Cursor Agent for quick one-off prompts.

---

## 2. Firecrawl MCP (Site Audit)

**What It Is:**  
Firecrawl MCP crawls a domain → extracts **site copy, structure, UVPs, brand voice, CTAs**.

**Setup Steps:**
1. Get a [Firecrawl account](https://firecrawl.dev) → copy your **API key**.  
2. In Cursor:  
   - Go to **Settings → Tools & Integrations → MCPs**.  
   - Click **“Integrate New MCP”** and search for *Firecrawl*.  
   - Copy the MCP template → it will generate `mcp.json` in your project.  
3. Open `mcp.json` → paste your API key where indicated.  
4. Restart Cursor → verify **Firecrawl MCP** shows in integrations.  
5. Test with a kickoff prompt:  
   ``` 
   Use Firecrawl MCP to audit https://example.com. 
   Summarize target industry, ICP, UVPs, proof points, and brand voice. 
   Save to Site-Executive-Summary.md
   ```

**Deliverable:** `Site-Executive-Summary.md` with brand analysis.

---

## 3. Perplexity MCP (Competitive Research)

**What It Is:**  
Perplexity MCP lets you query the web inside Cursor. Perfect for **competitive analysis + market gaps**.

**Setup Steps:**
1. Get a [Perplexity API key](https://perplexity.ai).  
2. In Cursor:  
   - Add a new MCP → choose **Perplexity**.  
   - Paste API key into `mcp.json`.  
3. Restart Cursor → confirm integration.  
4. Run a research task:  
   ``` 
   Given Site-Executive-Summary.md, use Perplexity MCP to 
   find 5–7 gaps in the market for community-driven marketing platforms. 
   Summarize each gap as: Gap → Unique Angle → Content Ideas. 
   Save as Market-Gap-Analysis.md
   ```

**Deliverable:** `Market-Gap-Analysis.md` with competitor gaps + content angles.

---

## 4. Synthesizing in Cursor

**What It Is:**  
You use Cursor Agent + Claude to **prioritize + turn research into action**.

**Setup Steps:**
1. Reference docs in prompt:  
   ``` 
   Reference Site-Executive-Summary.md and Market-Gap-Analysis.md.  
   Prioritize 3 low-effort, high-impact social content ideas we can publish today.  
   ```
2. Expand one idea into a **draft post**:  
   ``` 
   Based on the “Implementation Void” gap, 
   draft an on-brand LinkedIn post showing how to go from 0→1 
   with Firecrawl + Perplexity MCPs. 
   No emojis/hashtags. Direct, conversational tone. 
   ```
3. Iterate: give feedback like *“make it beginner-friendly”* or *“add step-by-step instructions”*.  

**Deliverables:**  
- Priority Content Plan (today / this week / later)  
- First Post Draft (ready to tweak/publish)  

---

## ⚡ End-to-End Workflow (Quick Recap)

1. **Firecrawl MCP** → crawl + summarize your site → `Site-Executive-Summary.md`  
2. **Perplexity MCP** → competitor scan → `Market-Gap-Analysis.md`  
3. **Cursor Agent** → prioritize content opportunities  
4. **Claude Code (optional)** → expand into **scripts, posts, or full calendars**  

---
