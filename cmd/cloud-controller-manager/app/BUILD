package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = ["controllermanager.go"],
    tags = ["automanaged"],
    deps = [
        "//cmd/cloud-controller-manager/app/options:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/client/clientset_generated/clientset/typed/core/v1:go_default_library",
        "//pkg/client/leaderelection:go_default_library",
        "//pkg/client/leaderelection/resourcelock:go_default_library",
        "//pkg/client/record:go_default_library",
        "//pkg/client/restclient:go_default_library",
        "//pkg/client/unversioned/clientcmd:go_default_library",
        "//pkg/cloudprovider:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/controller/cloud:go_default_library",
        "//pkg/controller/informers:go_default_library",
        "//pkg/controller/route:go_default_library",
        "//pkg/controller/service:go_default_library",
        "//pkg/util/configz:go_default_library",
        "//pkg/util/wait:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:github.com/prometheus/client_golang/prometheus",
        "//vendor:github.com/spf13/cobra",
        "//vendor:github.com/spf13/pflag",
        "//vendor:k8s.io/apiserver/pkg/healthz",
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
    srcs = [
        ":package-srcs",
        "//cmd/cloud-controller-manager/app/options:all-srcs",
    ],
    tags = ["automanaged"],
)
