---
name: all-skills-orchestrator
display-name: All Skills Orchestrator
description: Coordinate all installed skills for a user task by discovering
  available skills, inspecting their instructions, and applying every applicable
  skill.
user-invocable: true
disable-model-invocation: false
---

# All Skills Orchestrator

For each task:

1. Discover all installed skills available to the current session.
2. Build an inventory of their names and descriptions.
3. Identify the skills applicable to the user's task.
4. Read the complete SKILL.md for every applicable skill before execution.
5. Follow the applicable skills' instructions and dependencies.
6. Combine the outputs and resolve conflicts.
7. Report which skills were used, skipped, or unavailable.

Do not claim to have executed a skill unless its instructions were actually applied.

Do not execute unrelated skills merely to increase the skill count. Do not perform destructive operations, deploy services, publish content, or expose secrets without appropriate authorization.

If the available skill inventory is incomplete, report that limitation.

Always prioritize the user's actual task and return one consolidated result.
