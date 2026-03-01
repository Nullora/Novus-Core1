Write = write TO COMPONENT
Read = read TO BUS
24 bit instruction:
- OPCODE= 8
- A = 4
- B = 4
- RESULT = 4
- LEFT = 4
instruction structure:
 - 0000 0000 0000 0000 00000000
 -   left | result | B   |    A   |  opcode


 Instructions:
 -  ff = halt
 -  reg|01 = jump
 - number|reg|02 = load to register
 - address|reg|03 = register to ram
 - address|reg|04 = ram to register
 - C|B|A|05 = A+B -> C
 - C|B|A|06 = A-B -> C
 - C|B|A|07 = AxB -> C
 - C|B|A|08 = A/B -> C
 - C|B|A|09 = A and B -> C
 - C|B|A|0a = A or B -> C
 - C|B|A|0b = A xor B -> C
 - C|A|0c = not A -> C
 - reg|0d = keyboard to register
 - reg|0e = register to monitor
 - reg|0f = jump if equal flag is 1
 - reg|10 = jump if NOT equal
 - reg|11 = from register to rgb monitor