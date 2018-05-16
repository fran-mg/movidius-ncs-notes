## From Windows or MacOS

Here are simple step by step instructions for setting up a guest virtual machine to run ?ubuntu so you can use the Movidius Neural Compute Stick (NCS)

Use Oracle VirtualBox to host a linux guest OS
* Install Virtual Box
  * or you could use vmWare workstation if you prefer
  * you will also need Virtual Box Extension Pack to use USB2/3
    * https://www.virtualbox.org/wiki/Downloads
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
* pass the USB stick through to the VM
  * yes, you _may_ feel excited because you are pluging in your new blue wonder
  * no, it's **not** going to start doing anything awesome just yet
  * plug your NCS into a USB interface on your PC
    * many people refer to this being a USB3 socket, but it will work with USB2
  * In your Virtual Hosting software (VirtualBox or vmWare WS) open guest machine settings
  * Ports / USB / Device Filters / Add
  * you should see the plug and play (PNP) IDs for the NCS
    * here are suggested PNP ID values 
    * credit https://ncsforum.movidius.com/discussion/406/ncs-on-windows-10-with-virtualbox
    * 03E7:2150   (USB2) 
    * 03E7:F63B   (USB3)
    * 040e:f63b   (USB3, may be incorrect)
  * check you can see the device in ubuntu
    * from a terminal run the command 

```    
lsusb
```
* Enable copy & paste
 * Insert/ Mount guest additions cdrom
 * Open in file manager
 * press F4 to open a terminal in this folder
 * Install the guest additions with the command...

```
sudo ./VBoxLinuxAdditions.run
```
  * when you get the message 'installed you may need to restart'...
  * from the Start / Logout menu pick Reboot
  * After restart in the VM menu...
    * Devices / Shared Clipboard / Bidirectional
 
## Now you have ?ubuntu...

* Install the Movidius™ Neural Compute (MvNC) Software Development Kit (SDK)
  * NB: this is using the source code branch for the SDK VERSION 2  
  * open a Terminal window (CTRL-ALT-T)
  * paste in the following commands

```
# install the dependencies 
sudo apt install -y git make

# credit https://developer.movidius.com/start
mkdir -p ~/workspace
cd ~/workspace
# using branch for new v2 - see https://github.com/movidius/ncsdk
git clone -b ncsdk2 https://github.com/movidius/ncsdk.git
cd ~/workspace/ncsdk
make install
```

  * if the latter fails you may have to install some build dependencies
    * google what and add the steps in here above
  * 
* Run the examples

```
# credit https://developer.movidius.com/start
# Test installation by running built-in examples
cd ~/workspace/ncsdk
make examples
```

### Development workflow

* https://movidius.github.io/ncsdk/

#### Advanced usage with docker containers

see: 

* https://github.com/kwierman/docker_ncsdk
* https://stackoverflow.com/questions/49181354/run-ncsdk-movidius-neural-stick-on-macos


