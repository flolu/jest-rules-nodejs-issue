# Jest + Bazel Issue with `rules_nodejes@1.6.0`

## Setup

`yarn install`

## The Issue

`yarn test` will throw the following error:

```
FAIL ./test.spec.js
  ● Test suite failed to run

    Cannot find module 'jest_rules_nodejs_issue/num' from 'test.spec.js'

      at Resolver.resolveModule (../../../../../node_modules/jest-resolve/build/index.js:299:11)
      at ../../../test.spec.ts:1:1
      at test.spec.js:3:13
      at Object.<anonymous> (test.spec.js:8:3)
```

## Regression

But when reverting to `rules_nodejs` version 1.5.0 in `WORKSPACE` the `yarn test` passes!
