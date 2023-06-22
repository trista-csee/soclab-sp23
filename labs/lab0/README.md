# Install Ubuntu 20.04+ Virtual Machine on M1 MacBook Pro

Implement as the following steps and refer attached Illustration 1:
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
9. Specify the size of the Ubuntu virtual machine storage space to `40GB`, as attached __*figure 9*__
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
21. Go to setting and scale the display by 200%, as attached __*figure 20*__
22. Open the terminal and type the command: `sudo apt update` to updated the package, as attached __*figure 21*__
23. Type the command: `sudo apt install spice-vdagent spice-webdavd` to install the tools allowing access to shared directories of Host OS, and enableing to copy and paste Clipboard Memory between guest and Host OS, as attached __*figure 22*__
23. Type the command: `sudo apt install openssh-server` to install SSH Server, as attached __*figure 23*__
24. Type the command: `sudo systemctl status ssh` to check SSH Service is Active and Running, as attached __*figure 24*__
25. Type the command: `sudo ss -tulpn | grep ssh` to find out the SSH server port, as attached __*figure 25*__
26. Type the command: `ifconfig` to find out which IP the virtual machine is connected to the physical machine through.
    **Note**: The IP is not necessarily the same in everyone's virtual machine, as attached __*figure 26*__
27. Type the command: `ssh -X trista-csee@192.168.64.3` to SSH the remote Server, as attached __*figure 27*__

---

# Install Xilinx Vitis 2022.1 on Ubuntu 20.04+ Virtual Machine

Implement as the following steps and refer attached Illustration 2:
