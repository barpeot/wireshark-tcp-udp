# wireshark-tcp-udp
Oleh: Akbar Putra Asenti Priyanto (5025211004)

# Problem TCP

## 1. What is the IP address and TCP port number used by the client computer (source) that is transferring the alice.txt file to gaia.cs.umass.edu? 
Source ip is 192.168.86.68 while source port is 55639.

## 2. What is the IP address of gaia.cs.umass.edu? On what port number is it sending and receiving TCP segments for this connection?
Destination ip is 128.119.245.12 while Destination port is 80.

## 3. What is the sequence number of the TCP SYN segment that is used to initiate the TCP connection between the client computer and gaia.cs.umass.edu? What is it in this TCP segment that identifies the segment as a SYN segment? Will the TCP receiver in this session be able to use Selective Acknowledgments?
Sequence number is 4236649187, Flag 0x002 identifies the segment as SYN, and Yes, the receiver can use Selective Acknowledgements because SACK is permitted in the packet.

## 4. What is the sequence number of the SYNACK segment sent by gaia.cs.umass.edu to the client computer in reply to the SYN? What is it in the segment that identifies the segment as a SYNACK segment? What is the value of theAcknowledgement field in the SYNACK segment? How did gaia.cs.umass.edu determine that value? 
Sequence number is 1068969752, Flag 0x012 identifies the segment as SYNACK, Acknowledgement number is 4236649188, Acknowledgement number is determined as the next value after the sequence number of the SYN segment (4236649187).

## 5. What is the sequence number of the TCP segment containing the header of the HTTP POST command? How many bytes of data are contained in the payload (data) field of this TCP segment? Did all of the data in the transferred file alice.txt fit into this single segment?
Sequence number is 4236649188, Payload is 1514 bytes, and No.

## 6. Consider the TCP segment containing the HTTP “POST” as the first segment in the data transfer part of the TCP connection. 
### At what time was the first segment (the one containing the HTTP POST) in the data-transfer part of the TCP connection sent? 
0.024049 s

### At what time was the ACK for this first data-containing segment received?
0.052676 s

### What is the RTT for this first data-containing segment?
0.028627 s

### What is the RTT value the second data-carrying TCP segment and its ACK?

### What is the EstimatedRTT value (see Section 3.5.3, in the text) after the ACK for the second data-carrying segment is received?

### 7. What is the length (header plus payload) of each of the first four data-carrying TCP segments?

### 8. What is the minimum amount of available buffer space advertised to the client by gaia.cs.umass.edu among these first four data-carrying TCP segments? Does the lack of receiver buffer space ever throttle the sender for these first four datacarrying segments?
 
### 9. Are there any retransmitted segments in the trace file? What did you check for (in the trace) in order to answer this question?

### 10. How much data does the receiver typically acknowledge in an ACK among the first ten data-carrying segments sent from the client to gaia.cs.umass.edu? Can you identify cases where the receiver is ACKing every other received segment (see Table 3.2 in the text) among these first ten data-carrying segments?

### 11. What is the throughput (bytes transferred per unit time) for the TCP connection? 
