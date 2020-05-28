# BurpSuite

## Repos
- [Awesome Burp Extensions](https://github.com/snoopysecurity/awesome-burp-extensions)


## BurpSuite Workshop Notes
### What is BurpSuite?
Lets you see the requests and responses to and from your browser. You can intercept traffic on the way in or out. You can also replay requests.

### How to set up BurpSuite
#### New Profile
Using Firefox, make a new Browser Profile (go to `about:profiles` in the Firefox browser).
#### Proxy Setup
Go to `Prefences > General > Network Settings` and select `Manual proxy configuration` and enter `127.0.0.1` and `8080` for the port. Make sure to check `Use this proxy server for all protocols`. You should probably use a VPN in case you get your IP banned, so your "real" IP doesn't actually get banned.
#### Useful Extensions
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
