load("@bazel_skylib//rules:expand_template.bzl", "expand_template")

package(
    default_visibility = ["//visibility:public"],
)

expand_template(
    name = "config",
    out = "nanoarrow_config.h",
    substitutions = {
        "@NANOARROW_VERSION_MAJOR@": "0",
        "@NANOARROW_VERSION_MINOR@": "4",
        "@NANOARROW_VERSION_PATCH@": "0",
        "@NANOARROW_NAMESPACE_DEFINE@": "#define NANOARROW_NAMESPACE_DEFINE nano",
    },
    template = "nanoarrow_config.h.in",
)

cc_library(
    name = "nanoarrow",
    srcs = [
        "array.c",
        "array_stream.c",
        "schema.c",
        "utils.c",
    ],
    hdrs = [
        "array_inline.h",
        "buffer_inline.h",
        "nanoarrow.h",
        "nanoarrow.hpp",
        "nanoarrow_types.h",
        "nanoarrow_config.h",
    ],
    include_prefix = "nanoarrow",
    includes = ["."],
)

cc_library(
    name = "testing",
    hdrs = ["nanoarrow_testing.hpp"],
    includes = ["."],
    include_prefix = "nanoarrow",
    deps = ["nanoarrow"],
)

[cc_test(
    name = name,
    srcs = [name + ".cc"],
    deps = [
        "nanoarrow",
        "testing",
        "@googletest//:gtest_main",
        "@nlohmann_json//:json",
    ],
) for name in [
    "array_stream_test",
    #"array_test",
    "buffer_test",
    "nanoarrow_hpp_test",
    "nanoarrow_testing_test",
    #"schema_test",
    #"utils_test",
]]

cc_test(
    name = "schema_benchmark",
    srcs = ["schema_benchmark.cc"],
    deps = [
        "nanoarrow",
        "@google_benchmark//:benchmark_main",
    ]
)