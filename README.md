# heroku-buildpack-mongo-tools

Heroku buildpack that auto-installs the latest [MongoDB Database Tools](https://www.mongodb.com/docs/database-tools/) (`mongodump`, `mongorestore`, `mongoexport`, `mongoimport`, `bsondump`).

## Usage

```sh
heroku buildpacks:add https://github.com/AnonymousProDev/heroku-buildpack-mongo-tools
git push heroku main
heroku run mongodump --version
```

## Example

```sh
heroku run mongodump --uri="$MONGODB_URI" --archive=/tmp/backup.gz --gzip
```

## Notes

- Fetches the latest version from MongoDB's [official archive](https://www.mongodb.com/try/download/database-tools/releases/archive), falls back to a stable version if unavailable.

## Credits

Inspired by [siesgstarena/heroku-buildpack-mongo](https://github.com/siesgstarena/heroku-buildpack-mongo)

## License

[MIT](LICENSE)