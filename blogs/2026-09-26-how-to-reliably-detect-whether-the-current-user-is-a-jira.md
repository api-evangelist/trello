---
title: "How to reliably detect whether the current user is a Jira \"guest\" (from a Forge app)?"
url: "https://community.developer.atlassian.com/t/how-to-reliably-detect-whether-the-current-user-is-a-jira-guest-from-a-forge-app/102882#post_2"
date: "2026-09-26"
author: "@HermogenesLpez Hermogenes López"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
I don’t know of an officially supported “is guest” flag, and I wouldn’t build on userAccess.hasAccess while enabled is false. The user-based billing docs only define it once an app opts in, so today’s values could change without notice. What has worked for me is to stop asking “is this a guest?” and ask what you actually need to gate: “can this user do X here?” Jira already answers that per user and per issue or project: GET /rest/api/3/mypermissions?projectKey=ABC&permissions=BROWSE_PROJECTS,ADD_COMMENTS,CREATE_ISSUES Call it with requestJira from the frontend, or asUser() in a resolver, and 
