# k8s-bazel-go-example

This is a very simple Go client for kubernetes that uses [Bazel](https://bazel.build) for builds.

It exists to:

- *be a reliable reference* of a combination of repository versions that we know works for building docker Go clients
- *show it can be done*. Libraries don't have BUILD.bazel files but they don't need to because bazel's `go_repository` understands how to build most Go projects.
- easily reproduce various problems that make k8s.io/client-go unbuildable with Bazel. See the Issues for details.

## WORKSPACE
Normally Bazel-friendly repositories wouldn't shipt their own WORKSPACE files, but in this case we're intentionally making it self-contained. You may want to use it as a reference for your own WORKSPACE.

## How to build

1. Install [Bazel.build](https://bazel.build)
2. Run `$ bazel build :moby-bazel-go-example`

The first build will take a very long time because all remote dependencies have to be fetched and build. But repeated builds should be very fast.

## This is going to get stale over time
PRs for updating the repository commits to known-working are welcomed.

# See also

 - https://github.com/bazelbuild/rules_go/issues/1063
