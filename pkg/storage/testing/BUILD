package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "types.generated.go",
        "types.go",
        "utils.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api/meta:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/apis/meta/v1:go_default_library",
        "//pkg/runtime:go_default_library",
        "//pkg/runtime/schema:go_default_library",
        "//pkg/storage:go_default_library",
        "//pkg/types:go_default_library",
        "//vendor:github.com/ugorji/go/codec",
        "//vendor:golang.org/x/net/context",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
