licenses(["notice"])  # Apache 2

load(
    "//bazel:envoy_build_system.bzl",
    "envoy_package",
)
load(
    "//test/extensions:extensions_build_system.bzl",
    "envoy_extension_cc_test",
)

envoy_package()

envoy_extension_cc_test(
    name = "config_test",
    srcs = ["config_test.cc"],
    data = [
        "//test/extensions/filters/network/wasm/test_data:modules",
    ],
    extension_name = "envoy.filters.network.wasm",
    deps = [
        "//source/common/common:base64_lib",
        "//source/extensions/common/wasm:wasm_lib",
        "//source/extensions/filters/network/wasm:config",
        "//test/mocks/server:server_mocks",
        "//test/test_common:environment_lib",
        "@envoy_api//envoy/extensions/filters/network/wasm/v3:pkg_cc_proto",
    ],
)

envoy_extension_cc_test(
    name = "wasm_filter_test",
    srcs = ["wasm_filter_test.cc"],
    data = [
        "//test/extensions/filters/network/wasm/test_data:modules",
    ],
    extension_name = "envoy.filters.network.wasm",
    deps = [
        "//source/extensions/filters/network/wasm:wasm_filter_lib",
        "//test/mocks/network:network_mocks",
        "//test/mocks/server:server_mocks",
        "//test/test_common:environment_lib",
    ],
)
