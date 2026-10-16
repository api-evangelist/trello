---
title: "Forge apps can hang on Jira's loading skeleton forever after a transient ERR_SOCKET_NOT_CONNECTED (ECO-1823)"
url: "https://community.developer.atlassian.com/t/forge-apps-can-hang-on-jiras-loading-skeleton-forever-after-a-transient-err-socket-not-connected-eco-1823/103028#post_2"
date: "2026-10-07"
author: "@VladymyrPostnov Vladymyr Postnov"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
The HAR signature you describe is the useful part here. We have a small local script that sorts HAR failures into network, Atlassian or app vendor and strips tokens before anything is shared, and right now a zero-status document entry lands in the network bucket, which is exactly the wrong place to send someone for this. Adding your four conditions together (zero status on .cdn.prod.atlassian-dev.net, empty serverIPAddress, no _connectionId, dns/connect/ssl all -1) makes it a separate case with its own label, so it stops reading as a proxy problem.
