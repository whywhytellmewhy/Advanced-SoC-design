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
