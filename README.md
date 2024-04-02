# LLM Prompts Collection

This repository is a collection of LLM prompts. It includes a Taskfile for syncing the `pattern` folder with `~/.config/fabric/patterns/`, which allows them to be used with [Fabric](https://github.com/danielmiessler/fabric/tree/main).

## Prerequisites

- Task: A task runner / simpler Make alternative written in Go. [Install Task](https://taskfile.dev/#/installation)

## Usage

To sync the `pattern` folder with `~/.config/fabric/patterns/`, run the following command:

```bash
task sync
```

Then,

```bash
pbpaste | fabric -p thought_provoking
```