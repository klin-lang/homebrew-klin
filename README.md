# homebrew-klin

Homebrew tap for the [Klin](https://github.com/klin-lang/klin) compiler.

**Stable** installs a prebuilt GitHub Release binary. **No Dart.**
`dart-lang/dart` is only for `--HEAD` (build from `main`).

Details: [klin docs/17-homebrew.md](https://github.com/klin-lang/klin/blob/main/docs/17-homebrew.md).

## Install

```sh
brew install klin-lang/klin/klin
klin --version
```

Homebrew adds this tap automatically. If a short name is refused
(Homebrew 6+ [tap trust](https://docs.brew.sh/Tap-Trust)):

```sh
brew tap klin-lang/klin
brew trust --formula klin-lang/klin/klin
brew install klin
```

HEAD (`main` — needs [Dart tap](https://github.com/dart-lang/homebrew-dart)):

```sh
brew tap dart-lang/dart
brew trust --formula dart-lang/dart/dart
brew install --HEAD klin-lang/klin/klin
```

Upgrade (full name so Homebrew refreshes this tap):

```sh
brew update
brew upgrade klin-lang/klin/klin
```

## Notes

- `klin run` needs a host C compiler (`gcc`, `clang`, or `tcc`) on `PATH`.
- On macOS, Homebrew also needs current Xcode Command Line Tools, even
  for this prebuilt bottle. That is Apple/Homebrew, not Klin or Dart.
- Formula: [`Formula/klin.rb`](Formula/klin.rb). Keep in sync with
  [klin-lang/klin](https://github.com/klin-lang/klin) `Formula/klin.rb`.
- Binaries: [Klin releases](https://github.com/klin-lang/klin/releases).
