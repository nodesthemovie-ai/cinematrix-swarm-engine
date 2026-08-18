# CineMatrix Workflow Guide

## Overview

This repository supports **3 parallel git workflows** to accommodate different development styles and team structures. Choose the one that fits your needs.

---

## Workflow 1: Feature Branch → Pull Request to Main

**Best for:** Teams with formal review processes, stable releases

### Branches
- **main** — Production-ready releases (stable)
- **feature/*** — Individual feature work

### Process

```
main (stable)
    ↑
    ├─ (PR review & testing)
    │
feature/enhanced-dossier  (your work)
feature/advanced-agents   (your work)
```

### Steps

1. **Create feature branch** (already done)
   ```bash
   git checkout feature/enhanced-dossier
   ```

2. **Make changes** — Add commits to your feature branch

3. **Push to GitHub**
   ```bash
   git push origin feature/enhanced-dossier
   ```

4. **Create Pull Request**
   - Go to https://github.com/nodesthemovie-ai/cinematrix-swarm-engine
   - Click "New Pull Request"
   - Select: `main` ← `feature/enhanced-dossier`
   - Add description & request reviewers
   - Submit PR

5. **Code Review** — Address feedback in PR comments

6. **Merge** — Once approved, merge to main

### Current Status
- ✅ `feature/enhanced-dossier` — Ready for PR to main
  - File: `enhanced_dossier_template.md`
  - Changes: +63 lines
  
- ✅ `feature/advanced-agents` — Ready for PR to main
  - File: `advanced_agents.md`
  - Changes: +145 lines

### How to Create PR from Feature Branch

```bash
# Switch to feature branch
git checkout feature/enhanced-dossier

# Ensure latest pushed
git push origin feature/enhanced-dossier

# Then visit GitHub and click "Compare & Pull Request"
```

---

## Workflow 2: Develop as Integration Branch

**Best for:** Continuous integration, staged releases, team collaboration

### Branches
- **main** — Production releases (stable, tag releases)
- **develop** — Integration & testing (staging)
- **feature/*** — Individual work

### Process

```
main (v1.0, v1.1, v2.0 releases)
    ↑
    ├─ (Release candidate testing)
    │
develop (integration branch)
    ↑
    ├─ (Merged features)
    │
feature/enhanced-dossier  (your work)
feature/advanced-agents   (your work)
```

### Steps

1. **Feature branches merge to develop**
   ```bash
   git checkout develop
   git merge feature/enhanced-dossier
   git merge feature/advanced-agents
   git push origin develop
   ```
   ✅ Already completed above

2. **Test on develop** — Run full test suite

3. **When ready for release:**
   ```bash
   git checkout main
   git merge develop
   git tag v1.1.0
   git push origin main --tags
   ```

### Current Status
- ✅ **develop** branch has both features integrated
  - Contains: enhanced_dossier_template.md + advanced_agents.md
  - Ready for testing and staging
  - Can merge to main when stable

### Advantages
- Features tested together before main
- Easy to revert entire features
- Clear separation: main = stable, develop = testing
- Good for larger teams

---

## Workflow 3: Keep Main Clean (Current State)

**Best for:** Simple projects, solo developers, minimal overhead

### Branches
- **main** — Always production-ready (no breaking changes)
- **feature/*** — Work branches as needed

### Process

```
main (always stable)
    ↑
    ├─ (Direct commits when stable)
    │
feature/enhanced-dossier  (experimental)
feature/advanced-agents   (experimental)
```

### Current Status
- ✅ **main** is clean and stable
- ✅ Features in separate branches
- ✅ No PRs required (but can use them)

### When Ready
```bash
# If feature is stable, merge directly
git checkout main
git merge feature/enhanced-dossier
git push origin main

# Or create PR for visibility
```

---

## Comparison Table

| Aspect | Workflow 1 (PR) | Workflow 2 (Develop) | Workflow 3 (Simple) |
|--------|---|---|---|
| **Review Process** | Required | Optional | Not needed |
| **Staging Phase** | In PR | In develop | No |
| **Release Process** | Manual | Scheduled | On-demand |
| **Team Size** | Medium-Large | Large | Solo-Small |
| **Stability Risk** | Low | Medium | Medium |
| **Complexity** | High | Medium | Low |

---

## Recommended Usage

### For CineMatrix Project

**Primary: Workflow 1 + Workflow 2 Combined**

```
main (stable releases)
  ↓
develop (integration branch)
  ↓
feature/* (your work)
```

This allows:
- ✅ Feature branches for focused work
- ✅ develop for integration testing
- ✅ main for stable releases
- ✅ PR reviews for quality control

### Step-by-Step Recommendation

1. **Work on feature branches** (current state)
   - `feature/enhanced-dossier` ← do work here
   - `feature/advanced-agents` ← do work here

2. **Merge to develop for testing**
   ```bash
   git checkout develop
   git merge feature/enhanced-dossier
   ```

3. **Test on develop** — Ensure no conflicts

4. **Create PR to main when stable**
   - PR: develop → main
   - Include both features in one release

5. **Tag release on main**
   ```bash
   git checkout main
   git tag v1.1.0
   git push origin main --tags
   ```

---

## GitHub Branch Protection Rules (Optional)

For **main** branch, consider enabling:
- ✅ Require pull request reviews before merging
- ✅ Dismiss stale pull request approvals
- ✅ Require branches to be up to date before merging
- ✅ Require status checks to pass before merging

For **develop** branch, consider:
- ✅ Allow direct merges from feature branches
- ✅ Auto-delete head branches on merge

---

## Creating Pull Requests

### From Command Line (Using GitHub CLI)

```bash
# Create PR from current feature branch to main
gh pr create --base main --title "Add enhanced dossier template" \
  --body "Adds psychological profiling and risk analysis to dossier"

# Create PR from feature to develop
gh pr create --base develop --title "Merge enhanced features"
```

### From GitHub Web Interface

1. Navigate to https://github.com/nodesthemovie-ai/cinematrix-swarm-engine
2. Click "Pull requests" tab
3. Click "New pull request"
4. Select: `base: main` ← `compare: feature/enhanced-dossier`
5. Add title and description
6. Click "Create pull request"

---

## Current State Summary

### Branches Status

```
🟢 main (8e495a2)
   └─ ✅ Stable — production ready
   
🟡 develop (61db4c6)
   └─ ✅ Has both features integrated
   
🔵 feature/enhanced-dossier (5508f46)
   └─ ✅ Ready for PR or merge to develop
   
🔵 feature/advanced-agents (985e3fb)
   └─ ✅ Ready for PR or merge to develop
```

### Files Added
- `CineMatrix/enhanced_dossier_template.md` (+63 lines)
- `CineMatrix/advanced_agents.md` (+145 lines)

### Next Steps

Choose your workflow:

**Option A: Formal PR Process**
```bash
# Create PR: feature/enhanced-dossier → main
gh pr create --base main --title "Add enhanced dossier v2"

# Create PR: feature/advanced-agents → main  
gh pr create --base main --title "Add advanced agent extensions"
```

**Option B: Merge via Develop**
```bash
# Already done! develop has both features
# Just test develop, then merge to main when ready
git checkout main && git merge develop
```

**Option C: Direct Merge (Simple)**
```bash
# Merge features directly to main
git checkout main
git merge feature/enhanced-dossier feature/advanced-agents
```

---

## References

- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [Git-Flow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Trunk-Based Development](https://trunkbaseddevelopment.com/)

## Support

For workflow questions or issues:
- Create a GitHub issue with `workflow` tag
- Reference this guide in your PR description
- Ask in pull request comments
