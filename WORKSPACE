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
    #tag = "v4.0.0",
    commit = "HEAD",
    #commit = "72e1c2a1ef30b3f8da039e92d4a6a1f079f374e8",
    importpath = "k8s.io/client-go",
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
    strip_prefix = "apimachinery-c3862e5c4788be03d209390fef869f2a36302b46",
    # WORKAROUND:
    # Remove proto import of "k8s.io/apimachinery/pkg/util/intstr/generated.proto" from
    #  pkg/runtime/schema/generated.proto
    #  pkg/apis/meta/v1/generated.proto
    urls = ["https://github.com/nictuku/apimachinery/archive/c3862e5c4788be03d209390fef869f2a36302b46.tar.gz"],
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

go_repository(
    name = "com_github_go_openapi_spec",
    commit = "a4fa9574c7aa73b2fc54e251eb9524d0482bb592",
    importpath = "github.com/go-openapi/spec",
)

go_repository(
    name = "com_github_juju_ratelimit",
    commit = "59fac5042749a5afb9af70e813da1dd5474f0167",
    importpath = "github.com/juju/ratelimit",
)

go_repository(
    name = "in_gopkg_inf_v0",
    commit = "3887ee99ecf07df5b447e9b00d9c0b2adaa9f3e4",
    importpath = "gopkg.in/inf.v0",
)

go_repository(
    name = "com_github_go_openapi_jsonpointer",
    commit = "779f45308c19820f1a69e9a4cd965f496e0da10f",
    importpath = "github.com/go-openapi/jsonpointer",
)

go_repository(
    name = "com_github_go_openapi_swag",
    commit = "cf0bdb963811675a4d7e74901cefc7411a1df939",
    importpath = "github.com/go-openapi/swag",
)

go_repository(
    name = "com_github_emicklei_go_restful",
    commit = "2dd44038f0b95ae693b266c5f87593b5d2fdd78d",
    importpath = "github.com/emicklei/go-restful",
)

go_repository(
    name = "com_github_spf13_pflag",
    commit = "4c012f6dcd9546820e378d0bdda4d8fc772cdfea",
    importpath = "github.com/spf13/pflag",
)

go_repository(
    name = "com_github_go_openapi_jsonreference",
    commit = "36d33bfe519efae5632669801b180bf1a245da3b",
    importpath = "github.com/go-openapi/jsonreference",
)

go_repository(
    name = "com_github_PuerkitoBio_purell",
    commit = "1c4bec281e4bbc75b4f4a1bd923bdf1bd989a969",
    importpath = "github.com/PuerkitoBio/purell",
)

go_repository(
    name = "in_gopkg_yaml_v2",
    commit = "287cf08546ab5e7e37d55a84f7ed3fd1db036de5",
    importpath = "gopkg.in/yaml.v2",
)

go_repository(
    name = "com_github_mailru_easyjson",
    commit = "32fa128f234d041f196a9f3e0fea5ac9772c08e1",
    importpath = "github.com/mailru/easyjson",
)

go_repository(
    name = "com_github_PuerkitoBio_urlesc",
    commit = "de5bf2ad457846296e2031421a34e2568e304e35",
    importpath = "github.com/PuerkitoBio/urlesc",
)

go_repository(
    name = "io_k8s_api",
    #commit = "218912509d74a117d05a718bb926d0948e531c20",
    importpath = "k8s.io/api",
    strip_prefix = "api-657c6563f026725f4421bfde2b04e7bc494dff21",
    urls = ["https://github.com/nictuku/api/archive/657c6563f026725f4421bfde2b04e7bc494dff21.tar.gz"],
)

go_repository(
    name = "com_github_gregjones_httpcache",
    commit = "2bcd89a1743fd4b373f7370ce8ddc14dfbd18229",
    importpath = "github.com/gregjones/httpcache",
)

go_repository(
    name = "com_github_peterbourgon_diskv",
    commit = "2973218375c3d13162e1d3afe1708aaee318ef3f",
    importpath = "github.com/peterbourgon/diskv",
)

go_repository(
    name = "io_k8s_apiextensions_apiserver",
    commit = "51a1910459f074162eb4e25233e461fe91e99405",
    importpath = "k8s.io/apiextensions-apiserver",
)
