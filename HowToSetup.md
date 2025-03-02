May be works with windows but not recommended

MCU
Vendor      : STM
Type        : STM32F072 (STM32F072C8T6)
Evalbaord   : NUCLEO-F072RB 

Link to MCU : https://www.st.com/en/microcontrollers-microprocessors/stm32f072rb.html

Toochain:

STM32CubeMX : https://www.st.com/en/development-tools/stm32cubemx.html
Build with  : CMake
Compiler    : 
              Linux   - https://developer.arm.com/-/media/Files/downloads/gnu/14.2.rel1/binrel/arm-gnu-toolchain-14.2.rel1-x86_64-arm-none-eabi.tar.xz
              Windows - https://developer.arm.com/-/media/Files/downloads/gnu/14.2.rel1/binrel/arm-gnu-toolchain-14.2.rel1-mingw-w64-i686-arm-none-eabi.zip

Simulator   
Remode      : https://renode.io/

Hardware

- Use internal clocking
- CAN 
    -   clock 66.666 Kbit/s
    -   Time Quanta 1: 1
    -   Time Quanta 2: 1
    -   ReSynconization Jumpwidth: 1
    -   Operationmode: Loopback

- UART1
    - 19200 Baud
    - 7 Bit
    - Even parity
    - 1 Stopbit


//GET toolchain in place 
// assumes it has been extratced to /opt/software/arm-gnu-toolchain-14.2.rel1-x86_64-arm-none-eabi
// export PATH="$PATH:/opt/software/arm-gnu-toolchain-14.2.rel1-x86_64-arm-none-eabi/bin/"
// we need to add the export permantently to our enviroment
// - open ~/.bashrc
// - add the 'export .... ' form above as last command 
// - save he file

//Generate code for CMAKE go into projetc folder
//   mkdir build 
//   cd build
//   cmake ..

//For VSCode and STM32 tools
// use Strg+P and paste 'ext install stmicroelectronics.stm32-vscode-extension' 
// instructins can be found at : https://marketplace.visualstudio.com/items?itemName=stmicroelectronics.stm32-vscode-extension
//
// - install https://www.st.com/en/development-tools/stm32cubeclt.html#get-software 
// - isntall https://www.st.com/en/development-tools/st-mcu-finder-pc.html#get-software
// - apt-get install libncurses 
// - sudo apt install ninja-build




