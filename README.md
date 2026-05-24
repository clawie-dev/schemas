# @clawie-dev/schemas

Planned JSON Schema source-of-truth for every Clawie configuration file.
Consumed by the platform validator ([spec 018](https://github.com/clawie-dev/specs/tree/main/speckit/018-config-validation-pre-merge)),
IDE editors, CI pipelines, and third-party tooling.

> **Status:** Pending. The repo currently contains only README + LICENSE;
> no JSON Schema files have been authored yet. The package is not published
> to npm. Bootstrap lands when spec 018 enters delivery.

## Planned schemas

| Schema | Spec | Description |
|---|---|---|
| `clawie.yaml` | 001 | Root platform config |
| `team.yaml` | 013 | Team identity, roles, charter |
| `flows.yaml` | 013, 016 | Pipeline stage flows + messaging rules |
| `budgets.yaml` | 007 | Budget caps per scope |
| `task-management.yaml` | 026 | External driver + status-flow rules |
| `agent/SOUL.md` frontmatter | 008 | Agent identity meta |
| `agent/AGENTS.yaml` | 008 | Agent role + behavior |
| `agent/TOOLS.yaml` | 008 | Declared tools + permission requests |
| `agent/MODEL.yaml` | 008, 011 | Provider/model preferences + fallback |
| Plugin `manifest.yaml` | 010 | Skill/driver/connector manifest |
| Eval `fixture.yaml` | 019 | Benchmark fixture definition |
| Policy rule format | 003 | Permission rules |
| Outcall ruleset | 002 | Egress rules (mirrors Outcall's own schema) |

The agent file extensions (`AGENTS.yaml`, `TOOLS.yaml` — not `.md`) match
what `node ace agents:load` already reads from disk in Clawie's v1.0
agent loader.

## Planned install (once published)

```bash
npm install --save-dev @clawie-dev/schemas
```

Once shipped, IDE integration via the [redhat.vscode-yaml](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
extension will map file globs → schema URLs in `yaml.schemas`.

## Versioning

SemVer. Breaking schema changes increment major; new optional fields
increment minor; clarifications/fixes increment patch.

## License

MIT — see [LICENSE](LICENSE).
