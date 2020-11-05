# Web

## Concepts
- [Hidden directories and files as a source of sensitive information about web application](https://medium.com/@_bl4de/hidden-directories-and-files-as-a-source-of-sensitive-information-about-web-application-84e5c534e5ad )
- [The line of death](https://textslashplain.com/2017/01/14/the-line-of-death/)

## Practice
- [bWAPP](http://www.itsecgames.com/)
- [Damn Vulnerable Web App](http://www.dvwa.co.uk/)
- [EnigmaGroup](https://www.enigmagroup.org/)
- [Google Gruyere](https://google-gruyere.appspot.com/)
- [Hacker101 CTF](https://www.hacker101.com/)
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)
- [PortSwigger](https://portswigger.net/web-security)
- [Webhacking.kr](https://webhacking.kr/)
- [Websec.fr](https://websec.fr/)
- [XSS Game](https://xss-game.appspot.com/)

## Repos
- [Awesome Web Security](https://github.com/qazbnm456/awesome-web-security)

## Tools
### HTTPS & SSL
- [Charles](https://www.charlesproxy.com/)

### Web Applications
- [Burp Suite](https://portswigger.net/burp/) - Web vulnerability scanner
    <details>
        <summary>Burp Suite notes</summary>

  	### Repos
  	- [Awesome Burp Extensions](https://github.com/snoopysecurity/awesome-burp-extensions)

  	### What is BurpSuite?
  	Lets you see the requests and responses to and from your browser. You can intercept traffic on the way in or out. You can also replay requests.

  	### How to set up BurpSuite
  	#### New Profile
  	Using Firefox, make a new Browser Profile (go to `about:profiles` in the Firefox browser).
  	#### Proxy Setup
  	Go to `Prefences > General > Network Settings` and select `Manual proxy configuration` and enter `127.0.0.1` and `8080` for the port. Make sure to check `Use this proxy server for all protocols`. You should probably use a VPN in case you get your IP banned, so your "real" IP doesn't actually get banned.
  	### Useful Extensions
  	- User-Agent Switcher
  	  - Change your User Agent
  	- Wappalyzer
  	- BuiltWith
  	- HackBar
  	  - Send POST requests directly from the browser
  	- Web Developer
  	#### Download Burp Suite CA
  	Download the BurpSuite Certificate from http://burp.
  	#### Install BurpSuite CA
  	Go to `Preferences > Privacy & Security > Certificates > View Certificates` and click the `Authorities` tab. Import the certificate that you just downloaded.

  	### Target Tab
  	- Focus on specific sites
  	- Focus on specific functions
  	- Visualize attack surface
  	- Set "Scope" to filter all other tools
  	#### Site Map
  	The Target tab is a tree style view of all websites in scope.
  	#### Scope
  	Control what you're looking at. You can add specific domains or keywords. You can add things from this menu or right click to add things from the Site Map tab.

  	### Proxy Tab
  	#### HTTP History Tab
  	Shows requests and responses. It will show extra info in the `Params` tab, and the headers in the `Headers` tab.

  	### Spider Tab
  	Will automatically try to fill out information in the site map tab. It will try to explore and enumerate every link and subdomain from the given website to try to fill out an entire site map.

  	### Sequencer Tab
  	Test the entropy of cookies, session tokens, and CSRF tokens.

  	### Intruder Tab
  	A way to automate injections and form automation. You can specify payloads for BurpSuite to go through and try. The Community Edition of BurpSuite does not include any payloads automatically.

  	- Attack types: Sniper, Battering Ram, Pitchfork, Cluster Bomb.
  	- Allows you to fuxx parameters/paths
  	- Brute force passwords
  	- Content discovery
    </details>
- [CLOUDKiLL3R](https://github.com/inurlx/CLOUDKiLL3R) - Bypasses Cloudflare protection service via TOR Browser using crimeflare !
- [fuzzdb](https://github.com/fuzzdb-project/fuzzdb) - Dictionary of attack patterns and primitives
- [git-dumper](https://github.com/arthaud/git-dumper) - A tool to dump a git repository from a website.
- [Nikto](https://cirt.net/Nikto2) - Web server scanner
- [owtf](https://github.com/owtf/owtf) - Offensive Web Testing Framework (OWTF)
- [wafw00f](https://github.com/EnableSecurity/wafw00f) - Fingerprint Web Application Firewall (WAF)
- [w3af](http://w3af.org) - Web Application Attack and Audit Framework
- [Wfuzz](https://github.com/xmendez/wfuzz) - Web application fuzzer
- [WhatWaf](https://github.com/Ekultek/WhatWaf) - Detect and bypass web application firewalls and protection systems
- [WPscan](https://wpscan.org) - WordPress vulnerability scanner
- [JCS](https://github.com/TheM4hd1/JCS) - Joomla Vulnerability Component Scanner
- [JSONBee](https://github.com/zigoo0/JSONBee) - A ready to use JSONP endpoints/payloads to help bypass content security policy (CSP) of different websites.
- [testssl.sh](https://github.com/drwetter/testssl.sh) - Testing TLS/SSL encryption anywhere on any port
- [XSStrike](https://github.com/s0md3v/XSStrike) - Most advanced XSS scanner.

### Web Shells
- [weevely3](https://github.com/epinna/weevely3) - Weaponized web shell
- [b374k](https://github.com/b374k/b374k) - PHP Webshell with handy features
- [Miyachung](https://packetstormsecurity.com/files/122612/Miyachung-BackConnect-Shell.html) - PHP BackConnect Shell
- [wso-2.8-web-shell](https://github.com/rzkyh007/wso-web-shell-2-8) - Automatically exported from code.google.com/p/wso-web-shell-2-8
