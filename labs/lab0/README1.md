# VMware Fusion 13 Player virtual machine + Ubuntu 20.04.6 LTS + Xilinx Vitis 2022.1 install on MacBook Pro with Intel Core i7 processor - Implement1

> **NOTE:** VMware Fusion: Desktop Hypervisors for Mac install on `Intel or Apple Silicon` Macs.
>
> **NOTE:** Xilinx tools support the operating systems on `x86 and x86-64` , `except arm64` processor architectures `up to Now`.
> That is to say, Apple M1/M2 Silicon with aarch64 architecture are different from the commonly used 64-bit CPU cores with x86_64 Intel architecture.
> `Xilinx tools` are built with executables for `Intel architecture`.


## Implement1: Install VMware Fusion 13 Player virtual machine to execute Ubuntu 20.04.6 LTS Operating System on MacBook Pro with Intel Core i7 processor

**Implement1 as the following steps and refer Illustration:**
1. Download [VMware Fusion: Desktop Hypervisors for Mac](https://www.vmware.com/products/fusion.html).
   **Note:** Choose `Use for Free with a Personal Use License`. Register an account to get dowload key, and login to choose `Manually Download`.
   <img width="1536" alt="1-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d008ba00-c236-47b3-874d-3edf05cd4589">
   <img width="1536" alt="1-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/e41f9709-3b6a-4a40-8960-06f71125d4bf">
   <img width="1536" alt="1-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/21740589-7571-40a3-bb56-326d6378e87b">
   
2. Download [Ubuntu 20.04.6 LTS (Focal Fossa)](https://releases.ubuntu.com/focal/).
   **Note:** Choose `64-bit PC (AMD64) desktop image`.
   <img width="1536" alt="1-10-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/69535320-ba70-4716-a2c4-9cf524e4ce3c">
   <img width="663" alt="1-10-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/9ca424e5-73fa-4a75-b25f-29ab7711b997">

3. Double click on the `VMware-Fusion-13.0.2.dmg` to keyin the license key for VMware Fusion 13 and start VMware Fusion Player - Personal Use - 13 installation.
   <img width="893" alt="1-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/90db4b96-95be-43f4-b1fa-2afa71937b62">
   <img width="338" alt="1-5" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/055ae8f8-6ab0-4f4c-893d-bc07595ac89e">
   <img width="1535" alt="1-6" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/3d59ab7d-3d96-42ba-8cf2-31ce6c8bf038">

4. Complete installation, open VMware Fusion 13 Player, drag the step 2. dowload image iso file `Ubuntu 20.04.6 LTS (Focal Fossa)`.             
   <img width="686" alt="1-7" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/191425da-e656-496f-98fc-9b97185d0160">
   <img width="641" alt="1-8" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/5739201d-e4ef-4890-a3da-81400553e9cb">
   <img width="643" alt="1-9" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/450f3500-4cb6-4d2f-8b53-9a320ac22e4e">
   <img width="1246" alt="1-10-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/54227170-3590-4464-b1d2-37895f4c6d3e">

5. Configure login information, then check summary list.
   **Note:** Choose `Customize Settings` to name the Ubuntu virtual machine. Enable `Share this virtual machine with other users on this Mac` and save to `other hard drive`.
   <img width="640" alt="1-11" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/16fbbd25-682f-4405-94b4-921557db1316">
   <img width="642" alt="1-12" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/03947043-27e6-4769-bbb0-2152df953a7f">
   <img width="803" alt="1-13" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/e356f488-297f-4d86-94ac-65da4d4a3f5b">

6. Allocate `4 processor cores`, `8GB Ram`. `Enable Shared Folders` as the `download` folder.
   <img width="804" alt="1-14-0" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/0155b679-60b5-49ec-a048-28fdafb3b6ad">
   <img width="804" alt="1-14" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/0ea9dd70-8515-4973-8f16-8dadcbebc1e2">
   <img width="806" alt="1-15" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/720cfb3d-68c0-4987-8005-777f0ead7641">

7. Specify the size of the Ubuntu virtual machine storage space to `400GB` and enable `pre-allocated disk space`. 
   **Note:** Xilinx Vitis and Vivado take up quite a bit of hard drive space in their current versions.
   <img width="801" alt="1-16" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/9f27ed29-3343-4bd6-ba0f-ce9b54506951">

8. Start VMware Fusion 13 Player to install Ubuntu Operating System. Proceed with the standard installation.
   <img width="1289" alt="1-17" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/31405ebe-790b-4c34-93ba-c03225e19455">
   <img width="1353" alt="1-18" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/f19d21b0-082a-42fa-9e6d-a9cb5dc3f4c4">
   <img width="800" alt="1-19" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/be37dede-b92d-4eb5-9891-891438f383dc">

9. Complete Ubuntu Operating System installation, close the virtual machine, `disenable connect CD/DVD player` then restart the virtual machine and `open in Terminal`.   
   <img width="804" alt="1-23-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/155c6871-59ba-48f1-98e8-d5cbf5fef8de">
   <img width="813" alt="1-23-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/c6ce94e0-402a-46fc-ba89-785477941cad">
   <img width="1536" alt="2-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d5ffc63a-6445-4197-b7ae-a6507e6aa9dc">

10. Type the command: `sudo apt install openssh-server` to install SSH Server.
    <img width="740" alt="2-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/bc28c402-1c77-495d-90c4-6219a30fd23a">

11. Type the command: `ifconfig` to find out which IP the virtual machine is connected to the physical machine through.
    **Note:** The IP is not necessarily the same in everyone's virtual machine.
    <img width="741" alt="2-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/ac60a597-6a30-4c1c-8c95-d55ee7606287">
    <img width="741" alt="2-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/adbe5e44-e944-49ab-8ea0-c25b280e89ce">

12. Type the command: `ssh -X [username]@[IP step11. found]`, such as `ssh -X trista@192.168.3.130` to SSH the remote Server.       
    <img width="743" alt="2-5" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/6d4df2f6-4bd3-46a7-931d-e6a1c5203eac">
 
---
