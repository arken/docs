# Configuration
### `config.toml`
Ark's default configuration is located at `~/.ark/config.toml`.

```toml
[core]
  editor = "nano"

[manifest]
  path = "/home/arken-user/.ark/manifest"
  [manifest.aliases]
    core = "https://github.com/arken/core-manifest"

[git]
  name = "Arken User"
  username = "arken"
  email = "team@arken.io"
  token = "SECRET-GIT-TOKEN"
```

## core
### core.editor
By default Ark uses `nano` as its default terminal editor. To change the default to anything else you may update the file or use,

```bash
ark config core.editor emacs
```

## manifest
### manifest.path
By default Ark downloads manifests to `/home/user/.ark/manifest/`. To change the default to anything else you may update the file or use,

```bash
ark config manifest.path ~/Downloads/manifests
```

### manifest.aliases
By default Ark comes with one alias for the [core manifest](https://github.com/arken/core-manifest) setup as `core`. To add, remove or modify aliases you may use, 

```bash
ark alias core https://github.com/arken/core-manifest

ark alias core # show the value of an alias
https://github.com/arken/core-manifest

ark alias -d core # remove an existing alias
```

## git
By default Ark starts without a Git configuration and will ask for your Git details the first time you create a submission.

### git.name
Name of the user's git profile.
To manually set a git user's name you may use,

```bash
ark config git.name "Arken User"
```

### git.username
Username of user on GitHub, GitLab, etc...
To manually set a git username you may use,
```bash
ark config git.username arken
```

### git.email
Email associated with a user's account on GitHub, GitLab, etc...
To manually set a git user email you may use,
```bash
ark config git.email team@arken.io
```

### git.token
A Git Token is a personal access token used to authenticate to GitHub, GitLab, etc.... When submitting your additions to a repository on GitHub, Ark can automatically create a personal access token through GitHub's OAuth system.
To manually set a git user token you may use,
```bash
ark config git.token SECRET-TOKEN
```
