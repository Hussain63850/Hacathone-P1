# Quickstart: Module 4 - Vision-Language-Action (VLA)

**Feature**: 004-vision-language-action
**Date**: 2025-12-30

## Developer Setup

This module adds content to an existing Docusaurus site. No additional dependencies are required.

### Prerequisites

1. **Node.js 18+** installed
2. **Existing Docusaurus site** in `frontend/` directory
3. **Modules 1, 2, and 3** already present in `frontend/docs/`

### Verify Existing Setup

```bash
# Navigate to frontend directory
cd frontend

# Verify dependencies are installed
npm install

# Test existing site builds
npm run build

# Start development server (optional)
npm run start
```

## Content Development Workflow

### Step 1: Create Module Structure

```bash
# Create module-4 directory
mkdir -p frontend/docs/module-4
```

### Step 2: Add Category Configuration

Create `frontend/docs/module-4/_category_.json`:

```json
{
  "label": "Module 4: Vision-Language-Action",
  "position": 4,
  "link": {
    "type": "generated-index",
    "description": "Learn how VLA models, voice interfaces, and cognitive planning enable intelligent humanoid robots."
  }
}
```

### Step 3: Create Chapter Files

Create the following files in `frontend/docs/module-4/`:

| File | Purpose |
|------|---------|
| `index.md` | Module overview and navigation |
| `chapter-1-vla-models.md` | Multimodal Foundation Models content |
| `chapter-2-voice-interfaces.md` | Voice and Language Interfaces content |
| `chapter-3-cognitive-planning.md` | Cognitive Architectures content |

### Step 4: Validate Build

```bash
# Build the site
npm run build

# Check for errors in output
# Expected: "Build completed successfully"
```

### Step 5: Preview Locally

```bash
# Start development server
npm run start

# Open browser to http://localhost:3000
# Navigate to Module 4 in sidebar
```

## Content Guidelines

### Front Matter Template

```yaml
---
title: "Chapter Title"
sidebar_label: "N. Short Label"
sidebar_position: N
description: "Brief description for SEO and preview"
---
```

### Admonition Syntax

```markdown
:::note Title (optional)
Content for notes and clarifications
:::

:::tip Title (optional)
Best practices and recommendations
:::

:::warning Title (optional)
Common pitfalls and limitations
:::
```

### Code Snippet Format

Always include language identifier:

```markdown
```python
# Python code here (conceptual/illustrative)
```

```yaml
# YAML configuration here
```

```text
# Plain text diagrams here
```
```

## Validation Checklist

Before committing content:

- [ ] All files have correct front matter
- [ ] `npm run build` completes without errors
- [ ] Sidebar shows Modules 1, 2, 3, and 4 in order
- [ ] All internal links work
- [ ] No H4 or deeper headings used
- [ ] Each chapter has at least 2 admonitions
- [ ] All code snippets have language identifiers
- [ ] No setup/installation instructions in content
- [ ] No API keys or service configurations
- [ ] No model training code

## Common Issues

### Issue: Module not appearing in sidebar

**Solution**: Check `_category_.json` position value and ensure it's unique (should be 4).

### Issue: Build fails with markdown errors

**Solution**: Verify front matter YAML is valid (no tabs, proper quoting).

### Issue: Links between chapters broken

**Solution**: Use relative links like `./chapter-1-vla-models` without `.md` extension.

### Issue: Admonitions not rendering

**Solution**: Ensure `:::note`, `:::tip`, `:::warning` syntax has no spaces before colons.

## File Reference

```text
frontend/docs/module-4/
├── _category_.json               # position: 4
├── index.md                      # sidebar_position: 0
├── chapter-1-vla-models.md       # sidebar_position: 1
├── chapter-2-voice-interfaces.md # sidebar_position: 2
└── chapter-3-cognitive-planning.md # sidebar_position: 3
```

## Next Steps

After content is complete:

1. Run full build validation: `npm run build`
2. Preview with `npm run serve`
3. Review against spec.md success criteria
4. Commit changes with `/sp.git.commit_pr`
