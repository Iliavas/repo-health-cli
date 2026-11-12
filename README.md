# Repo Health CLI

Native command-line client of [explainscore.com](https://explainscore.com): it measures a
local repository or a public GitHub repository on your machine and scores it through
the Repo Health service. Repository code is never executed or uploaded; only numeric
measurements are sent for scoring.

This repository only hosts release packages. Download them from
[Releases](https://github.com/Iliavas/repo-health-cli/releases): **Latest** is the
stable build, `repo-health-cli-dev-*` prereleases are automatic development builds.

## Install

macOS / Linux:

```sh
curl -fsSL https://explainscore.com/install.sh | sh
```

Windows (PowerShell):

```powershell
irm https://explainscore.com/install.ps1 | iex
```

The installer picks the package for your platform, verifies its SHA-256 checksums
and puts `repo-health` into `~/.local/bin` (`%LOCALAPPDATA%\repo-health\bin` on Windows).

Packages: `darwin-arm64`, `darwin-amd64`, `linux-amd64`, `linux-arm64` (glibc 2.39+),
`windows-amd64`.

## Usage

```sh
repo-health scan .
```

The first run opens the Telegram sign-in page; after you press **Start** in the bot the
scan continues and prints the health score with prioritized recommendations, and a
private link to your project page with the score history. New accounts get $1 of
credit; a report costs $0.10.

Other commands: `repo-health login`, `whoami`, `topup`, `logout`, `version`, `help`.

---

# Repo Health CLI (RU)

Консольный клиент [explainscore.com](https://explainscore.com): оценивает локальный
репозиторий или публичный репозиторий GitHub на вашем компьютере. Код не запускается
и не загружается, на сервис уходят только числовые измерения.

Установка: `curl -fsSL https://explainscore.com/install.sh | sh` (Windows:
`irm https://explainscore.com/install.ps1 | iex`), затем `repo-health scan .` —
при первом запуске откроется вход через Telegram, после него — оценка, рекомендации
и ссылка на страницу проекта с историей оценок.
