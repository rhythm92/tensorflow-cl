licenses(["restricted"])

package(default_visibility = ["//visibility:public"])

cc_toolchain_suite(
    name = "toolchain",
    toolchains = {
        "local|compiler": ":cc-compiler-local",
        "darwin|compiler": ":cc-compiler-darwin",
    },
)

cc_toolchain(
    name = "cc-compiler-local",
    all_files = ":empty",
    compiler_files = ":empty",
    cpu = "local",
    dwp_files = ":empty",
    dynamic_runtime_libs = [":empty"],
    linker_files = ":empty",
    objcopy_files = ":empty",
    static_runtime_libs = [":empty"],
    strip_files = ":empty",
    supports_param_files = 0,
)

cc_toolchain(
    name = "cc-compiler-darwin",
    all_files = ":empty",
    compiler_files = ":empty",
    cpu = "darwin",
    dwp_files = ":empty",
    dynamic_runtime_libs = [":empty"],
    linker_files = ":empty",
    objcopy_files = ":empty",
    static_runtime_libs = [":empty"],
    strip_files = ":empty",
    supports_param_files = 0,
)

filegroup(
    name = "empty",
    srcs = [],
)

cc_binary(
    name = "testcu",
    srcs = [
        'test/testcu.cu.cc',
    ],
    linkopts = [
        '-lcocl',
        '-lOpenCL',
    ],
    deps = [
        "@cocl//:cocl-headers",
        "@usr_local_lib//:libcocl",
        "@usr_lib_x8664linux//:libopencl",
    ],
    copts = [
        '-x', 'cuda',
    ],
)
