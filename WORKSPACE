workspace(name = "com_aliyun_ons")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_aliyun_ons_client_cpp",
    #sha256 = "44ff76803dff9b5db0f2af74596382b03ff058f31f0676d0772b8b43e8c5606d",
    urls = [
        "https://github.com/aliyun-mq/ons-client-cpp/archive/refs/tags/v1.0-alpha5.tar.gz",
    ],
    strip_prefix = "ons-client-cpp-1.0-alpha5",
)

load("@com_aliyun_ons_client_cpp//bazel:deps.bzl", "ons_deps")
ons_deps()

load("@org_apache_rocketmq//bazel:rocketmq_deps.bzl", "rocketmq_deps")
rocketmq_deps()

load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps", "grpc_test_only_deps")
grpc_deps()
grpc_test_only_deps()
load("@com_github_grpc_grpc//bazel:grpc_extra_deps.bzl", "grpc_extra_deps")
grpc_extra_deps()


load("@rules_proto_grpc//:repositories.bzl", "rules_proto_grpc_toolchains", "rules_proto_grpc_repos")
rules_proto_grpc_toolchains()
rules_proto_grpc_repos()

load("@rules_proto//proto:repositories.bzl", "rules_proto_dependencies", "rules_proto_toolchains")
rules_proto_dependencies()
rules_proto_toolchains()
