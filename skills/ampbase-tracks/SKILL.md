---
name: ampbase-tracks
description: "Change the configurations of an Ampbase channel with the Ampbase API, through a track. Use when a task changes a configuration Ampbase manages: open a track for the task, save the change into it, soundcheck it on a few hosts and mark it ready for a rollout."
---

# Ampbase tracks

Use this skill to change the configurations an Ampbase channel serves its agents, through a track, with the Ampbase API.

Before your first call, fetch https://ampbase.io/docs/tracks-api.md and follow its working rules. It holds every call this work makes and the rules for making them, as this Ampbase serves them now. For anything else, https://ampbase.io/llms.txt lists every page of the Ampbase documentation as markdown.

Your API token is in the `AMPBASE_TOKEN` environment variable. Send it as `Authorization: Bearer $AMPBASE_TOKEN` on API calls only: the documentation pages need no token, so fetch them without it. Never print it, log it or write it to a file.
