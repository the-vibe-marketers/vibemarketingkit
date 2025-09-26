
This guide shows you how to set up **Perplexity MCP** inside Cursor so you can query the web for **competitive research and market gaps**.

---

## ⚠️ Before You Begin
- A [Perplexity API key](https://perplexity.ai)  
- Cursor IDE installed  
- (Optional) `Site-Executive-Summary.md` already created with Firecrawl MCP  

---

## 1. Add Perplexity MCP

1. In Cursor, go to:  
   **Settings → Tools & Integrations → MCPs**
2. Click **“Integrate New MCP”** and search for **Perplexity**.  
   Cursor will generate or update a `mcp.json` file inside your project.

---

## 2. Configure `mcp.json`

Open the generated `mcp.json` and add your API key. Example:

```json
{
  "mcpServers": {
    "perplexity": {
      "command": "npx",
      "args": ["perplexity-mcp"],
      "env": {
        "PERPLEXITY_API_KEY": "your_api_key_here"
      }
    }
  }
}
````

👉 Replace `"your_api_key_here"` with your Perplexity API key.

---

## 3. Enable Perplexity MCP

* In Cursor, go back to **Settings → Tools & Integrations → MCPs**
* Toggle **Perplexity** to **ON**
* Restart Cursor to load the MCP

---

## 4. Sanity Check

Run this in Cursor’s integrated terminal:

```bash
perplexity search "top competitors in community-driven marketing platforms"
```

✅ If Perplexity is set up correctly, you’ll see search results returned.

---

## 5. First Prompt to Run in Cursor

Now test inside Cursor’s chat panel:

```
Given Site-Executive-Summary.md, use Perplexity MCP to 
find 5–7 gaps in the market for community-driven marketing platforms. 
Summarize each gap as: Gap → Unique Angle → Content Ideas. 
Save as Market-Gap-Analysis.md
```

**Deliverable:** `Market-Gap-Analysis.md` with competitor gaps + content angles.

---

## ✅ Quick Recap

1. Add Perplexity MCP in **Settings → MCPs**
2. Paste API key into `mcp.json`
3. Toggle Perplexity **ON** + Restart Cursor
4. Run `perplexity search "query"` to confirm
5. Start generating **Market-Gap-Analysis.md** reports

```

---

⚡ Now you’ll have **Firecrawl MCP** (site audit) + **Perplexity MCP** (competitive research) working side by side.  

Do you also want me to write a **combined setup.md** (Firecrawl + Perplexity in the same `mcp.json`) so users don’t get confused managing multiple MCPs?
```
