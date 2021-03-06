![npm](https://img.shields.io/npm/v/@immfly/js-toolkit.svg) [![Build Status](https://travis-ci.org/immfly/js-toolkit.svg?branch=master)](https://travis-ci.org/immfly/js-toolkit) [![MIT license](http://img.shields.io/badge/license-MIT-blue.svg)](http://opensource.org/licenses/MIT)

# js-toolkit
<img src='https://wallpaperaccess.com/full/1880033.jpg' />

This package exports utils modules used through `javascript` projects.

## Installation
```
npm install --save-dev @immfly/js-toolkit
```

## tool

### Shell
Allows to run bash commands.
```js
const { Shell } = require('@immfly/js-toolkit' )

...
await Shell.execute('echo "Hellow"')
```

### FileWriter
Allows to write files given the output file and its content.
```js
const { FileWriter } = require('@immfly/js-toolkit' )

...
await FileWriter.write('file.txt', '::content::'))
```

### EnvFiler
Allows generate `.env` files given the output file and the data to generate.
```js
const { EnvFiler } = require('@immfly/js-toolkit' )

...
await EnvFiler.build({
  file: 'file.txt',
  data1: '::data1::',
  data2: '::data2::'
})
```

The result of this example whould be a file named `file.txt` with this content:
```bash
DATA1=::data1
DATA2=::data2

```


## Contributing
Contributions welcome; Please submit all pull requests the against master branch. If your pull request contains JavaScript patches or features, you should include relevant unit tests. Please check the [Contributing Guidelines](contributng.md) for more details. Thanks!

## Author
Albert Pérez Farrés 

## License
 - **MIT** : http://opensource.org/licenses/MIT
