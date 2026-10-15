# ApexAiOfficial fork of anthropics/claude-plugins-official

This fork is the ApexAI workstation's authoritative source for the components it
uses from [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official). Architecture, provenance and runbooks:
ApexAiOfficial/agent-skills-platform (private).

## Branches

| Branch | Meaning | Who moves it |
|---|---|---|
| `main` | Untouched mirror of upstream `main`. Never commit here. | `scripts/upstream-sync` (fast-forward only) |
| `apex/dev` | ApexAI changes on top of upstream. Upstream is merged in here first. | ApexAI maintainers |
| `apex/stable` | Reviewed, known-good revision that runtimes pin to. | `scripts/promote` (fast-forward + `apex-stable-*` tag) |

## ApexAI changes

Marketplace renamed so Claude Code / Codex accept it from a non-upstream source
(upstream names are reserved for the upstream organisation):

| Manifest | Upstream name | ApexAI name |
|---|---|---|
| `.claude-plugin/marketplace.json` | `claude-plugins-official` | `apex-claude-plugins` |

Plugin and skill names are unchanged. Each component keeps its own upstream license
and terms; see the component's LICENSE file.
