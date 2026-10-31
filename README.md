![Banner](banner.png)

# monitor-registrychanges
Monitors the values of one named registry key for modifications, which can indicate malware persistence or configuration changes. Subkeys are not monitored, and one key is monitored per run. Windows only: this tool uses only the Python standard library (winreg) and has no third party dependencies. By default changes are reported as value names only. Pass `--include-value-data` to include value data for added and modified values in the same local console, log file, and output file reports. Warning: value data can hold commands and paths. - Focused on System monitoring and alerts

## Install
`git clone https://github.com/ShadowStrikeHQ/monitor-registrychanges`

## Usage
`./monitor-registrychanges [params]`

## Parameters
- `-h`: Show help message and exit
- `-k`: The one registry key whose values are monitored. Subkeys are not monitored.
- `-i`: The monitoring interval in seconds. Must be positive; a non positive interval exits with code 1 at startup.
- `-l`: No description provided
- `-v`: No description provided
- `-o`: Output changes to a file. Useful for offline analysis.
- `--include-value-data`: Include value data for added and modified values. Default is value names only. Warning: value data can hold commands and paths.

## License
Copyright (c) ShadowStrikeHQ
