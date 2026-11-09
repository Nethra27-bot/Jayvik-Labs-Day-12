# Jayvik-Labs-Day-12


Below is a professionally structured version of your Day 12 – Linux Networking assignment, suitable for a cybersecurity student portfolio, academic submission, and GitHub repository.

The content uses formal technical language, clear explanations, proper command formatting, and a professional report structure.

# DAY 12 – LINUX NETWORKING

CYBERSECURITY TRAINING# Linux Networking Fundamentals

Day 12 | Theory and Practical Learning Report

Student Name: Nethra M

Course: Cybersecurity

Assignment: Day 12

Topic: Linux Networking Fundamentals

Operating System: Kali Linux

Virtualization Platform: Oracle VirtualBox

Assignment Type: Theory and Practical Learning

Recommended PDF filename

`StudentName_Day12_LinuxNetworking.pdf`

## 1. Introduction

Linux networking is an essential component of cybersecurity. It provides the foundation for understanding how computers communicate, exchange information, and interact with other devices over networks.

Linux offers several built-in networking utilities that allow users to inspect network interfaces, configure IP addresses, examine routing tables, troubleshoot connectivity, resolve domain names, and monitor network connections.

This assignment focuses on understanding fundamental Linux networking concepts and exploring commonly used networking commands in Kali Linux.

## 2. Objectives

The primary objectives of this assignment are:

- To understand the fundamentals of Linux networking.
- To identify different network interfaces and their functions.
- To understand IP addressing, routing, and default gateways.
- To learn how DNS resolves domain names.
- To understand the purpose of TCP and UDP protocols.
- To explore Linux networking and troubleshooting commands.
- To inspect network sockets and active listening services.
- To understand the importance of networking knowledge in cybersecurity.

## 3. Theory – Questions and Answers

### Q1. What is a network interface?

A network interface is a hardware or software component that enables a computer to establish communication with other devices over a network.

It acts as a connection point through which data is transmitted and received. Common examples include Ethernet interfaces, wireless interfaces, and virtual network interfaces.

### Q2. What is the loopback interface?

The loopback interface is a special virtual network interface that allows a computer to communicate with itself without sending data through an external network.

In Linux, it is commonly identified as `lo`, and its standard IPv4 address is `127.0.0.1`.

It is primarily used for local testing, software development, and network diagnostics.

### Q3. What does `ip addr` display?

The `ip addr` command displays information about the network interfaces configured on a Linux system.

It provides details such as:

- Network interface names.
- IPv4 and IPv6 addresses.
- Interface status.
- MAC addresses.
- Network prefix information.

It is useful for identifying the IP configuration of a system.

### Q4. What is the purpose of `ip link`?

The `ip link` command is used to view and manage network interface settings in Linux.

It displays information about available network interfaces, including their operational state, MAC addresses, and interface properties.

It can also be used by authorized administrators to enable or disable network interfaces.

### Q5. What does `hostname -I` display?

The `hostname -I` command displays the IP addresses assigned to the system's network interfaces.

It provides a quick way to identify the system's network addresses without displaying all interface configuration details.

### Q6. What does `ip route show` display?

The `ip route show` command displays the routing table maintained by the Linux operating system.

The routing table contains information about available network destinations, gateways, and interfaces used to forward outgoing network traffic.

It helps administrators understand how a system determines where network packets should be sent.

### Q7. What is a default route?

A default route is a predefined network path used when no specific routing entry exists for a destination address.

In most home and office networks, the default route directs outgoing traffic to a router or gateway, which forwards it toward other networks or the internet.

### Q8. What does `ping` test?

The `ping` command is a network diagnostic utility used to test connectivity between two network devices.

It sends Internet Control Message Protocol (ICMP) echo requests to a destination and checks whether responses are received.

It can provide useful information about:

- Network reachability.
- Response time.
- Packet loss.
- Connectivity problems.

### Q9. Why can a failed ping be misleading?

A failed ping does not necessarily indicate that the destination device is offline.

