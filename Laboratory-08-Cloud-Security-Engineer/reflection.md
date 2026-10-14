# Mission Reflection

Completing Mission 8 helped me understand that server security does not depend only on the physical or external network perimeter. A host-based firewall provides another layer of protection directly on the server. Even if an attacker gets past a network-level security control, the firewall on the server can still restrict which incoming connections are accepted. This demonstrates the defense-in-depth approach because security is applied at more than one layer.

Managing open network ports is also important because every exposed service can become a possible entry point for an attacker. If a server has many unnecessary ports open, its attack surface becomes larger. In this mission, the Default Deny policy reduced the number of accessible services, while SSH and port 8080 were allowed only because they were required. This showed me that firewall rules should be based on actual business and application requirements instead of simply allowing everything.

Leaving a database port such as 3306 for MySQL open to the public internet can be dangerous in an enterprise environment. It exposes the database service to unauthorized connection attempts and possible attacks. A database should normally be protected so that only trusted application servers or administrators can reach it.

This mission also changed my perspective on how easily a server can become exposed when basic security controls are missing. A running service can be reachable over the network unless access is deliberately restricted. Configuring UFW made the idea of reducing attack surface more practical and understandable.

Finally, having eight completed missions makes my GitHub cloud computing portfolio more organized and meaningful. Each laboratory shows a different part of cloud administration and security. Mission 8 added an important security layer to the skills I developed in the previous activities.
