# Network Traffic Analysis with Wireshark

## Objective

The objective of this portfolio project is to provide a comprehensive exploration of network traffic analysis techniques, focusing on understanding various authentication protocols and secure communication methods. Through practical hands-on experience, participants will gain insight into the intricacies of network traffic, including the transmission of authentication credentials, encryption mechanisms, and the exchange of data between clients and servers. By dissecting real-world scenarios and employing packet capture and analysis tools, participants will develop a deeper understanding of network security principles, vulnerabilities, and best practices. Ultimately, this project aims to equip individuals with the skills necessary to analyze, troubleshoot, and secure network environments effectively.

## Steps

### 1.Generate and Capture RADIUS Traffic
- Set up a RADIUS Server: Install and configure a RADIUS server software such as FreeRADIUS on a dedicated machine or virtual environment. Configure user accounts and network devices to authenticate users through this server.
- Configure Network Devices: Configure routers, switches, or other network devices to utilize RADIUS for authentication. This typically involves specifying the RADIUS server's IP address and shared secret.
- Capture RADIUS Packets: Use packet capture software such as Wireshark to capture network traffic. Filter the capture to focus on RADIUS traffic specifically.
- Analyze Captured Packets: Analyze the captured packets to observe the authentication exchanges between the RADIUS server and network devices. Identify attributes such as usernames, passwords, authentication success or failure, and any other relevant information.

### 2.Analyze HTTP Basic Authentication
- Capture Network Traffic: Use packet capture software like Wireshark to capture network traffic containing HTTP Basic Authentication. This can be achieved by filtering the capture for HTTP traffic.
- Identify Authentication Headers: In the captured packets, identify the HTTP headers associated with Basic Authentication. These headers typically include the "Authorization" header containing the Base64-encoded username and password.
- Assess Security Implications: Evaluate the security risks of transmitting credentials in plaintext over the network. Consider potential vulnerabilities such as eavesdropping attacks and the importance of using secure authentication methods.

### 3.HTTP Form-Based Authentication and DNS
- Capture Network Traffic: Capture network traffic during sessions involving HTTP Form-Based Authentication using packet capture software.
- Analyze DNS Queries: Identify DNS queries and responses related to the authentication process. DNS requests may include domain lookups for authentication servers or other relevant resources.
- Examine Data Flow: Analyze the sequence of data exchanges between the client and server during the authentication process. This includes HTTP requests and responses containing form data and authentication tokens.

### 4.Initiate, Capture, and Analyze Telnet Sessions
- Initiate Telnet Sessions: Use Telnet client software to establish Telnet sessions between a client and a Telnet server.
- Capture Telnet Traffic: Capture Telnet traffic using packet capture software like Wireshark. Ensure that the capture is filtered to capture only Telnet traffic.
- Analyze Telnet Commands: Examine the captured packets to analyze Telnet commands issued by the client and corresponding responses from the server. Look for any sensitive information transmitted in plaintext.

### 5.Capturing and Analyzing SSH Sessions
- Establish SSH Connections: Initiate SSH connections between a client and an SSH server using SSH client software.
- Capture SSH Traffic: Capture SSH traffic using packet capture software such as Wireshark, filtering for SSH traffic specifically.
- Analyze SSH Negotiation: Analyze the SSH negotiation process, including key exchange, encryption algorithms, and authentication methods. Examine SSH packets to understand the security mechanisms employed.

### 6. Generate, Capture, Analyze then Decrypt HTTPS Traffic
- Access Secure Websites: Use a web browser to access secure websites (those using HTTPS) to generate HTTPS traffic.
- Capture HTTPS Packets: Capture HTTPS packets using packet capture software like Wireshark, ensuring that SSL/TLS decryption is enabled and properly configured.
- Decrypt SSL/TLS Traffic: Configure Wireshark to decrypt SSL/TLS encrypted traffic using appropriate keys or certificates. This allows for the analysis of decrypted HTTPS data.
- Analyze Decrypted Data: Analyze the decrypted HTTPS data to understand the content exchanged between the client and server. This may include HTTP requests, responses, cookies, and other relevant information for security assessment and troubleshooting.

### Conclusion
Through this project, you have gained valuable hands-on experience in network traffic analysis, covering a variety of authentication protocols and secure communication methods. By capturing and analyzing network traffic, you have developed insights into the security implications of different authentication mechanisms and encrypted communication protocols. This knowledge equips you with valuable skills for securing network environments and troubleshooting potential issues related to authentication and secure communication.
