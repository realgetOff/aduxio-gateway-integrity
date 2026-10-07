```sh
curl -s https://aduxio.com/gateway/ | grep -oE '/gateway/assets/[A-Za-z0-9_-]+\.js' | LC_ALL=C sort -u | while read -r f; do curl -s "https://aduxio.com$f"; done | sha256sum
```
