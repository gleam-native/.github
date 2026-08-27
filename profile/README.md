# Gleam-native

Gleam-native is a highly experimental unofficial fork of awesome [Gleam](https://github.com/gleam-lang/gleam) language targeting native runtime via Cranelift.

Gleam relies heavily on BEAM abstractions. I highly regard Erlang and BEAM myself so decided to mimic parts of it in my native runtime for ecosystem capability. Native runtime currently is essentially tokio polling corosensei fibers as lightweight processes communicating via messages. The runtime features BEAM-like primitives for actor model like process mailboxes, links and monitors attached

I created this project just for fun, don't use it anywhere!

## Repos

- [gleam-native](https://github.com/gleam-native/gleam-native) - compiler fork with native target introduced. Compiler lowers Gleam code to Cranelift-like intermediate `.nir` representation and compiles JIT/AOT targets using Cranelift infrastructure
- [gleam-native-stdlib](https://github.com/gleam-native/gleam-native-stdlib) - stdlib fork providing `@external` native implementations for all its functions. Native code itself resides currently in gleam-native's native-runtime-stdlib crate. It will be moved to a separate dynamic library later
- [gleam-native-gleeunit](https://github.com/gleam-native/gleam-native-gleeunit) - lean gleeunit fork for native target
- [gleam-native-erlang](https://github.com/gleam-native/gleam-native-erlang) - gleam_erlang fork. Absolute abomination. Native runtime implements parts of Erlang processing and communication model OTP is built upon. Some parts of it are Erlang-only: of course immature native runtime wouldn't feature stuff like distributed nodes
- [gleam-native-otp](https://github.com/gleam-native/gleam-native-otp) - gleam_otp fork with native runtime support
- [glimmer](https://github.com/gleam-native/glimmer) - toy example showcasing Gleam and its stdlib capabilities. It has benchmarks comparing BEAM, Node, Deno, Bun, and native AOT/JIT targets
- [hive](https://github.com/gleam-native/hive) - toy example showcasing actor runtime. Benchmarks BEAM vs native AOT/JIT
- [gleam-native-process](https://github.com/gleam-native/gleam-native-process) - some leftovers after initial process model implementation. The most valuable part of it is isolated tests
- [proc-spike](https://github.com/gleam-native/proc-spike) - process model showcase I created to debug workstealing fibers. Almost no value, might delete later
