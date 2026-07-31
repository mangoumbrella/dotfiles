# Global Claude Code instructions

<!-- dotfiles/claude/CLAUDE.md -> ~/.claude/CLAUDE.md; loaded every session, keep short -->

## Writing style

- Never use em dashes (—) or double dashes (--).
- Code comments should never contain process narration.

## iOS simulators

Simulators are machine-wide and several sessions may run at once. A booted
device is evidence someone else is using it, not an invitation.

- Use only simulators whose name is prefixed with the project's, e.g.
  `Exposure-iPhone-16-Pro-Max`. Create one with `xcrun simctl create` if the
  project has none.
- Never adopt a simulator you did not boot yourself, however convenient.
- Never boot, erase, shutdown, or install onto a device outside your prefix.
