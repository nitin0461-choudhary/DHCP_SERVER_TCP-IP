# Dynamic Lease Time Management in DHCP Servers

This project implements a custom **DHCP (Dynamic Host Configuration Protocol) server** in C, with a focus on **dynamic lease time management** based on client behavior and network load. The goal is to efficiently allocate IP addresses and optimize lease times to reduce congestion and improve network performance.

## 🧠 Project Aim

To design and implement a DHCP server that dynamically adjusts lease times by analyzing:
- Client type (mobile or stationary)
- Network utilization
- Time of day
- Retry patterns and priorities

## 📚 Overview

DHCP is a protocol that automates IP address allocation to clients on a network. Traditional DHCP servers use static lease durations, which may result in inefficient IP utilization. This project addresses that by dynamically calculating lease durations.

### DHCP Workflow:
- **DHCP Discover**: Client broadcasts a discovery request.
- **DHCP Offer**: Server responds with IP and lease time.
- **DHCP Request**: Client requests the offered IP.
- **DHCP Acknowledge**: Server confirms the allocation.

## ⚙️ System Architecture

- **DHCP Server**: Handles all communication with clients.
- **Lease Management System**: Dynamically assigns and monitors lease times.
- **Client Database**: Stores client info, IPs, lease time, and status.

<img src="https://via.placeholder.com/600x300.png?text=System+Architecture" alt="System Architecture" />

## 🛠️ Technologies Used

- **Language**: C
- **OS**: Ubuntu 22.04
- **Libraries**: POSIX Threads, Sockets
- **Tools**: Log files for monitoring server activity

## 🚀 Features

- Dynamic lease time adjustment based on:
  - Client retry count
  - Priority flag
  - Network conditions
- IP allocation with priority handling
- Lease monitoring and automatic expiry
- Server logs for debugging and performance evaluation

## 🧪 Testing Summary

| Test ID | Description                                   | Result |
|---------|-----------------------------------------------|--------|
| 1       | DHCP Discover and Offer Process               | ✅     |
| 2       | Lease Time Adjustment Based on Network Load   | ✅     |
| 3       | Client Lease Renewal and Reassignment         | ❌     |
| 4       | IP Address Exhaustion Handling                | ✅     |

## 📂 File Structure

