# Demo for Vite

## What?

It contains a React app, a Web app, and four libraries, two React ones, and two plain js ones. Both the apps import the libraries, and the libraries import each other.

## Why?

We want to test the tsconfig paths resolution, among other things. Hence the deep imports, etc. Works with `vite-tsconfig-paths` version `3.6.0`, does NOT work with version `4.0.0-alpha.4`.

On an unrelated note, we are also testing the cypress+vite integration on the `test/cypress` branch.

## How to work

### For path resoltion: On `main` branch

You can try

```
nx build rv1
```

and see it failing due to the incorrect path resolution.

You can install the working version of `vite-tsconfig-paths` with

```
yarn add -D vite-tsconfig-paths@3.6.0
```

and then build again.

### For cypress+vite integration: On the `test/cypress`

Checkout the `test/cypress` branch

```
git checkout test/cypress
```

to test out the cypress+vite integration.

Do

```
nx e2e rv1-e2e
```

and see it failing.

Look into the [apps/rv1-e2e/cypress.config.ts](apps/rv1-e2e/cypress.config.ts) and see all the addititons for `cypress` and `vite`.
