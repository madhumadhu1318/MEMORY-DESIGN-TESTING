## MEMORY-DESIGN-TESTING
# PROJECT REPORT DESIGN OF 4X4 SRAM MEMORY ARRAY

# Introduction
Memory is the process of storing and recalling information that was 
previously acquired. Memory is the means of storing information 
(data and Instructions) in the form of 1s and 0s. A large portion of 
Digital Design is dedicated to the storage of data and Program 
Instruction i.e., believed to take up to 80% of the chip area. Starting 
from Intel’s first 1Kb DRAM chip in the seventies, nowadays DRAM 
capacities have reached beyond 1Gb. The advent of virtual memory 
in personal computers contributed to the hierarchical structure of 
various kinds of memory ranging from the small capacity, fast but 
more costly cache memories to large capacity, slower but more 
affordable magnetic and optical storage. Depending on the 
Application the amount of Memory requirement varies. More than 
half of the transistors in high-performance Microprocessors are 
devoted to cache memories and the ratio is expected to further 
increase.

# MEMORY HIERARCHY AND NEED FOR SRAM MEMORY
The pyramid-like hierarchy of memory types in a personal computer, 
shown in Figure 1.1 reflects the growing speed and cost/bit as we 
move from the bottom Level 5 (L5) remote secondary storage to the 
topmost register Level (L ). The introduction of the memory
hierarchy is a fundamental consequence of maintaining the randomaccess memory abstraction and practical limits on cost and power 
consumption .The growing gap between the Micro Processor Unit 
(MPU) cycle time and DRAM access time necessitated introducing 
several caching levels in modern data processors. In personal 
computer MPUs, such levels are often represented by LI and L2 onchip embedded SRAM cache memories. As the speed gap between 
MPU, memory, and mass storage continues to widen, deeper memory 
hierarchies have been introduced in high-end server microprocessors.
Memory design and testing
 

# SRAM CELL
• Two Cross Couple CM S Inverters are formed by using 
Transistor pairs Q1 -Q3 and Q2 - Q4.
• Two Bit Lines are used to transfer data and are a complement 
to each other and form the cell.
• The generic structure of the M S static RAM cell, consists of 
two cross-coupled CM S inverters and two access transistors 
as shown.
• Access to the cell is enabled by the word line, WL, which 
controls the 2 pass transistors, Q5 and Q6.
• These access M S devices provide the provision to Write / 
Read the stable state stored in back-toback connected 
Inverters.
• These Access Transistors also Isolate one Cell from another in 
a Memory Array.
• Q indicates the data stored in the Cell.
• Bit Line (BL) and BL’ are the lines through which data access is 
done.


# Implementation and Simulation Result
We have implemented a 6T SRAM with CR=1.25 and PR=0.85 using 
180nm technology by keeping the length of all devices as 180nm. 
We verified the Read and Write operation and also plotted the 
Butterfly curve for Hold state and Read state.

![1](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/ee3600a3-f05b-4fde-9285-e5af34b63bf1)

# Circuit diagram
(Width of pull up transistors = 400nm, Width of access transistors = 
470nm, = Width of pull down transistors = 590nm)



# SRAM Operations

![2](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/8c13c0bc-132a-4acb-8dc9-564b586f2c86)

 # Write operation
Initially word line WL is high and hence bit lines BL and Bl’ are 
connected to the SRAM cell. Then the write driver circuit provides 
the required voltage to BL and BL’ ( For write 0, BL = 0, BL’ = 1 and 
for write 1, BL=1, BL’ = 0). The corresponding data will be then 
written into the cell (Q = 0 for write 0 and Q = 1 for write 1). For a 
successful write operation, access transistors should be stronger 
than the pull up transistors which is taken care by the pull-up ratio.

# Write ‘0’ operation

![3](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/46a4bf85-090e-43ed-816c-0c5b99729b4c)

# Timing diagram for Write ‘0’

