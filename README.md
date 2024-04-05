# Network Traffic Analysis using Wireshark


## Introduction

This project is a comprehensive exploration of network traffic analysis using Wireshark, a powerful tool for capturing and dissecting network packets. Wireshark provides insights into the behavior of different network protocols, aiding in troubleshooting, optimization, and security assessment.Through a series of steps, this portfolio demonstrates practical applications of Wireshark in analyzing diverse network scenarios. From capturing RADIUS traffic to deciphering HTTPS communication, each segment delves into specific protocols and their interactions within a network.
<br />
<br />
## Steps

### 1. Generate and Capture RADIUS Traffic

   - Launch Wireshark on your computer to start capturing network traffic.
   - Configure Wireshark to capture traffic on the desired network interface (Ethernet, Wi-Fi, etc.).
   - Use an application such as NTRadPing or any RADIUS client to generate RADIUS traffic by initiating authentication requests to a RADIUS server.
<br />

<img width="900" alt="min1Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/93fbcc1e-5766-48b1-8f9a-054fcb179ebd">
<br />
<br />

   - Monitor the Wireshark capture to observe the RADIUS traffic, including authentication requests, responses, and other RADIUS protocol messages.
   - Dive into packet details to understand the RADIUS protocol.Identify fields such as username and response codes.
   - Analyze the captured RADIUS traffic to understand the authentication process, including user authentication attempts, successful authentications, and any potential issues or errors.
<br />
<img width="900" alt="min3Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/c7120b3a-fa38-4286-8a3d-b38022dc3db7">
<br />
<br />

   - Explore the concept of shared secrets used in RADIUS for password protection.
   - Configure Wireshark to decrypt RADIUS passwords by providing the shared secret.
   - Navigate to Wireshark's preferences, locate the RADIUS protocol, and enter the shared secret.

<br />

<img width="900" alt="min4Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/29db4af8-c0ff-4618-b1e8-3066788e59e9">


<br />
<br />

- Reflect on the security implications of unencrypted RADIUS traffic.
- Acknowledge the importance of encryption in securing sensitive data.

<br />

<img width="900" alt="min5Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/2104e506-3335-4de2-adbe-3851182ec785">

  
<br />
<br />

### 2. Analyze a HTTP Basic Authentication

   - Access a web application or webpage that requires HTTP Basic Authentication using a web browser.
   - Enter the required credentials (username and password) when prompted by the HTTP Basic Authentication dialog.
     
     <br />
<img width="900" alt="min6Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/2a90b2b0-d7f0-4e12-ba03-e1d0d74e8866">

  
<br />
<br />

   - Apply a capture filter to capture HTTP traffic by specifying port 80, the default port for HTTP.
   - Monitor the Wireshark capture to capture the HTTP traffic exchanged between the client (web browser) and the server.
   - Analyze the captured HTTP traffic to identify the HTTP Basic Authentication requests and responses, including the base64-encoded credentials sent by the client.
     
<br />
     <img width="900" alt="min7Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/3615b27e-8584-4d09-83e7-006aad19a578">

<br />
<br />

   - Note the lack of encryption in HTTP traffic, allowing anyone to intercept and view sensitive information, including usernames and passwords.
   - Understand the importance of using HTTPS for secure communication, which encrypts data using TLS (Transport Layer Security).

<br />

### 3. HTTP Form-Based Authentication and DNS

   - Access a website or web application that utilizes form-based authentication, requiring users to enter credentials into an HTML form.
   - Enter credentials (e.g., username: admin, password: 12345) and submit the form.
     
<br />
     <img width="900" alt="min8Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/730c6357-3ed2-4a98-a4f5-567f322c11bf">


<br />
<br />

   - Monitor the Wireshark capture to capture the HTTP traffic exchanged during the form-based authentication process.
   - Look for POST requests containing form field data, including usernames and passwords, transmitted in clear text.
   - Compare the security implications of Form-Based Authentication with Basic Authentication, noting the lack of encryption for transmitted credentials.

 <br />
   <img width="900" alt="min9Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/c47696c0-033a-496f-8f9a-82e537c1b774">



<br />
<br />

   - Return to Wireshark and configure it to capture DNS traffic by applying a capture filter specifying port 53.
   - Generate DNS traffic by performing a DNS lookup (e.g., using the "ping" command in Command Prompt).
   - Stop the packet capture and analyze the captured DNS packets.
     
 <br />
     <img width="900" alt="min10Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/001927ca-a280-4128-95b1-d6135c68e18e">


<br />
<br />
    
   - Note that DNS traffic is transmitted in clear text, allowing anyone to view domain names being resolved and corresponding IP addresses.
     
  <br />

### 4. Initiate, Capture and Analyze Telnet Sessions

   - Launch Wireshark and set up a capture filter to capture Telnet traffic on port 23 by typing "port 23" and double-clicking on your network interface.
   - Open Windows PowerShell by clicking on Start and typing "powershell."
   - Type the command telnet tty.sdf.org to initiate a Telnet session.

 <br />
 
