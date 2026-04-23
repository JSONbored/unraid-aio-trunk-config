# unraid-aio-trunk-config

Shared Trunk configuration for the Unraid AIO fleet.

## Usage

Add this repo to a consumer repository's `.trunk/trunk.yaml`:

```yaml
version: 0.1
cli:
  version: 1.25.0
plugins:
  sources:
    - id: trunk
      uri: https://github.com/trunk-io/plugins
      ref: v1.7.6
    - id: unraid-aio
      uri: https://github.com/JSONbored/unraid-aio-trunk-config
      ref: v0.1.0
```

Repo-local `.trunk/trunk.yaml` files should keep only:
- `version`
- `cli.version`
- `plugins.sources`
- any true repo-specific overrides

## Updating

Update the shared plugin repo first, then tag a new release. Consumer repos can
pin the new tag when they are ready to adopt it.
Shared Trunk configuration for the Unraid AIO fleet
