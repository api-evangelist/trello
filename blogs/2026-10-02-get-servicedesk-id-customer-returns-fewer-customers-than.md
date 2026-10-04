---
title: "GET /servicedesk/{id}/customer returns fewer customers than the JSM Customers page shows"
url: "https://community.developer.atlassian.com/t/get-servicedesk-id-customer-returns-fewer-customers-than-the-jsm-customers-page-shows/103066#post_1"
date: "2026-10-02"
author: "@PranayChhibber Pranay Chhibber"
feed_url: "https://community.developer.atlassian.com/posts.rss"
---
The Get customers API for our service desk returns far fewer customers than the Customers page in the JSM project. Endpoint used GET https://<>.atlassian.net/rest/servicedeskapi/servicedesk/36/customer?start=0&limit=50 What we see API response: size: [13] , isLastPage: true . There is no next page.
