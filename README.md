# Fedora VM host

Use Ansible to set up a Fedora Virtual Machine host with a basic GUI for
management.

The server boots to the console but the user can run `weston-launch` to get a
basic Weston desktop, with **virt-viewer** for viewing the VM consoles and
**cockpit-desktop** for creating and managing machines.

This only installs the required packages and sets up a basic desktop
environment. VM host configuration (storage, ISOs, etc.) is left up to the user.

## Configure SELinux

If you store your VM images outside of `/var/lib/libvirt/images` and
`/var/lib/libvirt/isos`, you will need to make an additional SELinux change.

Assuming you will store your files in `/virt`, run the following commands as
root:

    semanage fcontext -a -t virt_image_t "/virt(/.*)?"
    restorecon -Rv /virt

If you use a different path, replace `/virt` in the commands above with the
location of your images.

## Help! How do I exit Weston?

Press `Ctrl+Alt+Backspace`.
