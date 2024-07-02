# Advanced-SoC-design 各lab實作結果上傳檔案的註記
This repository is created on 2024.3.1~

## Lab 1-1
1. 此work最初是從 [/bol-edu/fsic_fpga](https://github.com/bol-edu/fsic_fpga/tree/main) 這個repository所clone而來，而非由 [/bol-edu/caravel-soc_fpga-lab/fsic-sim](https://github.com/bol-edu/caravel-soc_fpga-lab/tree/main/fsic-sim) 而來。因此在 /bol-edu/caravel-soc_fpga-lab/fsic-sim 中所修改到的部分（詳見/bol-edu/caravel-soc_fpga-lab/fsic-sim的README.md中的`For more information`部分），以及`/reference_FIR`皆無出現在此。
2. 在其中的`/lab_1`為實作過程中完整的資料，而在外層的檔案則是從其中複製出workbook中所提到的相關檔案，其對應路徑如下表所示：
   | 分類 | 名稱 | 原路徑 |
   |:---------:|:---------:|:----------:|
   | Design source | /Design_sources/bram11.v | /lab_1/fsic_fpga/rtl/user/user_subsys/user_prj/user_prj1/rtl/bram11.v |
   | Design source | /Design_sources/fir.v | /lab_1/fsic_fpga/rtl/user/user_subsys/user_prj/user_prj1/rtl/fir.v |
   | Design source | /Design_sources/fir_ver1.v | /lab_1/fsic_fpga/rtl/user/user_subsys/user_prj/user_prj1/rtl/fir_ver1.v |
   | Design source | /Design_sources/multiplier_adder.v | /lab_1/fsic_fpga/rtl/user/user_subsys/user_prj/user_prj1/rtl/multiplier_adder.v |
   | Design source | /Design_sources/rtl.f | /lab_1/fsic_fpga/rtl/user/user_subsys/user_prj/user_prj1/rtl/rtl.f |
   | Design source | /Design_sources/user_prj1.v | /lab_1/fsic_fpga/rtl/user/user_subsys/user_prj/user_prj1/rtl/user_prj1.v |
   | Testbench | /Testbench/filelist | /lab_1/fsic_fpga/rtl/user/testbench/tc/filelist |
   | Testbench | /Testbench/tb_fsic.v | /lab_1/fsic_fpga/rtl/user/testbench/tb_fsic.v |
   | Testbench<br/>(after integrating fir.v into design) | /Testbench/xsim.log | /lab_1/fsic_fpga/rtl/user/testbench/tc/xsim.log |
3. To run the simulation of the testbench, use the following commands:
   ```
   cd /lab_1/fsic_fpga/rtl/user/testbench/tc
   ./run_xsim
   ```

## Lab 4 (Team work)
1. 此work是從 [/bol-edu/fsic_fpga](https://github.com/bol-edu/fsic_fpga/tree/main) 這個repository所clone而來，並放在[這個Github小組協作repository](https://github.com/ZheChen-Bill/ASoC_lab4_FSIC_FPGA)中，主要是關於lab4-3實作的內容，而 lab4-1 (simulation) 與 lab4-2 (validation) 的結果已在lab4-3的實作過程中被覆蓋掉。
2. To run the **simulation** of the testbench, use the following commands:
   ```
   cd /ASoC_lab4_FSIC_FPGA/vivado
   ./run_vivado_fsic_sim
   ```
3. To run the **FPGA validation**, use the following steps:
   1. ```
      cd /ASoC_lab4_FSIC_FPGA/vivado
      ./run_vivado_fsic
      ```
   2. Open Vivado GUI, and open project in `/ASoC_lab4_FSIC_FPGA/vivado/vvd_caravel_fpga` directory.
   3. 匯入 userDMA 的 Vitis project (已export成 Vivado IP) located in `/ASoC_lab4_FSIC_FPGA/vivado/vitis_prj/userdma_fir` directory.
   4. 開啟block design並將 userDMA 加入
   5. 用[這個討論區](https://github.com/bol-edu/HLS-SOC-Discussions/discussions/221)所述的方式接線：「兩條instream跟outstream需要自己手動接到userdmaso跟userdmasir」
   6. Generate bistream
   7. 將產生的.bit及.hwh檔放置於`/ASoC_lab4_FSIC_FPGA/vivado/jupyter_notebook_fir`資料夾
   8. 上傳相關檔案至 onlineFPGA，如[Github協作repository](https://github.com/ZheChen-Bill/ASoC_lab4_FSIC_FPGA/tree/main/vivado/jupyter_notebook_result)中的README.md的敘述

## Final project (Team work)
1. 此work是從 [lab4 的 repository](https://github.com/ZheChen-Bill/ASoC_lab4_FSIC_FPGA) 為基底，所繼續發展而來，並放在[這個Github小組協作repository](https://github.com/whywhytellmewhy/ASoC-Final_project-optical_flow)中，更詳細的實作流程的說明可參閱上述「Github小組協作repository」中的「README.md」

2. Final project的時程回顧
   | Proposal簡報檔繳交期限 | Proposal presentation<br/>(實體口頭報告) | lab5_fsic-ap<br/>(HLS實作進度) report繳交期限 | Intermediate status report | Final presentation簡報檔繳交期限 | Final presentation<br/>(實體口頭報告) | Final Report繳交期限 |
   |:---------:|:---------:|:----------:|:----------:|:----------:|:----------:|:----------:|
   | 2024.5.1 8:00 | 2024.5.1 | 2024.6.9 | 2024.6.14 | 2024.6.19 8:00 | 2024.6.19 | 2024.6.23 23:59 |

3. 相關的report及presentation檔案有上傳到 [/bol-edu/2024-Advanced-SOC/nthu/Team6--Optical_Flow](https://github.com/bol-edu/2024-Advanced-SOC/tree/main/nthu/Team6--Optical_Flow)，檔案說明如下：
   1. `Final_project_proposal_Team6.pptx`為proposal報告時所搭配的簡報檔，也是繳交至NTHU eeclass上的Final project proposal檔案
   2. `Final_project_intermediate_status_report_Team6.pdf`為繳交至NTHU eeclass上的Final project intermediate status report檔案
   3. `Final_project_presentation_Team6.pptx`為[Final project presentation報告](https://www.youtube.com/watch?v=nXY4YCJLHuk&list=PLTA_T2FLzYNBtCq70wCKWC5lS8P3_DVHI&index=3)時所搭配的簡報檔，此與上傳至 [ASoC Design 課程教材連結](https://drive.google.com/drive/folders/1cGNs2LfW5ZdoaEpi_Nh6iANl7V4f6rtv?usp=sharing)中的`/lab-presentation/nthu/final-project-presentation`是相同的檔案，但與繳交至NTHU eeclass上的Final project presentation檔案並不相同，而是更新的版本
   4. `Final_project_report_Team6.pdf`為繳交至NTHU eeclass上的**report檔案**

4. 沒有上傳「檔案太大(超過100MB)」的檔案（透過`run_list_big_files`偵測，且透過`run_delete_big_files`刪除），包含2個`.vcd`檔及2個`.wdb`檔


