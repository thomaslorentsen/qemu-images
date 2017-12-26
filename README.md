# Packer Images
Qemu images built by packer

```bash
packer build debian-virtualbox.json
```

```bash
VBoxManage clonehd output-virtualbox-iso/packer-virtualbox-iso-1514258306-disk001.vmdk disk.raw --format raw 
```

```bash
qemu-img convert -f raw disk.raw -O qcow2 disk.qcow2
```

```bash
qemu-img convert -f vmdk -O qcow2 output-virtualbox-iso/packer-virtualbox-iso-1514258306-disk001.vmdk disk.qcow2
```