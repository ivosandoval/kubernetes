package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "fakes.go",
        "identity_mappers.go",
        "iterator.go",
        "pet.go",
        "pet_set.go",
        "pet_set_utils.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api/errors:go_default_library",
        "//pkg/api/resource:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/api/v1/pod:go_default_library",
        "//pkg/apis/apps/v1beta1:go_default_library",
        "//pkg/apis/meta/v1:go_default_library",
        "//pkg/client/cache:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/client/clientset_generated/clientset/typed/apps/v1beta1:go_default_library",
        "//pkg/client/clientset_generated/clientset/typed/core/v1:go_default_library",
        "//pkg/client/record:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/runtime:go_default_library",
        "//pkg/types:go_default_library",
        "//pkg/util/errors:go_default_library",
        "//pkg/util/runtime:go_default_library",
        "//pkg/util/sets:go_default_library",
        "//pkg/util/wait:go_default_library",
        "//pkg/util/workqueue:go_default_library",
        "//pkg/watch:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:gopkg.in/inf.v0",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "identity_mappers_test.go",
        "iterator_test.go",
        "pet_set_test.go",
        "pet_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api/testapi:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/api/v1/pod:go_default_library",
        "//pkg/apimachinery/registered:go_default_library",
        "//pkg/apis/apps/v1beta1:go_default_library",
        "//pkg/client/cache:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/client/clientset_generated/clientset/fake:go_default_library",
        "//pkg/client/clientset_generated/clientset/typed/apps/v1beta1:go_default_library",
        "//pkg/client/clientset_generated/clientset/typed/apps/v1beta1/fake:go_default_library",
        "//pkg/client/restclient:go_default_library",
        "//pkg/client/testing/core:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/runtime:go_default_library",
        "//pkg/util/errors:go_default_library",
        "//pkg/util/sets:go_default_library",
        "//pkg/util/testing:go_default_library",
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
