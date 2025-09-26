

1. **MCP Code Template**

   * When you “Integrate New MCP” in Cursor, it auto-generates a `mcp.json` (or updates your main MCP config).
   * This JSON file defines:

     * `name` → `"firecrawl"`
     * `type` → `"http"`
     * `endpoint` → the Firecrawl API URL
     * `auth` → placeholder for API key
   * Users need to **paste the API key** in the right place inside this JSON.
   * Without showing a stub of the code template, people new to Cursor/MCPs get lost.

   Example snippet you could add to the doc:

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
   ```

---

2. **Toggle / Enable MCP in Cursor**

   * After editing `mcp.json`, you also need to:

     * Go to **Settings → Tools & Integrations → MCPs**.
     * Ensure the toggle for **Firecrawl** is switched **ON**.
   * Then **restart Cursor** so the MCP actually loads.

---

3. **Sanity Check Command**

   * Add a one-liner for quick verification before people run prompts:

   ```bash
   firecrawl scrape https://example.com
   ```

   If it responds with HTML/JSON snippets, you know the integration works.

