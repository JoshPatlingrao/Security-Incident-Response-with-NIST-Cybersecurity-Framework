# Security-Incident-Response-with-NIST-Cybersecurity-Framework

## Objective

This project was facilitated by the Google Cybersecurity Professional Certificate in Coursera. The student was in a scenario where their organization has undergone an ICMP flood attack. They must document and analyse the security incident through the NIST cybersecurity framework by giving a summary of the incident, identify the source, the protective methods deployed, the detection methods used, the response of the team and their receovery plan.

### Skills Learned
- Responding to a security incident using the NIST cybersecurity framework
- Writing an effective summary of security incident
- Concisely identifying source of the incident
- Record the protections deployed, detection methods and reponse of the team to the incident
- Outline the steps taken to recover from the incident

### Tools Used
- NIST Cybersecurity Framework

## Analysis

| Response | Notes |
| --- | --- |
| Summary | At a certain time during work hours, the company started receiving requests from visitors and customers that their services can’t be accessed. The IT team tried accessing the network servers through their devices and got the same result. They used their network log analyzer, tcpdump, and checked the network traffic. They found that the network was being sent ICMP packets from various IP addresses non-stop, a DDOS attack. The team responded by blocking the attack and stopping all non-critical network services so that critical network services could be restored.  |
| Identify | The company’s cybersecurity team audited the system and found that the attacker sent the flood of ICMP pings into the company’s network through an unconfigured firewall. It's likely a zero-day exploit, as the firewall is regularly audited by the cybersecurity team. All network resources needed to be secured and restored to functioning state. |
| Protect | The team has implemented a new firewall rule to limit the rate of incoming ICMP packet to prevent the network from being overwhelmed even with heavy traffic. Furthermore there will be additional verification for each IP address requesting to access the network, this is to check if the IP address has been spoofed and sending large number of ICMP packets. |
| Detect | To detect this type of attack in the future, the team implements a network monitoring interface which would detect abnormal traffic patterns and report this to the teams SIEM tool. Another layer of defense is the implementation of the IDS/IPS hardware to the network which would alert the team for any suspicious packets that could have come from a spoofed IP address. |
| Respond | The team will contact upper management or legal authorities based on severity of security incident. Stronger access controls such as segmentation will be implemented to make it easier to isolate the affected systems and prevent further disruption on operations. Regular monitoring of network logs will make it easier to spot potential incidents and results in faster reponse. |
| Recover | To recover from the DDOS attack, access to network services need to be restored to normal functioning state. All non-critical network services will be stopped to reduce internal network traffic. Critical network services will receive priority in restoration. Once DDOS attack has timed out, all non-critical network systems and services can be brought back online. As additional note, ICMP flood attacks can be blocked with a firewall. |

## Reflections & Notes

- The team could invest in NGFW which has more robust defenses and detection for suspicious network activity from external and internal traffic
