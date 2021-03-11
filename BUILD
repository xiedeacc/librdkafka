cc_library(
    name = "librdkafka",
    srcs = [
        "build/lib/librdkafka.a",
    ],
    hdrs = glob(["build/include/*.h"]),
    linkopts = [
        "-lpthread",
        "-ldl",
    ],
    strip_include_prefix = "build/include",
    visibility = ["//visibility:public"],
    deps = [
        "//external:ssl",
        "//external:zlib",
    ],
)

cc_library(
    name = "librdkafka++",
    srcs = ["build/lib/librdkafka++.a"],
    hdrs = glob(["build/include/*.h"]),
    strip_include_prefix = "build/include",
    visibility = ["//visibility:public"],
    deps = [":librdkafka"],
)
