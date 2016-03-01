---
title: Authentication
---

<p>Some Snyk commands require authentication. We use GitHub for authentication, but <strong>do not require access to your repositories</strong>, only your email address. You can authenticate by clicking <a href="https://snyk.io/auth/github">“Sign Up”</a>, and pasting in the lines from your dashboard, which look roughly like this:</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">snyk auth &lt;your key&gt;</span></code></pre></div>

<p>Alternatively, you can simply run <code>snyk auth</code> in your terminal and it’ll guide you through this process. Or jump right into Snyk’s <a href="#wizard"><code>wizard</code></a>, that will also take you through authentication.</p>
