# Fedora VM host

Use Ansible to set up a Fedora Virtual Machine host with a basic GUI for
management.

The server boots to the console, but the user can run `weston-launch` to get a
basic Weston desktop, with *virt-viewer* for viewing the VM consoles and
*cockpit-desktop* for creating and managing machines.

This only installs the packages and sets up a basic desktop environment. VM host
configuration is left up to the user.

## Help! How do I exit Weston?

Press `Ctrl+Alt+Backspace`.
