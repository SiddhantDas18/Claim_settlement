# Claim_settlement

## Add 2 existing repositories into this repo (monorepo-style)

Yes, it is possible.  
If you want both projects to stay linked to their original upstream repositories, use **Git submodules**.

### 1) Add both existing repositories

```bash
git submodule add -b main <repo-1-url> projects/repo-1
git submodule add -b main <repo-2-url> projects/repo-2
git commit -m "Add repo-1 and repo-2 as submodules"
```

### 2) Make pull also update linked repositories

```bash
git config pull.rebase false
git config submodule.recurse true
git config fetch.recurseSubmodules on-demand
```

Now a normal pull will recurse into submodules:

```bash
git pull --recurse-submodules
```

### 3) Pull latest changes from each upstream later

```bash
git submodule update --remote --merge
git add .gitmodules projects/repo-1 projects/repo-2
git commit -m "Update submodules to latest upstream commits"
```

### Notes
- Replace `<repo-1-url>` and `<repo-2-url>` with your real repository URLs.
- If your default branch is `master` (or something else), replace `-b main` accordingly.