# NASSCOM RISC-V based MYTH Program Notes

This repository contains day-wise notes, lab writeups, and lecture documentation for the NASSCOM RISC-V based MYTH program.

---

## RV Day 1 - Introduction to RISC-V ISA and GNU compiler toolchain

### D1SK1 - Introduction to RISC-V basic keywords
- [0-RV_D1SK1_L1_Introduction](day1/0-RV_D1SK1_L1_Introduction.md)
- [1-RV_D1SK1_L2_From Apps To Hardware](day1/1-RV_D1SK1_L2_From_Apps_To_Hardware.md)
- [2-RV_D1SK1_L3_Detailed Description Of Course Content](day1/2-RV_D1SK1_L3_Detailed_Description_Of_Course_Content.md)

### D1SK2 - Labwork for RISC-V software toolchain
- [3-RV_D1SK2_L1_C Program To Compute Sum From 1 to N](day1/3-RV_D1SK2_L1_C_Program_To_Compute_Sum_From_1_to_N.md)
- [4-RV_D1SK2_L2_RISCV GCC compile And Disassemble](day1/4-RV_D1SK2_L2_RISCV_GCC_compile_And_Disassemble.md)
- [5-RV_D1SK2_L3_Spike Simulation And Debug](day1/5-RV_D1SK2_L3_Spike_Simulation_And_Debug.md)

### D1SK3 - Integer number representation
- [6-RV_D1SK3_L1_Bit_Number_System_For_Unsigned_Numbers](day1/6-RV_D1SK3_L1_Bit_Number_System_For_Unsigned_Numbers.md)
- [7-Bit Number System For Signed Numbers](day1/7-Bit_Number_System_For_Signed_Numbers.md)
- [8-RV_D1SK3_L3_Lab For Signed And Unsigned Numbers](day1/8-RV_D1SK3_L3_Lab_For_Signed_And_Unsigned_Numbers.md)

---

## RV Day 2 - Introduction to ABI and basic verification flow

### D2SK1 - Application Binary Interface (ABI)
- [9-RV_D2SK1_L1_Introduction To Application Binary Interface](day2/9-RV_D2SK1_L1_Introduction_To_Application_Binary_Interface.md)
- [10-RV_D2SK1_L2_Memory Allocation For Double Words](day2/10-RV_D2SK1_L2_Memory_Allocation_For_Double_Words.md)
- [11-RV_D2SK1_L3_Load, Add And Store Instructions With Example](day2/11-RV_D2SK1_L3_Load_Add_And_Store_Instructions_With_Example.md)
- [12-registers And Their Respective ABI Names](day2/12-registers_And_Their_Respective_ABI_Names.md)

### D2SK2 - Lab work using ABI function calls
- [13-RV_D2SK2_L1_Study New Algorithm For Sum 1 to N Using ASM](day2/13-RV_D2SK2_L1_Study_New_Algorithm_For_Sum_1_to_N_Using_ASM.md)
- [14-RV_D2SK2_L2_Review ASM Function Call](day2/14-RV_D2SK2_L2_Review_ASM_Function_Call.md)
- [15-RV_D2SK2_L3_Simulate New C Program With Function Call](day2/15-RV_D2SK2_L3_Simulate_New_C_Program_With_Function_Call.md)

### D2SK3 - Basic verification flow using iverilog
- [16-Program On RISC-V CPU](day2/16-Program_On_RISC-V_CPU.md)

---

## RV Day 3 - Digital Logic with TL-Verilog and Makerchip

### D3SK1 - Combinational logic in TL-Verilog using Makerchip
- [17-RV_D3SK1_L0_Welcome](day3/17-RV_D3SK1_L0_Welcome.md)
- [18-RV_D3SK1_L1_Introduction To Logic Gates](day3/18-RV_D3SK1_L1_Introduction_To_Logic_Gates.md)
- [19-RV_D3SK1_L2_Basic Mux Implementation And Introduction To Makerchip](day3/19-RV_D3SK1_L2_Basic_Mux_Implementation_And_Introduction_To_Makerchip.md)
- [20-RV_D3SK1_L3_Labs For Combinational Logic](day3/20-RV_D3SK1_L3_Labs_For_Combinational_Logic.md)

