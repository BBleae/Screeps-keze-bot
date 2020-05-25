# Screeps-keze-bot

orginal bot for Screeps

## Deploying

This codebase uses [Gulp](https://gulpjs.com/) to deploy to the screeps server. It uses a configuration file, `.screeps.json`, which can save multiple configurations.

```json
{
  "main": {
    "username": "Keze",
    "password": "random123",
    "branch": "main"
  },
  "127.0.0.1": {
    "username": "Keze",
    "password": "random123"
  },
  "myserver.example.com": {
    "username": "Keze",
    "password": "random123",
    "ssl": true
  }
}
```

By default `Gulp` will deploy to the `main` server, but this can be changed with the `server` flag.

```
gulp --server=127.0.0.1
```

By default gulp will push to the `default` branch. This can be changed in the configuration file or by passing the `branch` option to gulp.
