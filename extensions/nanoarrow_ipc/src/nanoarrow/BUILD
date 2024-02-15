package(
    default_visibility = ["//visibility:public"],
)

cc_library(
    name = "ipc",
    srcs = [
        "nanoarrow_ipc_decoder.c",
        "nanoarrow_ipc_reader.c",
        "nanoarrow_ipc_flatcc_generated.h",
    ],
    hdrs = [
        "nanoarrow_ipc.h",
        "nanoarrow_ipc.hpp",
    ],
    include_prefix = "nanoarrow",
    deps = [
        "//src/nanoarrow",
        "//extensions/nanoarrow_ipc/thirdparty/flatcc",
    ]
)

[cc_test(
    name = name,
    srcs = [name + ".cc"],
    deps = [
        "ipc",
        "@googletest//:gtest_main",
        "@zlib",
        "@nlohmann_json//:json",
        "@com_github_malkia_arrow//cpp/src/arrow",
        "@com_github_malkia_arrow//cpp/src/arrow/c:bridge",
    ],
) for name in [
    "nanoarrow_ipc_decoder_test",
    "nanoarrow_ipc_files_test",
    "nanoarrow_ipc_hpp_test",
    "nanoarrow_ipc_reader_test",
]]