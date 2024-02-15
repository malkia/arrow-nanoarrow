cc_library(
    name = "linesplitter",
    srcs = ["linesplitter.cc"],
    hdrs = ["linesplitter.h"],
    deps = [
        "//src/nanoarrow",
    ],
)

cc_test(
    name = "linesplitter_test",
    srcs = ["linesplitter_test.cc"],
    deps = ["linesplitter", "@googletest//:gtest_main"],
)