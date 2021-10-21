workspace(name = "com_aliyun_ons")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_aliyun_ons_client_cpp",
    sha256 = "9277a8f7f8dfdf3f6e16f9b5858ca10e215c8f169ee77e4cb7e2c0db295a7c72",
    urls = [
        "https://ons-client-sdk.oss-cn-hangzhou.aliyuncs.com/ons-client-cpp/source/ons-client-cpp-3.0.0.tar.gz",
        "https://github.com/aliyun-mq/ons-client-cpp/archive/refs/tags/v3.0.0.tar.gz",
    ],
    strip_prefix = "ons-client-cpp-3.0.0",
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