![4](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/f1f302a8-ca7d-4142-abf5-691522b8cab2)

# Write ‘1’ operation
![5](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/51c60778-6666-488f-ad25-489733caf3c7)

# Timing diagram for Write ‘1’
![6](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/58e4cf75-7779-4c4d-96dd-3f287960f4ee)

# Read operation
To perform read operation, the memory cell should have some value. 
Consider, ‘1’ is stored in the memory cell (Q =1 and Q’ = 0). Initially 
the bit lines BL and BL’ are pre-charged to Vdd. Then the word line 
WL is made high. So the transistors M1, M4, M5 and M6 (From Fig 1) 
will turn N. Therefore BL’ gets discharged through the series 
transistors M5-M1 and BL will remain at its pre-charged state. As the 
difference between the two bit lines build up, the sense amplifier is 
activated which gives output i.e. ‘1’ is read from the memory cell.

# Read ‘0’ operation
![7](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/f2bf0ae5-c01c-4a23-925e-558f797e341e)
# Timing diagram for Read ‘0’
![8](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/b9062860-1e0a-4d8b-b89a-0d5805955601)
# Read ‘1’ operation
![9](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/0bac817f-9328-4856-a999-cb30683b10aa)
# Timing diagram for Read ‘1’
![10](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/f3bc839f-e0be-4643-ab5a-39fa0bca80b3)

# Stability of SRAM cell
The stability of the SRAM cell can be described by the ‘Butterfly curve’
which is obtained by superimposing the voltage transfer curves (VTC) of 
the two inverters of the memory cell. Stability of the SRAM cell can be 
analysed by measuring the Static Noise Margin (SNM). SNM is the measure 
of stability of the SRAM cell to hold its data against noise. The Stability 
of the cell is given by the size of the maximum square box that can fit 
inside the Butterfly wing.

![11](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/d169193e-540d-4bd6-bee6-ec7b8d4d1552)

Butterfly curve for the SRAM cell

# Butterfly curve for Read state

![12](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/d9d1260e-ff75-4569-bdb9-015b6d702258)
# Pre-Charge Circuit
![13](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/cde5cebb-104f-47b6-884d-490ec6c5edd4)
# Sense Amplifier
![14](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/327e5b1d-b030-4e6b-b948-00c77549b838)
# Isolation Circuit
![15](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/abb40827-a721-499c-933b-f055e2b374b1)
# Write Driver Circuit
![16](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/da2f633a-87bc-401a-8596-42d57df37b46)

# Read/Write Operations
# Read Operation Circuit
![17](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/4b369f60-53b9-4778-ac00-5389d73821fc)

# Timing Diagram for Read ‘0’

![18](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/37edd1ce-5e94-4a7d-bf29-43a8516dfa54)

# Timing Diagram for Read ‘1’
![19](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/afb25ba3-44d9-46b9-8fd7-b47fff06093c)

# Write Operation Circuit
![20](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/8136b0be-785b-42e7-8e77-a0fdd9aa5ba5)

# Timing Diagram for Write ‘0’ when Write Enable is High
![21](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/fc450e8b-6267-44f0-b9f5-930fc0439d72)
# Timing Diagram for Write ‘1’ when Write Enable is High
![22](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/35b74469-3cec-4842-b47f-adbdef500d95)

# Making of a 4 x 4 SRAM Array
# A 4 x 1 SRAM Array
![23](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/99a48fbf-4103-4524-b92e-8df90d608f73)

# A 4 x 4 SRAM Array
![24](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/fc9becb8-d4fc-488d-9ff4-64ad06386920)
# A 4 x 4 SRAM Array Symbol
![25](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/38132344-ae30-423d-8524-ade1fda418d9)
# Timing Diagram
![26](https://github.com/madhumadhu1318/MEMORY-DESIGN-TESTING/assets/90201844/88c0199b-4b94-4725-a54e-63ac860b4967)
