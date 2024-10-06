# Description
Install Windows 11 PRO from sratch in Mac M1 computer

## Steps

- **STEP01**: Install UTM Hypervisor

This tool manage VM in your Mac M1.

- **STEP02**: Install CrystalFetch

This tool will create the last Windows 11, 10 ISO installer from [UUPDump](https://uupdump.net/)

Select Windows 11 and this tool download the sources and compile the ISO installer to be used from UTM

- **STEP03**: Install Windows 11:

1.  After create the Windows 11 ISO Installer.
2.  Open UTM and click the “+” button to open the VM creation wizard.
3. Select “Virtualize”.
4. Select “Windows”.
5. Make sure “Import VHDX Image” is unchecked and “Install Windows 10 or higher” is checked. Also make sure “Install drivers and SPICE tools” is checked. Press “Browse” and select the ISO you built in step 1.
6. Pick the amount of RAM and CPU cores you wish to give access to the VM. Press “Next” to continue.
7. Specify the maximum amount of drive space to allocate. Press “Next” to continue.
8. If you have a directory you want to mount in the VM, you can select it here. Alternatively, you can skip this and select the directory later from the VM window’s toolbar. The shared directory will be available after installing SPICE tools (see below). Press “Next” to continue.
9. Press “Save” to create the VM. Wait for the guest tools to finish downloading and press the Run button to start the VM.
10. Press any key to start the Windows installer and follow the instructions on screen. If you have issues with the mouse, press the mouse capture button in the toolbar to send mouse input directly. Press Control+Option together to exit mouse capture mode. Sometimes, due to driver issues, you can enter and exit capture mode and the mouse cursor works normally again



- **STEP04**: IActivate Windows 11:

In a Powershell terminal execute these commands:

```
slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX

slmgr /skms kms8.msguides.com

slmgr /ato 
```