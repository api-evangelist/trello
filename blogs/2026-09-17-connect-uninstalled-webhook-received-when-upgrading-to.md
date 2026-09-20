---
title: "Connect uninstalled webhook received when upgrading to Forge version (same app key) - Is this Expected?"
url: "https://community.developer.atlassian.com/t/connect-uninstalled-webhook-received-when-upgrading-to-forge-version-same-app-key-is-this-expected/102742#post_1"
date: "2026-09-17"
author: "@JPires J. Pires"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
We maintain a Connect app that we migrated to Forge module by module. Until today we had two types of installations: Connect-on-Forge version (new installations and upgrades from Connect) Legacy Connect version (customers that never upgraded to our Connect-on-Forge version); Our latest major version removed the last Connect artefacts from the manifest (lifecycle, scopes, etc). We kept app.connect.key , as the docs require.
