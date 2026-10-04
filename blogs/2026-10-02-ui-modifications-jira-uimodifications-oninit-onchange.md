---
title: "UI Modifications (jira:uiModifications): onInit/onChange callbacks appear to not execute reliably on Global Issue Create — no console output, no invoke() reaching resolver, despite confirmed UI modification entity creation"
url: "https://community.developer.atlassian.com/t/ui-modifications-jira-uimodifications-oninit-onchange-callbacks-appear-to-not-execute-reliably-on-global-issue-create-no-console-output-no-invoke-reaching-resolver-despite-confirmed-ui-modification-entity-creation/102818#post_3"
date: "2026-10-02"
author: "@RolfEriksen Rolf Eriksen"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Adding to Mihai’s console tips: here are a few Global Issue Create specifics that can make it look like nothing runs. They come from building on UI modifications in the Create dialog. 1.
