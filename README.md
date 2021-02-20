# @selfage/tsconfig

## Overview
Provides a opinionated but consistent tsconfig file across all @selfage packages.

## Highlight

1. Compile to ES6 and compile incrementally.
2. No --strictNullChecks because it might give false impression that we are safe from null pointer exceptions at runtime. Every type is implicitly an union with `undefined & null`.
3. Inline source map and inline source to avoid specifying source map/source when mapping especially in browser, with the downside of larger JS file.
4. Generate `.d.ts`.

## Usage

Add `extends: "@selfage/tsconfig"` to your tsconfig.json.

## Full compiler options

```JSON
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "moduleResolution": "Node",
    "esModuleInterop": true,
    "alwaysStrict": true,
    "noImplicitAny": true,
    "noImplicitThis": true,
    "noImplicitReturns": true,
    "noUnusedLocals": true,
    "inlineSourceMap": true,
    "inlineSources": true,
    "skipLibCheck": true,
    "declaration": true,
    "incremental": true
  }
}
```