Several factors can prevent successful ping responses, including:

- Firewall restrictions.
- ICMP traffic filtering.
- Network security policies.
- Incorrect routing configurations.
- Temporary network interruptions.

Therefore, additional diagnostic methods should be used before concluding that a system is unreachable.

### Q10. What is DNS?

DNS stands for Domain Name System. It is a naming service that translates human-readable domain names into IP addresses.

For example, DNS helps computers locate a website when a user enters a domain name such as `google.com` instead of manually entering its IP address.

DNS is an important component of internet communication and network infrastructure.

### Q11. What does `getent hosts` do?

The `getent hosts` command retrieves hostname and IP address information using the system's configured name resolution services.

It can be used to determine whether a hostname can be resolved into an associated IP address.

This command is useful for troubleshooting DNS and hostname resolution problems.

### Q12. What information does `ip neigh` display?

The `ip neigh` command displays information about neighboring devices known to the local Linux system.

It provides details such as:

- Neighboring IP addresses.
- Corresponding MAC addresses.
- Network interface information.
- Neighbor reachability states.

This information is useful for understanding communication between devices on a local network.

### Q13. What is a socket?

A socket is a communication endpoint that allows applications to exchange data locally or across a network.

A network socket is generally associated with an IP address, a transport protocol, and a port number.

Sockets are essential for applications such as web browsers, email services, and network servers.

### Q14. What does `ss -tuln` display?

The `ss -tuln` command displays listening TCP and UDP network sockets in numerical format.

The command options have the following meanings:

| Option | Description |
| --- | --- |
| `-t` | Displays TCP sockets |
| `-u` | Displays UDP sockets |
| `-l` | Displays listening sockets |
| `-n` | Displays numerical addresses and port numbers |

This command helps administrators identify services waiting for incoming network connections.

### Q15. What is the difference between TCP and UDP conceptually?

TCP and UDP are transport-layer protocols responsible for communication between applications across networks.

TCP – Transmission Control Protocol

- Connection-oriented communication.
- Provides reliable data delivery.
- Uses acknowledgements and retransmissions.
- Maintains data ordering.

UDP – User Datagram Protocol

- Connectionless communication.
- Has lower communication overhead.
- Does not guarantee packet delivery.
- Does not guarantee packet ordering.

Learn more

TCP is commonly used for applications that require reliable communication, while UDP is useful for applications where low latency and reduced overhead are important.

### Q16. What is curl used for?

`curl` is a command-line utility used to transfer data between a local system and remote servers.

It supports several protocols, including HTTP and HTTPS.

In Linux networking, it is commonly used for:

- Testing web server connectivity.
- Sending HTTP requests.
- Retrieving web resources.
- Checking API responses.
- Troubleshooting web services.

### Q17. What does `curl -I` request?

The `curl -I` command sends an HTTP HEAD request to a web server.

It retrieves the HTTP response headers without downloading the response body.

The response headers may contain information such as the HTTP status code, server information, content type, and other metadata.

### Q18. What is traceroute used for?

Traceroute is a network diagnostic utility used to identify the intermediate network devices through which packets travel to reach a destination.

It helps network administrators understand network paths and investigate possible routing delays or connectivity issues.

It is particularly useful for identifying where communication problems may occur along a network route.

### Q19. Why is ss commonly preferred over netstat on modern Linux?

The `ss` command is generally preferred over `netstat` because it is a modern networking utility designed to provide detailed socket information efficiently.

Its advantages include:

- Faster socket information retrieval.
- Detailed network connection information.
- Support for modern Linux networking features.
- Integration with the `iproute2` networking utilities.

The `netstat` command belongs to the older `net-tools` package, which is considered legacy on many modern Linux distributions.

### Q20. Why are Linux networking commands useful in cybersecurity?

Linux networking commands are essential in cybersecurity because they help security professionals understand, inspect, and troubleshoot network environments.

They support several important activities, including:

