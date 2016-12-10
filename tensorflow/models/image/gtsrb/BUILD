# Description:
# Example TensorFlow models for GTSRB

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

py_library(
    name = "gtsrb_input",
    srcs = ["gtsrb_input.py"],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:internal"],
    deps = [
        "//tensorflow:tensorflow_py",
    ],
)

py_test(
    name = "gtsrb_input_test",
    size = "small",
    srcs = ["gtsrb_input_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":gtsrb_input",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_library(
    name = "gtsrb",
    srcs = ["gtsrb.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":gtsrb_input",
        "//tensorflow:tensorflow_py",
    ],
)

py_binary(
    name = "gtsrb_eval",
    srcs = [
        "gtsrb_eval.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        ":gtsrb",
    ],
)

py_binary(
    name = "gtsrb_train",
    srcs = [
        "gtsrb_train.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        ":gtsrb",
    ],
)

py_binary(
    name = "gtsrb_multi_gpu_train",
    srcs = [
        "gtsrb_multi_gpu_train.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        ":gtsrb",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(
        ["**/*"],
        exclude = [
            "**/METADATA",
            "**/OWNERS",
        ],
    ),
    visibility = ["//tensorflow:__subpackages__"],
)
