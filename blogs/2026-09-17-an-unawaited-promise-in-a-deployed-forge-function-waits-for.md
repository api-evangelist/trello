---
title: "An unawaited promise in a deployed Forge function waits for the next thaw, fires milliseconds before the next handler, and its log is lost"
url: "https://community.developer.atlassian.com/t/an-unawaited-promise-in-a-deployed-forge-function-waits-for-the-next-thaw-fires-milliseconds-before-the-next-handler-and-its-log-is-lost/102728#post_1"
date: "2026-09-17"
author: "@Mihai_leanzero Mihai Perdum"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
A deployed Forge function does not wait for a promise it left unawaited. If another invocation lands on the same warm container, the pending callback runs. Where its log goes depends on when it came due.
