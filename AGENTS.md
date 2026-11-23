# Steps for supporting a new version of pyo3-ffi-nolink

- Create a new branch corresponding to the new version (e.g. `0.30.1`)
- Find the download link for a zip archive from crates.io page, e.g. `https://crates.io/crates/pyo3-ffi/0.30.1`.
- Replace the content of the repo, aside from this AGENTS.md file, with what is in the archive.
- Remove the `links = "python"` line from `Cargo.toml`. This is the only intended change from the upstream archive.
- New files under src can be git-add'ed.
- By default, do not git-add new top-level files without confirming with the user.
  - `meson.build` and `Cargo.toml.orig` can be ignored.
- Make a commit to the new branch, and push it to remote with user's confirmation (e.g. to `origin/0.30.1`)
- Push a new tag corresponding to the version with `v` prefix, e.g. `v0.30.1` to the remote with user's confirmation.


