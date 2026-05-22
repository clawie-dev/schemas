# @clawie-dev/schemas

JSON Schemas for every Clawie configuration file. The schema source-of-truth — consumed by the platform validator (spec 018), IDE editors, CI pipelines, and third-party tooling.

## Schemas

| Schema | Spec | Description |
|---|---|---|
| `clawie.yaml` | 001 | Root platform config |
| `team.yaml` | 013 | Team identity, roles, charter |
| `flows.yaml` | 013, 016 | Pipeline stage flows + messaging rules |
| `budgets.yaml` | 007 | Budget caps per scope |
| `task-management.yaml` | 026 | External driver + status-flow rules |
| `agent/SOUL.md` frontmatter | 008 | Agent identity meta |
| `agent/AGENTS.md` frontmatter | 008 | Agent role + behavior |
| `agent/TOOLS.md` | 008 | Declared tools + permission requests |
| `agent/MODEL.yaml` | 008, 011 | Provider/model preferences + fallback |
| Plugin `manifest.yaml` | 010 | Skill/driver/connector manifest |
| Eval `fixture.yaml` | 019 | Benchmark fixture definition |
| Policy rule format | 003 | Permission rules |
| Outcall ruleset | 002 | Egress rules (mirrors Outcall's own schema) |

## Publishing

```bash
# Published to npm
npm install --save-dev @clawie-dev/schemas

# Used in VS Code via redhat.vscode-yaml extension
# yaml.schemas in settings.json maps file globs → schema URLs
```

## Versioning

SemVer. Breaking schema changes increment major; new optional fields increment minor; clarifications/fixes increment patch.

## Status

Bootstrap pending. Tracked in [`clawie-dev/specs/speckit/018-config-validation-pre-merge`](https://github.com/clawie-dev/specs/tree/main/speckit/018-config-validation-pre-merge).

## License

MIT — see [LICENSE](LICENSE).