### D3SK2 - Sequential logic
- [21-RV_D3SK2_L1_Introduction To Sequential Logic And Counter Lab](day3/21-RV_D3SK2_L1_Introduction_To_Sequential_Logic_And_Counter_Lab.md)
- [22-RV_D3SK2_L2_Sequential Calculator Lab](day3/22-RV_D3SK2_L2_Sequential_Calculator_Lab.md)

### D3SK3 - Pipelined logic
- [23-Timing](day3/23-Timing.md)
- [24-RV_D3SK3_L2_Pipeline Logic Advantages And Demo In Platform](day3/24-RV_D3SK3_L2_Pipeline_Logic_Advantages_And_Demo_In_Platform.md)
- [25-RV_D3SK3_L3_Lab On Error Conditions Within Computation Pipeline](day3/25-RV_D3SK3_L3_Lab_On_Error_Conditions_Within_Computation_Pipeline.md)
- [26-Cycle Calculator](day3/26-Cycle_Calculator.md)

### D3SK4 - Validity
- [27-RV_D3SK4_L1_Introduction To Validity And Its Advantages](day3/27-RV_D3SK4_L1_Introduction_To_Validity_And_Its_Advantages.md)
- [28-RV_D3SK4_L2_Lab On Validity And Valid When Condition](day3/28-RV_D3SK4_L2_Lab_On_Validity_And_Valid_When_Condition.md)
- [29-RV_D3SK4_L3_Lab To Compute Total Distance](day3/29-RV_D3SK4_L3_Lab_To_Compute_Total_Distance.md)
- [30-cycle Calculator with Validity](day3/30-cycle_Calculator_with_Validity.md)
- [31-RV_D3SK4_L5_Calulator Single Value Memory Lab](day3/31-RV_D3SK4_L5_Calulator_Single_Value_Memory_Lab.md)

### D3SK5 - Hierarchy concept
- [32-(Bonus) RV_D3SK5_L1_Introduction To Hierarchy Concept](day3/32-Bonus_RV_D3SK5_L1_Introduction_To_Hierarchy_Concept.md)
- [33-RV_D3SK5_L2_Day3_closer](day3/33-RV_D3SK5_L2_Day3_closer.md)

---

## RV Day 4 - Basic RISC-V CPU micro-architecture

### D4SK1 - Introduction to Simple RISC-V Micro-architecture
- [34-architecture of Single Cycle RISC-V CPU](day4/34-architecture_of_Single_Cycle_RISC-V_CPU.md)
- [35-V Labs Part-1](day4/35-V_Labs_Part-1.md)
- [36-V Labs Part-2](day4/36-V_Labs_Part-2.md)

### D4SK2 - Fetch and decode
- [37-RV_D4SK2_L1_Implementation Plan and Lab for PC](day4/37-RV_D4SK2_L1_Implementation_Plan_and_Lab_for_PC.md)
- [38-RV_D4SK2_L2_Lab For Instruction Fetch Logic](day4/38-RV_D4SK2_L2_Lab_For_Instruction_Fetch_Logic.md)
- [39-RV_D4SK2_L3_Lab For RV Instruction Types IRSBJU Decode Logic](day4/39-RV_D4SK2_L3_Lab_For_RV_Instruction_Types_IRSBJU_Decode_Logic.md)
- [42-ISBUJ](day4/42-ISBUJ.md)
- [43-RV_D4SK2_L7_Lab To Decode Individual Instruction](day4/43-RV_D4SK2_L7_Lab_To_Decode_Individual_Instruction.md)

