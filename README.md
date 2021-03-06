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

It simply exposes [`fs-extra`](https://www.npmjs.com/package/fs-extra#methods) functionalities. Examples:
```
fsbin emptyDir <dir>
fsbin copy <srcdir> <destdir>
fsbin mkdirs build/static/styles
fsbin remove build/static
```

In [`create-mithril-app`](https://www.npmjs.com/package/create-mithril-app), I used the following for the `build` pipeline:
```js
"scripts": {
  "build": "fsbin emptyDir build && fsbin copy public build && webpack"
}
```
The above script empties the `build` folder, then repopulates it with both static files and webpacked files.

## Special Thanks
Special thanks to the `fs-extra` team.
