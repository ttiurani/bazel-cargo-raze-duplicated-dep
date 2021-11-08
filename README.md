# Bazel Cargo Raze Duplicate Deps Problem

A simple dependency to the [sha-1 crate](https://docs.rs/sha-1/0.9.8/sha1/index.html) fails to compile (at least on OSX), due to the [platform specific deps in cpufeatures](https://github.com/RustCrypto/utils/blob/master/cpufeatures/Cargo.toml#L17-L21).

```bash
$ bazel test //... --sandbox_debug --verbose_failures
ERROR: [clip]/external/raze__cpufeatures__0_2_1/BUILD.bazel:34:13: Label '@raze__libc__0_2_107//:libc' is duplicated in the 'deps' attribute of rule 'cpufeatures'
ERROR: [clip]/external/raze__sha_1__0_9_8/BUILD.bazel:47:13: Target '@raze__cpufeatures__0_2_1//:cpufeatures' contains an error and its package is in error and referenced by '@raze__sha_1__0_9_8//:sha1'
```
