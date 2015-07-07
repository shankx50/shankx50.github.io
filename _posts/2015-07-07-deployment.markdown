---
layout: post
title:  "Deployment Best Practices"
date:   2015-07-07
categories: devops
permalink: /deployment
---
{% include stupid.html %}

###In a nutshell:

<ul class="showcase">
	<li>Use your repository’s default working branch as your “development” branch.
	</li>
	<li>Create a branch for each environment, including staging and production.
	</li>
	<li>Never merge into an environment branch unless you are ready to deploy to that environment.
	</li>
	<li>Perform a diff between branches before merging—this can help prevent merging something that wasn't intended, and can also help with writing release notes.
	</li>
	<li>Merges should only flow in one direction: first from feature to staging for testing; then from feature to stable once tested; then from stable to production to ship/
	</li>
</ul>


Some developers (and even development firms) omit to define a deployment process around their development activities. This can quickly turn against you. Chaos is guaranteed because nobody really knows which version of the codebase is current. Hence the paramount importance for a well defined deployment process.

Beanstalk published a <a href="http://guides.beanstalkapp.com/deployments/best-practices.html" target="_blank">really good article about the topic</a> which is summarized here.

{% include deploymentsvg.html %}

In order for this to make sense, you need a basic understanding of <a href="https://git-scm.com/" target="_blank">git</a> (version control system) and its use in conjunction with an online project hosting provider such as <a href="https://github.com/" target="_blank">GitHub</a>, <a href="https://bitbucket.org" target="_blank">Bitbucket</a>, or <a href="http://beanstalkapp.com/" target="_blank">beanstalk</a>. I like Bitbucket because they offer free private repositories for up to 5 users. If you are new to git and online project hosting, give yourself enough time to understand those concepts. They are not necessarily straight-forward for beginners. However, this is a required skill if you are serious about software development.

Each branch is linked to a specific server. Setting up these servers and their automated integration with respective repositories is a challenge that I am still overcoming myself. I will document my findings here, of course.

For instance, I set up a local development environment on my computer using <a href="https://www.vagrantup.com/" target="_blank">Vagrant</a> that mimics the production server. This approach minimizes deployment issues to production.<br/>
I use <a href="https://heroku.com" target="_blank">Heroku</a> to act as my staging server. Heroku is the simplest way of deploying a rails application I have found so far. Pushing your code to Heroku using a simple git command is all it takes. If you want you can quickly turn Heroku into your production server. Just pay for some additional resources and you're good to go.<br/>
If you are looking for more control over your production server you are likely to use a VPS (virtual private server in the cloud) or maybe even a dedicated server. I am still learning VPS use and will keep you posted here as I find out more.

{% include disqus.html %}
