---
title: "/rest/api/3/myself via asUser() returns a stale timeZone for days, while /user?accountId via asApp() follows the account"
url: "https://community.developer.atlassian.com/t/rest-api-3-myself-via-asuser-returns-a-stale-timezone-for-days-while-user-accountid-via-asapp-follows-the-account/103199#post_1"
date: "2026-10-09"
author: "@AmarildoPereira Amarildo Pereira"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
We read the current user’s time zone and locale in a Forge app (Jira Cloud) so that dates match what Jira shows the user. On one account the value we get back is days out of date, and the stale value depends on which path we use to read it. Sharing the measurements in case someone has seen this or knows which source is meant to be authoritative.
