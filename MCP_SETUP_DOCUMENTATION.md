

# MCP Setup Documentation

## What You Did

* Configured VS Code with **GitHub Copilot** and **Copilot Chat** extensions.
* Added MCP server in `.vscode/mcp.json`:

  * Server name: **tenxfeedbackanalytics**
  * URL: `https://mcppulse.10academy.org/proxy`
  * Headers: `X-Device: windows`, `X-Coding-Tool: vscode`
* Created **rules file** `.github/copilot-instructions.md` with instructions for AI agent behavior, error handling, and MCP logging.
* Tested prompts in Copilot Chat, including Python data-processing tasks, to verify server logging and agent adherence to rules.

## What Worked

* MCP server added successfully and shows status **"Running"** in VS Code.
* After GitHub authentication, server logging became active.
* Reloading VS Code keeps MCP server active and tools visible.
* Copilot Chat generated Python and small code snippets correctly according to rules.

## What Didn't Work

* Initial **"Add Server"** click did not respond until GitHub authentication was completed.
* Python code generation sometimes stuck on **"Activating MCP extensions"**; retrying the prompt after a short wait resolved it.
* Some prompts produced long responses; shortening instructions helped the agent produce concise outputs.

## Insights Gained

* MCP server **captures interactions automatically**, including prompts, responses, and summaries, which is key for evaluation.
* **Rules file** significantly influences agent behavior: clarifying ambiguities, incremental code generation, and structured logging.
* Proper **headers and authentication** are critical; missing or incorrect values prevent logging.
* Testing multiple prompts and AI behaviors helps refine the rules and ensures effective AI-agent collaboration.

## Research & Exploration

* Studied **Boris Cherny’s workflow** for Claude Code and GitHub Copilot best practices.
* Explored **different prompts** and agent modes (Agent, Auto) to observe AI behavior.
* Verified MCP logging by checking **tool options** in Copilot Chat (`tenxfeedbackanalytics`), `list_manager_servers`, and logging triggers (`log_passage_time_trigger`, `log_performance_outlier_trigger`).
* Tested **rules adaptations** for Python code generation, data-processing tasks, and concise responses.

## Effort & Engagement Artifacts

* Multiple commits for **rules file iterations** and MCP setup testing:

  * Initial MCP server setup.
  * Rules file creation and shortening for concise outputs.
  * Documented troubleshooting and retries for stuck prompts.
* Screenshots/logs of Copilot Chat showing **MCP server tools**, active logging, and agent responses.
* Explored multiple **AI agent behaviors** and adjusted rules to guide code generation effectively.


