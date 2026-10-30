# AWS Multi-VPC Peering Infrastructure Lab

## 🌐 Project Overview
Designed and deployed a highly segregated, secure dual-VPC infrastructure on AWS to enforce administrative isolation boundaries and partition private app server workloads.

## 📊 Cloud Architecture Properties
*   **VPC A (Management Cloud):** 10.10.0.0/16
*   **VPC B (Isolated Compute Cloud):** 10.20.0.0/16
*   **Transit Pipeline:** Active VPC Peering Connection Tunnel (ewb-a-b-peer)
*   **Gatekeeper Node (Bastion):** Static Private IP 10.10.1.10 / Public Gateway IP 15.135.78.1
*   **App Node A (Private VPC A):** Static Private IP 10.10.2.10
*   **App Node B (Private VPC B):** Static Private IP 10.20.1.10

## 🔒 Connection Strategy (Zero-Trust Multi-Hop Proxy)
Ingress access to private application matrices is locked down using an OpenSSH multi-hop ProxyJump configuration via the cryptographic access key ewb-lab.pem.

## 📡 Empirical Connectivity Verification Status
*   **Transmission Efficiency:** 4 Packets Sent, 4 Packets Received
*   **Packet Loss Rate:** 0% Packet Loss
*   **Routing Latency Average:** ~0.201 ms (Traffic completely retained inside high-speed private cloud paths)
