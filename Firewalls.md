What is a Firewall?
A firewall is a tool designed to intercept and assess incoming and outgoing packets. Depending on the types of devices we are protecting, and what we are protecting them from, we may choose to use different types of firewalls.

We can set rules for a firewall to either accept or deny a packet in the network. Those rules can be based on the source IP address of a packet, the details of a network session, or the contents of a packet. Below, we’ll discuss some common types of firewalls.

Packet-Filtering Firewalls
Packet-Filtering Firewalls are the simplest of all firewalls.

Packet-filtering firewalls do not check content, but they can inspect and filter on information like:

Source IP
Destination IP
Destination port numbers on a packet
Because of the simplicity of the rules, packet-filtering firewalls are best-suited:

Within your network
To control traffic from internal network to internal network
For example, within an organization, we can use a packet-filtering firewall to prevent the flow of packets between different parts of the network.

Circuit-Level Firewalls
Circuit-level firewalls review content related to individual sessions.

Circuit-level firewalls:

Ensure that sessions are properly configured
Identify illegitimate connections
While these may help to prevent malformed sessions from connecting, they might still allow certain threats to pass through. For example, a valid session transferring malware could be allowed as long as the session is established properly. As such, it’s best to use this type of firewall with other, more advanced types as described below.

Stateful Inspection Firewalls
Stateful inspection firewalls maintain a table of active sessions, similar to circuit-level firewalls.

Stateful inspection firewalls:

Are able to limit activity based on source and destination data, like packet-filtering firewalls
Attempt to review the contents of active sessions, dropping packets that don’t comply with the logged session
While stateful inspection firewalls have capabilities similar to packet-filtering and circuit-level firewalls, they offer additional protections. By dropping unexpected packets, it is much more difficult for attackers to breach a network.

Application Firewalls
Application firewalls offer security in ways that the three types of firewalls above cannot. Using pattern-matching, application firewalls can detect and block much more sophisticated attacks.

Application firewalls:

Utilize application-specific rules to identify malicious traffic
For example, a firewall may use a pattern designed to identify a specific attack. A request containing the string “UNION SELECT”, indicating a potential SQL injection, may be blocked by an application firewall.

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/firewalls/Cybersecurity_ApplicationFirewall_v2-10.svg)

In another example, an HTTP request may be passing data to a web server. While the request’s IP and session information may appear safe, content sent in individual HTTP requests could pose a danger to the receiving web servers. An application firewall could identify malicious content in HTTP requests and block the content.

Next-Generation Level Firewalls
* Next-generation level firewalls (NGLF) are considered the most advanced firewalls. On top of using all of the above methods, they will also identify additional malicious content in real-time.

Next-generation level firewalls:

May use artificial intelligence, or even global networks, to identify new and emerging threats in real-time
Are extremely complex
Usually require a much higher operating cost

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/firewalls/Cybersecurity_NextGenFirewall_2.svg)

