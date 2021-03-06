---
title: Supabase
taxonomy:
    category:
        - tool
    tag:
        - database
        - api
aura:
    pagetype: website
feed:
    limit: 10
metadata:
    'og:url': 'https://tempopedia.org/directory/supabase'
    'og:type': website
    'og:title': 'Supabase | Tempopedia'
    'og:image': 'https://tempopedia.org/directory/supabase/og-image.jpg'
    'og:image:type': image/jpeg
    'og:image:width': '1200'
    'og:image:height': '630'
    'og:author': Tempopedia
    'twitter:card': summary_large_image
    'twitter:title': 'Supabase | Tempopedia'
    'twitter:site': '@tempopediaorg'
    'twitter:creator': '@tempopediaorg'
    'twitter:image': 'https://tempopedia.org/directory/supabase/og-image.jpg'
    'article:published_time': '2021-02-22T17:17:23+00:00'
    'article:modified_time': '2021-02-22T17:17:23+00:00'
    'article:author': Tempopedia
media_order: og-image.jpg
published: false
---

The open source database alternative to Google Firebase

===

! Website: https://supabase.io
! Price: Free (self-hosted) or Freemium (cloud-hosted)
! License: Open Source

What it is.
-----------------------------------------------------------------------------

Supabase is an open source Firebase alternative. We are a service to:

-   listen to database changes
-   query your tables, including filtering, pagination, and deeply nested relationships (like GraphQL)
-   create, update, and delete rows
-   manage your users and their permissions
-   interact with your database using a simple UI

What it isn't.
----------------------------------------------------------------------------------

Supabase is not a 1-to-1 mapping of Firebase. While we are building many of the features that Firebase offers, we are not going about it the same way.

Our technological choices are quite different to Firebase. Everything we use is open source. Wherever possible we use and support existing tools in the ecosystem, rather than developing from scratch.

Most notably, we use Postgres rather than a NoSQL store. This was a deliberate choice. We believe that no other database on the market offers the scalability and functionality required to legitimately compete with Firebase.

How it works.
---------------------------------------------------------------------------------

At its core, Supabase is a suite of open source tools, stitched together to build a seamless developer experience:

![Supabase Architecture](https://supabase.io/assets/images/supabase-architecture-0a162cd9b23053a55074d7dda5b6c4ad.png)

-   [PostgreSQL](https://www.postgresql.org/) is an object-relational database system with over 30 years of active development that has earned it a strong reputation for reliability, feature robustness, and performance.
-   [Realtime](https://github.com/supabase/realtime) is an Elixir server that allows you to listen to PostgreSQL inserts, updates, and deletes using websockets. Supabase listens to Postgres' built-in replication functionality, converts the replication byte stream into JSON, then broadcasts the JSON over websockets.
-   [PostgREST](http://postgrest.org/) is a web server that turns your PostgreSQL database directly into a RESTful API
-   [postgres-meta](https://github.com/supabase/postgres-meta) is a RESTful API for managing your Postgres, allowing you to fetch tables, add roles, and run queries etc.
-   [GoTrue](https://github.com/netlify/gotrue) is an SWT based API for managing users and issuing SWT tokens.
-   [Kong](https://github.com/Kong/kong) is a cloud-native API gateway.