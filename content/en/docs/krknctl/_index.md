
---
title: What is krknctl?
description: Krkn CLI tool
weight: 7
---

`Krknctl` is a tool designed to run and orchestrate [krkn](../krkn/) chaos scenarios utilizing
container images from the [krkn-hub](../krkn-hub.md).
Its primary objective is to streamline the usage of `krkn` by providing features like:

- Command auto-completion
- Input validation
- Scenario descriptions and detailed instructions

and much more, effectively abstracting the complexities of the container environment. 
This allows users to focus solely on implementing chaos engineering practices without worrying about runtime complexities.


## CLI Flags
The CLI flags in `krknctl` provide a way to customize the behavior of the tool and fine-tune its functionality. The following table lists some of the available flags:

| Flag | Type | Default | Description |
|------|------|---------|-------------|
| test-flag-doc-sync-2 | string |  | flag added to test documentation sync pipeline 2 |
| --help |  |  | Displays help information about the available flags and their usage |
| --version |  |  | Displays the version of `krknctl` being used |
| --verbose |  |  | Enables verbose logging to provide more detailed output |
| --debug |  |  | Enables debug mode to provide more detailed error messages and debugging information |

In addition to the flags listed above, `krknctl` also supports a range of advanced flags that can be used to customize its behavior. These flags can be used to specify options such as the container runtime to use, the network interface to bind to, and the logging level. For more information on the available flags and their usage, users can refer to the `krknctl` documentation or run the command with the `--help` flag. The CLI flags can be combined in various ways to achieve the desired outcome, and users are encouraged to experiment with different flag combinations to find the one that works best for their use case.
