# setup-musl

GitHub Action to set up a musl toolchain for cross-compiling on Linux.

## Usage

```yaml
steps:
- uses: actions/setup-musl@v1
  with:
    target: 'x86_64' # Required. The target architecture to set up.
                     # Currently supported architecture: x86_64, aarch64, riscv64, loongarch64.
- run: |
    x86_64-linux-musl-gcc --version
```

Authored by @equation314, ported by @aarkegz.
