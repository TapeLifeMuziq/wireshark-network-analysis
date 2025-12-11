# Network Analysis Report

**PCAP source:** Wireshark sample capture (uploaded file: a6151746-105a-4bdf-aa2b-77cb1f3c5f67.pcap)

## Overview
This analysis inspects network traffic captured in the sample PCAP. Objectives were to identify protocol distribution, examine notable conversations, reconstruct TCP streams, and highlight anomalies or notable behaviors.

## Tools
- Wireshark (version: 4.6.2)
- OS: macOS (version: 15.7.2)

## Key Observations
- Protocol breakdown: The protocol hierarchy indicates that the majority of traffic in the capture is TCP-based, representing 57.5% of all observed packets. DNS traffic accounts for approximately 5%, reflecting periodic hostname resolution activity. HTTP makes up roughly 1.3% of the traffic, indicating limited but present web-related communication. The remaining traffic consists of various lower-level or background protocols not significant in volume.

- Top conversation: [10.1.101.168 → 10.1.102.121, ports 41342 → 46584] — Most of the data flows from 10.1.102.121 back to 10.1.101.168, with 60,066 of 60,734 bytes sent in that direction over a very short 0.006-second exchange.
- Notable packet behaviors:
- No retransmissions observed
- No repeated DNS requests detected
- No unencrypted HTTP payloads observed; traffic appears to consist of normal TCP data

##Detailed Findings
1. **Protocol Hierarchy**
	- Summary: TCP traffic dominates the capture, with small amounts of DNS and HTTP activity observed.
2. **TCP Conversations**
	 	- Top Conversation: 10.1.101.168 → 10.1.102.121 (ports 41342 → 46584) is notable for transferring 60,734 bytes in a very short 0.006-second window, with most data flowing from the destination back to the source.
3.	 **TCP Stream Reconstruction**
		- Summary of Stream: Conversation shows standard TCP data transfer; no HTTP GETs, unencrypted payloads, or suspicious content detected.
4.	 **DNS Analysis**
		- Observed Queries and Answers: No repeated or suspicious DNS queries noted in this segment; standard resolution behavior consistent with normal network activity.

Conclusions & Next Steps
	- No immediate evidence of malware or malicious traffic observed.
	- Suggested next steps: run deeper DNS reputation lookups, correlate with host logs, import PCAP into a SIEM, or convert findings into test alerts for monitoring.

Artifacts
	- Screenshots: /screenshots/protocol_hierarchy.png, /screenshots/tcp_conversations.png, /screenshots/tcp_stream_1.png, /screenshots/packet_details_1.png
	- PCAP: cisco-nexus92-erspan-marker.pcap
