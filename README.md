# s3-mongodump

[![version](https://img.shields.io/npm/v/s3-mongodump.svg?style=flat-square)][version]
[![build](https://img.shields.io/travis/theworkflow/s3-mongodump/master.svg?style=flat-square)][build]
[![license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)][license]

Perform mongodump on database host and send backup to s3

## Install

`$ npm install -g s3-mongodump`

### CLI Usage

  Usage: s3-mongodump [options]

  Options:

    -h, --help                           output usage information
    -V, --version                        output the version number
    -h, --host <mongo host>              Host connection to mongo database host
    -d, --db                             Mongo database to connect to
    -u --username <username>             DB host admin username
    -p, --password <password>            DB host admin password
    --oplog                              Oplog flag for mongodump command
    -o --output <path>                   Output path to store tar file
    -b --bucket <bucket>                 AWS bucket location (includes path to uploaded folder)
    --accessKeyId <accessKeyId>          AWS accessKeyId
    --secretAccessKey <secretAccessKey>  AWS secretAccessKey
    --retry <number>                     Number of time to retry on sending backup to S3

### API Usage

```javascript
const Backup = require('s3-mongodump')

Backup(options, (err) => {
  if (err) throw err
})
```

## Contributing

Contributions welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.

## License

[MIT](LICENSE.md)

[version]: https://www.npmjs.com/package/s3-mongodump
[build]: https://travis-ci.org/theworkflow/s3-mongodump
[license]: https://raw.githubusercontent.com/theworkflow/s3-mongodump/master/LICENSE
