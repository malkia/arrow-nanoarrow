
cc_binary(
    name = "vendored-ipc",
    srcs = ["src/library.c", "src/library.h", "src/app.c"],
    data = [
        "schema-valid.arrows"
    ],
    deps = [
        "//extensions/nanoarrow_ipc/src/nanoarrow:ipc",
    ],
    args = [
        "<$(rootpath schema-valid.arrows)"
    ],
)