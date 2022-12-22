# Command-line reference for libvirt/virsh

Example command used to install **ubuntu 22.04** on **Debian 11**.

```sh
virt-install --name boost \     
--os-type linux \
--os-variant ubuntu20.04 \
--ram 2048 \
--disk /media/kyle/8TB/kvm/disk/boost.img,device=disk,bus=virtio,size=20,format=qcow2 \
--graphics vnc,listen=0.0.0.0 \
--noautoconsole \
--hvm \
--cdrom /media/kyle/8TB/kvm/iso/ubuntu-22.04.1-live-server-amd64.iso \
--boot cdrom,hd
```

**Cheatsheet**:
|Explanation|Command|
|-----------|-------|
|List all VMs|`virsh list --all`|
|Start a VM|`virsh start boost`|
|Reboot a VM|`virsh reboot boost`|
|Shutdown a VM|`virsh shutdown boost`|
|Force shutdown a VM|`virsh destroy boost`|
|Delete a VM|`virsh undefine boost --remove-all-storage`|
|Display VMs VNC listen port|`virsh vncdisplay boost`|
|Connect to VMs VNC port|`tigervnc-viewer localhost:0`|
|Lists OS definitions for use with virt-install|`osinfo-query os`|

* Tutorial utilized: <https://adamtheautomator.com/virsh/>

    #virsh #libvrt #kvm #virtualization #hypervisor #vnc
