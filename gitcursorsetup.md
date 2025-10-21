**Connect GitHub with Cursor before** (takes <5 min):

# 🧩 **First-Time GitHub Setup in Cursor**

### 1. Create a GitHub Account

If you don’t have one yet:
👉(https://github.com/signup)

---

### 2. Create a Repository (a project folder on GitHub)

1. Go to [https://github.com/new](https://github.com/new)
2. Name it something like `vibe-marketing-kit`
3. Choose **Public** or **Private**
4. Click **“Create repository”**

---

### 3. Copy the Repo URL

After it’s created, copy the **HTTPS URL**
(e.g. `https://github.com/yourname/vibe-marketing-kit.git`)

---

### 4. Open Cursor

1. Launch Cursor on your computer
2. Open your local project folder (or make a new empty one)

---

### 5. Open Terminal in Cursor

Go to the bottom → click **“+ Terminal”**
or press:

```
Ctrl + `  (Windows)
Cmd + `  (Mac)
```

---

### 6. Connect Your Folder to GitHub

In the terminal, type these commands one by one:

```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/yourname/vibe-marketing-kit.git
git push -u origin main
```

---

### 7. When Asked to Log In

Git will open a browser window asking you to sign in to GitHub.
Click **Authorize GitHub Desktop / Git CLI** → done ✅

If it asks for a **Personal Access Token (PAT)** instead:

* Go here: [https://github.com/settings/tokens](https://github.com/settings/tokens)
* Create a new one with scopes:
  `repo`, `workflow`, `read:org`
* Copy the token and paste it instead of your password.

---

### ✅ You’re Done!

Now Cursor is connected to GitHub.
Every time you save and push, it’ll sync your changes automatically.

