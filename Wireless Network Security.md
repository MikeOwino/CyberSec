### Wireless Network Security

Protocols and security measures are keeping up with the advent of Wi-Fi. With Wi-Fi, users have experienced an increase in device freedom, but wireless technology carries the risk that we are may not physically see who is accessing a network. We’ll discuss some of the best practices around wireless network infrastructure:

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/wireless-security/Cybersecurity_WirelessNetworkSecurity-11.svg)

### Network Segmentation
Network Segmentation is the basic practice of breaking apart larger networks into smaller, functionally similar networks with different access levels. This improves both security and performance.

Generally, when using network segmentation, we want to consider the role of each segmented network. For example, in an organization, does a computer in the Human Resources department need access to the servers used by the Engineering department or the Marketing department? Most likely no. Should a friend visiting the office be able to access the company login portal? Definitely not!

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/wireless-security/Cybersecurity_Segmentation_1-11.svg)

In segmenting networks, we should consider:

Which assets are we trying to protect?
Who can access which networks?
These questions naturally lead us to access control lists that determine who can connect to which networks.

Often the first place people start is just implementing a guest network that’s separate from the rest of your network environment. Segmentation allows us to balance!

By segmenting our networks, we can also make more strategic use of firewalls as well. We can place stricter firewall rules on the segmented networks we most need to protect.

Access Point Placement
It is important we consider both the placement and strength of our access points. Access points are the systems and nodes used to distribute wireless signals. If an attacker can access the network, they may be able to attack the users on the network!

This risk is especially true in places like coffee shops or libraries. It would not be very wise to keep the router in plain sight so that anyone could physically configure it.

If we think about wireless access points that offer WiFi in different parts of a city, it is network segmentation and administration that tries to ensure people who connect to that large network aren’t able to hack into other people’s network use.

Encryption
All wireless activity should be securely encrypted. Currently, the accepted standard for security is WPA2. WPA2-Personal will require a single password to access Wi-Fi, while WPA2-Enterprise will require multi-factor authentication.

It’s recommended to set your own network name and password when you set up your wireless Internet at home, instead of using the default one that comes with the router!

Of course, using a single-factor (just a password) on a wireless network isn’t fully secure, but this is the current standard for Wi-Fi. You can personally implement more security through the use of firewalls and the methods mentioned above.