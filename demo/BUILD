package(default_visibility = ["//visibility:public"])

load("@rules_rust//rust:defs.bzl", "rust_binary")

rust_binary(
    name = "demo",
    deps = [
            "//third_party/cargo:sha_1",
    ],
    srcs = glob(["src/**"]),
)
