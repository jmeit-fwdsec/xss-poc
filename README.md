# xss-poc
Place to put XSS that can be used by CDNs like jsdelivr.


## Use Case
When a site has a CSP with `script-src:` that includes a CDN domain, where we can host JS files on that CDN.

In the case of JSDelivr it's even simpler because they will load any file in any public Github repo using the following syntax: 
- `https://cdn.jsdelivr.net/gh/GITHUB_USER/REPO_NAME/path/to/script.js`

### Example
#### Exploitable Evidence
Assuming you have found an XSS vector that is being blocked by 'unsafe-inline'.

```
Content-Security-Policy: ... srcipt-src: 'https://cdn.jsdelivr.net' ; ...
```
#### Payload URL
- `https://cdn.jsdelivr.net/gh/jmeit-fwdsec/xss-poc/basic.js`
### Remediation
The CSP should use either hashes or nonces instead of hostnames.
