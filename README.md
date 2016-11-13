# gomono

Prototypes of tools for dealing with monolithic golang repos.

**Caution: rough draft**

## Vendoring code via Git Hooks

These hooks are meant to address vendoring repos that were retrieved via `go get`.

The git hooks in this repo can be put into the `.git/hooks` directory of a git repo in which an entire Golang workspace is stored (client-side).
They assume that the GOPATH has been set to `<repo-root>/go`.
The hooks will find all nested `.git` directories in the pre-commit hook and move these directories to `.gitvendor`.
They will also remove any `.git/objects/*` from the nested git repositories before committing them.
