---
title: Using Snyk
draft: false
---

<h3 class="h4">Why should I add Snyk `test` to my Continuous Integration (CI)?</h3> 

<p>Integrating Snyk will prevent code changes from introducing new vulnerable packages. <a href="https://snyk.io/docs/using-snyk/#integrating-snyk-into-your-dev-workflow">Find out how to integrate Snyk into your workflow.</a></p> 

<h3 class="h4">How can I test a Github repository from the command-line interface tool (CLI)?</h3> 

<p>Currently, we support testing public Github repositories only. 
To test a public Github repository, just run snyk test and include the Github URL to the repo.</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">snyk test https://github.com/snyk/snyk</span></code></pre></div>

<p>The following git URL formats are supported:</p>
<ul>
	<li>git://github.com/user/project.git#commit-ish</li>
	<li>https://github.com/user/project#commit-ish</li>
	<li>user/project#commit-ish</li>
</ul>
<p>This also works for Bitbucket and GitLab.<p>
<p>You can also test a public npm package or Github project via the <a href="https://snyk.io/test/">Test page on snyk.io.</a></p>

<h3 class="h4">How can I delete my data?</h3> 

<p>You can delete a project on the project page on the Snyk website. This will delete the project, and all snapshots that are related to it, and you won’t be able to access it. Please note that the data remains in our database, so if you would like to restore it, let us know. If you would like us to delete your project data permanently from the database, <a href="mailto:support@snyk.io">email us</a> and we’ll sort it out.</p> 

<h3 class="h4">How can I delete my account?</h3> 

<p>Until we support deleting your account via the Snyk website, this is a manual process. <a href="mailto:support@snyk.io">Email us</a>, and we will remove your account and all your data from our database.</p>

<h3 class="h4">What analytics do you track? How can I opt out?</h3>

<p>We are using a range of web analytics tools to understand and analyse user behaviour on snyk.io. If you’d like to block tracking, use one of the many browser tools available.</p> 

<p>Our CLI tool reports an event for each command to our analytics, including the version of the CLI tool, the User ID, and the package name. This allows us to better understand how the CLI client is used, and informs our product development decisions.</p>
<p>If you would like to opt out, you can do so by running the following command:</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">snyk config set disable-analytics=1</span></code></pre></div>

<p>To remove the flag, run:</p>
<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">snyk config unset disable-analytics</span></code></pre></div>

<p>If you have any questions or problems, please <a href="mailto:support@snyk.io">email us</a>.</p>


