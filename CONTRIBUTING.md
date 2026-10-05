# Contributing

## Workflow

1. Start from the latest `develop` branch.
2. Create a focused branch, for example `feature/auth` or `feature/tours`.
3. Keep commits small and use the conventional prefixes below.
4. Open a pull request into `develop`.
5. Ask at least one teammate to review the pull request.
6. Merge only after the work is tested and reviewed.

Do not push directly to `main` or commit secrets, generated files, or editor settings.

## Commit prefixes

```text
feat: add tour cards
fix: correct booking validation
style: update responsive layout
docs: update project requirements
refactor: simplify storage helper
```

## Code conventions

- Use semantic HTML and labels for form controls.
- Use `kebab-case` for CSS classes.
- Use `const` and `let` in JavaScript.
- Keep shared styles in `css/style.css`.
- Keep responsive rules in `css/responsive.css`.
- Test changes at mobile, tablet, and desktop widths.
