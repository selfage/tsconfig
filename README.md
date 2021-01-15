# @selfage/tsconfig

Provides a opinionated but consistent tsconfig file across all @selfage packages.

Compiling to ES6.

No --strictNullChecks because it might give false impression that we are safe
from null pointer exceptions at runtime.

## Usage

Add `extends: "@selfage/tsconfig"` to your tsconfig.json.
