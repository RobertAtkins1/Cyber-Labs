# Setting up a Home Lab

To build a home lab we must start by downloading a hypervisor. The two most popular options are WMware and VirtualBox I am going to be using VMware Workstation Pro for this lab. You can download WMware Workstation [here](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html).

Download the .exe file and execute. You will be greeted with WMware Workstation setup wizard.

![WMare Wizard](attachments\VMwareWorkstation.png)

Follow the VMware wizard to complete the installation.

## Windows VM Install

The next step is to download a Windows 10 iso. I will be using a the Windows 10 media creation tool. which can be downloaded from Microsoft [media creation tool]( https://www.microsoft.com/en-ca/software-download/windows10). 

When it is downloaded run the media creation tool and accept the license terms. Then select create installation media and select language, Edition, and Architecture. Finally, select iso file and save it to your computer.

![iso File](attachments\MediaCreation.png)

Once it is done download open VMWare and click on create a virtual machine. This will bring up the new virtual machine wizard, select the default of typical and hit next. Now you must choses an install disk. Since I downloaded an iso file I selected the second option and browsed to where the iso file downloaded. VMware detected the iso file as a windows 10 vm.

![Select iso](attachments\CreateVM.png)

Name the virtual machine and choose where you want VMware to put the files for this VM. Now choose what hardware you want the virtual machine to have. This is dependent on the hardware specifications of your host machine. Going with the default options is safe. The VM hardware can be changed if you find it too slow or is slowing down host machine too much. Click finish and wait for VMware to finalize the setup

Now it is time to start the Windows 10 virtual machine, Click on power on this virtual machine.

![Windows 10 VM](attachments\Win10HomeLab.png)

Now it is time to start the Windows 10 virtual machine, Click on power on this virtual machine.  Quickly press any key to boot into the Windows 10 iso when prompted to. This will bring up Windows setup.

![Windows Setup](attachments\WinSetup.png)

Selected what language you want and click on install now. Then you will have to put in a Windows 10 product key. Next pick which version of Windows 10 to download and accept the licenses terms.

![Custom Install](attachments\CustomInstall.png)

Next click on custom install windows only and select the drive to install windows on. Should only be one option if you went with the default configuration given by VMware. Click next and wait for Windows to install on the virtual machine drive. The virtual machine will restart when it is done installing.

I **highly recommend** you take a snapshot of the VM in this state so you can start with a fresh install when you inevitably break something on virtual machine. To take a snapshot of a virtual machine on VMware click on the clock icon with a plus sign on it, located on the top screen. Name the snapshot something descriptive so you know what is it when you want to revert to it at a later date.

![snapshot](attachments\snapshot.png)

The final step in setting up a VM is to install VMware tools. On the bottom of the VM you can see VMware asking you to install the tools click on install tools

![VMWare tools](attachments\ToolInstall.png)

Go to file explore to and click on the DVD drive (D) VMware tools a wizard will open and complete it to install the tools at the end you will have to restart the VM. Also, take a snapshot when the VM restarts.

![File Explore](attachments\FIleExTools.png)

## Linux VM Install

The second virtual machine I will be downloading for this lab is Kali Linux. Which can be found at Kali Linux website [Kali Download](https://www.kali.org/get-kali/#kali-platforms). Kali Linux has many different iso to choose from. I will be using their pre-built virtual machine which comes preconfigured. Click on the virtual machine tab, that will bring you to pre-built virtual machines page.

![Kali Website](attachments\kalipage.png)
Select which type of operating system you have 64 bit or 32 bit. I will be downloading the recommended VMware version. Once the zip file is done downloading, we can check the integrity of the file with PowerShell use the command 
> Get-FileHash
> 
![Powershell output](attachments\kalihash.png)

The file I download has a SHA256 sum of 5D9B11DFFD047C679A5B5398AA12BE6A2159CABC8FD6A896E13DBBC84F7233A8

Copy the string off PowerShell and click the sum button to see the SHA256 sum and compare it with yours, use control f quickly see if the string matches. If the sum matches then the files has not been altered in transit.

You will need to download 7-zip to extract the zip files contents[7-zip](https://7-zip.org/).

On the home page of VMware click on open a virtual machine and browse to where you put the Kali Linux files. Click open on the .vmx file. That will bring you to the Kali Linux tab.

![Kali Tab](attachments\KaliLinuxTab.png)

Click power on this virtual machine and that is the Kali Linux install with preconfigured virtual machine much faster and easier than the windows install. The default username and password is kali to login. When you first boot into Kali create a snapshot.  
