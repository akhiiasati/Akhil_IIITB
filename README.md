# Physical Design Using ASIC

## Content
- [Day 0: Software Installation](#day-0-software-installation)
- [Day 1: Introduction to Verilog RTL Design and Synthesis](#day-1-introduction-to-verilog-rtl-design-and-synthesis)
- [Day 2: Timing libs, hierarchical vs flat synthesis and efficient flop coding styles](#day-2-timing-libs-hierarchical-vs-flat-synthesis-and-efficient-flop-coding-styles)
- [Day 3: Combinational and sequential optmizations](#day-3-combinational-and-sequential-optmizations)
- [Day 4: GLS, blocking vs non-blocking and Synthesis-Simulation mismatch](#day-4-GLS-blocking-vs-non-blocking-and-synthesis-Simulation-mismatch)
- [Day 5: If, case, for loop and for generate](#Day-5-if-case-for-loop-and-for-generate)
- [References](#references)

## Day 0: Software Installation

<p>List of necessary Tools:</p>

- [Icarus Verilog](#icarus-verilog)
- [Yosys](#yosys)
- [GTKwave](#gtkwave)
- [OpenSTA](#opensta)
- [NGSpice](#ngspice)
- [Magic](#magic)
- [OpenLANE](#openlane)
  

## Icarus Verilog

### Overview:
Icarus Verilog is an open-source hardware description language (HDL) compiler and simulator. It allows users to describe digital systems using a hardware description language and simulate their behavior. This brief guide provides an introduction to Icarus Verilog for your GitHub documentation, covering key features, installation, basic usage, and important links.

### Key Features:

1.HDL Support: Icarus Verilog supports both Verilog (IEEE Standard 1364) and SystemVerilog (IEEE Standard 1800) hardware description languages.

2.Cross-Platform: It is cross-platform and can be used on various operating systems including Linux, Windows, and macOS.

3.Simulation: Icarus Verilog simulates digital designs, helping users verify their functionality before actual hardware implementation.

4.VCD File Generation: It produces Value Change Dump (VCD) files which allow visualizing waveform simulations in waveform viewer tools.

5.Open-Source: Being open-source, Icarus Verilog encourages community contribution and enhancement.

### Installation:

To install Icarus Verilog on Ubuntu, use the following command in the terminal:</p>

```bash
$ sudo apt-get update
$ sudo apt-get install iverilog

```
Screenshot after installation-
![Screenshot from 2023-08-13 17-59-59](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/8c368b03-67e9-44f3-89b8-caba407cac15)


## Yosys

### Overview:
Yosys is an open-source framework for Verilog RTL synthesis. It takes RTL (Register Transfer Level) descriptions written in Verilog and transforms them into optimized gate-level representations. This brief guide provides an introduction to Yosys for your GitHub documentation, covering key features, installation, basic usage, and important links.

### Key Features:

1.RTL Synthesis: Yosys performs RTL synthesis, converting high-level RTL code into a gate-level representation suitable for implementation on hardware.

2.Open-Source: Yosys is open-source software, encouraging community collaboration, improvement, and customization.

3.Wide Hardware Support: It supports a wide range of FPGA and ASIC architectures, making it versatile for various hardware design projects.

4.Optimization: Yosys applies various optimization techniques to improve the efficiency and performance of the synthesized hardware.

5.Scriptable Flow: Yosys can be scripted using synthesis scripts written in a simple and powerful scripting language.

### Installation:

To install Yosys on Ubuntu, use the following command in the terminal:</p>

```bash
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys-master 
$ sudo apt install make (If make is not installed please install it) 
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make 
$ sudo make install
```
Screenshot after installation-
![Yosys](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/edca2369-c785-4b3e-80ef-b768361f0444)


## GTKWave

### Overview:
GTKWave is an open-source waveform viewer that allows you to visualize and analyze simulation results in the form of Value Change Dump (VCD) files. It provides an intuitive graphical interface to view waveforms and helps you understand the behavior of digital designs. This brief guide introduces GTKWave for your GitHub documentation, covering key features, installation, basic usage, and important links.

### Key Features:

1.Waveform Visualization: GTKWave provides a user-friendly interface to display and analyze simulation waveforms from VCD files.

2.Zoom and Pan: You can zoom in and out on specific parts of the waveform and pan through the time axis for detailed analysis.

3.Signals Hierarchy: Waveform signals are organized hierarchically, making it easy to navigate and locate specific signals.

4.Color Customization: Customize waveform colors and display options for a personalized viewing experience.

5.Cross-Platform: GTKWave is available for Linux, Windows, and macOS platforms.

### Installation:

To install GTKwave on Ubuntu, use the following command in the terminal:

```bash
$ sudo apt update
$ sudo apt install gtkwave
```
Screenshot after installation-
![GTKwave](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/210934bb-e8e1-479d-afae-d0d2807e61ed)


## OpenSTA
  
### Overview:
OpenSTA (Static Timing Analysis) is an open-source tool used for analyzing and optimizing the timing performance of digital designs. It performs static timing analysis to ensure that a design meets timing requirements, helping to identify potential issues before fabrication or implementation. This brief guide introduces OpenSTA for your GitHub documentation, covering key features, installation, basic usage, and important links.

### Key Features:

1.Static Timing Analysis: OpenSTA performs comprehensive timing analysis on digital designs to identify setup, hold, and other timing violations.

2.Path Analysis: It analyzes critical paths in a design to identify areas that require optimization for meeting timing constraints.

3.Constraint Validation: OpenSTA checks the accuracy of timing constraints specified in the design and performs setup and hold time analysis.

4.Report Generation: Detailed timing reports are generated, highlighting violations, paths, and other relevant information.

5.Open-Source: Being open-source, OpenSTA encourages collaboration and community contributions.

### Installation:

To install OpenSTA on Ubuntu, use the following command in the terminal:

```bash
https://github.com/The-OpenROAD-Project/OpenSTA
```

```bash
$ sudo apt-get install cmake
$ sudo apt-get install clang
$ sudo apt-get install gcc
$ sudo apt-get install tcl
$ sudo apt-get install swig
$ sudo apt-get install bison
$ sudo apt-get install flex
```

Installation commands for openSTA
```bash
$ git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
$ cd OpenSTA
$ mkdir build
$ cd build
$ cmake ..
$ make
```
Screenshot after installation-
![STA](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/1dec98a7-9bf6-4367-bf26-fd42dbc9594a)


## NGSpice
   
### Overview:
NGSpice is an open-source mixed-level/mixed-signal electronic circuit simulator based on the Berkeley SPICE project. It enables users to simulate and analyze analog, digital, and mixed-signal circuits, helping in design validation, analysis, and optimization. This brief guide introduces NGSpice for your GitHub documentation, covering key features, installation, basic usage, and important links.

### Key Features:

1.Mixed-Level Simulation: NGSpice supports both analog and digital simulation, making it suitable for mixed-level/mixed-signal designs.

2.Extensive Component Library: It includes a wide range of built-in models for various electronic components, facilitating accurate circuit representation.

3.Transient and Steady-State Analysis: NGSpice can perform transient, DC, AC, and other types of analyses to study circuit behavior over time or at specific operating points.

4.Interactive Plotting: The tool provides interactive plotting capabilities to visualize simulation results through waveform plots.

5.Open-Source: Being open-source, NGSpice encourages community contribution and customization.

### Installation:

To install NGspice on Ubuntu, use the following command in the terminal:

After downloading the tarball from https://sourceforge.net/projects/ngspice/files/ to a local directory, unpack it using:

```bash
$ tar -zxvf ngspice-37.tar.gz
$ cd ngspice-37
$ mkdir release
$ cd release
$ ../configure  --with-x --with-readline=yes --disable-debug
$ make
$ sudo make install
```
Screenshot after installation-

![ngspice](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/0a0f66d0-e963-4203-bf73-a3a48acfd93c)

## Magic
  
### Overview:
Magic is an open-source VLSI layout tool used for designing and analyzing integrated circuits (ICs). It provides a versatile environment for drawing and manipulating physical layouts of circuits, helping engineers and designers visualize and verify the layout of their designs. This brief guide introduces Magic for your GitHub documentation, covering key features, installation, basic usage, and important links.

### Key Features:

1.Physical Layout Design: Magic allows you to create and manipulate physical layouts of ICs, including transistors, wires, vias, and other components.

2.GDSII Format Support: It supports the GDSII (Graphic Data System II) format, enabling seamless integration with other EDA tools in the IC design flow.

3.Hierarchy and Hierarchical Editing: Magic supports hierarchical design, making it suitable for both small and complex designs.

4.Design Rule Checking (DRC): Magic can perform basic design rule checking to identify violations and ensure layout conformity.

5.Interactive Layout Editing: The interactive GUI allows you to modify and optimize layouts in real-time.

### Installation:

To install Magic on Ubuntu, use the following command in the terminal:

```bash
$   sudo apt-get install m4
$   sudo apt-get install tcsh
$   sudo apt-get install csh
$   sudo apt-get install libx11-dev
$   sudo apt-get install tcl-dev tk-dev
$   sudo apt-get install libcairo2-dev
$   sudo apt-get install mesa-common-dev libglu1-mesa-dev
$   sudo apt-get install libncurses-dev
$   git clone https://github.com/RTimothyEdwards/magic
$   cd magic
$   ./configure
$   make
$   sudo make install

```
Screenshot after installation-
![Screenshot from 2023-07-31 21-35-44](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/cefda874-22ed-4b78-ae7a-c4b150fd31f3)
    
## OpenLANE
   
### Overview:
OpenLANE is an open-source digital RTL to GDSII flow that aims to provide a complete, automated, and predictable path for designing digital integrated circuits. It encompasses various open-source tools and methodologies to automate the design process from RTL (Register Transfer Level) to the final layout for manufacturing. This brief guide introduces OpenLANE for your GitHub documentation, covering key features, installation, basic usage, and important links.

### Key Features:

1.Automated RTL-to-GDSII Flow: OpenLANE automates the entire digital design flow, from RTL synthesis to GDSII layout generation.

2.Open-Source Tools Integration: It integrates various open-source EDA (Electronic Design Automation) tools, enabling a comprehensive and customizable design flow.

3.Predictable and Reproducible Results: OpenLANE focuses on producing consistent and reproducible design results across different designs and process nodes.

4.Design Exploration: OpenLANE supports design exploration to optimize various design metrics such as area, power, and timing.

5.Hierarchical Design: It supports hierarchical design methodologies, making it suitable for complex designs.

### Installation:
    
To install OpenLANE on Ubuntu, use the following command in the terminal:

```bash
$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo apt install -y build-essential python3 python3-venv python3-pip make git
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
$ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
$ sudo apt update
$ sudo apt install docker-ce docker-ce-cli containerd.io
$ sudo docker run hello-world
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ sudo reboot 
```

After Reboot
```bash
docker run hello-world
```

Screenshot after installation-
![OpenLANE](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/74d108c4-c5aa-406a-8f40-87b0e71f0c4e)

## Day 1: Introduction to Verilog RTL Design and Synthesis

- [Part A: Introduction to open-source simulator iverilog](#part-A-introduction-to-open-source-simulator-iverilog)
  -  [Introduction to Iverilog Design Testbench](#introduction-to-iverilog-design-testbench)
  -  [Labs using Iverilog and GTKwave](#labs-using-iverilog-and-gtkwave)
  -  [Iverilog and GTKwave Lab Demonstration](#Iverilog-and-gtkwave-lab-demonstration)

- [Part B: Introduction to Yosys and Logic Synthesis](#introduction-to-yosys-and-logic-synthesis)
  - [Synthesizer](#synthesizer)
  - [Need of Setup and Hold Time](#need-of-setup-and-hold-time)
  - [Demonstration of Yosys](#demonstration-of-yosys)
## Part A: Introduction to open-source simulator iverilog

In Icarus Verilog, a simulator is a core component responsible for emulating the behavior of digital designs described in Verilog code. It allows users to virtually test and validate their designs before proceeding to physical implementation. The simulator compiles Verilog source code, simulates the logical operations of the design, and generates results that aid in functional verification.

## Introduction to Iverilog Design Testbench
### Simulation
### Overview:
RTL (Register Transfer Level) simulation is a fundamental step in digital design verification. It involves simulating the behavior of a digital design at the register transfer level, which focuses on the flow of data between registers. This process helps ensure the correctness and functionality of the design before proceeding to further stages of the design flow. This brief guide introduces RTL simulation for your GitHub documentation, covering key concepts, tools, steps, and important links.

### Key Concepts:

1.RTL Representation: RTL describes the behavior of a digital circuit in terms of registers, data transfers, and logical operations.

2.Simulation: RTL simulation involves applying test vectors to the design and observing its responses to verify its functionality.

3.Testbench: A testbench is essential for providing inputs, controlling the simulation, and verifying the design's outputs.

4.Functional Verification: RTL simulation focuses on verifying that the design functions as intended.

![Screenshot (8)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/6847baa6-e0c8-4493-aebe-81e5c52532bd)

### Testbench:

### Overview:
A testbench is a critical component in digital design and verification. It's used to simulate and validate the behavior of your digital design, ensuring its correctness before hardware implementation. This brief guide introduces testbenches for your GitHub documentation, covering key concepts, types, creation, and important links.

### Key Concepts:

1.Verification: Testbenches are crucial for verifying that your digital design functions correctly under various scenarios.

2.Simulation: Testbenches simulate the interactions between your design and its environment, helping to uncover bugs and issues.

3.Inputs and Outputs: Testbenches provide inputs to your design and capture its outputs to compare against expected results.

![Screenshot (9)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/de5f3687-5332-47fa-a281-58e63e1ed7c6)

### Labs using Iverilog and GTKwave

Steps to setup lab for iverilog and gtkwave:

- Create a directory named "VLSI" or choose another name if you prefer.
```bash
$ mk dir VLSI
```
- Navigate to the "VLSI" directory.
```bash
$ cd VLSI
```

- To create a copy of a remote Git repository onto your local machine, run the following command in the command prompt (CMD):
```bash
$ git clone https://github.com/kunalg123/vsdflow.git
$ git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
```
Now we can check the 'lab folder' to see which files are present in it using the following command
```bash
$ cd VLSI/sky130RTLDesignAndSynthesisWorkshop
$ ls -R 
```
Using the 'ls -R' command, we can list all files and directories, including those within subdirectories.

After executing the command above, we will see the output displayed in the screenshot below:
![Screenshot from 2023-08-13 19-22-43](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/507cbb7a-0300-4b03-bdca-e579e6431170)
![Screenshot from 2023-08-13 19-25-19](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/c34fb6d4-9cdb-41dc-8f10-d1c35635370a)
![Screenshot from 2023-08-13 19-25-48](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/751ec771-806e-4220-bb9e-e710de292160)

In the directory /home/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib, you will find the SkyWater 130nm standard cell library file named "sky130_fd_sc_hd__tt_025C_1v80.lib," which will be utilized for our lab exercises.

(A standard cell library is a collection of predefined and characterized digital logic cells used in integrated circuit (IC) design. These cells are the fundamental building blocks of digital designs, such as CPUs, memory units, and other complex digital systems. Standard cell libraries play a crucial role in enabling efficient and optimized chip design.)

In the directory /home/VLSI/sky130RTLDesignAndSynthesisWorkshop/my_lib/verilog_model, you will discover the Verilog model files that we will utilize for our lab exercises.

In the directory /home/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files, you will find Verilog code files along with their corresponding testbench files, which will be used for our lab activities.

### Iverilog and GTKwave Lab Demonstration:

Open your terminal and navigate to the directory containing the Verilog files and their corresponding testbench files:
```bash
$ cd path/to/your/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
Test the Verilog file and its corresponding testbench using the iverilog command. Replace good_mux.v and tb_good_mux.v with your actual Verilog file and testbench filenames.
```bash
$ iverilog good_mux.v tb_good_mux.v
```
The provided command compiles the Verilog design file good_mux.v along with its associated testbench tb_good_mux.v using the Icarus Verilog compiler. This compilation process produces a simulation executable, often named a.out, which captures the interplay between the design and its testbench. By running ./a.out, this executable is executed, simulating the design's behavior according to the test scenarios defined in the testbench. This command holds significant importance in ensuring the accuracy and operational effectiveness of digital logic designs through simulation methodologies.

To execute the simulation, use the command:
```bash
$ ./a.out
```
When the command ./a.out is executed, it triggers the compiled simulation of your Verilog design and its corresponding testbench. Our testbench is set up to generate VCD files, this command also creates a VCD file.

The VCD (Value Change Dump) file is a crucial output generated during Verilog simulation. It captures the dynamic changes in signal values over the course of the simulation, representing how the digital circuit behaves over time. VCD files are commonly used for waveform visualization and analysis using tools like GTKWave. 

To visualize the simulation results, you can execute the following command:

```bash
$ gtkwave tb_good_mux.vcd
```
The command gtkwave tb_good_mux.vcd is used to open the GTKWave waveform viewer to visualize the contents of a VCD (Value Change Dump) file named tb_good_mux.vcd.This command allows you to observe how signals in your design change over time, helping you to verify the correctness of your digital logic design.

After executing above commands, you can see the final waveform, similar to the picture below:
![Screenshot from 2023-08-14 13-00-36](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/91bc2a13-0903-4c92-925d-2e2b36c20a97)

Now, let's take a look at the Verilog code for good_mux and its corresponding testbench, tb_good_mux.

Run the below command in the directory /home/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```bash
$ iverilog tb_good_mux.v good_mux.v
```
After executing above command, you can see the verilog code for good_mux and tb_good_mux, similar to the picture below:
![Screenshot from 2023-08-14 13-24-48](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/490b63d5-7af7-47b7-8646-d662cca9f3de)

Lets first understand verliog code of good_mux
```bash
module good_mux (input i0 , input i1 , input sel , output reg y);
always @ (*)
begin
	if(sel)
		y <= i1;
	else 
		y <= i0;
end
endmodule
```
Let's break down the code step by step:

- input i0, i1, sel: These are input ports of the module. i0 and i1 are the two input signals that you want to multiplex (select from), and sel is the control signal that determines which input to choose.

- output reg y: This is an output port of the module. y is the output signal of the multiplexer that will carry the selected input.

- always @ (*): This is a combinational logic block that is sensitive to any change in its input signals (* is a wildcard indicating sensitivity to all inputs). This block will execute whenever there is a change in any of the input signals.

- The if(sel) statement checks the value of the sel signal:
        - If sel is high (1), y is assigned the value of i1.
        - If sel is low (0), y is assigned the value of i0.

Let's understand the testbench "tb_good_mux"
```bash
`timescale 1ns / 1ps

module tb_good_mux;
    // Inputs
    reg i0, i1, sel;
    // Outputs
    wire y;

    // Instantiate the Unit Under Test (UUT)
    good_mux uut (
        .sel(sel),
        .i0(i0),
        .i1(i1),
        .y(y)
    );

    initial begin
        $dumpfile("tb_good_mux.vcd");
        $dumpvars(0, tb_good_mux);
        // Initialize Inputs
        sel = 0;
        i0 = 0;
        i1 = 0;
        #300 $finish;
    end

    // Toggle sel, i0, and i1 signals at different time intervals
    always #75 sel = ~sel;
    always #10 i0 = ~i0;
    always #55 i1 = ~i1;

endmodule
```
Let's break down the code step by step:
```bash
`timescale 1ns / 1ps
```
This line sets the simulation timescale to 1 nanosecond per simulation time unit and 1 picosecond per simulation time precision. It defines the units used for time delays and calculations in the simulation.
```bash
module tb_good_mux;
```
This line starts the definition of the testbench module named tb_good_mux
```bash
// Inputs
reg i0, i1, sel;
// Outputs
wire y;
```
These lines define the input and output signals for the testbench. i0, i1, and sel are the input signals, and y is the output signal of the multiplexer.
```bash
// Instantiate the Unit Under Test (UUT)
good_mux uut (
    .sel(sel),
    .i0(i0),
    .i1(i1),
    .y(y)
);
```
This code instantiates the good_mux module (the unit under test) with the specified connections. It connects the testbench signals to the corresponding module ports.
```bash
initial begin
    $dumpfile("tb_good_mux.vcd");
    $dumpvars(0, tb_good_mux);
    // Initialize Inputs
    sel = 0;
    i0 = 0;
    i1 = 0;
    #300 $finish;
end
```
This initial block sets up the simulation environment. It specifies that the simulation output should be written to a VCD (Value Change Dump) file named "tb_good_mux.vcd". It initializes the input signals sel, i0, and i1 to specific values. After a simulation time of 300 time units, the simulation is finished using the $finish system task.
```bash
always #75 sel = ~sel;
always #10 i0 = ~i0;
always #55 i1 = ~i1;
```
These always blocks simulate the toggling behavior of the input signals. They change the values of sel, i0, and i1 at different time intervals to observe how the multiplexer responds.
```bash
    endmodule
```
    This line ends the definition of the testbench module.

## Part B: Introduction to Yosys and Logic Synthesis
### Synthesizer:
A synthesizer, in the context of digital design and electronics, refers to a software tool or toolchain that automates the process of transforming a high-level hardware description into a lower-level representation suitable for implementation on specific hardware platforms. Synthesizers are an integral part of the electronic design automation (EDA) ecosystem, enabling designers to efficiently create and optimize digital circuits.

![Screenshot (10)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/5495762b-a519-4aa3-948b-47756f8f471b)

![Screenshot (11)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/d234624c-01da-47d1-a575-b4a82db311f4)
### Liberty(.lib):

A Liberty (.lib) file is a standard format used in electronic design automation (EDA) for representing the electrical and timing characteristics of library cells, which are the fundamental building blocks of digital integrated circuits. The Liberty format is widely used to define library cells' timing, power, and noise attributes, allowing designers to accurately model and analyze the behavior of these cells during various stages of the design process.

In a Liberty file, you can typically find information such as:

- Cell Definitions
- Timing Models
- Power Models
- Operational Constraints
- Variation and Process Corners
- Noise and Signal Integrity
- Library Hierarchies

Liberty files play a crucial role in the design and optimization of digital circuits. They enable designers to make informed decisions about cell selection, logic synthesis, timing analysis, and power optimization. These files are used by various EDA tools to ensure accurate modeling and simulation of digital circuits, ultimately contributing to the successful creation of efficient and functional integrated circuits.

### Netlist file

A netlist file is a fundamental component in electronic design automation (EDA) and digital circuit design. It represents a structural description of a digital circuit, specifying the interconnections and logic components that make up the circuit. Netlist files play a crucial role in various stages of the design process, including logic synthesis, simulation, and physical design.

Netlist files are crucial for simulation, where they serve as inputs to simulators to validate the circuit's behavior under different scenarios. They are also used for physical design, including place-and-route, where the circuit is mapped to physical locations on a chip and interconnections are established.

Netlist formats can vary depending on the EDA tool and the design's target technology. Common formats include Verilog netlist (.v), VHDL netlist (.vhd), and Electronic Design Interchange Format (EDIF) files (.edn). These files facilitate communication between different design tools and enable a seamless flow from high-level design to physical implementation.

### Verify the Synthesis:
- Output of the syntheis should be same as output obtained during RTL simulation.
- Netlist is the true representation of our design, i.e., design was written as a behavioral Verilog code, and the netlist is Verilog code in terms of standard cells. However, between the design and synthesized netlist, the primary inputs and outputs are not changed, which means we can use the same testbench that we use in RTL simulation.

![Screenshot (12)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/a5d83ad7-5c67-4374-b9f0-2e8a0db1895f)

### Need of Setup and Hold Time

![Screenshot (18)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/c4766f8e-64c2-41df-bc5d-4e8f2cefb204)
![Screenshot (13)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/761c83be-5817-4e43-a110-e82b534e1048)
![Screenshot (14)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/fb1c343a-e62b-4158-b3c6-515a1fa13584)
![Screenshot (15)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/f0203bfd-d31f-432a-9839-c954ea650110)
![Screenshot (17)](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/0cfb4ff3-ea88-4bfe-82d6-a994a64db409)

## Demonstration of Yosys
Step 1: Navigate to the Verilog Files Directory

Open a terminal and navigate to the directory containing the Verilog files for the project.

```bash
cd /home/akhilasati/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
Step 2: Launch Yosys

Launch Yosys, the synthesis tool, by entering the following command:
```bash
yosys
```
Step 3: Read Liberty Library

Read the Liberty library file containing standard cell characterization data for the target technology (SkyWater 130nm process). This library will be used for technology mapping during synthesis.

-lib: This flag indicates that a library file is being read.
```bash
read_liberty -lib /home/akhilasati/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
```
Step 4: Read Verilog Design

Read the Verilog design file (good_mux.v) that you want to synthesize.
```bash
read_verilog good_mux.v 
```
![Screenshot from 2023-08-14 16-02-56](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/6d138ae7-d2a7-4329-bfd5-55d1835e9d16)

Step 5: Perform Synthesis

Perform synthesis on the design, specifying good_mux as the top module for synthesis.
- synth: This is the command in Yosys that initiates the synthesis process.
- top good_mux: This flag specifies the top-level module for synthesis. In this case, the module name is good_mux. The top-level module is the entry point of your design that you want to synthesize. Yosys will analyze and optimize the logic within this module.
```bash
synth -top good_mux
```


Step 6: Perform Technology Mapping using ABC

Perform technology mapping using the ABC (A System for Sequential Logic Synthesis and Verification) tool, and provide the previously read Liberty library for cell mapping.

```bash
abc -liberty /home/akhilasati/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Step 7: Display Design Hierarchy

Display the design hierarchy and cells after synthesis to inspect the results.
```bash
show
```
Step 8: Write Synthesized Netlist

Write the synthesized netlist to a new Verilog file named good_mux_netlist.v. Exclude attributes from the netlist for simplification.
```bash
write_verilog -noattr good_mux_netlist.v
```
Step 9: Exit Yosys

Exit Yosys by typing exit or pressing Ctrl + D in the terminal.

![Screenshot from 2023-08-14 16-47-25](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/edf4aaec-4b25-4466-821a-857c486106ab)
![Screenshot from 2023-08-14 16-49-57](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/16ad0e7c-ab69-4bc4-a872-2cbd33710ed7)
![Screenshot from 2023-08-14 16-50-35](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/c4302b92-f6d8-41ee-913d-bf870c28c966)
![Screenshot from 2023-08-14 16-50-21](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/397e1c41-5267-4b62-a5f7-b4d9f3ca6500)
![Screenshot from 2023-08-14 16-49-39](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/155bc47d-6732-4230-9437-55e0299f9277)
## Day 2: Timing libs, hierarchical vs flat synthesis and efficient flop coding styles

## Day 3: Combinational and sequential optmizations

## Day 4: GLS, blocking vs non-blocking and Synthesis-Simulation mismatch

## Day 5: If, case, for loop and for generate

# References:
- https://iverilog.fandom.com/wiki/Simulation
- https://github.com/steveicarus/iverilog
- http://www.clifford.at/yosys/documentation.html
- https://www.vsdiat.com/
