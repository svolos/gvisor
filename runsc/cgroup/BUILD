load("//tools:defs.bzl", "go_library", "go_test")

package(licenses = ["notice"])

go_library(
    name = "cgroup",
    srcs = ["cgroup.go"],
    visibility = ["//:sandbox"],
    deps = [
        "//pkg/cleanup",
        "//pkg/log",
        "@com_github_cenkalti_backoff//:go_default_library",
        "@com_github_opencontainers_runtime_spec//specs-go:go_default_library",
    ],
)

go_test(
    name = "cgroup_test",
    size = "small",
    srcs = ["cgroup_test.go"],
    library = ":cgroup",
    tags = ["local"],
    deps = [
        "//pkg/test/testutil",
        "@com_github_opencontainers_runtime_spec//specs-go:go_default_library",
    ],
)
