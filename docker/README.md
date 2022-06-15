## docker

*depends_on*
```yaml
  depends_on:
    - "db"
```

*timezone*
```yaml
  environment:
    TZ: "Asia/Bangkok"
```

*Start containers automatically*
```yaml
  restart: "always"
```