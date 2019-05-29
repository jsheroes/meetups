# Let's talk about open source security!

### Speaker: [Liran Tal](https://twitter.com/liran_tal)
### Date: 09.04.2019
### Venue: Yonder
### Description:


I will share insights from the state of open source security report that I released earlier this year and we can discuss the role of security for developers.

* How would you rate your security knowledge?
* How do you bake security as part of your projects? at work and open source?
* What are some action items to follow-up on?

We will follow-up this open discussion with a Live Hack! exploiting several well-known vulnerability types that lurk in your open source projects.

*Stranger Danger, Finding Security Vulnerabilities Before They Find You!*

Open source modules are undoubtedly awesome. However, they also represent an undeniable and massive risk. You're introducing someone else's code into your system, often with little or no scrutiny. The wrong package can introduce severe vulnerabilities into your application, exposing your application and your user's data.

This talk will use a sample application, Goof, which uses various vulnerable dependencies, which we will exploit as an attacker would. For each issue, we'll explain why it happened, show its impact, and – most importantly – see how to avoid or fix it. We'll live hack exploits like the classic struts vulnerability that recently made it famous, along with Spring Break and several others.

About Liran:

Liran Tal is a Developer Advocate at Snyk and a member of the Node.js Security working group. He is a JSHeroes ambassador, passionate about building communities and the open source movement and greatly enjoys pizza, wine, web technologies, and CLIs.

Liran is also the author of Essential Node.js Security, a core contributor to OWASP NodeGoat project and loves to dabble about code, testing, and software philosophy.
### Slides: 


### Tools


### References

* [Snyk - open source security platform](https://snyk.io/)
* Awesome Node.js Security repo to follow-up on tools we mentioned, security incidents in the JavaScript world and more.
* We'll keep a full list of resources from the talk at: https://github.com/jsheroes/meetups/blob/master/websec/lets-talk-about-open-source-security.md
* The 50 pages report I mentioned during the talk with *tons* of insights about the state of open source security, covering everything from docker, containers to Node.js and JavaScript application vulnerabilities: https://snyk.io/opensourcesecurity-2019/ (there's a link to download the PDF from there)
* Snyk the developer-friendly security tooling obviously: http://snyk.io - encourage everyone to try it out, either as a CLI (npm install -g snyk) or connect your projects over GitHub and this way you can have automated fix PRs opened for your repos in order to fix security vulnerabilities (what can you ask more than this? :-))

