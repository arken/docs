# Usage
## Commands
- [`ark add`](#command-ark-add) — Stage a file for set of files for a submission.
- [`ark alias`](#command-ark-alias) — Create a shortcut for a manifest URL.
- [`ark config`](#command-ark-config) — Update an one of Ark's Configuration Values.
- [`ark init`](#command-ark-init) — Initialize a dataset's local configuration.
- [`ark pull`](#command-ark-pull) — Pull a file from an Arken Cluster.
- [`ark remove`](#command-ark-remove) — Remove a file from the internal submission cache.
- [`ark status`](#command-ark-status) — view what files are currently staged for submission.
- [`ark submit`](#command-ark-submit) — Submit your files to a manifest repository.
- [`ark update`](#command-ark-update) — Update Ark to the latest version available.
- [`ark upload`](#command-ark-upload) — Upload files to an Arken cluster after an accepted submission.

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
https://github.com/arken/core-manifest
```

### Command: `ark config`
#### Usage
```
USAGE: ark config [OPTIONS] <Key> [Value...]
```

#### Description
Update an one of Ark's Configuration Values.

#### Arguments
- `<Key>` - Name of a configuration value such as git.username.
- `[Value...]` - Corresponding  

#### Example
Change your name for git submissions.

```bash
ark config git.name "Bilbo Baggins"

ark config git.name
Bilbo Baggins
```

### Command: `ark init`
#### Usage
```
USAGE: ark init
```

#### Description
Initialize a dataset's local configuration.

#### Example
Initialize an Ark submission at the current working directory.

```bash
ark init
```

### Command: `ark pull`
#### Usage
```
USAGE: ark pull [OPTIONS] <Manifest> [Filepaths...]
```

#### Description
Pull a file from an Arken Cluster.

#### Arguments
- `<Manifest>` - Alias or URL of manifest to pull data from.
- `[Filepaths...]` - Path to the file(s) within Arken.

#### Example
Pull an image from the Deaver botanical collection.

```bash
ark pull core deaver/ASC00001234.jpg
[-] Pulling ASC00001234.jpg...
```

### Command: `ark remove`
#### Usage
```
USAGE: ark remove [OPTIONS] [Paths...]
```

#### Description
Remove a file from the internal submission cache.

#### Arguments
- `[Paths...]` - Path to the file(s) you would like to remove from the submission.

#### Example
Remove a test.csv file from a submission

```bash
ark remove tests/test.csv
```

### Command: `ark status`
#### Usage
```
ark status [OPTIONS]
```

#### Description
View what files are currently staged for submission.

#### Example
Check the number of files in a submission.

```bash
ark status
1 file(s) currently staged for submission
	 tests/test.csv

```

### Command: `ark submit`
#### Usage
```
USAGE: ark submit [OPTIONS] <Manifest>
```

#### Description
Create and upload a submission to an Arken manifest.

#### Arguments
- `<Manifest>` - Alias or URL of a manifest git repository.

#### Example
Submit `tests/test.csv` to the Core Arken Cluster.

```bash
ark submit https://github.com/arken/core-manifest

ark submit core
```

### Command: `ark update`
#### Usage
```
USAGE: ark update [OPTIONS]
```

#### Description
Update Ark to the latest version available.

#### Flags
- `-y, --yes` - If a newer version is found update without prompting the user.

#### Example
Check for an update to Arken

```bash
ark update

Current Version: v0.2.1
Latest Version: v0.2.1
Already Up-To-Date!

```

### Command: `ark upload`
#### Usage
```
USAGE: ark upload [OPTIONS] <Manifest>
```

#### Description
Upload files to an Arken cluster after an accepted submission.

#### Arguments
- `<Manifest>` - Alias or URL of a manifest git repository.

#### Example
Upload `tests/test.csv` to the Core Arken Cluster.

```bash
ark upload https://github.com/arken/core-manifest
Uploading Files to Cluster
   0% |                              | (0/1, 0 it/min) [1s:-1s]
```
```bash
ark upload core
Uploading Files to Cluster
   0% |                              | (0/1, 0 it/min) [1s:-1s]
```
