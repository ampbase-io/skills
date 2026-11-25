# Ampbase skills

Agent Skills for working with [Ampbase](https://ampbase.io) from a coding agent such as Claude Code, Codex CLI or Cursor.

## ampbase-tracks

Changes the configurations an Ampbase channel serves its agents, through a track. The agent opens a track for the task, saves the change into it, soundchecks it on a host of each build, and marks it ready for a rollout. The skill itself is a few lines: it sends the agent to [Tracks through the API](https://ampbase.io/docs/tracks-api), so the agent always works from the current calls and rules.

## Install

From the root of your repository:

```bash
npx skills add ampbase-io/skills --skill ampbase-tracks
```

The installer asks which agents to install for. To choose them up front, add `-a` once per agent, for example `-a claude-code -a codex`. Commit the installed files so everyone working in the repository gets the skill.

To install by hand, copy `skills/ampbase-tracks/` into `.agents/skills/`, which Codex, Cursor and most other agents read. For Claude Code, copy it into `.claude/skills/` instead.

## Give the agent a token

The agent needs an Ampbase API token at the Editor role in the `AMPBASE_TOKEN` environment variable. [API tokens](https://ampbase.io/docs/api-tokens) shows how to mint one. With it the agent can read the channel, save into tracks, soundcheck them and mark them ready.

An Editor token cannot ship a track. Shipping it takes an Admin, so a track the agent marks ready waits for the next rollout.
