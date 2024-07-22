# Pipelined CPU Project

This is a ModelSim project that implements a MIPS pipelined CPU using Verilog. This project builds upon the concepts from the single cycle CPU to create a more efficient CPU by using pipelining.

## Phase 1

- IF/ID (Instruction Fetch/Instruction Decode): This register holds the instruction fetched from memory and the incremented PC value, passing them to the next stage.
- ID/EX (Instruction Decode/Execution): This register stores the decoded instruction, read data from the registers, and control signals, preparing them for the execution stage.
- EX/MEM (Execution/Memory Access): This register captures the results of the ALU operations, the data to be written to memory, and control signals, moving them to the memory access stage.
- MEM/WB (Memory Access/Write Back): This register holds the data read from memory or the ALU result, along with control signals, and passes them to the final stage for writing back to the register file.

## Datapath

![Datapath](https://i.imgur.com/LNYuwiF.jpeg)

## Requirements

- ModelSim
- Verilog compiler
- A basic understanding of Verilog and digital logic

## Running the Project

Clone the project

```bash
git clone https://github.com/VesalBargi/verilog-pipeline.git
```

Open ModelSim and load the project

```bash
ModelSim> project open Pipeline_Phase_3.mpf
```

Compile all Verilog files

```bash
ModelSim> vlog *.v
```

Run the simulation

```bash
ModelSim> vsim test_Main
ModelSim> run -all
```

## Testing

- Testbenches are provided for each pipeline stage.
- Ensure all testbenches pass before running the full CPU simulation.

## License

This project is licensed under the MIT License.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)