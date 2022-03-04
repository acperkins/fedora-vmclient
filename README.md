# Fedora VM client

Use Ansible to set up a Fedora Virtual Machine client with a basic GUI for
management.

The server boots to the console but the user can run `weston-launch` to get a
basic Weston desktop, with **virt-viewer** for viewing the VM consoles and
**cockpit-desktop** for creating and managing machines.

This only installs the required packages and sets up a basic desktop
environment.

## Connecting to your VM host

Create an entry in `~/.ssh/config` for `vmhost` pointing at your real VM server.

## Help! How do I exit Weston?

Press `Ctrl+Alt+Backspace`.
