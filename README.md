# Collect FPS

[![Build Status](https://travis-ci.org/batata-frita/collect-fps.svg)](https://travis-ci.org/batata-frita/collect-fps)
[![npm version](https://badge.fury.io/js/collect-fps.svg)](https://badge.fury.io/js/collect-fps)

Small module that uses `requestAnimationFrame` to collect what is the current FPS.

## Usage

First install it:

```bash
npm install --save collect-fps
```

Calling it will initialize the collection and return a function. When invoked, that function will stop the collection and return the frame per seconds value (a float number).

```javascript
import collectFPS from 'collect-fps'

const endCollection = collectFPS()

setTimeout(() => {
  const fps = endCollection()
  console.log(fps)
}, 1000)
```

If `requestAnimationFrame` is not available in your runtime, it will throw an error when invoked

## License

[MIT](LICENSE)