### D4SK3 - RISC-V control logic
- [44-RV_D4SK3_L1_Lab For Register File Read Part1 (USE UPDATED SHELL CODE)](day4/44-RV_D4SK3_L1_Lab_For_Register_File_Read_Part1.md)
- [45-2](day4/45-2.md)
- [46-RV_D4SK3_L3_Lab For ALU Operations For add/addi](day4/46-RV_D4SK3_L3_Lab_For_ALU_Operations_For_add_addi.md)
- [47-RV_D4SK3_L4_Lab For Register File Write](day4/47-RV_D4SK3_L4_Lab_For_Register_File_Write.md)
- [48-RV_D4SK3_L5_Concept of Array And Register File Details](day4/48-RV_D4SK3_L5_Concept_Of_Array_And_Register_File_Details.md)
- [49-RV_D4SK3_L6_Lab For Implementing Branch Instructions](day4/49-RV_D4SK3_L6_Lab_For_Implementing_Branch_Instructions.md)
- [50-RV_D4SK3_L7_Lab For Completing Branch Instruction Implementation](day4/50-RV_D4SK3_L7_Lab_For_Completing_Branch_Instruction_Implementation.md)
- [51-RV_D4SK3_L8_Lab To Create Simple Testbench](day4/51-RV_D4SK3_L8_Lab_To_Create_Simple_Testbench.md)

---

## RV Day 5 - Complete Pipelined RISC-V CPU micro-architecture

### D5SK1 - Pipelining the CPU
- [52-RV_D5SK1_L1_Introduction To Control Flow Hazard And Read After Write Hazard](day5/52-RV_D5SK1_L1_Introduction_To_Control_Flow_Hazard_And_Read_After_Write_Hazard.md)
- [53-Cycle Valid Signal](day5/53-Cycle_Valid_Signal.md)
- [54-Cycle RISC-V To Take Care Of Invalid Cycles](day5/54-Cycle_RISC-V_To_Take_Care_Of_Invalid_Cycles.md)
- [55-Cycle RISC-V To Distribute Logic](day5/55-Cycle_RISC-V_To_Distribute_Logic.md)

### D5SK2 - Solutions to Pipeline Hazards
- [56-After-Wr Hazard](day5/56-After-Wr_Hazard.md)
- [57-RV_D5SK2_L2_Lab For Branches To Correct The Branch Target Path](day5/57-RV_D5SK2_L2_Lab_For_Branches_To_Correct_The_Branch_Target_Path.md)
- [58-RV_D5SK2_L3_Lab To Complete Instruction Decode Except Fence, Ecall, Ebreak](day5/58-RV_D5SK2_L3_Lab_To_Complete_Instruction_Decode_Except_Fence_Ecall_Ebreak.md)
- [59-RV_D5SK2_L4_Lab To Code Complete ALU](day5/59-RV_D5SK2_L4_Lab_To_Code_Complete_ALU.md)

### D5SK3 - Load/Store Instructions and Completing RISC-V CPU
- [60-RV_D5SK3_L1_Introduction To Load Store Instructions And Lab To Redirect Loads](day5/60-RV_D5SK3_L1_Introduction_To_Load_Store_Instructions_And_Lab_To_Redirect_Loads.md)
- [61-RV_D5SK3_L2_Lab To Load Data From Memory To Register File](day5/61-RV_D5SK3_L2_Lab_To_Load_Data_From_Memory_To_Register_File.md)
- [62-RV_D5SK3_L3_Lab To Instantiate Data Memory To The CPU](day5/62-RV_D5SK3_L3_Lab_To_Instantiate_Data_Memory_To_The_CPU.md)
- [63-RV_D5SK3_L4_Lab To Add Stores And Loads To The Test Program](day5/63-RV_D5SK3_L4_Lab_To_Add_Stores_And_Loads_To_The_Test_Program.md)
- [64-RV_D5SK3_L5_Lab To Add Control Logic For Jump Instructions](day5/64-RV_D5SK3_L5_Lab_To_Add_Control_Logic_For_Jump_Instructions.md)
- [65-RV_D5SK3_L6_Wrap Up](day5/65-RV_D5SK3_L6_Wrap_Up.md)