---
name: running-snapcraft-commands
description: Provide guidelines on how to run the `snapcraft` command by an AI agent.  Should be used when running the `snapcraft` command to build the snap package, or a Snapcraft parts lifecycle steps(pull, build, stage, prime, pack).
---

# The running-snapcraft-commands agent skill

Provide guidelines on how to run the `snapcraft` command by an AI agent.  Should be used when running the `snapcraft` command to build the snap package, or a Snapcraft parts lifecycle steps(pull, build, stage, prime, pack).

## No sandboxing

As Snapcraft is shipped as a snap package, it is confined by the snap sandbox. Therefore, to ensure proper functionality, the `snapcraft` command should be run without any additional sandboxing.

## Enable log-friendly output

Always run the `snapcraft` command with `</dev/null 2>&1` appended to ensure log-friendly output.

This applies to the commands in the following sections.

## Enable verbose output

Unless it is not supported, always run the `snapcraft` command with the `--verbose` option to enable verbose output.

## Build snap

To build the snap package, run the `snapcraft pack` command in the root directory of the snap project.

Avoid running `snapcraft` without specifying the command or options, as it is a deprecated syntax.
