Repo containing for reproducing the error found in this [this comment](https://github.com/bazelbuild/rules_pkg/pull/154#pullrequestreview-402104856)

In WORKSPACE, change `/path/to/rules_pkg/` to wherever your checkout of rules_pkg is located:

```python
local_repository(
    name = "rules_pkg",
    # Change me to wherever your rules_pkg checkout is
    path = "/path/to/rules_pkg/pkg"
)
```

Then call `bazel build ...`.  Output error should look something like:

```
ERROR: error loading package '': in /home/apsaltis/.cache/bazel/_bazel_apsaltis/ca21bffe165d1853abbcdb2b62d6d44e/external/rules_pkg/experimental/rpm.bzl: Label '//experimental:pkg_filegroup.bzl' is invalid because 'experimental' is not a package; perhaps you meant to put the colon here: '//:experimental/pkg_filegroup.bzl'?
```
