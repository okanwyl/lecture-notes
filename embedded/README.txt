INTRODUCTION
---
---
---
Embedded system tanim?:
Embedded systems are information processing systems embedded into a larger product
in the slides
Application specific computer system
built into larger systems
often with realtime computing constratins
---
---
---
Why add a computer to larger system?
better perf, more func, lower cost for automation, more dependability
---
---
---
Cyber-Physical Systems and Embedded systems
CPS = ES + Physical env  -> trcesi : integration of computations + networking + physical processlerin butunu

Emerging CPS will be coordinated, disturbted, connnected olmasi gerekiyor ->  
CONNNECTED = internet uzerinden erisilebilir olmasi
DISTURBTED = Also known as disturbted computing and disturbted databases a collection of 
independent components located on different machines that share messages with each other in order to achieve common goals.
COORDINATED = you know that

examples -> smart transportations, smart buildings, next-gen air traffic etc..
---
---
---
 Ubiquitous computing => her yerde bulunan computing?
from wiki: where computing is made to appear anytime and everywhere. 
In contrast to desktop computing, ubiquitous computing can occur using any device, in any location, and in any format. 
example -> laptop tablets notebooks smartphones you got the idea
---
---
---
Microprocesscor (CPU)
as a single processor core that supports at least instruction fetching, decoding, and executing. 
important -L> Instruction fetching, decoding, executing must
contains Memory interface, Register banks

Instruction cycle -> meaning fetch-decode-execute
modern cpus execution cycle is concurrent and parallel

Instruction decoder -> The instruction decoder logic converts the op-code bits into settings for all the internal control lines. The operand provides a literal, file register address or program address, which will be used by the instruction.

from wiki - multipurpose , clock-driven, register-based, digital integrated circuit 
takes input binary output binary
---
---
---
MCU Microcontroller
VLSI -> Very Large Scale Integration mil-bil MOS transistor to one single chip

single processor core
memory block, digitial io, analog io
generally used for basic control
contains one system bus
we can think that as a SoC
---
---
---
Galiba bir embedded system tasarlarken dusunumemiz gereken stepler?
Functions
Constraits
Inputs
output
Performence metrics?
---
---
---
What is IoT?
The Internet of Things (IoT) describes the network of physical objects—“things”—that are embedded with sensors, 
software, and other technologies for the purpose of connecting and exchanging data with other devices and systems over the internet.

problems: 
scalibility -> huge amount of data
Interoperability -> doesn't include any standardatizion includes but not enought it is fragmanted
Lack of goverment support -> like FDA doesn't come up with standard commmitte
Safety op patients -> can be dangerous like wearable ones?
Security And Personal Privacy -> Security security vulnerabilities and its improvements.
Design based constraints -> limited computataion power, limited energy, limited memory
always on causes increased connectivity-> artan network ihtiyaci
demographic -> what? yozlasma mi

IoT cihazlarini 4 gruba ayiralim ->  mobile, embedded, networking, connected community


Why Iot -> Items can have more functionalites and become more intelligent
items can be managed in easier way?
more information becoma will available

---
---
---
Load Store architecture
that divides instructions into two categories: memory access (load and store between memory and registers) 
and ALU operations (which only occur between registers)
---
---
---
RISC 
Reduced Instruction Set Computing (RISC) vs Complex Instruction Set Computing? computer (CISC)
RISC probably need more instruction to set accompclish same exact result
RISC generally load/store model -> 16-32 bit high speed general purpose registers
---
---
---
ARM Family 
ARM chips are cheap to produce
extremly power efficent
sells license -> not manufactaring chips
Cortex-A -> High Performance
Cortex-P -> Fast Response --> doesn't include on slides
Cortex-M -> Low power
SecurCore -> Tamper resistant guess it magneticlly resistant?
---
---
---
Cortex-A  Family
Highest Performance
Reduced Instruction Set Computing (RISC)
32bit-64bit and 16bit/32-bit instruction sets
application processors 3rd party applications
telefonda direkt core

Cortex-R Family
embedded real time processing
signal processing, control applications
telefonda anten wifi 

Cortex-M Family
Microcontroller oriented processors for MCU,
ASSP(Application Specific System Processor)
SoC applications
telefonda flashi kontrol eden Microcontroller, touchscreen controller, power mgmnt, sensor hub
genelde bluetoothdada kullanilir
---
---
---
Armv7-A and Armv8-A architecture (Armv7 32bit instruction set, mobile devices
armv8 64bit instruction set focus on power efficent)
backward compatible
full os sport
---
---
---
Thumb2 vs Thumb
thumb normalde 32 bit olan instruction sette 2^^32 den 2 milyar komut var
toplasan 22bin kullaniriz 16bitlik olan instructionlarda kullanilsin
alandan tasarruf yapalim demisler ikisini birlikte kullanan thumb2
thumb2 ve thumb arasinda gecis yapabiliyor cortex a
thumb ise sike sike kullaniliyor cortex m de

