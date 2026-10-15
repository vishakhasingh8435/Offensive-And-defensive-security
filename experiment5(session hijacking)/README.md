# Experiment: Sniffing and Session Hijacking

## 1. Aim
To capture and analyze network traffic using Wireshark and understand ARP spoofing and session hijacking and their impact on network security.

## 2. Context / Theory

### Network Sniffing
Network sniffing is the process of capturing and analyzing data packets travelling through a network. Wireshark is a network protocol analyzer used to inspect packets, identify protocols, and investigate suspicious network activity.

### ARP Spoofing
ARP stands for Address Resolution Protocol. It maps an IPv4 address to a MAC address on a local network. In ARP spoofing, an attacker sends fake ARP messages to associate an incorrect MAC address with a device's IP address. This may redirect network traffic or interrupt communication.

### Session Hijacking
Session hijacking is an attack in which an attacker attempts to take control of a user's active session by stealing or misusing a valid session identifier, such as a session cookie.

### Working Diagram

```text
       Client Computer
              |
              | Network Traffic
              v
       +--------------+
       | Local Network|
       +--------------+
              |
              v
       Router / Gateway

 Wireshark captures and analyzes
 authorized network packets.
```

## 3. Tools Required
- Wireshark
- Kali Linux or another Linux system
- An authorized local test network or isolated virtual lab
- A test web application and test account

## 4. Methodology / Procedure

1. Open Wireshark and select the active network interface.
2. Start capturing network traffic.
3. Generate normal traffic using a browser or test application.
4. Apply the `arp` filter to display ARP packets.
5. Observe source IP addresses, destination IP addresses, and MAC addresses.
6. Examine unexpected ARP replies or IP-to-MAC mapping changes that may indicate ARP spoofing.
7. In an isolated, authorized lab, study how ARP spoofing can redirect network traffic.
8. Log in to a test web application and observe the session communication.
9. Examine whether the connection uses HTTP or HTTPS and understand how session information is protected.
10. Record observations and identify suitable preventive measures.

## 5. Wireshark Filters

| Filter | Purpose |
|---|---|
| `arp` | Displays ARP packets |
| `dns` | Displays DNS queries and responses |
| `tcp` | Displays TCP packets |
| `http` | Displays HTTP traffic, if present |
| `tls` | Displays TLS protocol traffic |
| `ip.addr == 192.168.1.10` | Displays traffic involving a specified IP address |

Replace the example IP address with the address used in the lab.

## 6. Results
- Network traffic was captured and analyzed using Wireshark.
- ARP packets were examined to understand IP-to-MAC address mapping.
- Potential indicators of ARP spoofing were studied.
- Session hijacking and its possible impact on user accounts were examined.
- Network security and prevention methods were identified.

*Report only the findings verified during the practical.*

## 7. Discussion
Wireshark helps administrators inspect network packets and investigate suspicious communication. ARP spoofing may allow traffic redirection, while session hijacking may allow unauthorized access if a valid session identifier is exposed or stolen. HTTPS, secure session management, and network monitoring help reduce these risks. Suspicious packet patterns should be investigated before confirming an attack.

## 8. Conclusion
This experiment helped us understand network sniffing, ARP spoofing, and session hijacking. Wireshark was used to analyze network traffic and examine potential security issues. The experiment highlighted the importance of encrypted communication, secure session management, and network monitoring.

## 9. Improvements
- Use HTTPS for web communication.
- Protect session cookies with `Secure`, `HttpOnly`, and appropriate `SameSite` attributes.
- Use Dynamic ARP Inspection where supported.
- Monitor unusual ARP traffic and network activity.
- Expire sessions securely and regenerate session identifiers after login.

## 10. Precautions
- Perform testing only on authorized systems and networks.
- Use test accounts and isolated lab environments.
- Do not capture or share real users' passwords or session cookies.
- Verify suspicious ARP activity before concluding that an attack occurred.
- Never attempt to hijack real users' sessions.

## 11. References
- Wireshark: https://www.wireshark.org/
- OWASP Session Management Cheat Sheet: https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html
- RFC 826 — Address Resolution Protocol: https://www.rfc-editor.org/rfc/rfc826
