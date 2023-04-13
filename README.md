# 6-Bit-CPU
<ul>
  <li>Word Size of CPU = 6</li>
  <li>ALU Operations = AND,ADD,ROR</li>
  <li>Register Number = 5</li>
  <li>Size of RAM = 9</li>
  <li>Word size of ISA and RAM = 15</li>
  <li>CPU Instructions = Register mode, Immediate mode, JMP,JL</li>
</ul>

#ISA
<ol>
  <li>Register Mode (type of op=00) : 2 bit (type of op) + 2 bit (op) + 3 bit (Reg1) + 3 bit (Reg1) + 5 bit (don't care)</li>
  <ul>
    <li>AND (OP= 00)</li>
    <li>ADD (OP= 01)</li>
    <li>ROR (OP= 10)</li>
  </ul>
  <li>Immediate Mode (type of op=01) : 2 bit (type of op) + 2 bit (op) + 3 bit (Reg1) + 6 bit (Imm value) + 2 bit (don't care)</li>
  <ul>
    <li>AND (OP= 00)</li>
    <li>ADD (OP= 01)</li>
    <li>ROR (OP= 10)</li>
  </ul>
  <li>Jump Mode (type of op=10) : 2 bit (type of op) + 2 bit (op) + 4 bit (Addr_of_sram) + 7 bit (don't care)</li>
  <ul> 
    <li>JMP (OP= 00)</li>
    <li>JL (OP= 01)</li>
  </ul>
</ol>

#Sample Assembly and Machine Code
<table>
  <tr>
    <th>Assembly Code</th>
    <th>Machine Code</th>
  </tr>
  <tr>
    <td>START: ADD R1, 0</td>
    <td>010100100000000</td>
  </tr>
  <tr>
    <td>ADD R2, 1</td>
    <td>010101000000100</td>
  </tr>
  <tr>
    <td>AND R1, R2</td>
    <td>000000101000000</td>
  </tr>
  <tr>
    <td>JMP START</td>
    <td>100000010000000</td>
  </tr>
</table>



