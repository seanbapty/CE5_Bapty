CE5_Bapty
=========
# TASK #1: Simple MIPS Assembly Program
```
addi $s0, $0, 44
addi $s1, $0, -37
add $s2, $s0, $s1
sw $s2, 84($0)
```
The above code stores 44 in $s0, -37 in $s1, then adds them and stores the result in $s2. The final step stores the value of $s2 in hex location 54 (decimal 84).
# TASK #2: Machine Code
```
addi $s0, $0, 44   | 0x2010002C
addi $s1, $0, -37  | 0x2011FFDB
add $s2, $s0, $s1  | 0x02119020
sw $s2, 84($0)     | 0xAC120036
```
![alt tag](https://raw.githubusercontent.com/seanbapty/CE5_Bapty/master/part2output.JPG)

The above output makes sense because -37 added to 44 equals 7. All these values are in the appropriate memory location.
# TASK #3: MIPS With The ori Instruction 
## ALU Schematic Modification
In order to implement a ORI, the MIPS processer had to include a zero extenter. In order to choose when to utulize the zero extender a two input multiplexer was needed. Additionally, the multiplexer needed to be driven by the ALUSrc signal, and therefore this signal had to be modified from one bit to two bits. 
![alt tag](https://raw.githubusercontent.com/seanbapty/CE5_Bapty/master/schematic.jpg)
## ALU Decoder Table Modification
![alt tag](https://raw.githubusercontent.com/seanbapty/CE5_Bapty/master/alu.jpg)
## Main Decoder Modification
![alt tag](https://raw.githubusercontent.com/seanbapty/CE5_Bapty/master/MainDecoderTable.jpg)
#### Documentation
I referenced Sabin Park's code while completing task 1 find out the notation of sw. I also referenced the textbook, and the previous lesson's PowerPoint when completing task 1.
While completing part 2 I checked my answers with Cassi McPeek's README on GitHub.
I referenced Sabin Park's code when completing part 3. It was from the book and his code that I got the idea to add a zero extender and a multiplexer to implement it.
