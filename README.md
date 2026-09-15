# Developer Arsenal

A practical developer encyclopedia and quick-reference manual for everyday development tools.

**Find the command. Understand the parts. Get back to building.**

Developer Arsenal is a personal documentation project: a single Markdown manual
for learning and recalling terminal, HTML, Python, Git/GitHub, Nano and Fish workflows.
It combines short lookups with explanations, diagrams and small examples.

## Choose your mode

| When you need… | Start here |
| --- | --- |
| A command you almost remember | [⚡ Quick Mode](ARSENAL.md#quick-mode) |
| The reason a command works | [🎓 Learning Mode](ARSENAL.md#learning-mode) |
| A specific tool or topic | [🗺️ Map](ARSENAL.md#map) |
| Upstream behavior and caveats | [References](ARSENAL.md#references) |

For example, [Quick Mode's staging reference](ARSENAL.md#quick-git-staging)
shows what `git add` selects. [Learning Mode](ARSENAL.md#learning-git-staging-changes)
explains why staging is separate from committing and publishing.

## What's inside

- **Terminal:** navigation, files, pattern search, command lookup, browser launch,
  pipes, redirection, terminal shortcuts and Wayland clipboard commands.
- **HTML:** [document structure, metadata and linking CSS](ARSENAL.md#learning-html),
  with a small page to read and try.
- **Python:** running a script and checking syntax, including what compilation does not test.
- **Git & GitHub:** local history, staging, identity, remotes, authentication and a branch-to-PR workflow.
- **Nano:** traditional editing shortcuts and version/configuration caveats.
- **Fish:** command lookup, function inspection, session state and persistence with `funcsave`.
- **Utilities:** inspecting tabs and reviewing a conversion before changing source files.

## How to use it

Open [ARSENAL.md](ARSENAL.md) directly on GitHub or in a Markdown viewer. No build,
service, account or package installation is needed to read it.

Examples target **Linux with GNU utilities**, with CachyOS/Arch as the local review
environment. Shared shell examples are intended for Bash and current Fish;
Fish functions and the Bash-only conversion block are labeled. Python examples
use Python 3; on systems where `python` is unavailable, check whether `python3`
is the intended interpreter. Clipboard commands require `wl-clipboard` and Wayland.

Commands are independent examples, not an installation script. Placeholder names
need replacing. Read the effects before copying: deletion, output redirection,
Git publishing and saved Fish functions can change files, remote history or configuration.
Practice on disposable files, never credentials or important working data.

## Project approach

The project turns everyday development questions into two useful reading paths:
fast recall and step-by-step understanding. The work here is technical writing,
information organization and careful explanation of command behavior.

It is a personal learning and portfolio project, not client work or an application.
Its scope is deliberately selective: it is not a complete Linux course, an official
manual, or proof that every example works on every platform.

Technical accuracy comes first. Humor comes second. Pedro remains under investigation.

## Repository guide

| File | Purpose |
| --- | --- |
| [ARSENAL.md](ARSENAL.md) | The manual, with linked modes, topics and references |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to review or add an entry without losing the two-mode structure |
| [docs/REVIEW.md](docs/REVIEW.md) | Dated audit, verification evidence and remaining limitations |
| [LICENSE](LICENSE) | MIT license, copyright 2026 Manu Fernández |

## Review and maintenance

The [2026-09-11 review](docs/REVIEW.md) covers the repository's original four files
and its three existing commits. Representative examples were checked in disposable
local environments; interactive tools and external publishing have separate limits
recorded there. Those checks are not a promise of universal compatibility.

To report an error, [open an issue](https://github.com/manufernandez-programmer/developer-arsenal/issues)
with the section, tool/shell version and a minimal example without secrets.
For edits, follow the [contribution guide](CONTRIBUTING.md) and submit a PR.

## License

[MIT](LICENSE). Keep the copyright and permission notice when reusing the material.
External references remain under their respective terms.
