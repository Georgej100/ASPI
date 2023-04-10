# ASPI
A high speed, adaptable communication protocol that delivers high speed and flexibility

============================================================================================

ASPI stands for Advanced Serial Peripheral Interface and is similar to the SPI protocol. ASPI uses 5 wires to comunicate in either Tx and Rx mode or dual lane Tx mode.
The five conections needed are:

CLK            |      Clock signal

DAT1           |      Data lane 1

DAT2           |      Data lane 2

MOD            |      Data lane mode

CS (optional)  |      Chip select

============================================================================================

Clock:
The clock signal for data. Data is read on the rising edge

DAT1:
DAT1 is the Tx signal for both mode 1 and 2.

DAT2:
DAT2 will act as the Rx if the MOD signal is high. If the MOD signal is low then DAT2 will act as a second Tx signal for faster data transfer.

MOD:
MOD defines the mode in which DAT2 will act. If set to high, DAT2 will act as a Rx signal but if low, DAT2 will act as a second Tx lane.

CS (optional):
This signal can be used to string multiple slaves together.

NOTE: Tx and Rx in this spec sheet refer to the masters perspective.

============================================================================================

Uses:
ASPI is great for screens or transmitter that do not need to send data back to the master.

-- GeorgeJ100 --
