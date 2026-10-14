# Project Structure
In general, I prefer projects to be built using make.

Per-language tools handle all of the actual build system, and the Makefile provides standard make targets that make it ergonomic for me to interact with multiple projects.

Those Makefile targets are:
- build: build a binary but do not run it. If the project involves more than one, disambiguate with hyphens, i.e. build-ui or build-server.
- dev: build, then run a local development server. Similarly disambiguated with hyphens. Not included for projects that don't run a server.
- test: runs all unit tests for the project.
- e2e: standard name for integration test make target, though those are usually omitted from the first draft of a project.


### The Minimal Project
The minimal project setup includes minimal make targets to build the code, and the code itself. Does not need to include tests and e2e out of the box.
