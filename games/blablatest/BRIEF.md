# blablatest

blablatest

---

## The JumPHP playground

This project was made on the JumPHP playground: the game's page is https://jumphp.net/blablatest
(category: Plates-formes).

- The game is `games/blablatest/`. Read `AGENTS.md` (the JumPHP contract) first; replace the skeleton with the game
  described above; follow the definition of done (tests, screenshots you look at, browser build).
- **Develop with game tests, visually**: for each mechanic, as you write it, a test in `games/blablatest/tests/` that
  extends `JumPHP\Testing\GameTestCase` and plays it ("the player jumps onto the platform", "the enemy dies
  when hit"; AGENTS.md "Game tests"); `bin/jumphp test blablatest` after each change. The user watches them play live
  in Claude Code (the `jumphp-live` pane) and, after a push, replays each test filmed in the studio (MCP
  `run_tests`).
- **Publishing**: every push to `main` is online within a minute (GitHub webhook). The MCP tool
  `sync_project` (server `jumphp`) publishes at once and returns the errors: a commit with a PHP syntax error
  is not published (the previous version stays online).
- The playground loads the game file by file with its shared engine: Composer packages other than
  `jumphp/engine` are not available there.
- **The game's home page**: make `games/blablatest/site/` (AGENTS.md section 13: themed with the game's own graphics,
  SEO, a link to `play/`); it is the game's page on the playground. Also `games/blablatest/assets/thumbnail.png`.
- When the game is done: MCP `update_project` with `listed: true` shows it in the playground's directory.