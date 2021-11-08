load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_rust",
    sha256 = "d6a8bc37502f252ef190b37945c922e0d0104dc2250940a3ea5f9c42e7a0dc10",
    strip_prefix = "rules_rust-e2f0fccda912daac686b533ad77c5bc5d2f2ddb7",
    urls = [
        # Master branch as of 2021-11-05
        "https://github.com/bazelbuild/rules_rust/archive/e2f0fccda912daac686b533ad77c5bc5d2f2ddb7.tar.gz",
    ],
)
load("@rules_rust//rust:repositories.bzl", "rust_repositories")
rust_repositories(version = "1.56.1", edition="2018", rustfmt_version = "1.56.1")

load("//third_party/cargo:crates.bzl", "raze_fetch_remote_crates")
raze_fetch_remote_crates()
