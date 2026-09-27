# Global Claude Code instructions

<!-- dotfiles/claude/CLAUDE.md -> ~/.claude/CLAUDE.md; loaded every session, keep short -->

## Writing style

- Never use em dashes (—) or double dashes (--).
- Code comments should never contain process narration.

## iOS simulators

Simulators are machine-wide and other projects may be using them. The name
prefix is the ownership boundary, not who booted the device.

- Use only simulators whose name is prefixed with the project's, e.g.
  `Exposure-iPhone-16-Pro-Max`. Create one with `xcrun simctl create` if the
  project has none.
- Reuse a device inside your prefix even when it is already booted. Only one
  session per project runs at a time, so it is left from an earlier one.
- Never boot, erase, shutdown, or install onto a device outside your prefix.
- Verify UI changes in the simulator yourself instead of handing the user a
  test checklist. Drive it with `axe` (tap, swipe, type, screenshot), and use
  `axe describe-ui --udid <UDID>` to read element frames and values, which is
  more reliable than judging from screenshots.
- After a focus change, wait about 2s before `axe type` or the keystrokes can
  be dropped.
