# SecurityEngineering-Week4-Ex
Task 1 :

Example of a Side-Channel Attack - Timing Attack

Timing attacks exploit the time it takes for a system to perform cryptographic operations. By measuring how long it takes to execute certain operations, an attacker can infer information about the data being processed, such as keys or passwords.

Timing attacks can affect any system that relies on cryptographic algorithms, including web servers, mobile devices, smart cards, and any application using encryption for data protection.

The timing attack can leak sensitive information such as cryptographic keys or the structure of data, allowing attackers to potentially decrypt sensitive information or forge signatures.

 Timing attacks have been documented in various real-world scenarios, such as the attack on RSA key generation. This attack successfully revealed secret keys through precise timing measurements.

Mitigations against timing attacks include implementing constant-time algorithms that ensure execution time does not vary based on input values. Random delays, blinding, and algorithmic modifications have been employed to obscure timing patterns.

Sources:
1.Kocher, P. C. (1996). "Timing attacks on implementations of Diffie-Hellman, RSA, DSS, and other systems."
2.Bernstein, D. J. (2005). "Cache-timing attacks on AES." 




Task 2 : 

 

The Slowloris attack works by opening multiple connections to a target server and sending partial HTTP requests. It keeps these connections alive by sending periodic HTTP headers, preventing the server from closing them. This exhausts the server's resources as it tries to maintain numerous open connections, ultimately leading to a denial of service.

Unlike high-bandwidth DDoS attacks, which overwhelm a server with massive traffic, Slowloris uses very little bandwidth and focuses on consuming server resources. This makes it particularly effective against web servers that are configured to handle a limited number of simultaneous connections.

The effects include service unavailability for legitimate users, as the server becomes overwhelmed by open connections. This can lead to slow response times or complete denial of access to the affected website.

Mitigation strategies include:
Configuring the server to limit the maximum number of concurrent connections.
Implementing timeouts for incomplete requests..
Employing rate limiting for incoming connections.

Notable instances include the attack on the New York Times website in 2012, where attackers used Slowloris to disrupt access.

Sources:
1.Greet, R. (2011). "Slowloris: The Attack That Works On Everything."
2."Slowloris DDoS Attack Explained," Akamai. 
3.Smith, S. (2012). "New York Times Hit by Slowloris Attack."
