# netcdf-gcms

  [![NPM version][npm-image]][npm-url]
  [![build status][travis-image]][travis-url]
  [![Test coverage][coveralls-image]][coveralls-url]
  [![David deps][david-image]][david-url]
  [![npm download][download-image]][download-url]
  
Parser from NetCDF files to JSON usable for GCMS

## Installation

`$ npm install netcdf-gcms`

## [API Documentation](https://cheminfo-js.github.io/netcdf-gcms/)

## Example

```js
const netcdfGcms = require('netcdf-gcms');
const fs = require('fs');

const data = fs.readFileSync('Agilent.cdf');

// reads the data from the file
const json = netcdfGcms(data);

// or if you already know the format
const agilentJson = netcdfGcms.fromAgilent(data);

json === {
  times: [/* ... */],
  series: [{
	name: 'tic',
	dimension: 1,
	data: [/* ... */]
  }, {
	name: 'ms',
	dimension: 2,
	data: [
	  [
	    [/* ... */],
       	[/* ... */]
      ]
	]
  }]
}
```


## License

[MIT](./LICENSE)

[npm-image]: https://img.shields.io/npm/v/netcdf-gcms.svg?style=flat-square
[npm-url]: https://npmjs.org/package/netcdf-gcms
[travis-image]: https://img.shields.io/travis/cheminfo-js/netcdf-gcms/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/cheminfo-js/netcdf-gcms
[coveralls-image]: https://img.shields.io/coveralls/cheminfo-js/netcdf-gcms.svg?style=flat-square
[coveralls-url]: https://coveralls.io/github/cheminfo-js/netcdf-gcms
[david-image]: https://img.shields.io/david/cheminfo-js/netcdf-gcms.svg?style=flat-square
[david-url]: https://david-dm.org/cheminfo-js/netcdf-gcms
[download-image]: https://img.shields.io/npm/dm/netcdf-gcms.svg?style=flat-square
[download-url]: https://npmjs.org/package/netcdf-gcms
