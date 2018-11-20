licenses(["notice"])  # Apache 2

# WASM service.

load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_package",
)

envoy_package()

envoy_cc_library(
    name = "config",
    srcs = [
        "config.cc",
        "wasm.cc",
    ],
    hdrs = [
        "config.h",
        "wasm.h",
    ],
    deps = [
        "//include/envoy/registry",
        "//include/envoy/server:wasm_config_interface",
        "//source/common/common:assert_lib",
        "//source/common/protobuf:utility_lib",
        "//source/extensions/common/wasm:wasm_lib",
        "//source/extensions/grpc_credentials:well_known_names",
    ],
)