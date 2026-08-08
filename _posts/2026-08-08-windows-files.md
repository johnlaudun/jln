---
layout: post
title: "Finding Files on Windows"
date: 2026-08-08
---

I am not a Windows native. It is a foreign land. The only time I use Windows is to play a game, and so my usage looks like this: turn on computer, log in, open Steam, select a game, click green button. That’s it. 

Recent events, however, have set me on a path to try to find save files for The Sims which have gone missing because OneDrive accidentally got turned on for the account in question. 

### Powershell

```powershell
Get-ChildItem -Path C:\ -Filter *.save -Recurse -ErrorAction SilentlyContinue | Select-Object FullName
```

or

```powershell
Get-ChildItem -Path "C:\Start\Search\Here" -Filter "*.save" -Recurse -ErrorAction SilentlyContinue | Select-Object FullName, DirectoryName
```

**What the Command Does:**

- `Get-ChildItem`: This is the core command, equivalent to `ls` or `dir`.
- `-Path "..."`: Specifies where the search should begin.
- `-Filter "*.save"`: Tells it to only look for files ending in `.save`.
- `-Recurse`: **This is the key.** It tells PowerShell to search through all subfolders within the starting path.
- `-ErrorAction SilentlyContinue`: This prevents the script from stopping or showing errors when it hits a folder it doesn't have permission to access (like system folders).
- `| Select-Object FullName, DirectoryName`: This pipes the results to a selection command, which neatly outputs two columns: the full path of the file and the directory it was found in.

### Command Prompt

```windows
dir C:\*.save /s /b
```

**How to Use It:**

1. Open **Command Prompt**.
2. Navigate to the root directory you want to search from using `cd` (e.g., `cd C:\Users\YourName`).
3. Run the command above.

**What the Command Does:**

- `dir`: The directory listing command.
- `/s`: **Recursive search.** This tells it to look in all subdirectories.
- `/b`: **Bare format.** This outputs only the file path and name, without extra headers or summary information.

**Limitation:** This command is less clean than PowerShell's output; it will just list the full path for every file found.
