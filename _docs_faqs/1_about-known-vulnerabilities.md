---
title: About known vulnerabilities
draft: true
---

<h3 class="h4">What are known vulnerabilities?</h3>

<p>Known vulnerabilities are publicly disclosed security bugs, typically found and logged by users, or reported by security researchers. Being public makes these issues the easiest ones for attackers to find and exploit <a href="http://www.theregister.co.uk/2015/02/23/hp_hack_vulnerable_threat_study/">[1]</a>, and therefore very important to address.</p>

<h3 class="h4">What are direct and deep dependencies?</h3>
<p>Known vulnerabilities can be introduced either via a direct or via a deep dependency.</p>
<ul>
	<li>A direct dependency is a is a package that you've included in your own project via package.json.</li>
	<li>A deep dependency, also referred to as an indirect, chained, or transitive dependency, is a package that you are not using directly, but one that is used by one of your direct dependencies.</li>
</ul>
<p>In other words, if your application is using module A, and module A is using module B, then your application is indirectly depending on module B. And if module B is vulnerable, you are vulnerable.</p>

<h3 class="h4">How do you determine the severity of a vulnerability?</h3>
<p>The severity of a vulnerability is manually assigned by our security research team. It’s based primarily on the impact of the vulnerability, and by how easy it is to exploit it.</p> 
</p>For instance, the <a href="https://snyk.io/vuln/npm:bassmaster:20140927">bassmaster vulnerability</a> allows an attacker to execute code on your server (a “remote command execution” vulnerability), and can easily be exploited with a well crafted request, making it a high severity issue. The <a href="https://snyk.io/vuln/npm:dns-sync:20141111">dns-sync vulnerability</a> also allows remote command execution, but to exploit it an attacker needs to control the name of the host you resolve - a less likely scenario. Therefore, it was deemed medium severity.</p>

<h3 class="h4">Why should I monitor my projects for known vulnerabilities? </h3>
<p>New vulnerabilities aren’t actually new security holes - they’re newly disclosed, but impact old, existing code. This means you could have new known vulnerabilities without making any code changes. <a href="https://snyk.io/docs/using-snyk/#monitor">Monitoring your projects</a> means you’ll be the first to know if you are affect by a newly disclosed vulnerability, and you can assess and act upon the vulnerability risk quickly.</p>


