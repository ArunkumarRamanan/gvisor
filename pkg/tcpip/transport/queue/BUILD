package(licenses = ["notice"])  # Apache 2.0

load("@io_bazel_rules_go//go:def.bzl", "go_library")
load("//tools/go_stateify:defs.bzl", "go_stateify")

go_stateify(
    name = "queue_state",
    srcs = [
        "queue.go",
    ],
    out = "queue_state.go",
    package = "queue",
)

go_library(
    name = "queue",
    srcs = [
        "queue.go",
        "queue_state.go",
    ],
    importpath = "gvisor.googlesource.com/gvisor/pkg/tcpip/transport/queue",
    visibility = ["//:sandbox"],
    deps = [
        "//pkg/ilist",
        "//pkg/state",
        "//pkg/tcpip",
        "//pkg/waiter",
    ],
)
