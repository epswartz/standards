# Project Structure
In general, I prefer projects to be built using bazel, and a Makefile.

Bazel handles all of the actual build system, and the Makefile provides standard make targets that make it ergonomic for me to interact with multiple projects.

Those Makefile targets are:
- build: build a binary but do not run it. If the project involves more than one, disambiguate with hyphens, i.e. build-ui or build-server.
- dev: build, then run a local development server. Similarly disambiguated with hyphens.
- test: runs all unit tests for the project.
- e2e: standard name for integration test make target, though those are usually omitted from the first draft of a project.
