---
title: "Stale hasCredentials() results on external auth provider"
url: "https://community.developer.atlassian.com/t/stale-hascredentials-results-on-external-auth-provider/100409#post_2"
date: "2026-10-01"
author: "@linklefebvre Maxime Lefebvre [Okapya]"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Hi @PeterSkriba , I raised a similar issue yesterday, and Mihai_leanzero pointed out your post. Our app also uses Forge external auth and we experienced both your Case A and Case B. At the moment, my experience is that Case A only happens if it’s the second time my user authenticates an external auth (our app has multiple OAuth2 providers).
