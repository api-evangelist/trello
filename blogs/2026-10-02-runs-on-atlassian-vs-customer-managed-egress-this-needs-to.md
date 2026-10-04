---
title: "Runs on Atlassian vs Customer-managed egress: this needs to change"
url: "https://community.developer.atlassian.com/t/runs-on-atlassian-vs-customer-managed-egress-this-needs-to-change/102172#post_10"
date: "2026-10-02"
author: "@NicoAcosta Nico Acosta"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Steffen, this matches the tradeoff I hit while building a small Forge-native Confluence app aimed at Runs on Atlassian. ROA is a sharp product constraint, not just a badge. In practice it means: - Forge-hosted compute + residency-enabled Forge storage (or host entity/content properties) - no remotes, no Connect modules, no dynamic web triggers - no “fetch whatever the page already embeds” unless you declare egress (and that usually kills ROA) So for a slideshow / renderer of Confluence content that must show Tableau, YouTube, or other embeds already on the page, CME (or wildcard client fetch) 
