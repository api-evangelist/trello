---
title: "Breaking behavior with Anonymous users and Atlassian Spring Connect"
url: "https://community.developer.atlassian.com/t/breaking-behavior-with-anonymous-users-and-atlassian-spring-connect/103152#post_3"
date: "2026-10-07"
author: "@RomanStoffel Roman Stoffel"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Correct: The Force Invocation Tokens FIT principal is set to unidentified for anonymous users. This is then taken 1:1 by the Atlassian Spring Connect implementation and breaks the previous behavior where was no getUserAccountId for anonymous user. Just to clarify: We’ll just fix in our application.
