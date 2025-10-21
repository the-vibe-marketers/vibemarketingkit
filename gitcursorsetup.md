Looks like I can’t access your GitHub content right now — no repositories are currently connected.
To fix this so I can pull the exact **GitHub × Cursor setup guide**, please:

1. Click **“Use Connectors”** (in the sidebar or toolbar).
2. Choose **GitHub** → select the repos you want me to access.
3. Then just say **“done”**, and I’ll fetch the correct setup instructions.

In the meantime, here’s a clean **manual guide** you can use immediately 👇

---

# ⚙️ Setup GitHub in Cursor

Connect GitHub so you can version-control Claude Code projects directly in your IDE.

---

## 1. **Sign in to GitHub**

* Go to [GitHub](https://github.com/login) and log in.
* If 2FA is enabled, make sure it’s accessible.

---

## 2. **Connect GitHub in Cursor**

1. Open Cursor → click the **Settings ⚙️ icon** in the bottom-left.
2. Navigate to **Integrations → GitHub**.
3. Click **“Connect GitHub Account”** and authorize Cursor.
4. Once connected, Cursor will show your available repositories.

---

## 3. **Clone or Create a Repo**

* To **clone**:
  Open the Command Palette (`⌘ + P` → `> Clone Repository`) → paste your GitHub repo URL.
* To **create a new repo**:

  1. In GitHub, click **New Repository** → name it (e.g., `vibe-marketing-kit`).
  2. In Cursor terminal:

     ```bash
     git init
     git remote add origin https://github.com/yourname/vibe-marketing-kit.git
     ```

---

## 4. **Authenticate Git from Cursor**

If prompted for authentication:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Then authenticate with a **Personal Access Token (PAT)** instead of a password:

* Create one at [github.com/settings/tokens](https://github.com/settings/tokens)
* Select scopes: `repo`, `workflow`, `read:org`

---

## 5. **Commit and Push from Cursor**

```bash
git add .
git commit -m "initial commit"
git push -u origin main
```

You can now use Claude Code + GitHub seamlessly — building, committing, and iterating without leaving Cursor.

