# 🏎️ Go-Kart Organization — Contributor Guide

Welcome to the **Go-Kart racing organization website project**!  
This guide explains step by step how to work with our repositories.  
We are building **5 HTML/CSS-only pages**, each in its own repository.

---

## 📂 Repositories
- `golf-home` — landing page (hero, highlights, nav).  
- `golf-events` — upcoming race schedule & registration info.  
- `golf-membeership` — past results, leaderboards, tables.  
- `golf-about-us` — about the org, racers & staff profiles.  
- `golf-contact` — contact details and simple contact page.  

---

## ⚙️ Prerequisites
1. Install **Git for Windows** (includes Git Bash):  
   👉 https://git-scm.com/download/win  
2. Install **Visual Studio Code**:  
   👉 https://code.visualstudio.com/  
3. Set your Git identity (open **Git Bash**):
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "you@example.com"
   git config --global core.autocrlf true

---

# 🚀 First-time setup

1. Copy the repo URL from GitHub (**Code → HTTPS**).
2. Open **Git Bash** and run:

   ```bash
   cd /c/Users/<your-user>/Documents
   git clone https://github.com/<org>/<repo>.git
   cd <repo>
   code .   # open project in VS Code
   ```

---

## 🌿 Branch workflow

* Do **not** commit directly to `main`.
* Create a feature branch for every change:

  ```bash
  git checkout main
  git pull origin main
  git checkout -b feature/<short-topic>
  ```
* Examples: `feature/hero-banner`, `feature/footer-links`.

---

## 📝 Editing files

* Work only in:

  ```
  index.html
  assets/css/styles.css
  assets/img/...
  ```
* Preview changes locally in VS Code (install **Live Server** extension).

---

## 💾 Save, commit & push

1. After editing, open **Git Bash** inside the repo:

   ```bash
   git status
   git add .
   git commit -m "feat: add hero banner section"
   git push -u origin feature/<short-topic>
   ```
2. GitHub will give you a link → open it to create a Pull Request.

---

## 🔀 Pull Requests (PR)

1. On GitHub → **Compare & pull request**.
2. Fill title & description (what you changed).
3. Add screenshots if it’s a visual change.
4. Click **Create pull request**.
5. Teammates review → **Merge pull request** → choose **Squash and merge**.

---

## 🧹 After merging

Clean up your branch:

```bash
git checkout main
git pull origin main
git branch -d feature/<short-topic>
git push origin --delete feature/<short-topic>
```

---

## 🔄 Keeping up to date

Always update your branch before working:

```bash
git checkout main
git pull origin main
git checkout feature/<your-branch>
git merge main
```

---

## ✅ Pull Request checklist

* [ ] Worked on a **feature branch**, not `main`.
* [ ] Only changed HTML/CSS files.
* [ ] Previewed changes locally.
* [ ] PR title is descriptive (e.g., `feat: add events table`).
* [ ] Added screenshots if visual.

---

## 🛠️ Git cheat sheet

```bash
git status                     # check changes
git branch                     # list branches
git checkout -b feature/topic  # new branch
git add .                      # stage all
git commit -m "msg"            # commit
git push -u origin branch      # push
git pull origin main           # update
git merge main                 # merge latest main
git branch -d feature/topic    # delete local branch
git push origin --delete ...   # delete remote branch
```

---

## 📌 Project rules

* ✅ One task = one branch = one PR.
* ✅ Never push to `main` directly.
* ✅ Keep PRs small and clear.
* ✅ Use meaningful commit messages.
* ✅ Always pull latest `main` before starting new work.

---

👏 That’s it! If you follow this guide — clone → branch → edit → commit → push → PR → merge —
our Go-Kart website will be built smoothly with no conflicts 🚦
