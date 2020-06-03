licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

py_library(
    name = "layers",
    srcs = glob(["*.py"]),
    data = [
        "//tensorflow_addons/custom_ops/layers:_correlation_cost_ops.so",
        "//tensorflow_addons/custom_ops/layers:_deformable_conv2d_ops.so",
    ],
    deps = [
        "//tensorflow_addons/activations",
        "//tensorflow_addons/rnn",
        "//tensorflow_addons/testing",
        "//tensorflow_addons/utils",
    ],
)

py_test(
    name = "layers_test",
    size = "small",
    srcs = glob(["tests/*"]),
    main = "tests/run_all_test.py",
    deps = [
        ":layers",
    ],
)

py_test(
    name = "deformable_conv_test",
    size = "small",
    srcs = [
        "deformable_conv2d_test.py",
    ],
    main = "deformable_conv2d_test.py",
    deps = [
        ":layers",
    ],
)

py_test(
    name = "equi_conv_test",
    size = "small",
    srcs = [
        "equi_conv_test.py",
    ],
    main = "equi_conv_test.py",
    deps = [
        ":layers",
    ],
)
