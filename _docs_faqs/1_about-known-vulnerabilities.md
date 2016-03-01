---
title: About known vulnerabilities
draft: true
---

<p>Snyk is installed via npm. Run these commands to install it for local use:</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">npm install -g snyk</span></code></pre></div>

<p>Once installed, you can perform a quick test on a public package, for instance:</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">snyk test ionic@1.6.5</span></code></pre></div>

<p>As you can see, Snyk found and reported several vulnerabilities in the package. For each issue found, Snyk provides the severity of the issue, a link to a detailed description, the path through which the vulnerable module got into your system, and guidance on how to fix the problem.</p>

<div class="screenshot">
<h3 class="screenshot__label">Example output</h3>
<pre class="code">$ snyk test
<span class="syn--red">✗ Vulnerability found on gm@1.13.3</span>
Info: https://snyk.io/vuln/npm:gm:20151026
From: snyk-demo-app@latest &gt; gm@1.13.3
<span class="syn--white syn--bold">Upgrade direct dependency gm@1.13.3 to gm@1.21.1</span>

<span class="syn--red">✗ Vulnerability found on qs@0.6.6</span>
Info: https://snyk.io/vuln/npm:qs:20140806
From: snyk-demo-app@latest &gt; webdriverio@2.4.5 &gt; request@2.34.0 &gt; qs@0.6.6
<span class="syn--white syn--bold">Upgrade direct dependency webdriverio@2.4.5 to webdriverio@3.0.1 (triggers upgrades to request@2.40.0 &gt; qs@1.0.0)</span>

<span class="syn--red">✗ Vulnerability found on qs@0.4.2</span>
Info: https://snyk.io/vuln/npm:qs:20140806-1
From: snyk-demo-app@latest &gt; cucumber@0.3.0 &gt; connect@2.3.2 &gt; qs@0.4.2
No direct dependency upgrade can address this issue.
<span class="syn--white syn--bold">Run `snyk wizard` to explore remediation options</span></pre>
</div>

<p>In the next sections we’ll explain how to run the same test on your own projects.</p>
