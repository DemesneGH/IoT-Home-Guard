
The tools use LINKSYS WRT AC1900 router ( Model NO. is WRT1900ACS V2) as a development platform (You can check if these software tools can be installed on your router at https://openwrt.org/toh/start.). Of course, you can also use the laptop directly as the operating environment for the tools. I chose router instead of laptop because the tool will be updated for a long time, it can help you detect more kinds of IoT devices in your home.

Before using these tools, you need to install the openwrt operating system by loading lede-17.01.5-mvebu-linksys-wrt1900acs-squashfs-sysupgrade.bin. When openwrt is installed and configured, you will need to place the IoT-Home-Guard project code in the router and connect the device to be detected to the router's wifi network. Please note that this route should be able to connect to the Internet.

You can use the following command to detect whether the target IoT device is implanted with a Trojan:

    ./IoT-Home-Guard.py

The complete inspection process will last 10-15 minutes. If you want to get results faster, you can use the following command:

    ./IoT-Home-Guard.py fast_mode

When the program finishes running, it will return the following results:

    [Result] WARINING: Trojan has been discovered.
    [Trojan Data]: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

or:

    [Result] No security issues.
  
or:

    [Result] I don't know this device, you can send this packet to luodalongde#gmail.com