---
---
---
Common characteristics of embedded systems

CPS/ES must be dependeble. -> cevresindeki islevlere insanlara zarar vermeden kesintisiz
yapabiliyorsa dependeble

reliability R(t)= ilk calismaya basladigi zamandan itibaren ne zaman task atansa yapiyor t=0 reliability tamdir? ne dedin hoca amk ne demek bu

reliability dusurebilecek caseler-> yetersiz secilmis bir hardware, hardware failaure, software bug

security -> identification eklenebilir, network kullaniliyorsa secure network connection eklenebilir,
storage integrity and confidentiality

maintanibility: bir ariza olustu sistemde tamir edilip calismaya basladigi surece denir?

availability: u know

safety: 

efficency : 
code size efficent 
run-time efficent
weight efficent
cost efficent
energy efficent

---
---
---

hardware in a loop
physical -> sensors -> A/D converter sample and hold -> information processing -> display D/a converter -> actutator

actuator -> degisik componentler

---
---
---
CCD
based on charge transfer to the next pixel (legacy)
pahali, bellek ihtiyaci az
based on:optic
tech:special
no logic on chip
access:serial
size:limited
power cons:low

CMOS image sensors
pixel area uzerinde dusen isiklar ile bir boolean space yaratilip hesaplama yapar
based on:vlsi
tech:standard
logic on chip
access:random
size:can be large
power cons:larger
---
---
---

sensors generate signals
filtreleme yapmamiz lazim noiseu
Dt -> dv
dt analog
dv dijital

neredeyse tum analog donusturucu devrelerinde sample and hold devresi var
sample and hold ise bildigimiz kalibrasyon. orn sensore sabit 3v yollayip o noktayi baz alir sonraki
olcumlerde farkini alarak islem yapar


aliasing: kotu ornekleme parametresi secilmesi dalgali
---
---
---
alternatives for processing unit

ASIC: 
2 cat: fully custom, semi custom
very fast, not flexible
vhdl

CPLD: 
PAL ve FPGA arasinda bir yer
building block is a macrocell
macrocell: programmable logic devices, programmable array logic
contains non-volatile memory external ROM not required
fast and somewhat flexible

FPGA: 
field of programmable gate array
large interconnection matrix logic gates, RAM
May have analogue capability A/D D/A
VHDL uses

DSP
Digital signal processor
yogun hesaplama?
i/o icin tasarlanmis

may include:
quadrature decoders
PWM
Serial communication


PLC
programmable logic controller
progrrammed graphically?
tens of thousand i/o
they are biggggggggg



uP
math icin perfect
runs an os
significant memory
may be single-board
not able to directly interface



---
---
---
Armv7-A
mmu memormy management support
highest performance at low power
multi-tasking OS
TrustZone for a safe extensible system

Armv7-R
Protected memory
low latency and predictability for real-time needs
tightly coupled memories for fast deterministic access


Armv7-M, ARMv6-M
lowest gate count entry point

---
---
---
MSP430
ultra low-power
16 bit RISC cpu
large register file


-- realtime?
dsp provides realtime
real time formula y(n) = E 99 dan 0=(a(k)x(n-k)

use dsp if cost saving smaller size, low power consumption, many high freq signals in real time
use gpp requrired large memory, advancing operating systems

typical dsp alghoritms: wtf is that -- ch4 information processing dsp?
dsp optimized for multiplication and addition operation in one machine cycle


high precision wide dynamic range, high signal to noise audio ease of use -> floating point processor? FPU
but it's bad for high power consumption can be more expensive can be slow for fixed point

asic specialized for application? ->  bad for dev cycle

-- programmable logic  PLD


large number of gates and flip flops
3 type -> SPLD simple plds -> earliest type of array logic used for fixed functiosn
cpld -> complex plds -> multiple spld arrays 
fpld -> field of programmable gate array more flexiable than cpld with much larger capacity

advantages of pld -> lower req, less board, simpler testing

all plds contains arrays. Two important one SPLDS are PALS(programmable array logic) and 
GALS(generic array logic) a typical matrix of conductors
one time programmable PALS
gal is reprogrammable


macrocells-> pal gal mixed outputs with or gate

information processing pld look up



--- 

3 dimesional 8 cubic, 64 bit,
read write, hit or miss
rams -> static ram, dynamic ram
sram is faster, but more complext and require more space
asynchronous sram -> everything is low
dram-> simple and cost effective
rom -> system initializon and not removed
prom -> programmable rom
eprom -> can be erased prom
eeprom -> electric pulses remove and program
flash memory -> usb flash drive -> one drawback is once a bit set to 1 need to erase entire block memory

simm -> 32 bit data path
dimm -> 64 bit data path
fifo memory -> first in first out shift registers
lifo memory -> last in first out stack -> temp


---
programming 
c-> disadvantages > limited or no direct access to core registers
. no direct control over stack
. no dirct control instructions
