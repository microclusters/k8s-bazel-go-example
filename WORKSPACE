http_archive(
    name = "io_bazel_rules_go",
    sha256 = "91fca9cf860a1476abdc185a5f675b641b60d3acf0596679a27b580af60bf19c",
    url = "https://github.com/bazelbuild/rules_go/releases/download/0.7.0/rules_go-0.7.0.tar.gz",
)

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_register_toolchains",
    "go_rules_dependencies",
    "go_repository",
)

go_rules_dependencies()

go_register_toolchains()

load(
    "@io_bazel_rules_go//proto:def.bzl",
    "proto_register_toolchains",
)

proto_register_toolchains()

go_repository(
    name = "io_k8s_client_go",
    #commit = "72e1c2a1ef30b3f8da039e92d4a6a1f079f374e8",
    importpath = "k8s.io/client-go",
    tag = "v4.0.0",
)

# WORKAROUND:
# Specific external repo name needed by io_k8s_client_go.
http_archive(
    name = "io_kubernetes_build",
    sha256 = "89788eb30f10258ae0c6ab8b8625a28cb4c101fba93a8a6725ba227bb778ff27",
    strip_prefix = "repo-infra-653485c1a6d554513266d55683da451bd41f7d65",
    urls = ["https://github.com/kubernetes/repo-infra/archive/653485c1a6d554513266d55683da451bd41f7d65.tar.gz"],
)

go_repository(
    name = "io_k8s_apimachinery",
    importpath = "k8s.io/apimachinery",
    strip_prefix = "apimachinery-d2536e3e90fd52c9ebc06c63c8ee44c2d2ef16fd",
    # WORKAROUND:
    # Remove proto import of "k8s.io/apimachinery/pkg/util/intstr/generated.proto" from
    #  pkg/runtime/schema/generated.proto
    urls = ["https://github.com/nictuku/apimachinery/archive/d2536e3e90fd52c9ebc06c63c8ee44c2d2ef16fd.tar.gz"],
)

go_repository(
    name = "io_k8s_kube_openapi",
    commit = "39a7bf85c140f972372c2a0d1ee40adbf0c8bfe1",
    importpath = "k8s.io/kube-openapi",
)

go_repository(
    name = "com_github_google_gofuzz",
    commit = "24818f796faf91cd76ec7bddd72458fbced7a6c1",
    importpath = "github.com/google/gofuzz",
)

go_repository(
    name = "com_github_go_openapi_spec",
    commit = "a4fa9574c7aa73b2fc54e251eb9524d0482bb592",
    importpath = "github.com/go-openapi/spec",
)
