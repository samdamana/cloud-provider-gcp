load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "elements.go",
        "fromvalue.go",
        "schemaschema.go",
    ],
    importmap = "k8s.io/cloud-provider-gcp/vendor/sigs.k8s.io/structured-merge-diff/schema",
    importpath = "sigs.k8s.io/structured-merge-diff/schema",
    visibility = ["//visibility:public"],
    deps = ["//vendor/sigs.k8s.io/structured-merge-diff/value:go_default_library"],
)
