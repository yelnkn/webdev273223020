# Agent log

One entry per agent session, newest at the bottom. Be honest: what went wrong is the useful part.

<!-- Copy this block for each session:

## YYYY-MM-DD · <short title>
- Goal:
- Delegated:
- Checkpoints:
- Went wrong:
- Changed by hand:

-->
## 2026-10-06 · MCP tool description experiment
- Goal: Connect Gemini CLI to my MCP server and test whether it could discover and use `find_lecture` without naming the tool.
- Delegated: Asked Gemini to answer what lecture 7 covers using the available MCP tools.
- Checkpoints: Gemini successfully connected to `my-project`, selected `find_lecture(number: 7)`, returned the lecture information, and `/stats` reported 24,089 input tokens and 88 output tokens.
- Went wrong: The first npm self-check initially failed because the `mcp` npm script had not been added yet. Running the server directly worked correctly.
- Changed by hand: Changed the `find_lecture` description to a vaguer description for the experiment, then created `package.json` and added the `mcp` script with `npm pkg set scripts.mcp="node mcp-server/server.js"`. The final npm self-check passed 12/12 checks.
