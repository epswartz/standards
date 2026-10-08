# Preferred Technology Stack

## Developer Tools
- Version control: Git, github
- Editor: vscode, hosted as a webserver on WSL.
- Languages: Python, Golang, Node, C++ (for embedded systems only, Go for general backend systems)
- Build system: bazel
- CICD: github actions that invoke bazel
- Releasing: github release tags, with built binaries attached.

## Deployment Architecture
- Relational DB: Postgres, typically deployed myself on a GCE VM because it's cheaper than cloud SQL.
- Blob store: GCS
- Other databases: Ask me as needed. I don't build much that needs them.
- Prod compute architecture: generally uses systemd to call the outputs of a bazel build. Actual underlying infrastructure varies a lot.
