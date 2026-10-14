# Reflection

## 1. How does a host-based firewall protect a server even if the physical network perimeter is breached?

A host-based firewall protects the server by controlling incoming and outgoing network connections directly on the server. Even if an attacker gets past the physical or external network security, the firewall can still block unauthorized connections and allow only required services. This provides an additional layer of security for the server.

## 2. Why is managing open network ports critical to reducing a server's attack surface?

Managing open network ports is important because every open port can be a possible entry point for attackers. Closing unnecessary ports reduces the number of services that can be accessed from the network. In this mission, allowing only SSH and port 8080 helped reduce the server's attack surface.

## 3. In a real enterprise environment, why is it dangerous to leave a database port like 3306 for MySQL open to the public internet?

Leaving port 3306 open to the public internet is dangerous because unauthorized users may attempt to connect to the database. This could expose sensitive information and increase the possibility of attacks. Database ports should only be accessible to trusted systems and users that require them.

## 4. How did completing this mission change your perspective on how easily a server can be compromised?

This mission showed me that a server can become vulnerable when security settings are not properly configured. I realized that even a simple open port or running service can increase the server's exposure. Configuring UFW helped me understand how important it is to control network access and apply security rules carefully.

## 5. How does your GitHub portfolio currently look with eight completed missions?

With eight completed missions, my GitHub portfolio looks more complete, organized, and professional. Each laboratory shows the different cloud computing skills I have learned and practiced. Mission 8 added an important security component to my portfolio and showed my progress from basic cloud concepts to practical server security and administration.
