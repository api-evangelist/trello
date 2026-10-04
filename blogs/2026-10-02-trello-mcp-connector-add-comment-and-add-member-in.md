---
title: "Trello MCP connector: add_comment and add_member in trelloWriteCard rejected with \"Invalid enum value\""
url: "https://community.developer.atlassian.com/t/trello-mcp-connector-add-comment-and-add-member-in-trellowritecard-rejected-with-invalid-enum-value/102839#post_2"
date: "2026-10-02"
author: "@LevelbrookConsulting Patrick Donahue"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
I can’t fix the connector side, but “Invalid enum value” is the wording a Zod schema check produces, so it looks like the tool description still lists those two actions while the validator on the server no longer accepts them. That’s something only Atlassian can change. If you need comments and assignments working in the meantime, the plain REST API still does both.
