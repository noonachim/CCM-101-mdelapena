# Laboratory Activity 8: The Cloud Security Engineer

## Mission Overview

This mission focused on securing an Ubuntu cloud server using a host-based firewall. The server was first prepared with a web application running on port 8080, then the Uncomplicated Firewall (UFW) was configured using a Default Deny policy. SSH access was allowed for administration, while port 8080 was explicitly allowed for legitimate web traffic.

## Objectives

- Understand the Principle of Least Privilege (PoLP) and Attack Surface.
- Perform a basic audit of network services and ports.
- Configure UFW with a Default Deny policy for incoming traffic.
- Allow SSH access for remote administration.
- Allow TCP port 8080 for the web application.
- Document security commands and best practices.
- Maintain an organized GitHub Cloud Computing portfolio.

## Commands Executed

```bash
# Run the web application
docker run -d --name secure-web-app -p 8080:80 nginx

# Test the application
curl http://localhost:8080

# Allow SSH before enabling UFW
sudo ufw allow ssh

# Set the default firewall policies
sudo ufw default deny incoming
sudo ufw default allow outgoing

# Enable and verify UFW
sudo ufw enable
sudo ufw status verbose

# Allow the web application
sudo ufw allow 8080/tcp

# Verify the firewall rules
sudo ufw status numbered

# Test the application again
curl http://localhost:8080
```

## Skills Learned

- Linux server security
- Host-based firewall configuration
- UFW rule management
- Port management
- Principle of Least Privilege
- Default Deny security
- Basic cloud security auditing
- Technical documentation using Markdown
- GitHub portfolio organization
