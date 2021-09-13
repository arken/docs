# Configuration
Arken can be configured either by its `config.toml` file or by environment variables on the system.

## (Option 1) `config.toml`
By default Arken looks for its [TOML](https://toml.io/en/) configuration file at `~/.arken/config.toml`. However, you can point Arken at a custom config location by using the `-c /path/to/config` flag when starting the daemon.

```toml
[database]
  path = "/home/user/.arken/arken.db"

[storage]
  limit = "50GB"
  path = "/home/user/.arken/storage"

[manifest]
  url = "https://github.com/arken/core-manifest"
  path = "/home/user/.arken/manifest"

[network]
  limit = "2TB"

[stats]
  enabled = "true"
  email = "user@example.com"
```

## (Option 2) Environment Variables
Arken can also be configured by system environment variables. Arken environment variables are generated in the form of `ARKEN_CATEGORY_KEY = VALUE`. For example to update the location of Arken's internal SQLite database you would use `ARKEN_DATABASE_PATH = /new/path/to/database.db`. 

#### List of Known Environment Variables
```plain
ARKEN_DATABASE_PATH

ARKEN_STORAGE_LIMIT
ARKEN_STORAGE_PATH

ARKEN_MANIFEST_URL
ARKEN_MANIFEST_PATH

ARKEN_NETWORK_LIMIT

ARKEN_STATS_ENABLED
ARKEN_STATS_EMAIL
```
