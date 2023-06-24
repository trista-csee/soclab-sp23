# Install UTM virtual machine to execute Ubuntu 20.04+ Operating System on MacBook Pro M1

Implement as the following steps and refer **attached Illustration 1**:
1. Download [Ubuntu 20.04.6 LTS (Focal Fossa)](https://releases.ubuntu.com/focal/).
   **Note**: Choose `64-bit PC (AMD64) desktop image`, as attached __*figure 1*__
2. Click `Download` [UTM](https://mac.getutm.app/), as attached __*figure 2*__
3. Double tap on the `UTM.dmg` and drag the `UTM` Icon into the `Applications` folder, as attached __*figure 3*__
4. Open `UTM app`, first choose `Create a New Virtual Machine`, as attached __*figure 4*__
5. Choose `Emulate` to start.
   **Note**: Because I am installing ARM64 based operating system on Apple Silicon, as attached __*figure 5*__
6. Next, Operating System preconfigured select `Linux`, as attached __*figure 6*__
7. Check Linux Boot ISO Image, Import the step 1. dowload image file `Ubuntu 20.04.6 LTS (Focal Fossa)`, as attached __*figure 7*__
8. Allocate `4GB Ram`, set `4 CPU cores`, and `enable hardware OpenGL acceleration`, as attached __*figure 8*__
9. Specify the size of the Ubuntu virtual machine storage space to `400GB`, as attached __*figure 9*__
10. Shared Directory select the `downloads` folder, as attached __*figure 10*__
11. Name the Ubuntu virtual machine and check summary list, as attached __*figure 11*__
12. Done creating the Ubuntu virtual machine. 
13. Select the virtual machine, click on the top right setting.
    Choose display and `enable Retina Mode`, as attached __*figure 12*__
14. Start the virtual machine and Install Ubuntu Operating System, as attached __*figure 13*__
15. Proceed with the standard installation, as attached __*figure 14*__
16. Configure login information, then running installation, as attached __*figure 15*__
17. `Complete Ubuntu Operating System installation`, close the dialog and `turn off the virtual machine`, as attached __*figure 16*__
18. Choose the `Drive image options` and `eject` the image file, as attached __*figure 17*__
19. Tap on the play button to `Restart the Ubuntu virtual machine`, as attached __*figure 18*__
20. Login `Ubuntu 20.04.6 Operating System` running inside the virtual machine on M1 MacBook Pro, as attached __*figure 19*__
21. Go to setting and scale the display by `200%`, as attached __*figure 20*__
22. Open the terminal and type the command: `sudo apt update` to updated the package, as attached __*figure 21*__
23. Type the command: `sudo apt install spice-vdagent spice-webdavd` to install the tools allowing access to shared directories of Host OS, and enableing to copy and paste Clipboard Memory between guest and Host OS, as attached __*figure 22*__
23. Type the command: `sudo apt install openssh-server` to install SSH Server, as attached __*figure 23*__
24. Type the command: `sudo systemctl status ssh` to check SSH Service is Active and Running, as attached __*figure 24*__
25. Type the command: `sudo ss -tulpn | grep ssh` to find out the SSH server port, as attached __*figure 25*__
26. Type the command: `ifconfig` to find out which IP the virtual machine is connected to the physical machine through.
    **Note**: The IP is not necessarily the same in everyone's virtual machine, as attached __*figure 26*__
27. Type the command: `ssh -X trista-csee@192.168.64.4` to SSH the remote Server, as attached __*figure 27*__

---

# Install Xilinx Vitis 2022.1 on Ubuntu 20.04+ Operating System through UTM virtual machine on MacBook Pro M1

Implement as the following steps and refer **attached Illustration 2**:
1. Download [Xilinx Vitis Core Development Kit - 2022.1 Full Product Installation](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vitis/2022-1.html).
   **Note**: Choose [Xilinx Unified Installer 2022.1 SFD (TAR/GZIP - 73.81 GB)](https://www.xilinx.com/member/forms/download/xef.html?filename=Xilinx_Unified_2022.1_0420_0327.tar.gz), as attached __*figure 1*__
2. Save `Xilinx Unified Installer 2022.1 SFD (TAR/GZIP - 73.81 GB)` in the `downloads` folder, as attached __*figure 2*__
3. Select the virtual machine, click on the top right setting. Choose Shared, **Note**: Manually change the `Directory Share Mode` from "VirtFS" to `SPICE WebDAV` in the UTM VM settings, as attached __*figure 3*__
4. Login `Ubuntu 20.04.6 Operating System`, Access shared folders from Files, Click `Other Locations` in the lower left corner, then click `Spice client folder`, it will mount the shared folder, as attached __*figure 4*__ 
5. Open the `Spice client folder`, there are the content of the folder shared by the host computer, as attached __*figure 5*__
6. Copy the TAR/GZIP file from the folder shared by the host computer to the `downloads` folder in the virtual machine, , as attached __*figure 6*__ 
7. Within the installation folder and type the command: `tar -xvf Xilinx_Unified_2022.1_0420_0327.tar.gz` to extract a tar.gz file, as attached __*figure 7*__
8. Type the command: `cd ./Downloads/Xilinx_Unified_2022.1_0420_0327/` to extract the installer, then type the command: `sudo ./xsetup` to run Xilinx Vitis 2022.1 Installation, as attached __*figure 8*__
9. Choose `Continue`, `Vitis`, tick `I Agree` and `Next` to configure Xilinx installer. Installation directory is `/tools/Xilinx`, choose `Install` to proceed with the standard installation, as attached __*figure 9*__
