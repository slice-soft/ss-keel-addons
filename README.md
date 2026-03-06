<img src="https://cdn.slicesoft.dev/boat.svg" width="400" />

# Keel Addons

[![Registry](https://img.shields.io/badge/Registry-ss--keel--addons-0A7F5A)](https://github.com/slice-soft/ss-keel-addons)
[![GitHub stars](https://img.shields.io/github/stars/slice-soft/ss-keel-addons?style=social)](https://github.com/slice-soft/ss-keel-addons)
[![GitHub contributors](https://img.shields.io/github/contributors/slice-soft/ss-keel-addons)](https://github.com/slice-soft/ss-keel-addons/graphs/contributors)
![License](https://img.shields.io/badge/License-MIT-green)
![Made in Colombia](https://img.shields.io/badge/Made%20in-Colombia-FCD116?labelColor=003893)

`ss-keel-addons` is the public alias registry used by the Keel CLI.

When a developer runs `keel add <alias>`, the CLI resolves that alias through this repository and then installs the addon from its source repository.

## What lives in this repository

This repository stores addon metadata only. It does not contain addon implementation code.

Each addon entry in `registry.json` includes:

- `alias`
- `repo`
- `description`
- `source`
- `tags`

## Registry format

`registry.json`:

```json
{
  "version": "1",
  "addons": [
    {
      "alias": "gorm",
      "repo": "github.com/slice-soft/ss-keel-gorm",
      "description": "SQL via GORM — Postgres, MySQL, SQLite, SQL Server",
      "source": "slice-soft",
      "tags": ["sql", "gorm", "postgres", "mysql", "sqlite", "sqlserver"]
    }
  ]
}
```

Field notes:

- `alias`: Unique short name used with `keel add <alias>`.
- `repo`: Public repository/module path where the addon lives.
- `description`: Short summary of the addon.
- `source`: Ownership/source label (for example `slice-soft`, `community`, or a company/org label).
- `tags`: Searchable keywords for discovery.

## `keel add` flow

1. Run `keel add gorm`.
2. The CLI checks this registry for alias `gorm`.
3. The CLI resolves the mapped `repo`.
4. The CLI downloads the addon from that repository.
5. The CLI validates and executes the addon's own integration contract.

## Add or update an alias

1. Fork this repository.
2. Edit `registry.json` with the addon metadata (`alias`, `repo`, `description`, `source`, `tags`).
3. Open a PR in this repository.
4. Include links to your addon repository (and docs/tests evidence in the PR description).
5. Optionally open a docs PR in `ss-keel-docs` and link it.
6. Share the PR in Discord for community/maintainer review.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the complete repository-specific process.

## Contributing

The base workflow, commit conventions, and community standards live in [ss-community](https://github.com/slice-soft/ss-community/blob/main/CONTRIBUTING.md).

## Community

| Document | |
|---|---|
| [CONTRIBUTING.md](https://github.com/slice-soft/ss-community/blob/main/CONTRIBUTING.md) | Workflow, commit conventions, and PR guidelines |
| [GOVERNANCE.md](https://github.com/slice-soft/ss-community/blob/main/GOVERNANCE.md) | Decision-making, roles, and release process |
| [CODE_OF_CONDUCT.md](https://github.com/slice-soft/ss-community/blob/main/CODE_OF_CONDUCT.md) | Community standards |
| [VERSIONING.md](https://github.com/slice-soft/ss-community/blob/main/VERSIONING.md) | SemVer policy and breaking changes |
| [SECURITY.md](https://github.com/slice-soft/ss-community/blob/main/SECURITY.md) | How to report vulnerabilities |
| [MAINTAINERS.md](https://github.com/slice-soft/ss-community/blob/main/MAINTAINERS.md) | Active maintainers |

## License

MIT License - see [LICENSE](LICENSE) for details.

## Links

- Website: [keel-go.dev](https://keel-go.dev)
- GitHub: [github.com/slice-soft/ss-keel-cli](https://github.com/slice-soft/ss-keel-cli)
- Documentation: [docs.keel-go.dev](https://docs.keel-go.dev)

---

Made by [SliceSoft](https://slicesoft.dev) - Colombia
