---
title: "Migrating Legacy Data Center User Macros to Confluence Cloud via Forge: Feasibility & Workaround Check"
url: "https://community.developer.atlassian.com/t/migrating-legacy-data-center-user-macros-to-confluence-cloud-via-forge-feasibility-workaround-check/102119#post_7"
date: "2026-10-02"
author: "@ChayutJarriyarponrun Chayut Jarriyarponrung"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Hi @GodlaKesavaPrasad , I’m working on this exact problem from the tooling side. I’ve built a small Forge app that scans a Cloud site after migration and lists every macro that fails to render, with how many pages use each. After your test migration, it could show which of these macros are used most, to help you decide which ones are worth rebuilding first.
