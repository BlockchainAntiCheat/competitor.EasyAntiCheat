https://forums.unraid.net/topic/127639-easy-anti-cheat-launch-error-cannot-run-under-virtual-machine/

OS: Windows 11

xml:
```
  <os firmware="efi">
    <type arch="x86_64" machine="pc-q35-8.2">hvm</type>
    <firmware>
      <feature enabled="yes" name="enrolled-keys"/>
      <feature enabled="yes" name="secure-boot"/>
    </firmware>
    <loader readonly="yes" secure="yes" type="pflash" format="qcow2">/usr/share/edk2/ovmf/OVMF_CODE_4M.secboot.qcow2</loader>
    <nvram template="/usr/share/edk2/ovmf/OVMF_VARS_4M.secboot.qcow2" format="qcow2">/var/lib/libvirt/qemu/nvram/win11_VARS.qcow2</nvram>
    <boot dev="hd"/>
    <smbios mode="host"/>
  </os>
```
