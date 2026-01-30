# Secure AWS VPC Architecture with Bastion Host

## Overview
This project demonstrates a secure AWS VPC architecture that allows administrators to remotely manage private EC2 instances using a Bastion Host while maintaining strict network isolation and defense-in-depth security.

The architecture follows AWS Well-Architected Framework security best practices.

---

## Architecture
- One VPC with public and private subnets
- Bastion Host deployed in public subnet
- Private EC2 instance with no internet exposure
- NAT Gateway for outbound internet access
- Security Groups and Network ACLs for layered security

---

## Key Features
- Secure SSH access via Bastion Host
- No direct internet access to private instances
- SSH agent forwarding (no private key stored on bastion)
- Custom Network ACL to control ICMP traffic
- Internet access for private instances via NAT Gateway

---

## AWS Services Used
- Amazon VPC
- EC2
- Internet Gateway
- NAT Gateway
- Security Groups
- Network ACLs

---

## Security Best Practices Implemented
- Principle of least privilege
- Defense in depth (SG + NACL)
- No public IP on private instances
- Key-based authentication
- Controlled administrative access

---

## Outcome
- Successfully established secure connectivity between public and private subnets
- Verified outbound internet access from private EC2 instance
- Demonstrated traffic control using custom Network ACL rules
