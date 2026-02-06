# IT Knowledge Base

Personal IT knowledge base containing:

- Windows / Linux tips and commands
- System configuration and tools
- Various technical notes

## Structure

Each topic is stored as a Markdown file.

Folders are organized by category:
- Windows
- Linux
- Virtualization
- Git

## Tools used

- Obsidian (note management)
- Markdown
- Git for versioning and synchronization

## Purpose

Centralize tested tools, commands and procedures
for personal use across Windows and Linux systems.

## Workflow

1 - In Obsidian, create a note :
```
02_Linux/<new_note>.md
```

2 - Git backup
```
git add .
git commit -m "message"
git push
```

3 - On the other OS
```
git pull
```
And everything appears on Obsidian.
