---
title: "Equivalent for API v2 - addons"
url: "https://community.developer.atlassian.com/t/equivalent-for-api-v2-addons/102891#post_1"
date: "2026-09-25"
author: "@adam.labus Adam Labus [it.Lab] 🚀💙🤟 Extender 4️⃣ Jira / Confluence"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Hi everyone, Until now, API (v2) allowed for the retrieval of quite useful information about any app on the marketplace without requiring authentication , example: https://marketplace.atlassian.com/rest/2/addons/com.itlab.jira.plugins.extender/versions/latest?application=jira&hosting=datacenter Unfortunately, the new version (v3) does not offer this capability. Interestingly, when analyzing network traffic from Jira DC, it turns out that Jira DC still uses this API (v2) and relies on it to check for new versions within the UPM. Is there an equivalent endpoint that doesn’t require authenticatio
