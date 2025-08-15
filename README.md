# RISC-V Pipelined Processor

A complete implementation of a 5-stage pipelined RISC-V processor with hazard detection and bubble sort algorithm execution, developed as part of Computer Architecture coursework at Habib University.

## 🎯 Project Overview

This project demonstrates the design and implementation of a fully functional RISC-V processor that progresses from a single-cycle implementation to a sophisticated pipelined architecture with hazard detection capabilities.

**Key Features:**
- ✅ Single-cycle RISC-V processor implementation
- ✅ 5-stage pipeline architecture (IF, ID, EX, MEM, WB)
- ✅ Comprehensive hazard detection and handling
- ✅ Data forwarding unit implementation
- ✅ Bubble sort algorithm execution and verification
- ✅ Performance analysis and comparison

## 🏗️ Architecture

### Pipeline Stages
1. **Instruction Fetch (IF)** - Fetches instructions from memory
2. **Instruction Decode (ID)** - Decodes instructions and reads registers
3. **Execute (EX)** - Performs ALU operations
4. **Memory Access (MEM)** - Handles load/store operations
5. **Write Back (WB)** - Writes results back to registers

### Pipeline Registers
- **IF/ID** - Stores instruction and PC between fetch and decode
- **ID/EX** - Stores control signals and data between decode and execute
- **EX/MEM** - Stores ALU results and memory control signals
- **MEM/WB** - Stores data for register write-back

## 📁 Project Structure

```
RISC-V-pipelined-processor/
├── task1/                  # Single-cycle processor implementation
├── Task 2 pipelined/       # Pipelined processor without hazard detection
├── Task 3/                 # Complete pipelined processor with hazard detection
├── CA_Project_Report.pdf   # Comprehensive project documentation
├── pipeline.png           # Pipeline architecture diagram
└── README.md              # Project documentation
```

## 🚀 Implementation Tasks

### Task 1: Single-Cycle Processor
- **Objective**: Implement bubble sort in RISC-V assembly and execute on single-cycle processor
- **Key Components**:
  - ALU with support for arithmetic and branch operations
  - Branch unit for conditional operations
  - Memory initialization with sorting algorithm
  - Support for 64-bit operations

### Task 2: Pipeline Implementation
- **Objective**: Convert single-cycle processor to 5-stage pipeline
- **Achievements**:
  - Successfully implemented pipeline registers
  - Added forwarding unit for data dependency resolution
  - Verified pipeline functionality with individual instruction testing

### Task 3: Hazard Detection
- **Objective**: Implement comprehensive hazard detection and handling
- **Features**:
  - **Data Hazards**: Detected and resolved through forwarding
  - **Control Hazards**: Handled via pipeline flushing
  - **Structural Hazards**: Managed through pipeline stalling
  - Hazard detection unit integration with forwarding logic

## 🔧 Technical Specifications

**Architecture**: RISC-V 64-bit  
**Pipeline Stages**: 5 (IF, ID, EX, MEM, WB)  
**Hazard Handling**: Forwarding, Stalling, Flushing  
**Test Algorithm**: Bubble Sort  
**Development Tools**: Vivado, Venus RISC-V Simulator  
**HDL**: Verilog/SystemVerilog  

## 📊 Performance Analysis

| Processor Type | Execution Time | Notes |
|----------------|----------------|-------|
| Single-Cycle   | ~3000ns       | Baseline implementation |
| Pipelined      | ~6000ns       | Current implementation with optimization opportunities |

**Note**: The pipelined processor shows higher latency in current implementation due to hazard handling overhead. Further optimization is planned to achieve expected performance improvements.

## 🛠️ Getting Started

### Prerequisites
- Xilinx Vivado Design Suite
- Venus RISC-V Simulator (for assembly verification)
- Basic understanding of computer architecture and Verilog HDL

### Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/RISC-V-pipelined-processor.git
   ```

2. Open the desired task folder in Vivado

3. Load the project files and run simulation

4. Observe the sorting algorithm execution and pipeline behavior

## 📈 Key Learning Outcomes

- Deep understanding of RISC-V instruction set architecture
- Hands-on experience with pipeline design and implementation
- Practical knowledge of hazard detection and resolution techniques
- Performance analysis skills for processor architectures
- Hardware description language (Verilog) proficiency

## 🤝 Contributors

**Team Members:**
- Basil Khowaja
- Hania Kashif  
- Saif Nazir

**Research Assistant:** Haseeb Khan  
**Course Instructor:** Dr. Muhammad Farhan

**Institution:** Habib University  
**Course:** CE/CS - 321/330: Computer Architecture  
**Semester:** Fall 2023

## 📚 References

- *Computer Organization and Design: The Hardware/Software Interface RISC-V Edition* by David A. Patterson, John L. Hennessy
- Course materials and laboratory exercises

## 🚧 Future Improvements

- [ ] Optimize pipeline performance to achieve sub-3000ns execution time
- [ ] Implement branch prediction for better control hazard handling
- [ ] Add cache memory support
- [ ] Extend instruction set support
- [ ] Implement out-of-order execution capabilities

## 📄 Documentation

For detailed technical documentation, implementation details, and simulation results, please refer to the [Project Report](CA_Project_Report.pdf).

---

**Disclaimer**: This project was developed for educational purposes as part of a Computer Architecture course. The implementation demonstrates fundamental concepts of processor design and pipelining.
