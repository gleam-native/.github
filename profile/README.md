# Gleam-native

Gleam-native is a highly experimental unofficial fork of awesome [Gleam](https://github.com/gleam-lang/gleam) language targeting native runtime via Cranelift. I created this project just for fun, don't use it anywhere!

## Repos

- [gleam-native](https://github.com/gleam-native/gleam-native) - compiler fork with native target introduced. Compiler lowers Gleam code to Cranelift-like native `.nir` representations and compiles JIT/AOC targets using Cranelift infrastructure
- [gleam-stdlib-native](https://github.com/gleam-native/gleam-stdlib-native) - stdlib fork providing `@external` native implementations for all its functions. Native code itself resides currently in gleam-native's in native-runtime-stdlib crate. It will be moved to a separate dynamic library later
- [glimmer](https://github.com/gleam-native/glimmer) - toy example showcasing Gleam and its stdlib capabilities. It has benchmarks comparing BEAM, Node, native JIT and native AOC targets
