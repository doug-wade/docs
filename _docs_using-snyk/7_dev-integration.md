---
title: Integrating Snyk into your dev workflow
---

<p>To continuously avoid known vulnerabilities in your dependencies, integrate Snyk into your continuous integration (a.k.a. build) system. Here are the steps required to to so:</p>

<ol>
  <li>Add <code>snyk</code> to your project’s dependencies (<code>npm install -S snyk</code>), and commit the modified <code>package.json</code> file.</li>
  <li>Ensure the <code>.snyk</code> file you generated was added to your source control (<code>git add .snyk</code>).</li>
  <li>After the <code>npm install</code> steps in your CI, run <a href="#protect"><code>snyk protect</code></a> to apply any necessary patches.</li>
  <li>Run <a href="#test"><code>snyk test</code></a> to identify on any known vulnerabilities not already ignored or patched. If such vulnerabilities were found, <a href="#test"><code>snyk test</code></a> will return a non-zero value to fail the test.</li>
</ol>
