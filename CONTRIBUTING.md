# Contributing Guide

Thank you for contributing! This document defines the workflow, standards, and expectations for working in this repository.

---

## 1. Branching Strategy

We follow a structured branching model to maintain code quality and stability.

### Main Branches

* `main` → Production-ready code only
* `develop` → Integration branch for ongoing development

### Supporting Branches

Create all work from `develop`:

* `feature/*` → New features
* `bugfix/*` → Non-critical fixes
* `hotfix/*` → Critical production fixes (branched from `main`)

### Naming Convention

Use clear, descriptive, and kebab-case names:

```
feature/auth-login
feature/navbar-ui
bugfix/form-validation-error
hotfix/build-crash
```

Avoid:

* vague names (`feature/update`)
* personal names (`feature/abdullah-work`)

---

## 2. Development Workflow

### Step-by-step

1. Sync latest changes:

```
git checkout develop
git pull origin develop
```

2. Create a branch:

```
git checkout -b feature/your-feature-name
```

3. Make changes and commit:

```
git add .
git commit -m "feat: add login form UI"
```

4. Push branch:

```
git push origin feature/your-feature-name
```

5. Open Pull Request → target: `develop`

---

## 3. Pull Request (PR) Rules

### Requirements

* PR must target `develop` (not `main`)
* Minimum approvals:

  * `develop` → 2 reviewers
  * `main` → 3 reviewers
* No direct pushes allowed

### PR Checklist

Before opening a PR, ensure:

* Code builds successfully with Parcel
* No console errors
* Code is formatted properly
* No unused files or dependencies
* Feature is scoped and focused (small PRs preferred)

### PR Title Format

Use conventional format:

```
feat: add responsive navbar
fix: resolve image loading issue
refactor: clean up build config
```

### PR Description Must Include

* What was changed
* Why it was changed
* Screenshots (for UI changes)
* Testing steps

---

## 4. Code Standards

### General Principles

* Keep code simple and readable
* Avoid duplication (DRY)
* Use meaningful naming
* Write modular and reusable code

---

### HTML Guidelines

* Use semantic tags (`header`, `main`, `section`, `footer`)
* Avoid unnecessary div nesting
* Maintain proper indentation (2 spaces)
* Keep accessibility in mind (alt tags, labels)

---

### CSS Guidelines

* Prefer modular structure (component-based styles)
* Avoid inline styles
* Use consistent naming (BEM or similar)

Example:

```
.navbar {}
.navbar__item {}
.navbar__item--active {}
```

---

### JavaScript Guidelines

* Use modern ES6+ syntax
* Avoid global variables
* Prefer `const` and `let` over `var`
* Keep functions small and focused

Example:

```
const fetchData = async () => {
  try {
    const res = await fetch('/api');
    return await res.json();
  } catch (err) {
    console.error(err);
  }
};
```

---

## 5. Commit Message Convention

Follow **Conventional Commits**:

```
feat: add new feature
fix: bug fix
refactor: code improvement without feature change
chore: maintenance tasks
docs: documentation updates
```

Examples:

```
feat: implement login form
fix: correct button alignment
refactor: optimize asset loading
```

---

## 6. Project Setup

### Install dependencies

```
npm install
```

### Run development server

```
npm run dev
```

### Build project

```
npm run build
```

---

## 7. Code Review Expectations

Reviewers will check:

* Code quality and readability
* Proper structure and naming
* No unnecessary complexity
* UI/UX consistency
* Build success

PRs may be rejected if:

* Standards are not followed
* Code is messy or unclear
* Feature scope is too large

---

## 8. Important Rules

* Never push directly to `main` or `develop`
* Always create a branch
* Always use Pull Requests
* Keep PRs small and focused
* Write clean, maintainable code

---

## 9. Future Improvements (Optional)

* Add linting (ESLint, Prettier)
* Add CI pipeline (GitHub Actions)
* Add testing setup

---

Following these guidelines ensures a clean, scalable, and professional codebase.
