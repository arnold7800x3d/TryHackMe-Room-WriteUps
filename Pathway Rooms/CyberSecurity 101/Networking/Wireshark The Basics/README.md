# Wireshark: The Basics
## Task 1 Introduction
Which file is used to __simulate__ the screenshots?
```
http1.pcapng
```
Which file is used to __answer__ the questions?
```
Exercise.pcapng
```

## Task 2 Tool Overview
Read the __"capture file comments"__. What is the flag?
```
TryHackMe_Wireshark_Demo
```
What is the total number of packets?
```
58620
```
What is the __SHA256 hash__ value of the capture file?
```
f446de335565fb0b0ee5e5a3266703c778b2f3dfad7efeaeccb2da5641a6d6eb
```

## Task 3 Packet Dissection
Use the "Exercise.pcapng" file to answer the questions. __View packet number 38.__ Which markup language is used under the HTTP protocol?<br>
*Checked under the HTTP protocol*
```
eXtensible Markup Language
```
What is the arrival date of the packet? (Answer format: Month/Day/Year)<br>
*Checked in the __Frame__ section of the packet*
```
05/13/2004
```
What is the TTL value?<br>
*Checked in the __IP__ section of the packet*
```
47
```
What is the TCP payload size?<br>
*Checked in the __TCP__ section of the packet*
```
424
```
What is the e-tag value?
(For example: 82ecb-6321-9e904585)
*Personally tricky but found it in the __HTTP__ section of the packet*
```
9a01a-4696-7e354b00
```

## Task 4 Packet Navigation
Use the "Exercise.pcapng" file to answer the questions. Search the "r4w" string in packet details. What is the name of artist 1?<br>
*Go to __Edit > Find Packet__ then in the search bar type __r4w__. The answer is in HTML <h3></h3> tags.*
```
r4w8173
```
Go to packet 12 and read the packet comments. What is the answer?<br>
*Go to __Go > Find packet__ then search for packet 12. From there read the comments from the packet details and search for packet 39765 and navigate to the __JPEG__ section. Right click and choose __Export Packet Bytes__ and save the file. From the terminal, run __md5sum <filename>__*
```
911cd574a42865a956ccde2d04495ebf
```
There is a ".txt" file inside the capture file. Find the file and read it; what is the alien's name?<br>
*Go to __Edit > Find Packet__ then in the search bar type __.txt__. Keep clicking on find till the text file appears*
```
PACKETMASTER
```
Look at the expert info section. What is the number of warnings?
*Click the small red button at the bottom left of the wireshark window. Find the __Warnings__ info and scroll to the right to see the count.*
```
1636
```