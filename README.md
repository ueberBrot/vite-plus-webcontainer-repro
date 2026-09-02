# Vite+ WebContainer reproduction

This repository reproduces a Vite+ CLI startup failure in a StackBlitz WebContainer.

StackBlitz installs the dependencies and runs:

```shell
pnpm run reproduce
```

The script invokes `vp --version`. Vite+ exits while loading its native binding, before it prints the version.

To reproduce the same failure with the environment command, run:

```shell
pnpm run environment
```

The native binding works on supported local platforms. To reproduce the missing WASI distribution explicitly, run:

```shell
pnpm run reproduce:wasi
```
