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

<img width="696" alt="min1Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/93fbcc1e-5766-48b1-8f9a-054fcb179ebd">
<br />
<br />

   - Monitor the Wireshark capture to observe the RADIUS traffic, including authentication requests, responses, and other RADIUS protocol messages.
   - Dive into packet details to understand the RADIUS protocol.Identify fields such as username and response codes.
   - Analyze the captured RADIUS traffic to understand the authentication process, including user authentication attempts, successful authentications, and any potential issues or errors.
<br />
<img width="696" alt="min3Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/c7120b3a-fa38-4286-8a3d-b38022dc3db7">
<br />
<br />

   - Explore the concept of shared secrets used in RADIUS for password protection.
   - Configure Wireshark to decrypt RADIUS passwords by providing the shared secret.
   - Navigate to Wireshark's preferences, locate the RADIUS protocol, and enter the shared secret.

<br />

<img width="696" alt="min4Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/29db4af8-c0ff-4618-b1e8-3066788e59e9">


<br />
<br />

- Reflect on the security implications of unencrypted RADIUS traffic.
- Acknowledge the importance of encryption in securing sensitive data.

<br />

<img width="696" alt="min5Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/2104e506-3335-4de2-adbe-3851182ec785">

  
<br />
<br />

### 2. Analyze a HTTP Basic Authentication

   - Open Wireshark and set it up to capture network traffic on the relevant interface.
   - Access a web application or webpage that requires HTTP Basic Authentication using a web browser.
   - Enter the required credentials (username and password) when prompted by the HTTP Basic Authentication dialog.
     
     <br />
<img width="698" alt="min6Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/2a90b2b0-d7f0-4e12-ba03-e1d0d74e8866">

  
<br />
<br />

   - Apply a capture filter to capture HTTP traffic by specifying port 80, the default port for HTTP.
   - Monitor the Wireshark capture to capture the HTTP traffic exchanged between the client (web browser) and the server.
   - Analyze the captured HTTP traffic to identify the HTTP Basic Authentication requests and responses, including the base64-encoded credentials sent by the client.
     
<br />
     <img width="651" alt="min7Capture" src="https://github.com/Pranavnathan23/Network-Traffic-Analysis-Wireshark/assets/163876627/3615b27e-8584-4d09-83e7-006aad19a578">

<br />
<br />

   - Note the lack of encryption in HTTP traffic, allowing anyone to intercept and view sensitive information, including usernames and passwords.
    - Understand the importance of using HTTPS for secure communication, which encrypts data using TLS (Transport Layer Security).

<br />

### 3. HTTP Form-Based Authentication and DNS

   - Start Wireshark and configure it to capture network traffic on the desired interface.
   - Access a website or web application that utilizes form-based authentication, requiring users to enter credentials into an HTML form.
   - Submit the form with valid credentials to authenticate with the web server.
   - Monitor the Wireshark capture to capture the HTTP traffic exchanged during the form-based authentication process.
   - Additionally, observe any DNS queries made by the client to resolve domain names associated with the web server.
   - Analyze the captured HTTP traffic to understand the form-based authentication process, including the structure of HTTP requests and responses involved.
<br />
<br />

### 4. Initiate, Capture and Analyze Telnet Sessions

   - Launch Wireshark and configure it to capture Telnet traffic on the desired interface.
   - Establish a Telnet session to a remote server or device using a Telnet client application.
   - Interact with the Telnet session by executing commands or performing actions on the remote server.
   - Monitor the Wireshark capture to capture the Telnet traffic exchanged between the Telnet client and server.
   - Analyze the captured Telnet traffic to understand the commands and data exchanged during the Telnet session, including login credentials, command execution, and session termination.
<br />
<br />

### 5. Capturing and Analyzing SSH Sessions

   - Open Wireshark and configure it to capture SSH traffic on the relevant network interface.
   - Establish an SSH connection to a remote server or device using an SSH client application (such as PuTTY or OpenSSH).
   - Perform various actions within the SSH session, such as executing commands, transferring files, or managing remote resources.
   - Monitor the Wireshark capture to capture the encrypted SSH traffic exchanged between the SSH client and server.
   - Analyze the captured SSH traffic to understand the encrypted communication between the client and server, including SSH protocol messages, encrypted data payloads, and session management.
<br />
<br />

### 6. Generate, Capture, Analyze then Decrypt HTTPS Traffic

   - Launch Wireshark and configure it to capture HTTPS traffic on the desired network interface.
   - Access a website or web application that uses HTTPS encryption to secure communication between the client and server.
   - Interact with the website by browsing pages, submitting forms, or performing other actions that trigger HTTPS requests and responses.
   - Monitor the Wireshark capture to capture the encrypted HTTPS traffic exchanged between the client (web browser) and the server.
   - Analyze the captured HTTPS traffic to understand the encrypted communication flow, including SSL/TLS handshake messages, encrypted data payloads, and HTTPS request/response headers.
   - Optionally, decrypt the captured HTTPS traffic in Wireshark by providing the necessary SSL/TLS keys or certificates, allowing you to view the plaintext data exchanged between the client and server.
<br />
<br />

## Conclusion

In summary, this portfolio project on Network Traffic Analysis using Wireshark reflects my dedication to continuous learning and growth within the field of networking. By showcasing my exploration of diverse authentication processes and encrypted communication, I aim to contribute to the collective understanding of network analysis techniques. This portfolio underscores my readiness to tackle the challenges of modern networking environments while maintaining a humble attitude towards ongoing development and improvement.
