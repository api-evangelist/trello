---
title: "How can I pull results from a CQL query into a custom email automation?"
url: "https://community.developer.atlassian.com/t/how-can-i-pull-results-from-a-cql-query-into-a-custom-email-automation/103045#post_1"
date: "2026-10-01"
author: "@SadajaRiddickJohnson Sadaja Riddick-Johnson"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
I am attempting to setup an automation that involves using a CQL query to find all pages in one of my organizations’ spaces that have not been updated in over a year, and then send an email with all of these found pages. I want this email to be sent to me once a month, so I have the initial trigger as Scheduled. I then created an IF or ELSE condition with the CQL query type = page AND lastModified .
