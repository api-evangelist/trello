---
title: "How to customize table content conditionally"
url: "https://community.developer.atlassian.com/t/how-to-customize-table-content-conditionally/35911#post_2"
date: "2026-10-08"
author: "@celestecs.supp CelesteCS"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Hi, I’m with CelesteCS - our Conditions for Confluence app (Cloud and Data Center) does this out of the box. Wrap the table in a Conditional Rules Manager and add one Conditional Rule per color: “Element text is one of” Done; Completed → background green “Element text is one of” In progress; Running → background yellow “Element text is one of” Started; Blocked → background red Set Applies to [Status] (the column header) and Affected elements Whole row if you want the whole row colored. There is also a ready-made “RAG status” preset, and if the column contains Confluence Status macros, “Element
