# homebrew-dlt

Homebrew tap for [COVESA DLT daemon](https://github.com/COVESA/dlt-daemon).

## Install

```sh
brew tap alexmohr/dlt
brew install dlt-daemon
```

## Formulae

### dlt-daemon

Builds the COVESA DLT daemon from the commit that includes macOS build support ([PR #819](https://github.com/COVESA/dlt-daemon/pull/819)).

Installs:
- `bin/dlt-daemon` — the daemon binary
- `lib/libdlt.dylib` — user library
- `include/dlt/` — public headers
- `lib/cmake/automotive-dlt/` — CMake config for `find_package`
- `lib/pkgconfig/automotive-dlt.pc` — pkg-config file

## Updating the formula

Once PR #819 is merged into a release tag, update `Formula/dlt-daemon.rb`:

1. Replace `url ... using: :git, revision:` with a tarball URL: `https://github.com/COVESA/dlt-daemon/archive/refs/tags/vX.Y.Z.tar.gz`
2. Add `sha256 "<checksum>"`
3. Update `version`
