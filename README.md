# Trojan detected in rollup by Windows Security

## Metadata
OS: Windows 11

rollup: 4.34.0


## Description

This is a newly created project using `npm create vite@latest`.

`@rollup/rollup-win32-x64-msvc` is a platform dependency for rollup [(link)](https://www.npmjs.com/package/@rollup/rollup-win32-x64-msvc), that contains a file `node_modules\@rollup\rollup-win32-x64-msvc\rollup.win32-x64-msvc.node` required for running rollup on Windows.

Upon running `npm run dev`, I am getting the error:

```

> rollup-bug@0.0.0 dev
> vite

D:\Personal\rollup-bug\node_modules\rollup\dist\native.js:64
                throw new Error(
                      ^

Error: Cannot find module @rollup/rollup-win32-x64-msvc. npm has a bug related to optional dependencies (https://github.com/npm/cli/issues/4828). Please try `npm i` again after removing both package-lock.json and node_modules directory.
    at requireWithFriendlyError (D:\Personal\rollup-bug\node_modules\rollup\dist\native.js:64:9)
    at Object.<anonymous> (D:\Personal\rollup-bug\node_modules\rollup\dist\native.js:73:76)
    at Module._compile (node:internal/modules/cjs/loader:1562:14)
    at Object..js (node:internal/modules/cjs/loader:1699:10)
    at Module.load (node:internal/modules/cjs/loader:1313:32)
    at Function._load (node:internal/modules/cjs/loader:1123:12)
    at TracingChannel.traceSync (node:diagnostics_channel:322:14)
    at wrapModuleLoad (node:internal/modules/cjs/loader:217:24)
    at cjsLoader (node:internal/modules/esm/translators:263:5)
    at ModuleWrap.<anonymous> (node:internal/modules/esm/translators:196:7) {
  [cause]: Error: Cannot find module 'D:\Personal\rollup-bug\node_modules\@rollup\rollup-win32-x64-msvc\rollup.win32-x64-msvc.node'. Please verify that the package.json has a valid "main" entry
      at tryPackage (node:internal/modules/cjs/loader:492:19)
      at Function._findPath (node:internal/modules/cjs/loader:790:18)
      at Function._resolveFilename (node:internal/modules/cjs/loader:1230:27)
      at Function._load (node:internal/modules/cjs/loader:1070:27)
      at TracingChannel.traceSync (node:diagnostics_channel:322:14)
      at wrapModuleLoad (node:internal/modules/cjs/loader:217:24)
      at Module.require (node:internal/modules/cjs/loader:1335:12)
      at require (node:internal/modules/helpers:136:16)
      at requireWithFriendlyError (D:\Personal\rollup-bug\node_modules\rollup\dist\native.js:46:10)
      at Object.<anonymous> (D:\Personal\rollup-bug\node_modules\rollup\dist\native.js:73:76) {
    code: 'MODULE_NOT_FOUND',
    path: '\\\\?\\D:\\Personal\\rollup-bug\\node_modules\\@rollup\\rollup-win32-x64-msvc\\package.json',
    requestPath: '@rollup/rollup-win32-x64-msvc'
  }
}

Node.js v22.13.1
```


Windows Security logs:
![image](https://github.com/user-attachments/assets/94e9bed9-a7a0-4eeb-a0e9-5a4023446e16)






