## Assembly Instructions Guide

Author: **7etsuo**  
- [X.com](https://twitter.com/7etsuo)

## Contents
1. [Abbreviations](#abbreviations)
   - [Meaning of Assembly Abbreviations](#meaning-of-assembly-abbreviations)
   - [Example Usage of Assembly Abbreviations](#example-usage-of-assembly-abbreviations)
2. [Assembly Mnemonics](#assembly-mnemonics)
   - [Description of x86 Assembly Instructions](#description-of-x86-assembly-instructions)
3. [Jxx - Jump Instructions Table](#jxx-jump-instructions-table)
   - [Jump Condition Meanings for Assembly](#jump-condition-meanings-for-assembly)
4. [Instructions](#instructions)

### 1. Abbreviations <a name="abbreviations"></a>
#### Meaning of Assembly Abbreviations

| Abbreviation | Meaning              |
| ------------ | -------------------- |
| 1            | the value 1          |
| accum        | register AX          |
| CL           | the register CL      |
| immed        | a value              |
| immed8       | an 8 bit value       |
| mem          | byte or word address |
| mem8         | byte address         |
| mem16        | word address         |
| reg          | 8 or 16 bit register |
| reg8         | 8 bit register       |
| reg16        | 16 bit register      |
| segreg       | segment registers    |

#### Example Usage of Assembly Abbreviations

| Abbreviation | Example        |
| ------------ | -------------- |
| 1            | SAL AX,1       |
| accum        | MOV AX,23      |
| CL           | SAL AX,CL      |
| immed        | MOV AX,2345    |
| immed8       | MOV AX,23      |
| mem          | MOV AX,lab1    |

### 2. Assembly Mnemonics <a name="assembly-mnemonics"></a>
#### Description of x86 Assembly Instructions

| Mnemonic | Description              |
| -------- | ------------------------ |
| ADC      | Add With Carry           |
| ADD      | Arithmetic Addition      |
| AND      | Logical And              |
| CALL     | Procedure Call           |
| CBW      | Convert Byte to Word     |
| CLC      | Clear Carry              |
| CLD      | Clear Direction Flag     |
| CLI      | Clear Interrupt Flag     |
| CMC      | Complement Carry Flag    |
| CMP      | Compare                  |
| CMPS     | Compare String           |
| CWD      | Convert Word to Double   |
| DEC      | Decrement                |
| DIV      | Divide                   |
| HLT      | Halt CPU                 |
| IDIV     | Signed Integer Division  |
| IMUL     | Signed Multiply          |
| IN       | Input Byte or Word From Port |
| INC      | Increment                |
| INS      | Input String from Port   |
| INT      | Interrupt                |
| INTO     | Interrupt on Overflow    |
| IRET     | Interrupt Return         |
| JCXZ     | Jump if Register CX is Zero |
| JMP      | Unconditional Jump       |
| LDS      | Load Pointer Using DS    |
| LEA      | Load Effective Address   |
| LES      | Load Pointer Using ES    |
| LODS     | Load String              |
| LOOP     | Decrement CX and Loop    |
| LOOPE    | Loop While Equal         |
| LOOPNZ   | Loop While Not Zero      |
| MOV      | Move Byte or Word        |
| MOVS     | Move String              |
| MUL      | Unsigned Multiply        |
| NEG      | Two's Complement Negation |
| NOP      | No Operation             |
| NOT      | One's Compliment Negation |
| OR       | Inclusive Logical OR     |
| OUT      | Output Data to Port      |
| OUTS     | Output String to Port    |
| POP      | Pop Word off Stack       |
| POPA     | Pop All Registers off Stack |
| POPF     | Pop Flags off Stack      |
| PUSH     | Push Word onto Stack     |
| PUSHA    | Push All Registers onto Stack |
| PUSHF    | Push Flags onto Stack    |
| RCL      | Rotate Through Carry Left |
| RCR      | Rotate Through Carry Right |
| REP      | Repeat String Operation  |
| REPE     | Repeat Equal             |
| REPNE    | Repeat Not Equal         |
| RET      | Return From Procedure    |
| ROL      | Rotate Left              |
| ROR      | Rotate Right             |
| SAL      | Shift Arithmetic Left    |
| SAR      | Shift Arithmetic Right   |
| SBB      | Subtract with Borrow     |
| SCAS     | Scan String              |
| SHL      | Shift Logical Left       |
| STC      | Set Carry                |
| STD      | Set Direction Flag       |
| STI      | Set Interrupt Flag       |
| STOS     | Store String             |
| SUB      | Subtract                 |
| TEST     | Test For Bit Pattern     |
| XCHG     | Exchange Register/Memory with Register |
| XLAT     | Translate Byte in AL Using Table in Memory |
| XOR      | Exclusive OR             |

### 3. Jxx - Jump Instructions Table <a name="jxx-jump-instructions-table"></a>
#### Jump Condition Meanings for Assembly

| Mnemonic | Meaning Jump Condition |
| -------- | ---------------------- |
| JA       | Jump if Above CF=0 and ZF=0 |
| JAE      | Jump if Above or Equal CF=0 |
| JB       | Jump if Below CF=1    |
| JBE      | Jump if Below or Equal CF=1 or ZF=1 |
| JC       | Jump if Carry CF=1    |
| JCXZ     | Jump if CX Zero CX=0  |
| JE       | Jump if Equal ZF=1    |
| JG       | Jump if Greater ZF=0 and SF=OF |
| JGE      | Jump if Greater or Equal SF=OF |
| JL       | Jump if Less SF != OF |
| JLE      | Jump if Less or Equal ZF=1 or SF != OF |
| JMP      | Unconditional Jump    |
| JNA      | Jump if Not Above CF=1 or ZF=1 |
| JNAE     | Jump if Not Above or Equal CF=1 |
| JNB      | Jump if Not Below CF=0 |
| JNBE     | Jump if Not Below or Equal CF=0 and ZF=0 |
| JNC      | Jump if Not Carry CF=0 |
| JNE      | Jump if Not Equal ZF=0 |
| JNG      | Jump if Not Greater ZF=1 or SF != OF |
| JNGE     | Jump if Not Greater or Equal SF != OF |
| JNL      | Jump if Not Less SF=OF |
| JNLE     | Jump if Not Less or Equal ZF=0 and SF=OF |
| JNO      | Jump if Not Overflow OF=0 |
| JNP      | Jump if No Parity PF=0 |
| JNS      | Jump if Not Signed SF=0 |
| JNZ      | Jump if Not Zero ZF=0 |
| JO       | Jump if Overflow OF=1 |
| JP       | Jump if Parity PF=1   |
| JPE      | Jump if Parity Even PF=1 |
| JPO      | Jump if Parity Odd PF=0 |
| JS       | Jump if Signed SF=1   |
| JZ       | Jump if Zero ZF=1     |

### 4. Instructions <a name="instructions"></a>
- [ADC - Add With Carry](#adc---add-with-carry)
- [ADD - Arithmetic Addition](#add---arithmetic-addition)
- [AND - Logical And](#and---logical-and)
- [CALL - Procedure Call](#call---procedure-call)
- [CBW - Convert Byte to Word](#cbw---convert-byte-to-word)
- [CLC - Clear Carry](#clc---clear-carry)
- [CLD - Clear Direction Flag](#cld---clear-direction-flag)
- [CLI - Clear Interrupt Flag (disable)](#cli---clear-interrupt-flag-disable)
- [CMC - Complement Carry Flag](#cmc---complement-carry-flag)
- [CMP - Compare](#cmp---compare)
- [CMPS - Compare String (Byte, Word)](#cmps---compare-string-byte-word)
- [CWD - Convert Word to Doubleword](#cwd---convert-word-to-doubleword)
- [DEC - Decrement](#dec---decrement)
- [DIV - Divide](#div---divide)
- [HLT - Halt CPU](#hlt---halt-cpu)
- [IDIV - Signed Integer Division](#idiv---signed-integer-division)
- [IMUL - Signed Multiply](#imul---signed-multiply)
- [IN - Input Byte or Word From Port](#in---input-byte-or-word-from-port)
- [INC - Increment](#inc---increment)
- [INS - Input String from Port (80188+)](#ins---input-string-from-port-80188)
- [INT - Interrupt](#int---interrupt)
- [INTO - Interrupt on Overflow](#into---interrupt-on-overflow)
- [IRET - Interrupt Return](#iret---interrupt-return)
- [JCXZ - Jump if Register CX is Zero](#jcxz---jump-if-register-cx-is-zero)
- [JMP - Unconditional Jump](#jmp---unconditional-jump)
- [LDS - Load Pointer Using DS](#lds---load-pointer-using-ds)
- [LEA - Load Effective Address](#lea---load-effective-address)
- [LES - Load Pointer Using ES](#les---load-pointer-using-es)
- [LODS - Load String (Byte, Word)](#lods---load-string-byte-word)
- [LOOP - Decrement CX and Loop if CX Not Zero](#loop---decrement-cx-and-loop-if-cx-not-zero)
- [LOOPE/LOOPZ - Loop While Equal / Loop While Zero](#loope-loopz---loop-while-equal--loop-while-zero)
- [LOOPNZ/LOOPNE - Loop While Not Zero / Loop While Not Equal](#loopnz-loopne---loop-while-not-zero--loop-while-not-equal)
- [MOV - Move Byte or Word](#mov---move-byte-or-word)
- [MOVS - Move String (Byte or Word)](#movs---move-string-byte-or-word)
- [MUL - Unsigned Multiply](#mul---unsigned-multiply)
- [NEG - Two's Complement Negation](#neg---twos-complement-negation)
- [NOP - No Operation (90h)](#nop---no-operation-90h)
- [NOT - One's Compliment Negation (Logical NOT)](#not---ones-compliment-negation-logical-not)
- [OR - Inclusive Logical OR](#or---inclusive-logical-or)
- [OUT - Output Data to Port](#out---output-data-to-port)
- [OUTS - Output String to Port (80188+)](#outs---output-string-to-port-80188)
- [POP - Pop Word off Stack](#pop---pop-word-off-stack)
- [POPA - Pop All Registers off Stack (80188+)](#popa---pop-all-registers-off-stack-80188)
- [POPF - Pop Flags off Stack](#popf---pop-flags-off-stack)
- [PUSH - Push Word onto Stack](#push---push-word-onto-stack)
- [PUSHA - Push All Registers onto Stack (80188+)](#pusha---push-all-registers-onto-stack-80188)
- [PUSHF - Push Flags onto Stack](#pushf---push-flags-onto-stack)
- [RCL - Rotate Through Carry Left](#rcl---rotate-through-carry-left)
- [RCR - Rotate Through Carry Right](#rcr---rotate-through-carry-right)
- [REP - Repeat String Operation](#rep---repeat-string-operation)
- [REPE/REPZ - Repeat Equal / Repeat Zero](#repe-repz---repeat-equal--repeat-zero)
- [REPNE/REPNZ - Repeat Not Equal / Repeat Not Zero](#repne-repnz---repeat-not-equal--repeat-not-zero)
- [RET/RETF - Return From Procedure](#ret-retf---return-from-procedure)
- [ROL - Rotate Left](#rol---rotate-left)
- [ROR - Rotate Right](#ror---rotate-right)
- [SAL/SHL - Shift Arithmetic Left / Shift Logical Left](#sal-shl---shift-arithmetic-left--shift-logical-left)
- [SAR - Shift Arithmetic Right](#sar---shift-arithmetic-right)
- [SBB - Subtract with Borrow/Carry](#sbb---subtract-with-borrow-carry)
- [SCAS - Scan String (Byte, Word)](#scas---scan-string-byte-word)
- [SHL - Shift Logical Left](#shl---shift-logical-left)
- [STC - Set Carry](#stc---set-carry)
- [STD - Set Direction Flag](#std---set-direction-flag)
- [STI - Set Interrupt Flag (Enable Interrupts)](#sti---set-interrupt-flag-enable-interrupts)
- [STOS - Store String (Byte, Word)](#stos---store-string-byte-word)
- [SUB - Subtract](#sub---subtract)
- [TEST - Test For Bit Pattern](#test---test-for-bit-pattern)
- [XCHG - Exchange Register/Memory with Register](#xchg---exchange-register-memory-with-register)
- [XLAT - Translate Byte in AL Using Table in Memory](#xlat---translate-byte-in-al-using-table-in-memory)
- [XOR - Exclusive OR](#xor---exclusive-or)

> It's a good programming practice to organize code so the expected case is executed without a jump since the actual jump takes longer to execute than falling through the test.

### ADC - Add With Carry
- Usage: ADC dest,src
- Modifies flags: AF CF OF SF PF ZF
- Sums two binary operands placing the result in the destination. If CF is set, a 1 is added to the destination.
- Arguments: reg,reg mem,reg reg,mem reg,immed mem,immed accum,immed

### ADD - Arithmetic Addition
- Usage: ADD dest,src
- Modifies flags: AF CF OF PF SF ZF
- Adds "src" to "dest" and replacing the original contents of "dest". Both operands are binary.
- Arguments: reg,reg mem,reg reg,mem reg,immed mem,immed accum,immed

### AND - Logical And
- Usage: AND dest,src
- Modifies flags: CF OF PF SF ZF (AF undefined)
- Performs a logical AND of the two operands replacing the destination with the result.
- Arguments: reg,reg mem,reg reg,mem reg,immed mem,immed accum,immed

### CALL - Procedure Call
- Usage: CALL destination
- Modifies flags: None
- Pushes Instruction Pointer (and Code Segment for far calls) onto stack and loads Instruction Pointer with the address of proc-name. Code continues with execution at CS:IP.

### CBW - Convert Byte to Word
- Usage: CBW
- Modifies flags: None
- Converts byte in AL to word Value in AX by extending sign of AL throughout register AH.

### CLC - Clear Carry
- Usage: CLC
- Modifies flags: CF
- Clears the Carry Flag.

### CLD - Clear Direction Flag
- Usage: CLD
- Modifies flags: DF
- Clears the Direction Flag causing string instructions to increment the SI and DI index registers.

### CLI - Clear Interrupt Flag (disable)
- Usage: CLI
- Modifies flags: IF
- Disables the maskable hardware interrupts by clearing the Interrupt flag. NMI's and software interrupts are not inhibited.

### CMC - Complement Carry Flag
- Usage: CMC
- Modifies flags: CF
- Toggles (inverts) the Carry Flag

### CMP - Compare
- Usage: CMP dest,src
- Modifies flags: AF CF OF PF SF ZF
- Subtracts source from destination and updates the flags but does not save result. Flags can subsequently be checked for conditions (e.g. with [Jxx instructions]).
- Arguments: reg,reg mem,reg reg,mem reg,immed mem,immed accum,immed

### CMPS - Compare String (Byte, Word)
- Usage: CMPS dest,src CMPSB CMPSW
- Modifies flags: AF CF OF PF SF ZF
- Subtracts destination value from source without saving results. Updates flags based on the subtraction and the index registers SI and DI are incremented or decremented depending on the state of the Direction Flag. CMPSB inc/decrements the index registers by 1, CMPSW inc/decrements by 2, while CMPSD increments or decrements by 4. The REP prefixes can be used to process entire data items.

### CWD - Convert Word to Doubleword
- Usage: CWD
- Modifies flags: None
- Extends sign of word in register AX throughout register DX forming a doubleword quantity in DX:AX.

### DEC - Decrement
- Usage: DEC dest
- Modifies flags: AF OF PF SF ZF
- Unsigned binary subtraction of one from the destination.

### DIV - Divide
- Usage: DIV src
- Modifies flags: (AF,CF,OF,PF,SF,ZF undefined)
- Unsigned binary division of accumulator by source. If the source divisor is a byte value then AX is divided by "src" and the quotient is placed in AL and the remainder in AH. If source operand is a word value, then DX:AX is divided by "src" and the quotient is stored in AX and the remainder in DX.
- Arguments: reg8 reg16 mem8 mem16

### HLT - Halt CPU
- Usage: HLT
- Modifies flags: None
- Halts CPU until RESET line is activated, NMI or maskable interrupt received. The CPU becomes dormant but retains the current CS:IP for later restart.

### IDIV - Signed Integer Division
- Usage: IDIV src
- Modifies flags: (AF,CF,OF,PF,SF,ZF undefined)
- Signed binary division of accumulator by source. If source is a byte value, AX is divided by "src" and the quotient is stored in AL and the remainder in AH. If source is a word value, DX:AX is divided by "src", and the quotient is stored in AL and the remainder in DX.
- Arguments: reg8 reg16 mem8 mem16

### IMUL - Signed Multiply
- Usage: IMUL src
- Modifies flags: CF OF (AF,PF,SF,ZF undefined)
- Signed multiplication of accumulator by "src" with result placed in the accumulator. If the source operand is a byte value, it is multiplied by AL and the result stored in AX. If the source operand is a word value it is multiplied by AX and the result is stored in DX:AX.
- Arguments: reg8 reg16 mem8 mem16

### IN - Input Byte or Word From Port
- Usage: IN accum,port
- Modifies flags: None
- A byte or word is read from "port" and placed in AL or AX respectively. If the port number is in the range of 0-255 it can be specified as an immediate, otherwise the port number must be specified in DX. Valid port ranges on the PC are 0-1024, though values through 65535 may be specified and recognized by third party vendors and PS/2's.

### INC - Increment
- Usage: INC dest
- Modifies flags: AF OF PF SF ZF
- Adds one to destination unsigned binary operand.

### INS - Input String from Port (80188+)
- Usage: INS dest,port INSB INSW
- Modifies flags: None
- Loads data from port to the destination ES:DI (even if a destination operand is supplied). DI is adjusted by the size of the operand and increased if the Direction Flag is cleared and decreased if the Direction Flag is set. For INSB, INSW no operands are allowed and the size is determined by the mnemonic.

### INT - Interrupt
- Usage: INT num
- Modifies flags: TF IF
- Initiates a software interrupt by pushing the flags, clearing the Trap and Interrupt Flags, pushing CS followed by IP and loading CS:IP with the value found in the interrupt vector table. Execution then begins at the location addressed by the new CS:IP.

### INTO - Interrupt on Overflow
- Usage: INTO
- Modifies flags: IF TF
- If the Overflow Flag is set this instruction generates an INT 4 which causes the code addressed by 0000:0010 to be executed.

### IRET - Interrupt Return
- Usage: IRET
- Modifies flags: AF CF DF IF PF SF TF ZF
- Returns from an interrupt procedure by popping IP, CS, and flags from stack, in that order.

### JA - Jump if Above
- Usage: JA label
- Modifies flags: None
- If CF=0 and ZF=0 transfers control to label, else continues with next instruction. Operands must be of same size. If they are not, you will need to use the data size override operator.

### JAE - Jump if Above or Equal
- Usage: JAE label
- Modifies flags: None
- If CF=0 transfers control to label, else continues with next instruction. Operands must be of same size. If they are not, you will need to use the data size override operator.

### JC - Jump if Carry (Same as JB)
- Usage: JC label
- Modifies flags: None
- If CF=1 transfers control to label, else continues with next instruction.

### JE - Jump if Equal (Same as JZ)
- Usage: JE label
- Modifies flags: None
- If ZF=1 transfers control to label, else continues with next instruction.

### JG - Jump if Greater
- Usage: JG label
- Modifies flags: None
- If ZF=0 and SF=OF transfers control to label, else continues with next instruction.

### JGE - Jump if Greater or Equal
- Usage: JGE label
- Modifies flags: None
- If SF=OF transfers control to label, else continues with next instruction.

### JL - Jump if Less
- Usage: JL label
- Modifies flags: None
- If SF<>OF transfers control to label, else continues with next instruction.

### JLE - Jump if Less or Equal
- Usage: JLE label
- Modifies flags: None
- If ZF=1 or SF<>OF transfers control to label, else continues with next instruction.

### JMP - Jump
- Usage: JMP label
- Modifies flags: None
- Transfers control unconditionally to label.

### LAHF - Load AH with Flags
- Usage: LAHF
- Modifies flags: None
- Loads AH with lower byte of flags. Bits 4-7 correspond to the flags, bits 0-3 are set to 1, 0, 0, and 0 respectively.

### LEA - Load Effective Address
- Usage: LEA reg,memory
- Modifies flags: None
- Loads register with offset of specified memory location.

### LDS - Load DS and Register
- Usage: LDS reg,memory
- Modifies flags: None
- Loads DS with word at memory location "memory" and loads the specified register with the word at memory location "memory"+2.

### LES - Load ES and Register
- Usage: LES reg,memory
- Modifies flags: None
- Loads ES with word at memory location "memory" and loads the specified register with the word at memory location "memory"+2.

### LOCK - Lock Bus
- Usage: LOCK
- Modifies flags: None
- Asserts the bus lock signal preventing other processors on the bus from gaining control of the system bus.

### LODS - Load String (Byte or Word)
- Usage: LODS src LODSB LODSW
- Modifies flags: None
- Loads AL or AX with the byte or word at memory location DS:SI. SI is then incremented or decremented based on the size of the operand and the state of the Direction Flag. For LODSB and LODSW no operands are allowed and size is determined by the mnemonic.

### LOOP - Loop
- Usage: LOOP label
- Modifies flags: None
- Decrements CX and transfers control to label if CX is not 0. If CX is 0, execution continues with the next instruction.

### LOOPZ - Loop While Equal (Same as LOOPE)
- Usage: LOOPZ label
- Modifies flags: None
- Decrements CX and transfers control to label if CX is not 0 and ZF is set. If either of these conditions are not met, execution continues with the next instruction.

### LOOPNZ - Loop While Not Equal (Same as LOOPNE)
- Usage: LOOPNZ label
- Modifies flags: None
- Decrements CX and transfers control to label if CX is not 0 and ZF is clear. If either of these conditions are not met, execution continues with the next instruction.

### MOV - Move Byte or Word
- Usage: MOV dest,src
- Modifies flags: None
- Transfers byte or word from source to destination. The source and destination operands cannot both be memory operands.
- Arguments: reg,reg mem,reg reg,mem reg,immed mem,immed accum,immed

### MOVS - Move String (Byte or Word)
- Usage: MOVS dest,src MOVSB MOVSW
- Modifies flags: None
- Moves byte or word at DS:SI to ES:DI. SI and DI are then adjusted based on the size of the operand and the state of the Direction Flag. For MOVSB and MOVSW no operands are allowed and size is determined by the mnemonic.

### MUL - Multiply
- Usage: MUL src
- Modifies flags: CF OF (AF,PF,SF,ZF undefined)
- Unsigned multiplication of accumulator by "src" with result placed in accumulator. If the source operand is a byte value it is multiplied by AL and the result is stored in AX. If the source operand is a word value it is multiplied by AX and the result is stored in DX:AX.

### NEG - Negate
- Usage: NEG dest
- Modifies flags: CF OF PF AF SF ZF
- Two's complement negation of the destination operand.

### NOP - No Operation
- Usage: NOP
- Modifies flags: None
- Performs no operation and continues with the next instruction.

### NOT - Logical Not
- Usage: NOT dest
- Modifies flags: None
- Logical NOT of destination (each bit is inverted: 0->1, 1->0).

### OR - Logical Or
- Usage: OR dest,src
- Modifies flags: CF OF PF SF ZF (AF undefined)
- Performs a logical OR of the two operands, replacing the destination with the result.

### OUT - Output Byte or Word to Port
- Usage: OUT port,accum
- Modifies flags: None
- A byte or word is transferred from AL or AX to "port". If the port number is in the range of 0-255 it can be specified as an immediate, otherwise the port number must be specified in DX. Valid port ranges on the PC are 0-1024, though values through 65535 may be specified and recognized by third party vendors and PS/2's.

### OUTS - Output String to Port (80188+)
- Usage: OUTS port,src OUTSB OUTSW
- Modifies flags: None
- Sends data from source operand to port. If no source operand is specified, DS:SI is assumed. SI is adjusted by the size of the operand and increased if the Direction Flag is cleared and decreased if the Direction Flag is set. For OUTSB, OUTSW no operands are allowed and the size is determined by the mnemonic.

### POP - Pop Word off Stack
- Usage: POP reg/mem
- Modifies flags: None
- A word is removed from the top of the stack and placed in the destination.

### POPF - Pop Flags off Stack
- Usage: POPF
- Modifies flags: AF CF DF IF PF SF TF ZF
- Flags are popped from the stack into the flag register. The value of the Interrupt Flag is not affected if the instruction was executed in Virtual 8086 mode.

### PUSH - Push Word onto Stack
- Usage: PUSH reg/mem
- Modifies flags: None
- Pushes the source operand onto the stack.

### PUSHF - Push Flags onto Stack
- Usage: PUSHF
- Modifies flags: None
- Pushes the flag register onto the stack.

### RCL - Rotate Left through Carry
- Usage: RCL dest,count
- Modifies flags: CF OF
- Shifts bits of destination to the left for count times (each shift count is given by the least significant bits of the count operand) with the bit going into the Carry Flag being shifted into the least significant bit of the destination and the bit going out of the most significant bit of the destination shifted into the Carry Flag.

### RCR - Rotate Right through Carry
- Usage: RCR dest,count
- Modifies flags: CF OF
- Shifts bits of destination to the right for count times (each shift count is given by the least significant bits of the count operand) with the bit going into the Carry Flag being shifted into the most significant bit of the destination and the bit going out of the least significant bit of the destination shifted into the Carry Flag.

### RET - Return from Procedure
- Usage: RET count?
- Modifies flags: None
- Pops IP (and optionally CS) from stack. If the optional count operand is used, it specifies the number of bytes to release from the stack after IP and CS are popped. This allows for the clearing of parameters pushed onto the stack before the procedure was called.

### ROL - Rotate Left
- Usage: ROL dest,count
- Modifies flags: CF OF
- Shifts bits of destination to the left for count times. The bit that was in the highest bit position is shifted into the lowest bit position.

### ROR - Rotate Right
- Usage: ROR dest,count
- Modifies flags: CF OF
- Shifts bits of destination to the right for count times. The bit that was in the lowest bit position is shifted into the highest bit position.

### SAHF - Store AH into Flags
- Usage: SAHF
- Modifies flags: AF CF PF SF ZF
- Bits 4-7 of AH are transferred to the equivalent flag bits. Bits 0-3 of AH are ignored.

### SAL - Shift Arithmetic Left (Same as SHL)
- Usage: SAL dest,count
- Modifies flags: CF OF PF SF ZF (AF undefined)
- Shifts bits of destination to the left count times, filling the vacated bit positions with zeros.

### SAR - Shift Arithmetic Right
- Usage: SAR dest,count
- Modifies flags: CF OF PF SF ZF (AF undefined)
- Shifts bits of destination to the right count times, filling the vacated bit positions with the original value of the high bit.

### SBB - Subtract with Borrow
- Usage: SBB dest,src
- Modifies flags: AF CF OF PF SF ZF
- Subtracts source and borrow flag (CF) from destination. The result is stored in destination.

### SCAS - Scan String (Byte, Word)
- Usage: SCAS dest SCASB SCASW
- Modifies flags: AF CF OF PF SF ZF
- Compares AL or AX with byte or word at ES:DI. DI is then adjusted based on the size of the operand and the state of the Direction Flag. For SCASB and SCASW no operands are allowed and size is determined by the mnemonic.

### SHL - Shift Logical Left (Same as SAL)
- Usage: SHL dest,count
- Modifies flags: CF OF PF SF ZF (AF undefined)
- Shifts bits of destination to the left count times, filling the vacated bit positions with zeros.

### SHR - Shift Logical Right
- Usage: SHR dest,count
- Modifies flags: CF OF PF SF ZF (AF undefined)
- Shifts bits of destination to the right count times, filling the vacated bit positions with zeros.

### STC - Set Carry Flag
- Usage: STC
- Modifies flags: CF
- Sets the Carry Flag.

### STD - Set Direction Flag
- Usage: STD
- Modifies flags: DF
- Sets the Direction Flag causing string instructions to decrement the SI and DI index registers.

### STI - Set Interrupt Flag (enable)
- Usage: STI
- Modifies flags: IF
- Enables the maskable hardware interrupts by setting the Interrupt flag. NMI's and software interrupts are not inhibited.

### STOS - Store String (Byte, Word)
- Usage: STOS dest STOSB STOSW
- Modifies flags: None
- Stores AL or AX in destination ES:DI. DI is then adjusted based on the size of the operand and the state of the Direction Flag. For STOSB and STOSW no operands are allowed and size is determined by the mnemonic.

### SUB - Subtract
- Usage: SUB dest,src
- Modifies flags: AF CF OF PF SF ZF
- Subtracts source operand from destination operand.

### TEST - Logical Compare
- Usage: TEST dest,src
- Modifies flags: CF OF PF SF ZF (AF undefined)
- Logical AND of operands updating flags but result is discarded.

### WAIT - Wait for Test
- Usage: WAIT
- Modifies flags: None
- Waits for the numeric processor's busy pin to go high.

### XCHG - Exchange
- Usage: XCHG dest,src
- Modifies flags: None
- Exchanges the contents of source and destination.

### XLAT - Table Lookup
- Usage: XLAT table?
- Modifies flags: None
- Replaces the byte in AL with the byte from the table in DS pointed to by BX and AL. If the optional table operand is used, the segment register in the operand is used instead of DS.

### XOR - Logical Exclusive OR
- Usage: XOR dest,src
- Modifies flags: CF OF PF SF ZF (AF undefined)
- Performs a logical exclusive OR of the two operands replacing the destination with the result.
