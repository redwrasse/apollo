load("@rules_cc//cc:defs.bzl", "cc_library", "cc_test")
load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "util",
    srcs = ["util.cc"],
    hdrs = ["util.h"],
    deps = [
        "//cyber/common:log",
        "//cyber/common:types",
        "//modules/common/configs:config_gflags",
        "//modules/common/math",
        "//modules/common/math:geometry",
        "//modules/common/proto:geometry_cc_proto",
        "//modules/common/proto:pnc_point_cc_proto",
    ],
)

cc_library(
    name = "future",
    hdrs = ["future.h"],
    deps = [
        "@com_google_absl//absl/memory",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/types:optional",
        "@com_google_absl//absl/utility",
    ],
)

cc_library(
    name = "point_factory",
    hdrs = ["point_factory.h"],
    deps = [
        "//modules/common/math:geometry",
        "//modules/common/proto:pnc_point_cc_proto",
    ],
)

cc_test(
    name = "util_test",
    size = "small",
    srcs = ["util_test.cc"],
    deps = [
        ":util",
        "//modules/common/util/testdata:simple_cc_proto",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_library(
    name = "lru_cache",
    hdrs = ["lru_cache.h"],
)

cc_library(
    name = "color",
    hdrs = ["color.h"],
)

cc_library(
    name = "string_util",
    srcs = ["string_util.cc"],
    hdrs = ["string_util.h"],
    deps = [
        ":future",
        "@com_google_absl//absl/strings:str_format",
    ],
)

cc_library(
    name = "message_util",
    hdrs = ["message_util.h"],
    deps = [
        "//cyber/common:file",
        "//cyber/time:clock",
        "@com_google_absl//absl/strings",
        "@com_google_protobuf//:protobuf",
    ],
)

cc_test(
    name = "message_util_test",
    size = "small",
    srcs = ["message_util_test.cc"],
    tags = [
        "external",
    ],
    deps = [
        ":message_util",
        "//modules/common/util/testdata:simple_cc_proto",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_test(
    name = "string_util_test",
    size = "small",
    srcs = ["string_util_test.cc"],
    deps = [
        ":string_util",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_library(
    name = "time_util",
    hdrs = ["time_util.h"],
    deps = [
        "//cyber/common:macros",
    ],
)

cc_test(
    name = "time_util_test",
    size = "small",
    srcs = ["time_util_test.cc"],
    deps = [
        ":time_util",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_library(
    name = "map_util",
    hdrs = ["map_util.h"],
    deps = [
        "@com_google_protobuf//:protobuf",
    ],
)

cc_library(
    name = "factory",
    hdrs = ["factory.h"],
    deps = [
        "//cyber/common",
    ],
)

cc_test(
    name = "factory_test",
    size = "small",
    srcs = ["factory_test.cc"],
    deps = [
        ":factory",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_test(
    name = "lru_cache_test",
    size = "small",
    srcs = ["lru_cache_test.cc"],
    deps = [
        "//modules/common/util:lru_cache",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_library(
    name = "points_downsampler",
    hdrs = ["points_downsampler.h"],
    deps = [
        "//cyber/common",
        "//modules/common/math:geometry",
    ],
)

cc_test(
    name = "points_downsampler_test",
    size = "small",
    srcs = ["points_downsampler_test.cc"],
    deps = [
        ":points_downsampler",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_library(
    name = "json_util",
    srcs = ["json_util.cc"],
    hdrs = ["json_util.h"],
    deps = [
        "//cyber/common",
        "@com_github_nlohmann_json//:json",
        "@com_google_protobuf//:protobuf",
    ],
)

cc_test(
    name = "json_util_test",
    size = "small",
    srcs = ["json_util_test.cc"],
    deps = [
        ":json_util",
        "//modules/common/proto:error_code_cc_proto",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_library(
    name = "eigen_defs",
    hdrs = ["eigen_defs.h"],
    deps = ["@eigen"],
)

cc_library(
    name = "perf_util",
    srcs = ["perf_util.cc"],
    hdrs = ["perf_util.h"],
    deps = [
        "//cyber/common:log",
        "//cyber/common:macros",
        "//cyber/time",
        "@com_google_absl//absl/strings",
    ],
)

cc_test(
    name = "perf_util_test",
    size = "small",
    srcs = ["perf_util_test.cc"],
    deps = [
        ":perf_util",
        "@com_google_googletest//:gtest_main",
    ],
)

cpplint()
