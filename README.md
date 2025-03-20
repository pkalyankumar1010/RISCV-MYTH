# RISCV-MYTH


- Follow VSDSquadronFMDatasheet.pdf and follow instructions
    - Download vdi file https://forgefunder.com/~kunal/riscv_workshop.vdi
    - Install Oracle Virtualbox https://www.virtualbox.org/wiki/Downloads
- Progress doc 
    - https://docs.google.com/spreadsheets/d/1GMimG56cLoMpC9Us7Ub7hMD22D16zcsfcVL7WmjurcE/edit?gid=0#gid=0

<details close>
<summary>Course Videos</summary>
    <br>
    <span>https://github.com/pkalyankumar1010/RISCV-MYTH-Course-Videos</span>
</details>

- TASK 0 
    - Created lab setup with OracleVirtual box and risv_workshop.vdi
    - ![setup](./images/myth_worskop_setup.jpg)
# **Day 1**
    - 
# **Day 2**
    - 
# **Day 3**
    - https://github.com/stevehoover/RISC-V_MYTH_Workshop?tab=readme-ov-file

## Buiding a RISCV-Core [Top](#RISCV-MYTH)

### Digital logic with TL-verilog in Makerchip IDE
- TL-verilog is extension of verilog called Transaction Level Verilog
- Topics
    - Logic gates
    - Makerchip platform
    - Combinational logic
    - Seqential logic
    - Pipelined logic
    - State
- Resources
    - https://github.com/stevehoover/RISC-V_MYTH_Workshop?tab=readme-ov-file

- Logic gates
    - ![alt text](./images/myth_worskop_logic_gates.jpg)
- And some other basic things
- Launching Makerchip 
- Lab : Combinational logic
    - ![alt text](./images/combinational_logic.png)
    - https://makerchip.com/sandbox/0Z6fMhxVk/02Rhp0Q
- Lab : Vector
    - ![alt text](./images/vectors.png)
- Lab : Mux
    - ![alt text](./images/mux.png)
- Lab : Comninational Calcualtor
    - ![alt text](./images/combinational_calculator.png)
- Lab : Counter
    - `>>1$num` mean 1 clock cycle before value f(t-1)
    - ![alt text](./images/counter_problem.png)
    - ![alt text](./images/counter.png)
- Lab : Sequential Calculator
    - ![alt text](./images/seq_calc_prob.png)
    - ![alt text](./images/seq_calc.png)

    - ```v
        $val1[31:0] = >>1$out;
        //$val2[31:0] = 32'b1;
        $sum[31:0] = $val1[31:0] + $val2[31:0];
        $diff[31:0] = $val1[31:0] - $val2[31:0];
        $prod[31:0] = $val1[31:0] * $val2[31:0];
        $quot[31:0] = $val1[31:0] / $val2[31:0];
        $out[31:0] =  $reset ? 32'b0 : (
                            ($op[1:0] == 2'b00) ? $sum[31:0] :
                            ($op[1:0] == 2'b01) ? $diff[31:0] :
                            ($op[1:0] == 2'b10) ? $prod[31:0] :
                            ($op[1:0] == 2'b11) ? $quot[31:0] : 32'b0 )
                            ;
        ```
- Should start with RV_D3SK3_L1_Pipelined Logic And Re-Timing video Tomorrow
### Coding a RISC-V CPU Subset

### Pipelining and Completing your CPU
