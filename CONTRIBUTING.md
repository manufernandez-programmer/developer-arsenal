# Contributing to Developer Arsenal

Keep the project a useful manual. A shorter, correct entry is better than a larger
catalog of commands no one has checked.

## Shape an entry

- **Quick Mode:** command, concise purpose, and any important write/delete/publish effect.
- **Learning Mode:** a small example, expected result, explanation and practical limits.
- Label shell-specific syntax. Keep diagrams in `text` fences, executable examples
  in the appropriate language fence, and explanations outside the fences.
- Quote paths when they contain spaces; explain placeholders. Use fictitious data.
- Preserve the existing explicit anchors. Add map/topic links for new sections.
- Link to upstream documentation when a behavior is subtle or version-dependent.

## Review a change

1. Work on a branch and inspect the diff before staging selected files.
2. Check both modes for contradictory wording or stale examples.
3. Preview Markdown and follow changed file/section links. Check heading order,
   code fences and diagrams; a successful render alone does not establish correctness.
4. Test relevant examples in a disposable directory or temporary Git repository.
   Check failure paths too: no matches, existing outputs, bad syntax or rejected operations.
5. Do not execute deletion or overwrite examples on real data. Do not publish a
   remote branch, modify global configuration, save a function, or overwrite the
   clipboard just to test the wording. Use isolated configuration or document the limit.
6. Record the tools, versions and result in the PR. Explain what was not tested.
7. Review `git diff --cached` for private data before committing and opening the PR.

Do not commit tokens, passwords, private keys, real client data or private logs.
`.gitignore` is a convenience, not a secret scanner or a way to erase history.
If a credential has been exposed, revoke/rotate it before discussing cleanup.

The repository has no build system or required CI pipeline. Use focused checks
that help maintain the documentation; do not add tooling solely for appearances.

Keep humor where it makes learning friendlier. Do not turn it into a substitute
for a precise explanation or imply experience, users or results not established
by the project.
