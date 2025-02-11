Vite bundles transitive dependencies of linked dependencies into the SSR build, which is not what we want to happen.

```console
$ git clone https://github.com/haines/vite-ssr-externals-repro.git
$ cd vite-ssr-externals-repro
$ pnpm run repro
...
ReferenceError: require is not defined in ES module scope, you can use import instead
This file is being treated as an ES module because it has a '.js' file extension and 'vite-ssr-externals-repro/packages/app/package.json' contains "type": "module". To treat it as a CommonJS script, rename it to use the '.cjs' file extension.
```
