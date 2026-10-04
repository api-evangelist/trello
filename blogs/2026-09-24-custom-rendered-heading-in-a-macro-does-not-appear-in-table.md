---
title: "Custom Rendered Heading in a macro does not appear in Table Of Contents"
url: "https://community.developer.atlassian.com/t/custom-rendered-heading-in-a-macro-does-not-appear-in-table-of-contents/102838#post_2"
date: "2026-09-24"
author: "@Mihai_leanzero Mihai Perdum"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Hi @RayHaddad , No supported way for a Forge macro today. The ToC only reads headings stored in the page body, and your Heading is rendered inside the macro’s iframe so it never gets into the page ADF. Same mechanism on CONFCLOUD-72469 , where support confirmed in January that the Questions list macro’s headings don’t show up either.
