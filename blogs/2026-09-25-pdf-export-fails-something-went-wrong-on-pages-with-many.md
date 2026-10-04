---
title: "PDF export fails (\"Something went wrong\") on pages with many Forge macros whose adfExport returns null for PDF"
url: "https://community.developer.atlassian.com/t/pdf-export-fails-something-went-wrong-on-pages-with-many-forge-macros-whose-adfexport-returns-null-for-pdf/102886#post_3"
date: "2026-09-25"
author: "@RolfEriksen Rolf Eriksen"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Hi, thanks for trying to reproduce it. Yes, it still fails for us today (25 Sep, 11:30 - 12:00~ GMT+2 ). Same site, same Custom UI macro (emitsReadyEvent on, adfExport returning null for pdf), pages with N copies of one small Mermaid sequence diagram: 1 macro: PDF ready in 31 s 8 macros: ready in 73 s 12 macros: “Something went wrong - An unexpected error occurred” after 245 s 18 macros: same error after 242 s Region: data residency isn’t pinned for this site, so Atlassian chooses where it’s hosted and we can’t see which AWS region it’s in.
