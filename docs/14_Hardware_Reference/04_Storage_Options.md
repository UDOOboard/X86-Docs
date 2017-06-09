### eMMC onboard

Depending on the [chosen model](!Hardware_Reference/Board_versions) of UDOO X86 you could have an embedded multi media card memory up to 32GB to install your favorite OS.  

The eMMC use a **SD 3.0** compliant interface.

<span class="label label-warning">Heads up!</span> As a flash-based storage device, excessive drive access, particularly write commands, reduces its useful life. Therefore, it is strongly suggested to NOT create a swap partition on the eMMC device.


### S-ATA

The N-series Intel® Pentium® / Celeron® and x5-Series Atom SoCs embed a SATA Controller, which offers two **SATA III 6.0 Gbps** interfaces.  
Of these interfaces, one SATA channel is carried out to a standard male S-ATA connector, CN18 (the other SATA channel is available on the M.2 Key B socket).

A dedicated power connector (*CN21*), can be used to give supply to *2.5"* Hard Disk Drives (or Solid State Drives) connected to the SATA male connector.  
The dedicated power connector is a 4-pin male connector. You can find this cable in the [SATA data and power cables for UDOO X86](http://shop.udoo.org/sata-data-and-power-cables-for-udoo-x86.html) kit.

<span class="label label-warning">Heads up!</span> To connect a *3.5"* Hard Drive you need to provide SATA +5V+12V combo power supply from an external source.

### μSD

The SoCs used on UDOO x86 module offer a **SD 3.0** compliant interface, that can be used to implement another mass storages media other than the optional internal eMMC and the two SATA interfaces.
This SD interface is carried to a standard μSD card slot (*CN17*), soldered on top side of the module, push-push type.

<span class="label label-warning">Heads up!</span> Due to a UEFI BIOS bug you couldn't be able to write data on the μSD connected. A bugfix is already released in the latest official UEFI BIOS version (1.02). Make sure to keep updated the firmware of your UDOO X86 using the [UEFI update](!/Advanced_Topics/UEFI_update) procedure.

### M.2 SATA/PCI-e Slot: Socket 2 Key B type 2242/3042/2260

The mass storage capabilities of the UDOO x86 are completed by an M.2 SSD Slot, which allow plugging **M.2 Socket 2 Key B** Solid State Drives with *SATA* interface or *PCI-e x2* interface (*PCI-e x1* is also supported).  

The connector used for the M.2 SATA/PCI-e slot is *CN20*, which is a standard 75 pin M.2 Key B connector.

On the UDOO x86 board there is also a Threaded Spacer which allows the placement of M.2 Socket 2 Key B SATA/PCI-e modules in `2260` size.

It is possible to place also modules in `2242` and `3042` size, by using a M/F Spacer which allows fixing the M.2 module on the spacer already available on the PCB, deemed for the fixing of the M.2 Wireless module.
