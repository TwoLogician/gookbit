## docker

*depends_on*
```yaml
  depends_on:
    - "db"
```

*localtime & timezone*
```yaml
  volumes:
    - "/etc/localtime:/etc/localtime:ro"
    - "/etc/timezone:/etc/timezone:ro"
```

*Start containers automatically*
```yaml
  restart: "always"
```