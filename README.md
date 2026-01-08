# github.io

Itori website - Academic planning for neurodivergent minds.

## Pre-commit Checks

This repository includes a pre-commit hook that automatically validates HTML and CSS files before each commit to prevent broken code from being committed.

### What it checks:

**HTML Files:**
- ✓ Valid HTML structure (DOCTYPE, html, head, body tags)
- ✓ Closing tags match opening tags
- ✓ Required meta tags (charset, viewport)
- ✓ Title tag present
- ✓ Referenced CSS files exist
- ⚠ Warnings for mismatched divs and sections

**CSS Files:**
- ✓ Matching braces

### How it works:

The pre-commit hook is automatically installed at `.git/hooks/pre-commit` and runs on every commit. If critical errors are found, the commit will be blocked until they're fixed. Warnings will be shown but won't block the commit.

### Testing the hook:

```bash
# Test with current staged files
bash .git/hooks/pre-commit
```

### Reinstalling the hook:

If the hook gets removed or needs to be reinstalled:

```bash
chmod +x .git/hooks/pre-commit
```
