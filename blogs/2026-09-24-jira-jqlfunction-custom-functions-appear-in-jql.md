---
title: "jira:jqlFunction custom functions appear in JQL autocomplete but fail with \"Unknown function\" at query execution — for every function, on every environment reset"
url: "https://community.developer.atlassian.com/t/jira-jqlfunction-custom-functions-appear-in-jql-autocomplete-but-fail-with-unknown-function-at-query-execution-for-every-function-on-every-environment-reset/102820#post_2"
date: "2026-09-24"
author: "@Mihai_leanzero Mihai Perdum"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Hi @celestecs.supp , The dot is fine. Tested today on a dev site with a dotted and a plain function side by side, both autocomplete, both return issues quoted or unquoted and both get a precomputation stored. What did break mine was a bad fragment.
