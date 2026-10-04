---
title: "Forge Invocation Token `context` claim appearing in backend function calls"
url: "https://community.developer.atlassian.com/t/forge-invocation-token-context-claim-appearing-in-backend-function-calls/102843#post_2"
date: "2026-09-25"
author: "@ShannonJohnson Shannon Johnson"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
You’re right, and our documentation is wrong here. When a Forge backend function calls invokeRemote , the Forge Invocation Token includes a context claim that contains only cloudId . This covers trigger and lifecycle event handlers too.
