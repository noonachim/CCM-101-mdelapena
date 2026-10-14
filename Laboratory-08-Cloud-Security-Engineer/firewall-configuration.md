# Firewall Configuration

## 1. Allow SSH

SSH must be allowed before enabling the firewall so that administrators can continue to manage the server.

```bash
sudo ufw allow ssh
```

## 2. Set the Default Deny Policy

Incoming connections are denied by default, while outgoing connections are allowed.

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

## 3. Enable the Firewall

```bash
sudo ufw enable
```

## 4. Check the Firewall Status

```bash
sudo ufw status verbose
```

## 5. Allow Port 8080

The web application requires TCP port 8080, so it is explicitly allowed.

```bash
sudo ufw allow 8080/tcp
```

## 6. Verify the Rules

```bash
sudo ufw status numbered
```

## Why SSH Must Be Allowed First

If `sudo ufw enable` is run before `sudo ufw allow ssh`, the firewall may block the SSH connection needed for remote administration, potentially locking the administrator out of the server.

## Final Security Configuration

The final configuration follows a Default Deny approach for incoming traffic while allowing the two required services:

- SSH: Port 22
- Web application: TCP Port 8080

All other incoming connections remain blocked unless an additional rule is intentionally created.