- Identifying network interfaces and IP configurations.
- Understanding network routes and gateways.
- Checking connectivity between authorized systems.
- Investigating DNS resolution problems.
- Identifying listening network services.
- Examining network communication endpoints.
- Troubleshooting network-related security issues.

These commands provide foundational knowledge for network security assessments, system administration, and authorized penetration testing.

## 4. Practical Implementation – Linux Networking Commands

The following commands can be executed in the Kali Linux terminal to understand basic network configuration and connectivity.

| Command | Purpose |
| --- | --- |
| `ip addr` | Displays network interface addresses |
| `ip link` | Displays network interface information |
| `hostname -I` | Displays assigned IP addresses |
| `ip route show` | Displays the routing table |
| `ping -c 4 google.com` | Tests network connectivity |
| `getent hosts google.com` | Retrieves hostname resolution information |
| `ip neigh` | Displays neighboring network devices |
| `ss -tuln` | Displays listening TCP and UDP sockets |
| `curl -I https://example.com` | Retrieves HTTP response headers |
| `traceroute google.com` | Examines the network path to a destination |

Note: Internet connectivity and installed utilities may affect command results. Use these commands only in your own or authorized lab environment.

## 5. Practical Evidence – Screenshots

Include genuine screenshots from your Kali Linux virtual machine to demonstrate the commands you executed.

Screenshot 1 – Network Interface Information

ip Command Examples in Linux

Suggested filename: `ip-addr.png`

Screenshot 2 – Routing Table

Deep Dive: The ip Command in Linux

Suggested filename: `ip-route.png`

Screenshot 3 – Network Connectivity

Thao tác với mạng cho người dùng Linux: 11 câu lệnh cần biết (Phần 1)

Suggested filename: `ping-test.png`

<img width="981" height="521" alt="image" src="https://github.com/user-attachments/assets/3434dda7-a683-41d5-922f-657c9bb449fa" />


Screenshot 4 – Listening Network Sockets

Check Open Ports in Ubuntu

Suggested filename: `ss-command.png`

<img width="607" height="320" alt="image" src="https://github.com/user-attachments/assets/ab8ccb1b-eb90-4119-bb8e-8f20d2eacb46" />

<img width="1190" height="505" alt="image" src="https://github.com/user-attachments/assets/679ed321-f0a0-42cf-b1fd-67acfa1cf73d" />


Screenshot 5 – Network Path Analysis

How to Diagnose Network Issues on Linux with Traceroute - Make Tech Easier

Suggested filename: `traceroute.png`

<img width="770" height="522" alt="image" src="https://github.com/user-attachments/assets/ac409cb9-ebfa-43d5-be88-76fe3a0c2208" />


These images are visual references only. Replace them with your own terminal screenshots before submission.

## 6. Learning Outcomes

After completing this assignment, I developed an understanding of the following concepts:

1. Fundamentals of Linux networking and network interfaces.
2. The purpose and functionality of the loopback interface.
3. IP addressing and network interface management.
4. Routing tables and default gateways.
5. Network connectivity testing and troubleshooting.
6. Domain Name System and hostname resolution.
7. Neighbor discovery and MAC address information.
8. Network sockets and listening services.
9. Differences between TCP and UDP protocols.
10. HTTP communication and network path analysis.
11. Modern Linux networking utilities.
12. The role of networking knowledge in cybersecurity.

## 7. Conclusion

This assignment provided a foundational understanding of Linux networking and its importance in cybersecurity.

Through theoretical concepts and practical command-line exercises, I learned how to inspect network interfaces, understand IP configurations, analyze routing information, verify connectivity, investigate hostname resolution, and examine listening network sockets.

I also gained an understanding of TCP and UDP communication, HTTP requests, and network path analysis.

These concepts establish an important foundation for further learning in network administration, network security, ethical hacking, and penetration testing.

<img width="1097" height="482" alt="image" src="https://github.com/user-attachments/assets/030f79ef-7d16-47ed-8254-1745ebb0cd76" />
