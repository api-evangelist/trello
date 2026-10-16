---
title: "\"Incoming webhook\" type automation triggers changed their base URL and have a new undocumented \"Secret\" parameter (randomly?!)"
url: "https://community.developer.atlassian.com/t/incoming-webhook-type-automation-triggers-changed-their-base-url-and-have-a-new-undocumented-secret-parameter-randomly/88104?page=2#post_31"
date: "2026-10-08"
author: "@IL1 IL"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
I’ve posted some thoughts about what 200/202 really does in a recent comment – just to go on a bit, I think by credential stuffing Diego is talking about a case like, a bot swarm attacks a user portal and each malicious attempt triggers a webhook alarm to a jira endpoint. The security risk here for Jira is in serving this huge concurrent swarm of requests. If they were to do credential checking and rate limiting at the edge they would be quickly overwhelmed.
