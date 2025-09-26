

This guide shows you how to set up **Firecrawl MCP** inside Cursor so you can crawl any website and extract **site copy, structure, UVPs, brand voice, and CTAs**.

---

## ⚠️ Before You Begin
- A [Firecrawl account](https://firecrawl.dev)  
- Your **Firecrawl API key** (copy from dashboard)  
- Cursor IDE installed  

---

## 1. Add Firecrawl MCP

1. In Cursor, go to:  
   **Settings → Tools & Integrations → MCPs**
2. Click **“Integrate New MCP”** and search for **Firecrawl**.  
   Cursor will generate or update a `mcp.json` file inside your project.

---

## 2. Configure `mcp.json`

Open the generated `mcp.json` and add your API key. Example:

```json
{
  "mcpServers": {
    "firecrawl": {
      "command": "npx",
      "args": ["firecrawl-mcp"],
      "env": {
        "FIRECRAWL_API_KEY": "your_api_key_here"
      }
    }
  }
}
````

👉 Replace `"your_api_key_here"` with the API key from Firecrawl.

---

## 3. Enable Firecrawl MCP

* In Cursor, go back to **Settings → Tools & Integrations → MCPs**
* Toggle **Firecrawl** to **ON**
* Restart Cursor to load the MCP

---

## 4. Sanity Check

Run this in Cursor’s integrated terminal:

```bash
firecrawl scrape https://example.com
```

✅ If Firecrawl is set up correctly, you’ll see scraped page data returned.

---

## 5. First Prompt to Run in Cursor

Now test inside Cursor’s chat panel:

```
Use Firecrawl MCP to audit https://example.com. 
Summarize target industry, ICP, UVPs, proof points, and brand voice. 
Save to Site-Executive-Summary.md
```

**Deliverable:** `Site-Executive-Summary.md` with a baseline brand/site analysis.

---

## ✅ Quick Recap

1. Add Firecrawl MCP in **Settings → MCPs**
2. Paste API key into `mcp.json`
3. Toggle Firecrawl **ON** + Restart Cursor
4. Run `firecrawl scrape https://example.com` to confirm
5. Start auditing sites → save insights into `.md` files

```

---

Would you like me to also draft a **parallel `Setup-Perplexity-MCP.md`** (with JSON snippet + toggle + sanity check) so both research MCPs match your setup style?
```
