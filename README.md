# setup-musl

GitHub Action to set up a musl toolchain for cross-compiling on Linux.

## Usage

```yaml
steps:
- id: setup-musl
  uses: actions/setup-musl@v1
  with:
    arch: 'x86_64' # Required. The target architecture to set up.
                   # Currently supported architecture: x86_64, aarch64, riscv64,
                   # loongarch64, arm.
- run: |
    ${{ steps.setup-musl.outputs.cross_compile }}-gcc --version
```

Authored by @equation314, ported by @aarkegz.
