# Obsidian Another Quick Switcher Plugin

[![release](https://img.shields.io/github/release/tadashi-aikawa/obsidian-another-quick-switcher.svg)](https://github.com/tadashi-aikawa/obsidian-another-quick-switcher/releases/latest)
[![Tests](https://github.com/tadashi-aikawa/obsidian-another-quick-switcher/workflows/Tests/badge.svg)](https://github.com/tadashi-aikawa/obsidian-another-quick-switcher/actions)
![downloads](https://img.shields.io/github/downloads/tadashi-aikawa/obsidian-another-quick-switcher/total)

This is an Obsidian plugin which is another choice of Quick switcher.

- It can create custom search commands (`Custom searches`)
- It can search backlinks and move them **without leaving from a keyboard** (`Backlink search`)
- It can move a file to another folder (`Move file to another folder`)
- It can search **regardless of the appearance order of tokens**
- It **only searches Markdown files** except for the case of `Move file to another folder`
- It does not search very fuzzy (e.g. searching for `201` doesn't match `2.01`) 
- It can search to **consider prefix emoji**
- It shows file names and directory names separately


## 👥 For users

### Feature requests / Bugs

Please create a new [issue].

### Pull requests

Before creating a pull request, please make an [issue] or a [discussion]😉

[issue]: https://github.com/tadashi-aikawa/obsidian-another-quick-switcher/issues
[discussion]: https://github.com/tadashi-aikawa/obsidian-another-quick-switcher/discussions

## ⏬ Install

You can download from `Community plugins` in Obsidian settings.

## ⌨️Features

### 1‍⃣ Custom searches

![Demo](https://raw.githubusercontent.com/tadashi-aikawa/obsidian-another-quick-switcher/master/demo/custom-searches.gif)


Custom searches enables you to create your original search commands.

![Demo](https://raw.githubusercontent.com/tadashi-aikawa/obsidian-another-quick-switcher/master/demo/search-commands-setting.png)

You can use the following names as a `Sort priorities`.

|        Name        |                      Description                      |
| ------------------ | ----------------------------------------------------- |
| Perfect word match | A query matches perfectly with a word in the filename |
| Prefix name match  | The filename starts with a query                      |
| Name match         | The filename includes a query                         |
| Tag match          | The tag name in the file includes a query             |
| Header match       | The header name in the file includes a query          |
| Link match         | The internal link name in the file includes a query   |
| Length             | Length of the filename                                |
| Last opened        | The time the file opened last                         |
| Last modified      | The time the file modified last                       |
| Star               | The file has a star                                   |

> **Warning**
> Please don't forget to click the `Save` button before you close Obsidian. Otherwise, the settings **will never restore** when you open Obsidian next time.
> ![](demo/save-button.png)

### 2‍⃣ Backlink search

![Demo](https://raw.githubusercontent.com/tadashi-aikawa/obsidian-another-quick-switcher/master/demo/backlink-search.gif)

### 3‍⃣ Header floating search in file / Header search in file

![Demo](https://raw.githubusercontent.com/tadashi-aikawa/obsidian-another-quick-switcher/master/demo/header-floating-search-in-file.gif)

- Show all headers even after filtering to retain file structures in the brain
- Jump to the first hit suggestion automatically and move next/previous by `Tab/Shift+Tab` as default

### 4️⃣ Grep

This feature requires [ripgrep](https://github.com/BurntSushi/ripgrep) that can call from anywhere. In other words, the `rg --version` command must be in a state to succeed everywhere.

![Demo](https://raw.githubusercontent.com/tadashi-aikawa/obsidian-another-quick-switcher/master/demo/grep.gif)

- `TAB`: Search (not realtime)
- `Ctrl+,`: preview
- Input regards as a regex pattern
- Because ripgrep search just fastly when you need to search, **it needs no indexes and caches, of course, no need to create them before!** ✨

## For users who use earlier than v6.0.0

v6.0.0 has some breaking changes related to settings.

|                            Before                             |                              After                               |
| ------------------------------------------------------------- | ---------------------------------------------------------------- |
| `Search by headers`                                           | in `Search commands`                                             |
| `Search by links`                                             | in `Search commands`                                             |
| `Ignore prefix path patterns for Normal search`               | in `Search commands`                                             |
| `Ignore prefix path patterns for Recent search`               | in `Search commands`                                             |
| `Ignore prefix path patterns for Filename Recent search`      | in `Search commands`                                             |
| `Ignore prefix path patterns for Backlink search`             | `Exclude prefix path patterns for "Backlink search"`             |
| `Ignore prefix path patterns for Move file to another folder` | `Exclude prefix path patterns for "Move file to another folder"` |

## 📱 Mobile support

It both supports desktop and mobile.

## 🖥️ For developers

- Requirements
  - [Task]

### Development

```console
task init
task dev
```

### Release

```console
# Beta
task release-beta VERSION=1.2.3-beta1

# Stable
task release VERSION=1.2.3
```

[task]: https://github.com/go-task/task
