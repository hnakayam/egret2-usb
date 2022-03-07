# TAS-P-001
This is Trackball and Paddle device for TAITO EGRET2-mini.

# USB Packet capture

2 USB capture files at this point: these capture files are taken using Total Phase / Beagle USB 480 capture device.
You can download .tdc file viewer (Datacenter Software) from their download site (with free e-mail addrress registeration)

https://www.totalphase.com/products/data-center/

* tas-p-001-windows10-configure.tdc

USB packet capture for first plugin to the Windows 10 PC.
Sometimes "Get String Descriptor" only occur in the first plugin only.
I didn't intended to operate for this capture but INPUT REPORT continuously sent from the device.

* tas-p-001-windows10-operation.tdc

USB packet capture (for the second time and so on...) to the Windows 10 PC.
1st I tried trackball move, then paddle, then all the buttons LEFT-A RIGHT-A START MENU CREDIT.
These input report occurs pereodically (different from USB Keyboard MAKE/BREAK like handling).
Trackball move is assigned to mouse axis X/Y, paddle move is assigned to mouse wheel.
All the buttons are mapped to mouse buttons. But using 16 bit (2 bytes) of input report.

See Configuration Descriptor Picture (tas-p-001-windows10-report_descriptor.png) for input format details.

# Attached Image files

* tas-p-001-windows10-configure.png

1st configuration getting string descriptor. You can see "TAITO..." strings in Unicode.

*tas-p-001-windows10-report_descriptor.png

Report Descripter defining the input report format.

*tas-p-001-windows10-trackball.png

For trackball, 3rd and 4th bytes of input report used.

*tas-p-001-windows10-button.png

For paddle, 5th byte of input report used.

*tas-p-001-windows10-paddlel.png

For buttons, 1st and 2nd byte of input report used.

LEFT-A : 80 00
RIGHT-A : 00 01
START : 02 00
MENU : 10 00
CREDIT : 04 00
