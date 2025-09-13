# observing-playwright

- Problem: Playwright repository does not install and run properly on macOS env
- Solution: Analyze the main repostiroy and fix the errors

# Issues on macOS 
- 
Error: Cannot find module '/Users/macbook/Desktop/Github/playwright/node_modules/@playwright/experimental-ct-core/lib/program.js'
    at createEsmNotFoundErr (node:internal/modules/cjs/loader:1405:15)
    at finalizeEsmResolution (node:internal/modules/cjs/loader:1394:15)
    at resolveExports (node:internal/modules/cjs/loader:650:14)
    at Module._findPath (node:internal/modules/cjs/loader:717:31)
    at Module._resolveFilename (node:internal/modules/cjs/loader:1355:27)
    at defaultResolveImpl (node:internal/modules/cjs/loader:1025:19)
    at resolveForCJSWithHooks (node:internal/modules/cjs/loader:1030:22)
    at Module._load (node:internal/modules/cjs/loader:1179:37)
    at TracingChannel.traceSync (node:diagnostics_channel:322:14)
    at wrapModuleLoad (node:internal/modules/cjs/loader:235:24) {
  code: 'MODULE_NOT_FOUND',

  - fixes trying:
      - run rm -rf node_modules package-lock.json
      npm install
- after that a security update for 150 packages appears
    - make those appropriatelly updated?
 
      ➜  playwright git:(main) ✗ npm install
npm warn deprecated @types/immutable@3.8.7: This is a stub types definition for Facebook's Immutable (https://github.com/facebook/immutable-js). Facebook's Immutable provides its own type definitions, so you don't need @types/immutable installed!
npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm warn deprecated debuglog@1.0.1: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm warn deprecated readdir-scoped-modules@1.1.0: This functionality has been moved to @npmcli/fs
npm warn deprecated osenv@0.1.5: This package is no longer supported.
npm warn deprecated read-package-json@2.1.2: This package is no longer supported. Please use @npmcli/package-json instead.
npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported
npm warn deprecated xterm-addon-fit@0.7.0: This package is now deprecated. Move to @xterm/addon-fit instead.
npm warn deprecated boolean@3.2.0: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm warn deprecated read-installed@4.0.3: This package is no longer supported.
npm warn deprecated xterm@5.3.0: This package is now deprecated. Move to @xterm/xterm instead.

added 656 packages, and audited 677 packages in 38s

157 packages are looking for funding
  run `npm fund` for details

1 moderate severity vulnerability

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
  
