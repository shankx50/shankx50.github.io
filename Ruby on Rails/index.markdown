---
layout: page
title: Ruby On Rails
date:   2015-07-12
permalink: /rails/
---
<p>Last update: {{ page.date | date: "%b %-d, %Y" }}</p>

<p>This is just a list of random notes about rails. It will probably evolve frequently.</p>
---

##Application Secrets

In Rails 4.1 the secrets.yml in the config folder stores the application's sensitive data., such as access keys and passwords required to use external APIs. Of course, **don't store in version control**.

##Database

- **Do not store config/database.yml in version control**. Rails 4.1 provides the ability to configure Active Record with an environment variable DATABASE_URL.

##Miscellanea

- The layout can be ignored by putting **layout false** into the controller.
- Any instance variables we define in a method of a controller become available for use in the views.

##Hosting

- [Heroku](http://www.heroku.com) seems to be the easiest solution that allows me to focus more on development, and less on setting up a server.
