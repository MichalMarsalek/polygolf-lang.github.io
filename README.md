## PolyGolf Playground

Compiles [PolyGolf](https://github.com/jared-hughes/polygolf) to [code.golf](https://code.golf) languages in your browser.

Link: [btnlq.github.io/polygolf-web/](https://polygolf-lang.github.io/polygolf-playground/)

### Development

The `polygolf.bundle.js` file is generated by running
```sh
esbuild src/polygolf.ts --bundle --outfile=polygolf.bundle.js
```
in [the PolyGolf project](https://github.com/polygolf-lang/polygolf).

The `codemirror.bundle.js` file is generated by running
```sh
npm install codemirror @codemirror/theme-one-dark codemirror-lang-polygolf rollup @rollup/plugin-node-resolve @rollup/plugin-terser
node_modules/.bin/rollup codemirror.js -f iife -n CodeMirror -o codemirror.bundle.js -p @rollup/plugin-node-resolve -p @rollup/plugin-terser
```

You can find `polygolf.ts` and `codemirror.js` in `/entries`.