<img width="900" alt="min 10 5 Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/642896de-63cc-479e-b5e5-fa9ebebd796b">

<br />
<br />

   - Monitor the Wireshark capture to capture the Telnet traffic exchanged between the Telnet client and server.
   - Analyze the captured Telnet traffic to understand the commands and data exchanged during the Telnet session, including login credentials, command execution, and session termination.
     
 <br />
 
<img width="900" alt="min11Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/b9eb2076-1d78-4b5c-874d-bf4bf588397f">

<br />
<br />
 
 - Observe that Telnet transmits data in clear text, including usernames, but not passwords.
 - Understand the implications of using Telnet for remote communication, considering its lack of encryption.

<br />

### 5. Capturing and Analyzing SSH Sessions

   - Telnet and SSH are both protocols used for remote access, but SSH encrypts data for secure communication while Telnet transmits data in clear text.
   - Establish an SSH connection to a remote server or device using an SSH client application (such as PuTTY or OpenSSH).
   - In Wireshark, instead of filtering by port number, capture all traffic between your device and the server by specifying the host (tty.sdf.org).
   - Begin capturing traffic and initiate a Telnet session to tty.sdf.org via PowerShell.

 <br />
 
<img width="900" alt="min12Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/31a71054-fb7e-4a78-b69c-f177a880d3cd">

<br />
<br />
      
- After running Telnet, leave the capture running and initiate an SSH session to the same server.     
- Monitor the Wireshark capture to capture the encrypted SSH traffic exchanged between the SSH client and server.   
- Click on the Telnet conversation and select "Follow Stream" to view the captured data.     
- Notice that Telnet traffic is unencrypted, exposing all transmitted data to potential eavesdropping.
  
 <br />
 

<img width="900" alt="min14Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/86282203-32c9-4152-a4c7-20bc1cd3bc3c">


<br />
<br />
      
   - Click on the SSH conversation and select "Follow Stream" to view the captured data.
- Observe that SSH traffic is encrypted, with the negotiation of encryption keys occurring at the beginning of the session.
- Understand that even if a malicious actor captures SSH traffic, they cannot decipher its contents due to encryption.

<br />
 
<img width="900" alt="min13Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/2eb58fa2-0238-4e78-9a4d-b96a7c756012">


<br />



### 6. Generate, Capture, Analyze then Decrypt HTTPS Traffic

   - Open Wireshark and begin capturing traffic on port 443, the default port for HTTPS.
   - Access a website or web application that uses HTTPS encryption to secure communication between the client and server.
   - Interact with the website by browsing pages, submitting forms, or performing other actions that trigger HTTPS requests and responses.
   - Monitor the Wireshark capture to capture the encrypted HTTPS traffic exchanged between the client (web browser) and the server.
   - Analyze the captured HTTPS traffic to understand the encrypted communication flow, including SSL/TLS handshake messages, encrypted data payloads, and HTTPS request/response headers.
       
<br />

<img width="900" alt="min15Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/c120d26a-426d-4363-bcf4-aabde12e6d05">

<br />
<br />
 
   - Set up an environment variable in Windows to instruct the browser to log pre-master secret keys.
   - Open Windows Start menu and type "Environment Variables", then click on it.
   - Click "New" and add a variable named SSLKEYLOGFILE with the file path for logging.
   - Verify that the key logging file is created by opening Google Chrome and browsing a website.
     
   <br />

<img width="900" alt="min16Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/b33cdd2c-8d07-471b-ba65-b2ce8643fb14">


<br />
<br />

   - Now decrypt the captured HTTPS traffic in Wireshark by providing the necessary SSL/TLS keys or certificates, allowing you to view the plaintext data exchanged between the client and server.
   - Open Wireshark and navigate to Edit > Preferences > Protocols > TLS.
   - Enter the file path of the pre-master secret log file created earlier.

<br />

<img width="900" alt="min19Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/d95bf48c-1c3e-4011-8b4d-37e7db29b206">



<br />
<br />

   - Check the captured conversations under Statistics > Conversations.

<br />


<img width="900" alt="min16 5Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/372d8b56-5735-4f94-91d7-cd9ae5d416bf">

<br />
<br />

   - Ping the website to determine the IP address.
   - Locate the corresponding IP address in Wireshark and click "Follow Stream" to view decrypted data.
   - Notice that HTTPS data, including headers and website source code, is now visible in plain text.

<br />   

<img width="900" alt="min17Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/78b1c22c-439e-4757-b8de-783adf286e64">


<br />
<br />

<br />  

<img width="900" alt="min18Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/467b2f89-d620-4607-abb7-6a07d2981f4a">

<br />
<br />

## Conclusion

In summary, this portfolio project on Network Traffic Analysis using Wireshark reflects my dedication to continuous learning and growth within the field of networking. By showcasing my exploration of diverse authentication processes and encrypted communication, I aim to contribute to the collective understanding of network analysis techniques. This portfolio underscores my readiness to tackle the challenges of modern networking environments while maintaining a humble attitude towards ongoing development and improvement.
