# Deno plugin adapter
Converts Node.js-based projects to Deno projects.

## Requirements
- your plugin should be written for ESM
- imports should not be shortened (e.g. `./myFolder` containing `index.ts` should be written as `./myFolder/index`)
- there should be an entry point for `fetch`, exported as a default
- `node` imports have to be explicit, e.g. `import { Buffer } from 'node:buffer'` if you want to use `Buffer` otherwise the plugin will crash during runtime
