---
id: w03-stewary2-skill-reload-needed
title: "Why did my installed skill need a full reload?"
author: "Sheetal Tewary (stewary2)"
---

For Homework 3 Question 1, I designed and saved a small explain-to-me skill under .claude/skills/explain-to-me/SKILL.md in my course repo, then asked my agent to invoke it. It reported "Unknown skill," even though the file existed and was well-formed. I checked the working directory and found the session was rooted one level above the repo, so I copied the same skill to the user-level skills directory instead, but that still failed until I fully reloaded the VS Code window, at which point the skill worked immediately.

This suggests skill discovery happens only once, at session start, rather than being rescanned per message or tool call. Is this a deliberate design choice, or an artifact of how the extension host caches available skills? And practically, is there a reliable way to force a skill reload mid-session without a full editor restart, especially when working from a subdirectory of the actual project root?
