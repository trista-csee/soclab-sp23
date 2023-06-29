# VMware Fusion 13 Player virtual machine + Ubuntu 20.04.6 LTS + Xilinx Vitis 2022.1 install on MacBook Pro with Intel Core i7 processor - Implement2

> **NOTE:** VMware Fusion: Desktop Hypervisors for Mac install on `Intel or Apple Silicon` Macs.
>
> **NOTE:** Xilinx tools support the operating systems on `x86 and x86-64` , `except arm64` processor architectures `up to Now`.
> That is to say, Apple M1/M2 Silicon with aarch64 architecture are different from the commonly used 64-bit CPU cores with x86_64 Intel architecture.
> `Xilinx tools` are built with executables for `Intel architecture`.


## Implement2: Install Xilinx Vitis 2022.1 on Ubuntu virtual machine in MacBook Pro with Intel Core i7 processor

**Implement2 as the following steps and refer Illustration:**
1. Open `Firefox Web Browser`, Download [Xilinx Vitis Core Development Kit - 2022.1 Full Product Installation](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vitis/2022-1.html). 
   **Note:** Choose [Xilinx Unified Installer 2022.1 SFD (TAR/GZIP - 73.81 GB)](https://www.xilinx.com/member/forms/download/xef.html?filename=Xilinx_Unified_2022.1_0420_0327.tar.gz).
   <img width="1536" alt="3-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/3ba9a8fc-5334-4691-af25-204793004427">
   <img width="1536" alt="3-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/74753731-f95c-4661-a449-a4ed95a367ca">
   <img width="1536" alt="3-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d9b6b252-a3d0-4816-b1e1-55db9349957b">

2. Save `Xilinx Unified Installer 2022.1 SFD (TAR/GZIP - 73.81 GB)` in the `downloads` folder of the Ubuntu virtual machine. Complete Xilinx Unified Installer 2022.1 SFD (TAR/GZIP - 73.81 GB) downloaded. Within the `Downloads` directory, open in Terminal.
   <img width="893" alt="3-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/fd6f4942-fba0-46d1-85e9-59402bbb38f7">

3. Within the `downloads` directory, type the command: `tar -xvf Xilinx_Unified_2022.1_0420_0327.tar.gz` to extract the tar.gz file in the current working directory.
   <img width="898" alt="3-5" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/32ddb242-6a58-459e-afc8-3661f2bbabf6">

4. Type the command: `cd ./Xilinx_Unified_2022.1_0420_0327/` to extract the installer.
   Type the command: `sudo apt intall libtinfo5` and `sudo apt intall libncurses5` to install libraries.
   **Note:** Avoid final processing hanging at *"Generating installed device list"*.
   <img width="740" alt="3-7-0" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/380fbbdd-5a4a-4274-a38c-25cbdf7460d4">
   <img width="1048" alt="3-7-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/c1b2b956-4747-40d3-a290-76d708460ee8">
   <img width="1046" alt="3-7-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d6d78e46-17da-4b2c-bc03-b3c450e15913">
   <img width="892" alt="3-7-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/8005242d-93e0-4638-8a85-816e062a425e">

5.  Type the command: `sudo ./xsetup` to start Xilinx Vitis 2022.1 Installation.
    Choose `Continue`, `Vitis`, tick `I Agree` and `Next` to configure Xilinx installer.
    By default, Installation directory is `/tools/Xilinx`, choose `Install` to proceed with the standard installation.
    <img width="814" alt="3-7" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/817ac0b0-d30e-4448-aa6f-3edfa2d93ac0">

    <img width="889" alt="3-8" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/8aad2376-1e8a-4911-9f56-08b04453a260">
    <img width="886" alt="3-9" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/00e3657a-68d3-4a95-bc02-8f3be8b7befd">
    <img width="888" alt="3-10" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/51bfeb35-1d6f-40a4-9bf9-0bf77e347c69">
    <img width="892" alt="3-11" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/c316896b-4f56-4408-9f3a-da6c48831bca">
    <img width="888" alt="3-12" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/9a820324-13dc-4fac-9742-740c671b95d9">
    <img width="890" alt="3-13" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/cb052a15-2eb8-4603-a221-93a4832a04ed">
    <img width="888" alt="3-14" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/240bb566-6287-440b-b420-02bfb34c575e">
    <img width="889" alt="3-15" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/8d9abcf2-8b58-4a95-8c3a-61c5ec2886d3">

6. At the end of the installation, within the installation directory, type the command: `cd /tools/Xilinx/Vitis/2022.1/scripts/` to enter the script directory, then type the command: `sudo ./installLibs.sh` to run an installation script to fill in any missing libraries for Versal ACAP tools.
   <img width="890" alt="3-17" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/98ad62e3-a074-4d72-b843-1120080db333">
   <img width="1157" alt="3-18" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/376ba00f-d300-4b52-bfc8-354b53ff07c8">
 
7. Type the command: `cd /tools/Xilinx/Vivado/2022.1/data/xicom/cable_drivers/lin64/install_script/install_drivers/` to enter the install_drivers directory, and type the command: `sudo ./install_drivers` to install various Xilinx programmer cable drivers.
   <img width="1353" alt="3-19" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/f56eb502-552e-41d8-833e-a795b5a8b4a3">

8. New Open in Terminal, Type the command: `gedit ~/.bashrc`. 
   Within the opened file, move to the last empty line, add the following three commands: `source /tools/Xilinx/Vivado/2022.1/settings64.sh`, `source /tools/Xilinx/Vitis/2022.1/settings64.sh`, `source /tools/Xilinx/Vitis_HLS/2022.1/settings64.sh`.
   Click `Save` to conserve the modified file, then close the file. 
   <img width="1536" alt="3-20-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/7459ee75-50dc-43ed-ba55-70d1ebeb0f6c">
   <img width="747" alt="3-20-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/b8f69d54-662b-4d4b-9935-295087d80f96">
   <img width="747" alt="3-20-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/12897156-db87-47a5-bf84-d3226a4c4027">

9. Back to the Terminal, Type the command: `source ~/.bashrc`. Finally, for test the installation.
   Type the command: `vitis` to launch VITIS IDE. 
   Type the command: `Vivado` to launch Vivado GUI. 
   Type the command: `vitis_hls` to launch VITIS HLS GUI.        
   <img width="740" alt="3-20-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/fca653b2-11b2-497c-a087-685690a9c2c9">
   
   <img width="959" alt="3-20-7" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/bea3de2a-f12f-4b19-85ea-c9eea31cbce4">
   <img width="1467" alt="3-20-8" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/6e83909d-dde3-47f6-a647-c00c0d1bcdff">
   
   <img width="933" alt="3-20-5" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/b219d224-7d3f-4a73-81ad-3a89697830af">
   <img width="1173" alt="3-20-6" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/419d2484-1579-44f5-8421-6bf18e745f35">

   <img width="933" alt="3-20-9" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/77b6ec03-41c2-4314-b893-34891f7ab24f">
   <img width="1464" alt="3-20-10" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/11c84fab-d1d8-4dc4-8e79-56aa2663c0c9">

---
