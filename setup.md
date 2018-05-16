## From Windows or MacOS

Use Oracle VirtualBox to host a linux guest OS
* Install Virtual Box
  * or you could use vmWare workstation if you prefer
* download Ubuntu ISO
  * Current [support](https://ncsforum.movidius.com/discussion/100/product-faq) only for Ubuntu 16.04
  * coming from Windows you may find it easier to use Lubuntu derivitive
  * http://cdimage.ubuntu.com/lubuntu/releases/16.04.4/release/lubuntu-16.04-desktop-amd64.iso
* create the VM
  * 20GB should be more than ample
  * mount the ISO in the virtual cdrom
  * start up the VM
  * choose Try Lubuntu 
  * once the desktop opens use the Install Lubuntu icon
  * use install type: Erase disk and install Lubuntu
    * this is safe because you're in a VM and the VMDK was just created empty :)
  * answer install steps as you prefer
  * follow through until reboot
  * unmount the ISO from the VM and restart
* 

