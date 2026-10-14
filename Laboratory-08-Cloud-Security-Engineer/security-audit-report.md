# Security Audit Report

## Principle of Least Privilege (PoLP)

The Principle of Least Privilege means giving a user, account, or service only the permissions it needs to perform its required task. In cloud environments, this reduces the possible damage if an account is misused or compromised because unnecessary access is not available.

## Attack Surface

The attack surface is the collection of possible points that an attacker could use to enter, interact with, or affect a system. For a virtual machine, this can include open network ports, running services, exposed applications, user accounts, and other accessible components.

## Default Deny Policy

A Default Deny policy blocks incoming traffic unless a specific rule allows it. This is safer than trying to block individual attackers because unknown or unwanted traffic is rejected automatically, while only the services that are intentionally exposed are permitted.
