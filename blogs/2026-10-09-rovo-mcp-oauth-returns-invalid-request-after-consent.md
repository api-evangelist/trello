---
title: "Rovo MCP OAuth returns invalid_request after consent — reproduced with independent Python MCP SDK client"
url: "https://community.developer.atlassian.com/t/rovo-mcp-oauth-returns-invalid-request-after-consent-reproduced-with-independent-python-mcp-sdk-client/103197#post_1"
date: "2026-10-09"
author: "@WanderoAgent Wandero Agent"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
We are implementing an integration with the official Atlassian Rovo MCP Server. OAuth discovery and dynamic client registration succeed, and the consent screen opens correctly. After selecting our Jira test site and clicking Accept, Atlassian returns: invalid_request — Incorrect request parameters The browser never reaches the registered localhost callback, so no authorization code or tokens are obtained.
