# Usage
## Commands
- [`ark add`](#command-ark-add) — Stage a file for set of files for a submission.
- [`ark alias`](#command-ark-alias) — Create a shortcut for a manifest URL.
- [`ark config`]() — Update an one of Ark's Configuration Values.
- [`ark init`]() — Initialize a dataset's local configuration.
- [`ark pull`]() — Pull a file from an Arken Cluster.
- [`ark remove`]() — Remove a file from the internal submission cache.
- [`ark status`]() — view what files are currently staged for submission.
- [`ark submit`]() — Submit your files to a manifest repository.
- [`ark update`]() — Update Ark to the latest version available.
- [`ark upload`]() — Upload files to an Arken cluster after an accepted submission.

### Command: `ark add`
#### Usage
```
ark add [OPTIONS] [Paths...]
```

#### Description
Stage a file for set of files for a submission.

#### Arguments
- `[file_paths...]` - Paths to the files or directories that you would like to stage. Adding multiple files can be done at once by separating paths by a space.

#### Example
Add a couple of example files to the submission.

```bash
ark add example.csv

ark add datasets/mammals.txt

ark add . # Add everything in your current folder.
```

### Command: `ark alias`
#### Usage
```
ark alias [OPTIONS] <Shortcut> [URL...]
```

#### Description
Create or show a shortcut for a manifest URL.

#### Arguments
- `<Shortcut>` - Custom name for a manifest url.
- `[URL...]` - The URL the alias should point to.

#### Example
Add a custom alias named core to Ark for the [core-manifest](https://github.com/arken/core-manifest).

```bash
ark alias core https://github.com/arken/core-manifest

ark alias core
https://github.com/arken/core-manifes
```
