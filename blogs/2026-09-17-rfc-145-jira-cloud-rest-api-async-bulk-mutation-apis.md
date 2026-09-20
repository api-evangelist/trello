---
title: "RFC-145: Jira Cloud REST API: Async Bulk Mutation APIs"
url: "https://community.developer.atlassian.com/t/rfc-145-jira-cloud-rest-api-async-bulk-mutation-apis/102577#post_12"
date: "2026-09-17"
author: "@PaulinaKumicka Paulina Kuźmicka"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
Thanks for the proposal — bulk entity property writes are the core of our Data Center to Cloud migration, so this lands right on our hot path. That write is where most of a migration’s time goes, across many work items, so anything that lets it run wider matters to us. Concurrency is the part I’d most like to understand, because today there effectively isn’t any: on the current endpoint ( POST /rest/api/2/issue/properties/multi ) a bulk property write is refused while another one is still running, even when the two calls cover different work items and different property keys.
