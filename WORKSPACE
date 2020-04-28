load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

local_repository(
    name = "rules_pkg",
    # Change me to wherever your rules_pkg checkout is
    path = "/path/to/rules_pkg/pkg"
)

load("@rules_pkg//:deps.bzl", "rules_pkg_dependencies")

rules_pkg_dependencies()

load("@bazel_skylib//:workspace.bzl", "bazel_skylib_workspace")

bazel_skylib_workspace()
