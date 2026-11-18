## Code signing policy

Free code signing provided by [SignPath.io](https://about.signpath.io), certificate by [SignPath Foundation](https://signpath.org/).

### Team roles

- Committers and reviewers: [Repository collaborators](https://github.com/ga00y/Pake/settings/access)
- Approvers (code signing): [ga00y](https://github.com/ga00y)

### Binaries we sign with this policy

| Application           | Publisher                                                        |
| --------------------- | ---------------------------------------------------------------- |
| `MarkdownEditor.exe`  | Free code signing provided by SignPath.io, certificate by SignPath Foundation |

`MarkdownEditor.exe` is built by this repository's GitHub Actions workflow
(`.github/workflows/build-and-sign-windows-signpath.yml`) on a GitHub-hosted
`windows-latest` runner, from the source in this repository (a fork of
[tw93/Pake](https://github.com/tw93/Pake), GPL-3.0-or-later). The only change
compared to upstream is the app configuration in `app/MarkdownEditor.json`,
which points the generic Pake shell at https://markdown.com.cn/editor/ .

### Privacy policy

This program will not transfer any information to other networked systems unless
specifically requested by the user or the person installing or operating it.

It is a WebView wrapper around one website; all page content is served by that
website. Notes are stored locally by the web engine under
`%LOCALAPPDATA%\com.pake.mdeditor`; nothing is uploaded by this app itself.

### Uninstall

Delete `MarkdownEditor.exe` (portable build) or uninstall "MarkdownEditor" from
Windows Settings > Apps (MSI build), then remove
`%LOCALAPPDATA%\com.pake.mdeditor` to clear local data.
