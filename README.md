hey guys! Azam here.It's my first repositiry in github so i hope you don't mind the beginner's mistake. 
Anyways as the projects states it is a 128 bit processor using verilog which can encrypt and decrypt plain text using AES (Advanced Encryption Standard).

**128-Bit AES Cryptographic Processor**
A high-performance hardware accelerator implementing the Advanced Encryption Standard (AES-128) algorithm using Verilog HDL. This design features a fully synthesized hardware architecture designed for optimized throughput and resource utilization, suitable for cryptographic security in VLSI applications.
**Key Features**
• Standard Compliant: Implements full 128-bit block encryption and decryption processing.
• Modular Architecture: Structured with dedicated independent hardware blocks for core transformations.
• Optimized Control Unit: Integrated finite state machine (FSM) controller managing synchronization and data routing across encryption rounds.
• Verification Suite: Includes extensive behavioral testbenches confirming algorithmic correctness against official NIST validation vectors.
**Repository Structure**
• /src or root files:
 • subbytes.zip: S-Box lookup table implementations for byte substitution.
 • shiftrows.zip: Row shifting permutation stage modules.
 • mixcolumns.zip: Galois Field (\(GF(2^8)\)) matrix multiplication blocks.
 • keyspansion_unit.zip: On-the-fly round key generator producing ten 128-bit subkeys from the original cipher key.
 • inv_controller.zip: Structural control paths managing inverse decryption pipelines.
 • aes_testbench.txt: Simulation script containing test scenarios and verification checks.
 **🛠️ Hardware Transformation Pipeline**
The processor sequences through the standard cryptographic transformations over 10 active operational rounds:
1. Key Expansion: Extends the primary 128-bit key into an expanded key array for individual round scheduling.
2. AddRoundKey: XORs the current intermediate state matrix with the corresponding 128-bit round subkey.
3. SubBytes / InvSubBytes: Non-linear byte substitution using calculated mathematical mappings.
4. ShiftRows / InvShiftRows: Cyclical byte transposition array shifts.
5. MixColumns / InvMixColumns: Column diffusion operations combining local elements linearly.

THANK YOU!!:)
