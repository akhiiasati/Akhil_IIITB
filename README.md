# Physical Design Using ASIC

## Content
- [Day 0: Software Installation](#day-0-software-installation)
- [Day 1: Introduction to Verilog RTL Design and Synthesis](#day-1-introduction-to-verilog-rtl-design-and-synthesis)

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
![iverilog](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/dd7e5d71-c77c-4709-a943-dcd79d88957a)


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

Automated RTL-to-GDSII Flow: OpenLANE automates the entire digital design flow, from RTL synthesis to GDSII layout generation.

Open-Source Tools Integration: It integrates various open-source EDA (Electronic Design Automation) tools, enabling a comprehensive and customizable design flow.

Predictable and Reproducible Results: OpenLANE focuses on producing consistent and reproducible design results across different designs and process nodes.

Design Exploration: OpenLANE supports design exploration to optimize various design metrics such as area, power, and timing.

Hierarchical Design: It supports hierarchical design methodologies, making it suitable for complex designs.

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

Simulation is the process of creating models that mimic the behavior of the device you are designing (simulation models) and creating models to exercise the device (test benches). The simulation model need not reflect any understanding of the underlying technology, and the simulator need not know that the design is intended for any specific technology.

### Overview:
A testbench is a critical component in digital design and verification. It's used to simulate and validate the behavior of your digital design, ensuring its correctness before hardware implementation. This brief guide introduces testbenches for your GitHub documentation, covering key concepts, types, creation, and important links.

### Key Concepts:

1.Verification: Testbenches are crucial for verifying that your digital design functions correctly under various scenarios.

2.Simulation: Testbenches simulate the interactions between your design and its environment, helping to uncover bugs and issues.

3.Inputs and Outputs: Testbenches provide inputs to your design and capture its outputs to compare against expected results.




