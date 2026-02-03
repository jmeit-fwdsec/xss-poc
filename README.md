# xss-poc
Place to put XSS that can be used by CDNs like jsdelivr.


## Use Case
When a site has a CSP with script-src including the domain for a CDN that allows anyone to upload JS files.

In the case of JSDelivr it's even simpler because they will load any file in a public Github repo using the following syntax: 
- `https://cdn.jsdelivr.net/gh/GITHUB_USER/REPO_NAME/path/to/script.js`
### Example
- `https://cdn.jsdelivr.net/gh/jmeit-fwdsec/xss-poc/basic.js`
