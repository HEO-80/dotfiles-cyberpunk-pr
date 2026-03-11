<div align="center">

<img src=".config/powershell/themes/cyberpunk/img/netwatch-header.svg" alt="NETWATCH OS v2.077"/>

**Cyberpunk theme contribution for [craftzdog/dotfiles-public](https://github.com/craftzdog/dotfiles-public)**

*Startup dashboard · NETWATCH Oh My Posh prompt · Docker status · Zero breaking changes*

</div>

---

## What is this?

This repo contains a pull request proposal for [Takuya's dotfiles](https://github.com/craftzdog/dotfiles-public).

It adds an **optional cyberpunk-themed layer** to the existing PowerShell setup — a single uncommented line activates it, and commenting it out reverts everything back to the original.

**Nothing in the original `user_profile.ps1` is broken or removed.**

---

## What it adds

| Feature | Description |
|---|---|
| Startup dashboard | System Info · Shortcuts · Features · Live Docker status |
| NETWATCH prompt | Oh My Posh theme with git branch, path, user, execution time |
| `Write-Cyber` | ANSI helper — print any hex color in PowerShell |
| Global palette `$CY` | Restyle everything by editing 6 hex values |
| `Show-Dashboard` | Re-run the dashboard at any time |
| `help-ps` | Full help with tools, shortcuts and commands |

---

## How to activate

In `user_profile.ps1`, uncomment the last line:

```powershell
. "$PSScriptRoot\themes\cyberpunk\cyberpunk.ps1"
```

That's it. One line.

---

## Structure

```
.config/powershell/
├── user_profile.ps1                ← original file + 1 optional line at the end
└── themes/
    └── cyberpunk/
        ├── cyberpunk.ps1           ← dashboard + NETWATCH prompt
        ├── omp_cyberpunk.json      ← Oh My Posh NETWATCH theme
        └── README.md               ← detailed docs
```

---

## What it does NOT change

- `EditMode Emacs` — preserved
- `Ctrl+F / Ctrl+R` fzf chords — preserved
- All existing aliases (`g`, `ll`, `vim`, `grep`, `tig`, `less`) — preserved
- `$env:GIT_SSH` and PATH additions — preserved
- `posh-git` module — preserved

---

## Related

- Full standalone version: [HEO-80/powershell-cyberpunk](https://github.com/HEO-80/powershell-cyberpunk)

---

<div align="center">
  <sub>PR proposal by <a href="https://github.com/HEO-80">HEO-80</a> · Héctor Oviedo</sub>
</div>