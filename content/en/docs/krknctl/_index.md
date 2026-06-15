
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
| --log-level | string | info | Specifies the logging level, which can be one of 'debug', 'info', 'warn', or 'error' |
| --runtime | string | docker | Specifies the container runtime to use, which can be one of 'docker' or 'podman' |
| --net | string |  | Specifies the network interface to bind to |

In addition to the flags listed above, `krknctl` also supports a range of advanced flags that can be used to customize its behavior. These flags can be used to specify options such as the container runtime to use, the network interface to bind to, and the logging level. For more information on the available flags and their usage, users can refer to the `krknctl` documentation or run the command with the `--help` flag. The CLI flags can be combined in various ways to achieve the desired outcome, and users are encouraged to experiment with different flag combinations to find the one that works best for their use case.

The usage of these flags can be demonstrated with the following examples:
- Running `krknctl` with the `--help` flag will display a list of all available flags along with their descriptions.
- Using the `--verbose` flag will provide more detailed output, which can be useful for debugging purposes.
- The `--debug` flag can be used to enable debug mode, which provides more detailed error messages and debugging information.
- To customize the logging level, users can use the `--log-level` flag followed by the desired logging level (e.g., `--log-level debug`).
- To specify the container runtime, users can use the `--runtime` flag followed by the name of the runtime (e.g., `--runtime docker`).
- To bind to a specific network interface, users can use the `--net` flag followed by the name of the interface (e.g., `--net eth0`).
- The `--log-level` flag can also be used to specify the logging level for a specific component, for example, `--log-level component_name=debug`.
- The `--runtime` flag can also be used to specify the container runtime options, for example, `--runtime docker --runtime-opts '--privileged'`.
- The `--net` flag can also be used to specify the network interface to bind to, for example, `--net eth0 --net ip=192.168.1.100`.

Some advanced use cases for the CLI flags include:
- Using the `--log-level` flag to specify different logging levels for different components, for example, `--log-level component1=debug --log-level component2=info`.
- Using the `--runtime` flag to specify the container runtime options, for example, `--runtime docker --runtime-opts '--privileged' --runtime-opts '--net=host'`.
- Using the `--net` flag to specify the network interface to bind to, for example, `--net eth0 --net ip=192.168.1.100`.

A more detailed explanation of each flag is as follows:
- `--help`: This flag displays help information about the available flags and their usage. It provides a list of all available flags, along with their descriptions and usage examples.
- `--version`: This flag displays the version of `krknctl` being used. It provides information about the current version of the tool, which can be useful for troubleshooting and debugging purposes.
- `--verbose`: This flag enables verbose logging to provide more detailed output. It can be used to debug issues and provides more detailed information about the execution of the tool.
- `--debug`: This flag enables debug mode to provide more detailed error messages and debugging information. It can be used to debug issues and provides more detailed information about the execution of the tool.
- `--log-level`: This flag specifies the logging level, which can be one of 'debug', 'info', 'warn', or 'error'. It can be used to customize the logging level and provides more flexibility in terms of logging.
- `--runtime`: This flag specifies the container runtime to use, which can be one of 'docker' or 'podman'. It provides more flexibility in terms of container runtime and allows users to choose the runtime that best suits their needs.
- `--net`: This flag specifies the network interface to bind to. It provides more flexibility in terms of network configuration and allows users to choose the network interface that best suits their needs.

Additionally, the following flags are also available:
- `--log-format`: This flag specifies the format of the log messages. It can be used to customize the log output and provides more flexibility in terms of logging.
- `--log-file`: This flag specifies the file to which log messages should be written. It can be used to customize the log output and provides more flexibility in terms of logging.
- `--runtime-opts`: This flag specifies additional options for the container runtime. It can be used to customize the behavior of the container runtime and provides more flexibility in terms of container runtime.

By using these flags, users can tailor the behavior of `krknctl` to suit their specific needs and requirements. It is recommended to explore the available flags and their usage to get the most out of the tool.

Additional considerations when using the CLI flags include:
- The order of the flags does not matter, as long as they are specified before the command.
- The flags can be combined in various ways to achieve the desired outcome.
- The flags can be used to override the default settings, which can be useful in certain situations.
- The flags can be used to enable or disable certain features, for example, the `--debug` flag can be used to enable debug mode.
- It is also important to note that some flags may have conflicting options, and users should be careful when combining flags to avoid any conflicts.
- Users should also be aware of the potential security implications of using certain flags, and should use them with caution.
- The documentation for `krknctl` provides more detailed information about the available flags and their usage, and users are encouraged to refer to it for more information.

## Subsection for more details on CLI Flags
To further expand on the CLI flags, here are some additional details:
- `--log-level` can also be used to specify the logging level for a specific file, for example, `--log-level file=debug`.
- `--runtime` can also be used to specify the container runtime options, for example, `--runtime docker --runtime-opts '--privileged' --runtime-opts '--net=host'`.
- `--net` can also be used to specify the network interface to bind to, for example, `--net eth0 --net ip=192.168.1.100`.
- The `--help` flag can also be used to display help information for a specific flag, for example, `--help --log-level`.
- The `--version` flag can also be used to display the version of a specific component, for example, `--version --runtime`.

These additional details provide more information on the usage of the CLI flags and their options, allowing users to better understand and utilize the flags to customize the behavior of `krknctl`.

Furthermore, the following examples illustrate the usage of the CLI flags:
- `krknctl --help --log-level` will display help information for the `--log-level` flag.
- `krknctl --version --runtime` will display the version of the container runtime.
- `krknctl --log-level debug --runtime docker` will run `krknctl` with the logging level set to debug and the container runtime set to docker.

It is also worth noting that the CLI flags can be used in combination with other features of `krknctl`, such as the scenario descriptions and detailed instructions, to provide a more comprehensive and customizable experience for users.
