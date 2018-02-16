# fsbin - simple file system utility for npm script
[![npm package](https://nodei.co/npm/fsbin.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/fsbin/)


## Purpose
I need some quick and dirty way to delete a directory or copy a directory in npm scripts. e.g.
```js
  "scripts": {
    "dev": "webpack-dev-server",
    "build": "fsbin emptyDir buid && webpack"
  }
```

## Usage
`npm install fsbin`, then use it in your package.json.

It simply exposes `fs-extra` functionalities. Examples:
```
fsbin emptyDir <dir>
fsbin copy <srcdir> <destdir>
```

## Special Thanks
Obviously special thanks to the `fs-extra` team.
