{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Wireshark Packet Analysis Lab\
\
Project demonstrating packet-level network analysis using Wireshark on a public sample PCAP.\
\
## Objectives\
- Inspect protocol hierarchy and conversations\
- Apply display filters (DNS, HTTP, TCP)\
- Reconstruct TCP streams and analyze payloads\
- Document findings and produce an audit-style report\
\
## Repository Structure\
- `/pcaps` \'97 sample_wireshark_traffic.pcap\
- `/screenshots` \'97 images from Wireshark analysis\
- `/report` \'97 `network-analysis.md` (detailed findings)\
\
## How to reproduce\
1. Open the PCAP in Wireshark\
2. Use `Statistics \uc0\u8594  Protocol Hierarchy` for overview\
3. Use `Statistics \uc0\u8594  Conversations \u8594  TCP` to find top talkers\
4. Apply filters like `dns`, `http`, `tcp.flags.syn == 1`\
5. Right-click a TCP packet and select **Follow \uc0\u8594  TCP Stream**\
\
## Notes\
This capture is a public sample from Wireshark's sample repository. Analysis focuses on protocol behavior and basic anomaly identification.}