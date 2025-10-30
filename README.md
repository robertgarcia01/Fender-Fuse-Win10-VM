Step 1: Install VirtualBox (pretty self explanatory, make sure virtualization is turned on in BIOS if necessary)

Step 2: get Tiny10 ISO image. I use version 23H2. https://archive.org/details/tiny-10-23-h2

Step 3: Create tiny10 Virtual Machine (at least 4g ram, 2 cores, and 20gb hdd). (before VM can boot, cancel the operation and disable network adapter before booting again.)
        TIP: Unattended install creates user without admin priveliges, to avoid the headache just manually install or see: https://forums.virtualbox.org/viewtopic.php?t=107778

NOW, tiny10 23H2 supposedly has net framework 3.5 fully functional, but it is disabled by default and requires reaching out to microsoft servers to acquire, so we are going to opt 
for an offline install. This is somewhat complicated, essentially you must import and mount a (standard, NOT tiny10) ISO image in your VM, then use DISM to install. the next steps will cover that. 

Step 4: Get windows 10 23H2 ISO here (this is a modded, not official image but it worked for this purpose): https://archive.org/details/Windows_10_23H2

Step 5: Transfer ISO to Virtual Machine (I used a USB drive) and select "mount" when right clicking. 

Step 6: 
