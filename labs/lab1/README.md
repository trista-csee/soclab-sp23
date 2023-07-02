# Xilinx Vitis HLS run Multiplication example on Ubuntu virtual machine in MacBook Pro with Intel Core i7 processor - Implement

> **NOTE:** 
> The implementation flow includes 1.Preparations, 2.Vitis HLS IP design Implementation, 3.Vivado IP import/Block design implementation, 4.Run PYNQ host program in sequence.
> 

## Implement: Xilinx Vitis 2022.1 run Multiplication example on Ubuntu 20.04.6 LTS + VMware Fusion 13 Player virtual machine in MacBook Pro with Intel Core i7 processor

**Implement as the following steps and refer Illustration:**

# 1.Preparations
1. Type the command: `sudo apt-get install build-essential -y` to install Prerequisite Package.
   <img width="742" alt="1-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/ac3030b4-0c42-46a3-a528-4059ee357415">
   
2. Type the command: `git clone https://github.com/bol-edu/course-lab_1 ~/workspace/course-lab_1` to 
   clone [Xilinx Vitis HLS Multiplication example](https://github.com/bol-edu/course-lab_1)
   to the lab directory of Ubuntu virtual machine **[~/workspace/course-lab_1]**.
   <img width="922" alt="1-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/150bbcd3-7010-4cbc-ae8c-bb895ad07094">

# 2.Vitis HLS IP design Implementation
1. **Creat Source Project**. Within the lab directory, Open in Terminal and Type the command: `vitis_hls` to invok Xilinx Vitis HLS.
   <img width="923" alt="1-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/94846933-7f1a-42ee-b2fc-a7af21035800">
   <img width="1460" alt="1-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/f41d16a6-444f-4a0c-b4ec-e5fbcde79655">

2. `Create Project` and name Project `hls_ip` under the lab directory **[~/workspace/course-lab_1]**.
   <img width="1465" alt="1-5" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/1788632d-834b-4b8e-9be0-be5f726558ce">
   <img width="1466" alt="1-6" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/33ab6d21-7f1e-413e-9e5c-965fdb242ed1">

3. Name Top Function `solution1`. **`DO NOT Add`** `Design Files & TestBench Files`.
   <img width="1466" alt="1-7" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/cd656c54-837d-418c-9b7e-ba144125489e">
   <img width="1467" alt="1-8" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/be3cf1c2-a78f-4064-8cc5-daad41c5b665">

4. Allocate `Clock period: 10 ns`, if Board: PYNQ-Z2 can run at a clock frequency above 200MHz. 
   Choose `part: xc7z020clg400-1`, the same part as PYNQ-Z2, because Xilinx Vitis 2022.1 version can not read the PYNQ-Z2 board file.
   <img width="1466" alt="1-9" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/21da3683-c9fa-48db-8aba-f6d658683c59">
   <img width="1465" alt="1-10" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d14f0db5-9773-4301-a740-0ca05be90988">
   <img width="1466" alt="1-11" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/db0caad3-548d-4943-ab3e-17abb95e4121">

5. In project hls_ip, `Righ click` on `Source`, choose `New Source File`, add `Multiplication.cpp` and `Multiplication.h` from **[~/workspace/course-lab_1/hls_Multiplication]**.
   <img width="1466" alt="1-12" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/2d8373b5-2494-4ade-9df7-c1a8364d7f59">
   <img width="1466" alt="1-13" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/27381943-7b2e-4ce9-ae8d-17b709d799e1">
   <img width="1466" alt="1-14" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/71b98cc6-9b90-42fe-a4bd-83bff0d4a119">
   <img width="1466" alt="1-15" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/aeb7939f-088e-44f0-bfc6-6c9bdf78ba9a">
   <img width="1464" alt="1-16" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/3094045f-4b5d-4178-9270-35057f9bbd44">

6. Open `Multiplication.cpp`, change to `#include Multiplication.h` from "#include multiplication.h". 
   **Note:** according to step7. add `Multiplication.h` and Ubuntu/Linux is case sensitivity.
   `Comment out #pragma HLS INTERFACE ap_ctrl_none port=return`, then save (ctrl+s).
   <img width="1467" alt="1-17" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/b123272d-55be-4ecb-b340-68d13eede9b1">

7. In project hls_ip, `Righ click` on `Test Bench`, choose `New Test Bench File`, add `MultipTester.cpp` from **[~/workspace/course-lab_1/hls_Multiplication]**.
   <img width="1465" alt="1-18" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/ac862cd3-64f6-4bcb-87ca-1e938d138900">
   <img width="1465" alt="1-19" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/6abc001c-cdd1-49a3-8d74-35e4e81cb7ca">
   <img width="1466" alt="1-20" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/31ee7dd1-b5ba-4cfc-9857-06c1ccc83748">

8. Open `MultipTester.cpp`, change to `#include Multiplication.h` from "#include multiplication.h". 
   **Note:** according to step7. add `Multiplication.h` and Ubuntu/Linux is case sensitivity then save (ctrl+s).
   <img width="1466" alt="1-21" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/b38d6e2e-a9e2-4a88-bd12-16f7cebcc397">

9. Choose `Project`, `Project Settings` in the left toolbar. Choose `Synthesis` within "Project Settings" and name `Top Function: multip_2num`. 
   **Note:** The project must specify Top Function exported by the IP. Top Function name is **Function name** in `Multiplication.cpp`.
   <img width="1466" alt="1-22" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/63a3bc85-2916-43c5-92bf-49c0365aa247">
   <img width="1467" alt="1-23" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/c5174a7b-4744-4bc0-a927-8ff7776b256d">
   <img width="1464" alt="1-24" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/da356b00-d7fd-41fc-b740-9c3a609ec46a">

10. **Directive Control**. **Note:** Directive must be added before starting Synthesis. There are two ways to add directive. 
    One is `inline - using #pragma`, and the other is controlled by `directives.tcl`. The Lab uses the first method, so there is no need to add additional Directive. 
    <img width="1464" alt="1-24-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/dd3add8a-246b-40c2-8125-d0dd8b901139">

11. **Start C Simulation validation**. The C Simulation source code files of Test Bench have already been imported into the project according to the above steps. 
    Execute the C Simulation to verify the execution results of the IP. The C Simulation result will be displayed in the console below.
    <img width="1466" alt="1-25" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/315a6f4f-e7e9-4bec-83cd-2af590a26ee8">
    <img width="1466" alt="1-26" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/6d191056-5715-4ea7-b5aa-e1dc4d0971c1">
    <img width="1465" alt="1-27" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/5dbf3d0e-b6dd-4751-b7f5-c393113fd90b">
    
12. **Start C Synthesis validation**. The C Synthesis result will be displayed in the console below.
    <img width="1467" alt="1-28" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/eee8a3bc-c718-4cad-b68d-9996b5c44797">
    <img width="1465" alt="1-29" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/e50afeb8-e1d1-40d9-9a7d-2973eea5bdad">
    <img width="1467" alt="1-30" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/25ef9462-b8aa-4f4f-bbc8-e42471591ced">

13. **Start C Cosimulation validation**. 
    **Note:** `Before C Cosimulation`, for Directive configuration, open `Multiplication.cpp`, `Comment out #pragma HLS INTERFACE ap_ctrl_none port=return`. 
    Within RTL Simulation setting, Select `Vivado XSIM`, `Dump Trace: all`. The C Cosimulation result will be displayed in the console below.
    <img width="1466" alt="1-31" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/aecec730-8439-499d-a760-e8891b68d56a">
    <img width="1466" alt="1-32" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/e21f09b7-1d8a-4f0a-b59d-d8524e04389e">
    <img width="1467" alt="1-33" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/3e5168a2-57c5-434e-9bdd-e804e435fe8c">

14. **Complete validations of C Simulation, C Synthesis, Cosimulation (Dump Trace all)**. `Open Wave Veiwer` for the Multiplication example.
    <img width="1466" alt="1-34" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/8e293f5f-d403-4b20-9898-c5fbc6b25757">

15. **Start Export IP**. 
    **Note:** `Before Export RTL as IP`, Open `Multiplication.cpp`, `remove comment out #pragma HLS INTERFACE ap_ctrl_none port=return`, and save (ctrl+s). 
    Then, **ReStart C Synthesis**, `before Export RTL as IP`. The C Synthesis result will be displayed in the console below.
    <img width="1464" alt="1-35" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d4063f54-d729-44ee-8ed0-8fb736de93ea">
    <img width="1464" alt="1-36" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/32216380-801d-40cc-acf6-078f5e9330fe">
    <img width="1467" alt="1-37" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/c8c3c804-e128-4620-8d9f-2963f0909397">
    <img width="1467" alt="1-38" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/66528004-19fd-49bb-97c2-e50b9f8da847">

16. **Exporting RTL as IP**. 
    The Multiplication example multip_2num is saved and exported as a IP by Vitis HLS in the project directory **[~/workspace/course-lab_1/hls_ip]**. 
    The Export RTL result will be displayed in the console below.
    **Note:** The IP will be reused in later `Vivado block design`.
    <img width="1465" alt="1-39" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/94580f8a-f801-40b5-85b4-d7e989d270e5">
    <img width="1466" alt="1-40" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/59f97d6f-067d-4c90-9bbf-797dd5101a11">
    <img width="1467" alt="1-41" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/2b22096f-517d-4b5b-ae81-57e7aa592338">                                                   

# 3.Vivado IP import/Block design Implementation
1. **Create Design Project**. Close Vitis HLS GUI. Type the command: `vivado` to invok Xilinx Vivado.
   `Create Project` and name Project `vivado` under the lab directory **[~/workspace/course-lab_1]**.
   <img width="1461" alt="2-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/62eaf05d-b8b0-4e25-b6aa-9e6aaa3290f2">
   <img width="1466" alt="2-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/457c7f4c-38ce-47d9-953f-7969adac4356">
   <img width="1466" alt="2-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/f3caaf34-1d56-4d6d-b1a5-41b0e2d7dd95">

2. Enable `Do not specify sources at this time`. **Note:** RTL Project, sources and constraints are left blank and added later. 
   Choose `part: xc7z020clg400-1`, the same part as PYNQ-Z2, because Xilinx Vitis 2022.1 version can not read the PYNQ-Z2 board file.
   <img width="1464" alt="2-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/f53172a7-0776-48ae-b22c-ccebf562a90f">
   <img width="1464" alt="2-5" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/b77d1d2e-cbec-4e65-95a3-82fe83ff1321">
   <img width="1465" alt="2-6" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/27cb521c-8c9e-4d39-acfa-2eedc462c95d"> 

3. **Start Import IP**. **Note:** The IP is exported by Vitis HLS in the project directory **[~/workspace/course-lab_1/hls_ip]** according to the above steps. 
   Choose `Settings` in the left Project Manager. Choose `IP`, `Repository` within "Project Settings". 
   `Add` IP Repositories, assign IP Repositories to the Vitis HLS project directory **[~/workspace/course-lab_1/hls_ip]**, select `Multip_2num`.
   <img width="1466" alt="2-7" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/739b44cb-935d-45fb-be21-6fb4e1866f7a">
   <img width="1464" alt="2-8" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/ee2d9647-90e1-444a-a6bd-ea08ece5f29f">
   <img width="1466" alt="2-9" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/0901576f-b71c-495c-b241-cc2cf6f84262">
   <img width="1465" alt="2-10" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/c30ab9bb-ab03-46d2-aed9-ab8a4aad083f">
   <img width="1463" alt="2-11" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/abb79d7b-077d-4de4-9f8b-6b7c1775503c">

4. **Before Block Design**. New Open in Terminal, 
   Type the command: `sudo apt update`, and `sudo apt install libcanberra-gtk-module libcanberra-gtk3-module -y` to install the Libcanberra library 
   which provides all the modules required to avoid failures loading the “canberra-gtk-module.
   <img width="933" alt="2-16-0" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/c814b913-8915-4b5e-8004-9c1f574fec8f">
   <img width="931" alt="2-16-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/e8c8d3cc-d3bc-4091-bfa7-12cda02fc1cc">
   <img width="735" alt="2-16-3拷貝" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/aede929d-6c92-4e8b-b474-13928237281d">

5. **Start Block Design**. Choose `Create Block Design` in the left Project Manager. Within "Diagram" tab,
   `Add IP` select `ZYNQ7 Processing System` and `multip_2num`.
   <img width="1465" alt="2-12" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/8ae9fb5e-ab77-4a50-9efc-f3c56b071df2">
   <img width="1466" alt="2-13" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/efa0cd65-c656-4f07-9a62-da3ff5fa206b">
   <img width="1466" alt="2-14" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/ea7d89fc-cb90-45bd-b61f-4f599ca8ee42">
   <img width="1466" alt="2-15" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/e6469f63-0bac-4422-9090-516b725dc6cf">
   <img width="1466" alt="2-16-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d958cb5b-b164-4555-b9a6-ad32ea5e025e">

6. `Regenerate layout`, then click `Run Block Automation`.  
   <img width="1466" alt="2-17" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/1fa1f59b-973d-4d63-ac53-fc1be7abc440">
   <img width="1464" alt="2-18" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/e3a018db-60e6-478f-b8ca-553fb280abe1">
   <img width="1462" alt="2-19" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/9c896d02-5d45-4168-95f4-7018a9830280">

7. Double click `ZYNQ7 Processing System` to open "Re-customize IP". 
   Click `Clock Configuration`, choose `PL Fabric Clocks`, `enable FCLK_CLK0`, reset `PCW FPGA0 PERIPHERAL FREQMHZ: 100`. **Note:** Due to the clock period is 10ns. 
   <img width="1466" alt="2-20" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/2252759c-f71e-44fc-8f90-03988b267198">
   <img width="1466" alt="2-21" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/585ce1e1-ec50-4078-b51b-250249c7f433">
   
8. After Run Block Automation, click `Run Connection Automation`. 
   **Note:** The block design only has one IP design, the connection can be completed automatically by the system.
   Complete Run Connection Automation, Choose `Diagram` tab, click `Regenerate Layout` to check whether the wiring is wrong, then switch to Address Editor tab to view the memory map.
   <img width="1462" alt="2-22" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d694b6dc-faa2-4485-9667-0087f78079dd">
   <img width="1465" alt="2-23" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d5697d2c-b697-4c71-b234-2fa21977d1d3">
   <img width="1466" alt="2-24" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/497e9ff8-68aa-4905-8c49-2b473dfc139d">

9. Within the `Sources` tab of the Block Design sub-window, choose `Design Sources`, Right click on `design_1`, choose `Create HDL Wrapper`. 
   The HDL Wrapper result will be displayed in the Tcl console below.
   <img width="1466" alt="2-25" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/81e28805-a732-466d-880f-fe2dcc741910">
   <img width="1466" alt="2-26" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/63dbe378-1894-42a8-8457-14a5c282e2e1">
   <img width="1465" alt="2-27" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/5f189f35-4a7f-4cc3-bb1e-fb48ea1ac261">

10. **Synthesis/Placement/Routing/Generate Bit-stream**. 
    Click `Generate Bitstream` in the top toolbar or in the left Project Manager to generate FPGA bitstream. 
    **Note:** The Synthesis/Placement/Routing steps are required to generate the bit-stream file, but the single-step process can be omitted, 
    and Vivado IDE can automatically complete all the processes with one-click execution.
    <img width="1466" alt="2-28" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/b44d92f1-a4b2-462b-9027-8f8d4a60a7d3">
    <img width="1466" alt="2-29" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/7a50e88b-32a1-438d-bde2-a7c88df52140">
    <img width="1465" alt="2-30" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/5b28f077-39e8-46c6-bbaf-c420edc73fcd">
    <img width="1465" alt="2-31" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/2040e0db-529c-48ba-bde2-f5a56554b204">
    <img width="1467" alt="2-32" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/08b1d0ef-6e94-430b-8d17-00b15a9141e9">

11. **Bit-stream Transfer from Development Kit to Device**. 
    After Bitstream Generation successfully completed, the bitstream files are ready to download via `Shared Folders` from Ubuntu virtual machine to MacBook Pro host. 
    <img width="1467" alt="2-33" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/aacebb3a-26fb-4840-9a46-c94074a05d15">
    <img width="1466" alt="2-34" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/9fe1a349-ed2c-403c-83fc-4fae11382a6d">

12. To Transfer the bitstream files from Development Kit to Device, first **Ubuntu virtual machine completes sharing setting**. 
    <img width="814" alt="3-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/ca2a5c01-1c59-49eb-a004-89503a0b037b">
    <img width="817" alt="3-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/56443028-4e86-4f78-b3f2-bc6307c127a5">
    <img width="908" alt="3-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/71cc3ba6-4211-4f2a-951b-7ebf0f3e7e70">
    <img width="817" alt="3-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/2c5f0a48-9f64-41ad-8ca4-57c90bf5215d">

13. Open in Terminal, Type the command: `sudo gedit /etc/fstab` to edit /etc/fstab. 
    Add an entry `vmhgfs-fuse   /mnt/hgfs    fuse    defaults,allow_other    0    0` in the last empty line to mount the Shared Folder automatically on boot.
    **Note:** If the VM is powered on, disable and enable the Shared Folder feature from the interface. For resolving the issue permanently, edit /etc/fstab 
    and add an entry to mount the Shared Folder automatically on boot.
    <img width="908" alt="3-5" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/1a4d8341-3ca2-4065-927a-403bc3809c4b">
    <img width="815" alt="3-6" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/b7f6c349-e161-47e4-a443-ef50f8ae3707">
    <img width="793" alt="3-7" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/51fb2b5f-46f5-4144-86e1-1ff3d7bf9ea9">

14. Type the command: `sudo cp -f ~/workspace/course-lab_1/vivado/vivado.runs/impl_1/design_1_wrapper.bit /mnt/hufs/ubuntushared/Multip2Num.bit`, 
    and `sudo cp -f ~/workspace/course-lab_1/vivado/vivado.gen/sources_1/bd/design_1/hw_handoff/design_1.hwh /mnt/hufs/ubuntushared/Multip2Num.hwh` 
    to copy design_1_wrapper.bit, design_1.hwh required for FPGA operation from the Vivado project directory **[~/workspace/course-lab_1/vivado]** 
    to the Shared Folder in Ubuntu virtual machine **[~/mnt/hufs/ubuntushared]**, and `Rename` as `Multip2Num.bit`, `Multip2Num.hwh`.
    <img width="1453" alt="3-8" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/17f7d610-061d-4dd2-80ef-a6f04ea22d16">

# 4.Run PYNQ host program
1. Transfer `Multip2Num.bit`, `Multip2Num.hwh` to PYNQ-Z2 board via `Shared Folders` from Ubuntu virtual machine to MacBook Pro host.  
   <img width="794" alt="3-11" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/88f6519e-63b6-4ca3-8114-637d3e2cecf1">

2. `In MacBook Pro host`, Open in Terminal, Type the command: `ssh -X -p 1000 boledupynq@140.112.207.200` 
   to `access to OnlineFPGA service`. Enter `1` to start login, enter `the register email and password` to complete login.
   Enter `2` to rent a specified device board. Enter `1` to select `pynq`. Enter `1` by choice or enter `2` by assignment.
   **Note:** Access to the pynq-z2 board from OnlineFPGA via `opening web browser to login the given URL`.
   <img width="939" alt="4-1" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/bc8e7f15-71ee-475c-a4c8-ea3557d0d8cc">
   <img width="1271" alt="4-2" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/ab25d4cb-c57c-4689-8d85-61086c85b4de">

3. `Upload` `Multip2Num.bit`, `Multip2Num.hwh` from `ubuntushared`, the Shared Folder from Ubuntu virtual machine to MacBook Pro host, 
   and [Multip2Num.ipynb](https://github.com/bol-edu/course-lab_1/blob/2022.1/ipy_Multip2Num/Multip2Num.ipynb) to Jupyter Notebook from local host via web browser.
   <img width="1536" alt="4-3" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/d41c66ec-6085-4840-98ee-1ed7bb1a5264">
   <img width="1536" alt="4-4" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/f976ede1-6bf9-4e30-8a1d-a10238e5f5c1">

4. Click `Multip2Num.ipynb` to open in new tab, and `Run` the cell. Finally, The verified multiplier multip_2num work correctly on FPGA board.
   <img width="1536" alt="4-5" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/b90cadd9-acac-4718-a121-d709d7f5acea">
   <img width="1536" alt="4-6" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/9fc4d93b-3243-486b-8593-0e2fe8ccc354">
   <img width="1536" alt="4-7" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/3b7a9930-f323-44aa-a3c0-510dac8eab84">
   <img width="1536" alt="4-8" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/c2659f91-3f59-4cc2-ae21-25c4ac2cabfb">
   <img width="1536" alt="4-9" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/674127e7-684d-46c0-861f-04e8e8676c68">

5. Back in Terminal, Enter `3` to return the rented device board. 
   Enter `the device name` to complete returning the device. Enter `0` to exit OnlineFPGA service.
   <img width="865" alt="4-10" src="https://github.com/trista-csee/soclab-sp23/assets/137249599/67aba9fa-2732-4038-855d-cab703659cd6">

---
