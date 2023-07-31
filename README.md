# DAY 0
<h2>Software Installation</h2>
<details>
<summary><mark>Icarus verilog</mark></summary>
    
<p>Icarus Verilog (iverilog) is a popular open-source Verilog simulator. It allows you to compile and simulate Verilog code, making it a valuable tool for hardware description language (HDL) development and testing.

To install Icarus Verilog on Ubuntu, use the following command in the terminal:</p>

```bash
$ sudo apt-get update
$ sudo apt-get install iverilog

```
Screenshot after installation-
![Iverilog](https://github.com/akhiiasati/Akhil_IIITB/assets/43675821/42339d5f-e006-4a2f-881b-b84fcbe3af7a)

</details>
<details>
<summary><h4>Yosys</h4></summary>

<p>Yosys is a powerful open-source tool for Verilog synthesis. It allows you to convert RTL (Register Transfer Level) code written in Verilog into a gate-level representation, such as a netlist. This netlist can then be used for further analysis, optimization, and implementation in various digital design flows.

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
![yosys](https://github.com/Shant1R/Shant_IIITB/assets/59409568/6ac97051-4660-4722-b384-26eb6aba3260)


</details>

<details>
<summary>Icarus verilog</summary>

Icarus Verilog also known as iverilog is installed using the following command.

```bash
$ sudo apt-get update
$ sudo apt-get install iverilog

```
Screenshot after installation-
![iverilog](https://github.com/Shant1R/Shant_IIITB/assets/59409568/4f77ee22-b0b3-4c96-9f8e-1b74443579e4)


</details>

<details>
<summary>GTKWave</summary>

GTKWave is installed using the following commands.

```bash
$ sudo apt update
$ sudo apt install gtkwave
```
Screenshot after installation-
![gtkwave](https://github.com/Shant1R/Shant_IIITB/assets/59409568/ae8c7922-c337-4157-839f-c8f1f62265b2)

</details>


<details>
<summary>OpenSTA</summary></summary>

To install OpenSTA, follow the given github link and download the following prerequisites- 

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
![opensta](https://github.com/Shant1R/Shant_IIITB/assets/59409568/36537253-8d3e-4f7a-9358-35c3f5c04e55)

</details>


<details>
<summary>NGSpice</summary>
NGSpice is installed using the following commands.

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
![ngspice](https://github.com/Shant1R/Shant_IIITB/assets/59409568/726fcc95-63eb-4089-87e3-f306cc37d83c)

    
</details>

<details>
<summary>Magic</summary>
Magic is installed using the following commands.

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
![magic](https://github.com/Shant1R/Shant_IIITB/assets/59409568/f5fe09ee-2f15-47c0-b4a6-5a41febf7e76)
    
</details>

<details>
<summary>OpenLANE</summary>
OpenLane is installed using the following commands.

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
![openlane](https://github.com/Shant1R/Shant_IIITB/assets/59409568/d55be32a-a662-4284-94b0-b0d53af2fbca)

    
</details>
