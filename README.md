# @selfage/tsconfig

Provides a opinionated but consistent tsconfig file across all @selfage packages.

Compiling to ES5 for best compability.

No --strictNullChecks because it might give false impression that we are safe from null pointer exceptions at runtime.

## Usage

Add `extends: "@selfage/tsconfig/tsconfig"` to your tsconfig.json.