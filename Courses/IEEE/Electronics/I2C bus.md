# Inter Integrated Circuit $I^2 C$
This works with 2 wires, that's an advantage. It need a start condition, ACK/NACK bit, (Acknowledge)/(Negative Acknowledge) it means the data has been received/sent successfully, data frames and stop condition. 

The 'normal position' is HIGH voltage, whenever it receives the data changes to a LOW voltage as a ACK for one bit. 
- 1.- Start Condition
- 2.- Each slave compares the address sent from the master to its own address. If the address matches, the slave returns an ACK bit by pulling the SDA line low for one bit.
- 3.- Data Transfer. Master sends or receive the data.
- 4.- When data transfer is over the master send the stop condition.