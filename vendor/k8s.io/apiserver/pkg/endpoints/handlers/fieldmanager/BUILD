load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["fieldmanager.go"],
    importmap = "k8s.io/cloud-provider-gcp/vendor/k8s.io/apiserver/pkg/endpoints/handlers/fieldmanager",
    importpath = "k8s.io/apiserver/pkg/endpoints/handlers/fieldmanager",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/k8s.io/apimachinery/pkg/api/meta:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/endpoints/handlers/fieldmanager/internal:go_default_library",
        "//vendor/k8s.io/kube-openapi/pkg/util/proto:go_default_library",
        "//vendor/sigs.k8s.io/structured-merge-diff/fieldpath:go_default_library",
        "//vendor/sigs.k8s.io/structured-merge-diff/merge:go_default_library",
    ],
)
