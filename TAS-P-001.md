# TAS-P-001
This is Trackball and Paddle device for TAITO EGRET2-mini.

# USB Packet capture

2 capture files at this point: these capture files are taken using Total Phase / Beagle USB 480 device.
You can download .tdc file viewer (Datacenter Software) from their download site (with free mail addrress registeration)

https://www.totalphase.com/products/data-center/

* tas-p-001-windows10-configure.tdc
USB packet capture for first plugin to the Windows 10 PC.
Sometimes "Get String Descriptor" only occur in the first plugin only.
I didn't intended to operate for this capture but INPUT REPORT continuously sent from the device.

* tas-p-001-windows10-operation.tdc
USB packet capture (for the second time and so on...) to the Windows 10 PC.
1st I tried trackball move, then paddle, then all the buttons LEFT-A RIGHT-A START MENU CREDIT.
Trackball move is assigned to mouse axis X/Y, paddle move is assigne to mouse wheel.
All the buttons are mapped to mouse button. But using 16 bit (2 bytes) of imput report.

See Configuration Descriptor Picture (tas-p-001-windows10-report_descriptor.png) for details.
