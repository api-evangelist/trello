---
title: "Forge Event Hooks should be signed"
url: "https://community.developer.atlassian.com/t/forge-event-hooks-should-be-signed/102770#post_2"
date: "2026-09-18"
author: "@AaronMorris1 Aaron Morris"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
I generally agree with this, but I’d like to pose two questions: scottjackson: If someone was able to forge a FIT somehow and hit an application endpoint with a malicious body, there’s no way on the application side to reject the forged body. FITs are cryptographically signed by Atlassian. So isn’t a stolen or leaked FIT a more likely threat than a forged FIT?
