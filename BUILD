package(default_visibility = ["//visibility:public"])

cc_library(
    name = "crow_headers",
    hdrs = glob([
        "include/crow/*.h",
    ]) + glob(["include/crow/*.hpp"]),
    linkopts = [
        "-lpthread",
    ],
    strip_include_prefix = "include",
    deps = [
        "@boost//:algorithm",
        "@boost//:asio_ssl",
        "@boost//:optional",
    ],
)

cc_library(
    name = "crow",
    srcs = ["include/crow.h"],
    hdrs = ["include/crow.h"],
    linkopts = [
        "-lpthread",
    ],
    strip_include_prefix = "include",
    deps = [
        ":crow_headers",
        "@boost//:algorithm",
        "@boost//:asio_ssl",
        "@boost//:optional",
    ],
)
