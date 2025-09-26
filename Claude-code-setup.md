
# Setup Claude Code in Cursor

This guide shows you how to set up **Claude Code** inside Cursor (or Windsurf / VS Code) so you can use **Opus 4** directly in your IDE.

---

## ⚠️ Before You Begin
- A **Claude Max subscription** ($100–$200/month) → [Sign up here](https://claude.ai)  
- Cursor (or Windsurf / VS Code) installed  
- Access to your **integrated terminal**

---

## 1. Subscribe to Claude Max
- Go to [Anthropic Claude](https://claude.ai)  
- Subscribe to a **Claude Max plan** ($100–$200/month)  
- Claude Code (with Opus 4) is included in this plan  

---

## 2. Install Claude Code
1. Copy the **install command** from Claude’s website (after subscription).  
2. Open **Cursor’s integrated terminal**.  
3. Paste the command, e.g.:

   ```bash
   npm install -g claude-code
````

---

## 3. Connect Cursor to Claude Code

* In Cursor’s terminal, type:

  ```bash
  cla
  ```
* You should see **“IDE connected”**.

If the Claude Code window doesn’t open:

* Hit `⌘ + P` → type `> Run Claude Code` → select it.

---

## 4. Verify Setup

Run in terminal:

```bash
cla --version
```


