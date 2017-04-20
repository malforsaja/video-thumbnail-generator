# Video Thumbnail Generator

[![Build Status](https://travis-ci.org/volumenetwork/video-thumbnail-generator.svg?branch=master)](https://travis-ci.org/volumenetwork/video-thumbnail-generator)

## Quick Start

```js
import ThumbnailGenerator from 'volume-thumbnail-generator';
// const ThumbnailGenerator = require('./build/index').default;

const tg = new ThumbnailGenerator({
  sourcePath: '/tmp/test.mp4',
  thumbnailPath: '/tmp/',
});

tg.generate()
  .then(console.log);
// [ 'test-thumbnail-320x240-0001.png' ]

tg.generateOneByPercent(90)
  .then(console.log);
// [ 'test-thumbnail-320x240-0001.png',
//  'test-thumbnail-320x240-0002.png',
//  'test-thumbnail-320x240-0003.png',
//  'test-thumbnail-320x240-0004.png',
//  'test-thumbnail-320x240-0005.png',
//  'test-thumbnail-320x240-0006.png',
//  'test-thumbnail-320x240-0007.png',
//  'test-thumbnail-320x240-0008.png',
//  'test-thumbnail-320x240-0009.png',
//  'test-thumbnail-320x240-0010.png' ]  
```