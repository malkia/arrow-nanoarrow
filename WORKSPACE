load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_github_malkia_arrow",
    integrity = "sha256-ssj8pxcVnyfA6oYf8Cz8YV3Dg51IeTrlvAz0Umbk690=",
    strip_prefix = "arrow-b99e37aa7d134d985b82b773ab1555be156dcd5c",
    url = "https://github.com/malkia/arrow/archive/b99e37aa7d134d985b82b773ab1555be156dcd5c.tar.gz",
)

http_archive(
    name = "com_github_google_flatbuffers",
    integrity = "sha256-HM4GsXzd2Ja21zzAR+NqJU+4301+oYpGrPFsTAzT8/M=",
    strip_prefix = "flatbuffers-23.5.26",
    url = "https://github.com/google/flatbuffers/archive/refs/tags/v23.5.26.tar.gz",
)

http_archive(
    name = "com_github_azure_sdk",
    build_file = "@com_github_malkia_arrow//bazel:azure.BUILD",
    integrity = "sha256-YNsLwrQARusy3gGsFN+Fq7tN95VNuJBoV9DZAnpuQh4=",
    strip_prefix = "azure-sdk-for-cpp-azure-core_1.11.1",
    url = "https://github.com/Azure/azure-sdk-for-cpp/archive/refs/tags/azure-core_1.11.1.tar.gz",
)

http_archive(
    name = "com_github_microsoft_wil",
    build_file = "@com_github_malkia_arrow//bazel:wil.BUILD",
    integrity = "sha256-5ZnyhDwBueSCfkbxHTZRGAZ1yOzbuova5zX1M2cpidM=",
    strip_prefix = "wil-1.0.240122.1",
    url = "https://github.com/microsoft/wil/archive/refs/tags/v1.0.240122.1.tar.gz",
)