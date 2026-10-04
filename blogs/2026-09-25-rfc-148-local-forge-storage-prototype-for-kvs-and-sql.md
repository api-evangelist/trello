---
title: "RFC-148: Local Forge Storage prototype for KVS and SQL"
url: "https://community.developer.atlassian.com/t/rfc-148-local-forge-storage-prototype-for-kvs-and-sql/102858#post_5"
date: "2026-09-25"
author: "@PaoloCampanelli Paolo Campanelli (Appfire)"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
I’m not saying you shouldn’t do it, but I don’t think we would use it. Our apps run in Forge and in Jira/Confluence: if we want to test them in isolation, the best we can do is write unit tests and hope our mocks are correct. If we want to test them within the host platform, we don’t want to mock anything: running in a tunnel is a necessary evil to get a decent hot-reloading time even if it means that we aren’t exactly mirroring the production setup.
