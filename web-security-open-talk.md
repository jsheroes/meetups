# Web Security - Open Discussion

### Date: 15.01.2019
### Venue: QCatalyst
### Description:

Web Security is an important topic and sometimes a bit neglected. Let's kickstart our 2019 meetups with this important topic.

Some of the topics will touch:
* sensitive data exposure
* input validation
* XSS
* CSRF
etc ...
Anyone is welcomed, those who want to share or just learn new things.

### Meeting notes:

#### Topics( proposed )
* Security mindset - Capture the flag games, break the current project that your work on 
* Dev ops / server security -> Preferably use a devops, and if you do it yourself at least have a checklist( 
* Audits ( tools ) -Snyc 
* Security for QA perspective
* Products / Not Tech
* NPM packages
* API
* Data leaks
* Error Handling
* External security audits
* 3rd party /lasting sec
* How much is enough
* Maintenance
* Newsletters
* Language specific
* Clients-side, CORS, etc
* UX / users education


#### Resources
* [Web Security cheetsheet](https://github.com/FortechRomania/js-team-showcase/blob/master/how-we-work/security/security-cheatsheet.png)
* [Web Security checklist](https://github.com/FortechRomania/js-team-showcase/blob/master/how-we-work/security/dev-security-checklist.md)

#### Penetration Testing tools (for self use purposes **only**)
- [Burp](https://portswigger.net) - pen testing tool
- [ZEP proxy](https://github.com/zaproxy/zaproxy) - Burp alternative
- [haveibeenpwned](https://haveibeenpwned.com/) - check email if it was leaked
- [file-buster](https://github.com/henshin/filebuster) - scan routes on domains
- [testssl](https://testssl.sh/) - test for ssl vul
- [slowhttp](https://github.com/shekyan/slowhttptest) - test for Slow Loris
- [metasploit](https://www.metasploit.com/) - the mother load
- [JSParser](https://github.com/nahamsec/JSParser) - parse js files and expose link concatenations
- [nmap](https://nmap.org/) - scanning tool
- [sqlmap](http://sqlmap.org/) - sql injection tool
- [Nessus](https://www.tenable.com/products/nessus/nessus-professional) - highly advanced security testing tool
- [wappalyzer](https://www.wappalyzer.com/) - analyze technologies used

#### Exploits and vulnerabilities databases
- [cve](https://www.cvedetails.com) Exploits DB
- [google cheatsheet](https://www.exploit-db.com/google-hacking-database)
- [searchsploit](https://www.exploit-db.com/searchsploit) - cli exploit search
- [xss-payloads](http://www.xss-payloads.com/index.html)

#### Web apps and VM to practice penetration testing
- [altormutual](http://altoromutual.com/) - vulnerable site to excercise on
- [OWASP JuiceShop](https://github.com/bkimminich/juice-shop) - hackable app
- [OWASP bWAPP](http://www.itsecgames.com/) - another hackable web app
- [Vulnhub](https://www.vulnhub.com/) - vulnerable VMs to practice on
- [NodeGoat](https://github.com/OWASP/NodeGoat) - vulnerable nodejs app

#### Mindset & methodologies 
- [OWASP ASVS](https://www.owasp.org/index.php/Category:OWASP_Application_Security_Verification_Standard_Project) - security standard
- [Security framework](https://www.securityknowledgeframework.org/) - a comprehensive security checklist
- [OWASP security checklist](https://www.owasp.org/index.php/File:OWASP_SCP_Quick_Reference_Guide_v2.pdf) 
- [OWASP testing guide](https://www.owasp.org/index.php/OWASP_Testing_Guide_v4_Table_of_Contents) - for QA and Pen Testers
- [http://owaspsamm.org/](http://owaspsamm.org/) - enterprise security model
- [BDD security](https://continuumsecurity.net/bdd-security/) - CI security scan
- [JS security code practices](https://checkmarx.gitbooks.io/js-scp/input-validation/data-types/files.html)

#### Packages 
* [Validator](https://www.npmjs.com/package/validator) for validation checks
* [Joi](https://www.npmjs.com/package/joi) - another popular validator package, with a [build](https://github.com/jeffbski/joi-browser) targeting browsers
* [Safe Regex](https://www.npmjs.com/package/safe-regex) to check if sa regex is safe or if could create infinit loops
* [express-rate-limit](https://www.npmjs.com/package/express-rate-limit) - rate limiter for Express.js
* [Helmet](https://www.npmjs.com/package/helmet) - express middleware for setting up application headers

