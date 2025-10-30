Step 1: Install VirtualBox (pretty self explanatory, make sure virtualization is turned on in BIOS if necessary)

Step 2: get Tiny10 ISO image. I use version 23H2. https://archive.org/details/tiny-10-23-h2

Step 3: Create tiny10 Virtual Machine (at least 4g ram, 2 cores, and 20gb hdd). (before VM can boot, cancel the operation and disable network adapter before booting again.)
        TIP: Unattended install creates user without admin priveliges, to avoid the headache just manually install or see: https://forums.virtualbox.org/viewtopic.php?t=107778

*NOW, tiny10 23H2 supposedly has .NET Framework 3.5 fully functional, but it is disabled by default and requires reaching out to microsoft servers to acquire, so we are going to opt for an offline install. This is somewhat complicated, essentially you must import and mount a (standard, NOT tiny10) ISO image in your VM, then use DISM to install. the next steps will cover that.*

Step 4: Get windows 10 23H2 ISO here (this is a modded, not official image but it worked for this purpose): https://archive.org/details/Windows_10_23H2

Step 5: Transfer ISO to Virtual Machine (I used a USB drive and enabled access to the drive in the VM options). Once inside the VM, right click and select "Mount". Check what drive letter the image was mounted to. 

Step 6: Open Command Prompt with Admin priveliges and type the following command (without the quotes, and change the drive letter to the drive that the ISO was mounted to): 

"DISM /Online /Enable-Feature /FeatureName:NetFx3 /All /LimitAccess /Source:d:\sources\sxs"

(More info available here: https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/deploy-net-framework-35-by-using-deployment-image-servicing-and-management--dism?view=windows-11)

Step 7: Wait for .NET to finish installing inside command prompt, then get silverlight.exe from this page or https://download.cnet.com/microsoft-silverlight-64-bit/3000-2378_4-75884713.html (again, I used a USB drive to transfer files between host PC and VM)

Step 8: Run and finish installing silverlight, then restart the system. 

From here, all of the dependencies for Fender Fuse have been met. InTheBlues/GuitarPedaldemos.com has an archive of the installer, manuals, and an archive of almost 10K amp preset files. https://guitarpedaldemos.com/fender-fuse-mustang-v2-archive/

Step 9. Download the software for Windows, and transfer the downloaded installer file, as well as any/all presets you want to the VM (again using USB drive). 

Step 10. Run installer. For further information on how to upload multiple presets and other tips, see: https://fender-mustang-amps-and-fuse.fandom.com/wiki/Fender_Fuse_on_Windows_11 
        TIP: Your VM may lag if you upload the entire archive into your media library, I just uploaded the InTheBlues and Fender Stock Presets and it works

Step 11. Enjoy! 
