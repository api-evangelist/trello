---
title: "Porting a small Connect app to Forge end to end: 10 things that broke, and what it took"
url: "https://community.developer.atlassian.com/t/porting-a-small-connect-app-to-forge-end-to-end-10-things-that-broke-and-what-it-took/102871#post_1"
date: "2026-09-24"
author: "@HermogenesLpez Hermogenes López"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
With Connect end of support starting on 31 January 2027, I ported a small open-source Connect app to Forge from start to finish, to see what a real migration involves. The app is samid737/jira-checklist-plugin : one issue panel for checklists, running on Express, atlassian-connect-express , SQLite and jQuery UI. The code and full write-up are here: GitHub - hermogenes-lopez/checklist-forge: Forge port of the open-source Jira checklist Connect app, with a Connect-to-Forge migration write-up · GitHub Before and after Connect Forge Hosting Own Node/Express server None Auth JWT per request (ACE) H
