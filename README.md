# Scripts

## Reminder
Make sure to add the directory where the script is installed to the following:

1. **User's PATH**:
   Add to `.bashrc` or a similar configuration file for the user.
2. **Root's PATH**:
   Add to `.bashrc` or a similar configuration file for the root user.
3. **Sudo PATH**:
   Add to the `secure_path` setting in `visudo`.

## Description

### `upgradeall`
The `upgradeall` script is designed to force an upgrade of all deferred and similar packages using the `apt-get --with-new-pkgs upgrade` command. It automates the process of identifying and installing deferred package upgrades, ensuring your system stays up to date.

### Usage

1. **Run the script**:
   ```bash
   sudo ./upgradeall
   ```

2. **Features**:
   - Checks if the script is run with root privileges.
   - Updates package lists using `apt update`.
   - Detects deferred package upgrades.
   - Automatically installs deferred packages without user confirmation.

3. **Requirements**:
   - A Debian-based Linux distribution with the `apt` package manager.
   - Root privileges (use `sudo`).