load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "alt_token_source.go",
        "cache.go",
        "main.go",
        "request.go",
        "tpm.go",
    ],
    importpath = "k8s.io/cloud-provider-gcp/cmd/gke-exec-auth-plugin",
    visibility = ["//visibility:private"],
    deps = [
        "//pkg/nodeidentity:go_default_library",
        "//pkg/tpmattest:go_default_library",
        "//vendor/cloud.google.com/go/compute/metadata:go_default_library",
        "//vendor/github.com/gofrs/flock:go_default_library",
        "//vendor/github.com/google/go-tpm/tpm2:go_default_library",
        "//vendor/github.com/google/go-tpm/tpmutil:go_default_library",
        "//vendor/golang.org/x/oauth2:go_default_library",
        "//vendor/golang.org/x/oauth2/google:go_default_library",
        "//vendor/google.golang.org/api/googleapi:go_default_library",
        "//vendor/k8s.io/api/certificates/v1beta1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/serializer:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/typed/certificates/v1beta1:go_default_library",
        "//vendor/k8s.io/client-go/pkg/apis/clientauthentication:go_default_library",
        "//vendor/k8s.io/client-go/pkg/apis/clientauthentication/v1alpha1:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/client-go/util/cert:go_default_library",
        "//vendor/k8s.io/client-go/util/certificate/csr:go_default_library",
        "//vendor/k8s.io/client-go/util/keyutil:go_default_library",
        "//vendor/k8s.io/klog:go_default_library",
    ],
)

go_binary(
    name = "gke-exec-auth-plugin",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = [
        "cache_test.go",
        "request_test.go",
        "tpm_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "//pkg/nodeidentity:go_default_library",
        "//vendor/github.com/google/go-tpm/tpm2:go_default_library",
        "//vendor/github.com/google/go-tpm/tpmutil:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
    ],
)
