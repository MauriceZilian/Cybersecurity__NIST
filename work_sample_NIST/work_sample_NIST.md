# 🔒 Work Sample: Analysis and Response to a Simulated ICMP Flood Attack (Based on NIST Framework)

This repository contains a practical cybersecurity work sample. It simulates a security incident involving an ICMP flood attack and presents a structured response based on the NIST Cybersecurity Framework.

---

## 📘 Scenario

As part of an exercise to apply the NIST Cybersecurity Framework, a security incident was simulated at a fictional company. Internal network communication suddenly came to a complete halt. Analysis revealed the cause to be a flood attack using ICMP packets – a classic form of Distributed Denial-of-Service (DDoS) attack in which massive, manipulated requests overload network resources.

---

## 🎯 Objective

The aim of this exercise was to develop realistic protective, detection, and recovery measures and apply cybersecurity concepts and tools in a practical context. The following analysis is structured according to the five core functions of the NIST Cybersecurity Framework: Identify, Protect, Detect, Respond, Recover.

---

## 🔍 NIST-Based Analysis

### 1. Identify

Network diagnostics revealed a sharp spike in incoming ICMP requests, quickly overwhelming communication paths. The root cause was the lack of ICMP rate limiting on network interfaces and the absence of specific packet control rules in the firewall.

---

### 2. Protect

To strengthen prevention, several technical measures were implemented:

- Firewall rules to limit the rate of incoming ICMP packets (packet filtering)
- Deployment of an Intrusion Detection System (e.g. Snort) to automatically flag ICMP traffic with abnormal frequency patterns
- Review and restriction of access controls to reduce unnecessary network traffic (permissions, network segmentation)

---

### 3. Detect

To improve early detection of similar attacks, monitoring systems were extended with:

- Source IP verification to detect spoofing attempts
- Pattern-based alerts on sudden spikes in ICMP connections
- Real-time logging and analysis through a centralized SIEM (Security Information and Event Management) system

---

### 4. Respond

During the simulated incident, the following actions were taken:

- Prioritized shutdown of non-critical systems to reduce network load
- Isolation of affected network segments to contain the impact
- Reporting the incident to the internal response team and to management

---

### 5. Recover

The recovery phase was carried out in stages:

- Gradual reactivation of critical services after traffic stabilization
- Retrospective log analysis to identify anomalies or secondary effects
- Review and refinement of emergency plans for future incidents

---


## 📝 Note

This work sample was created independently as part of my preparation for a dual study program in Computer Science with a focus on cybersecurity. The scenario and content were developed from scratch and serve to demonstrate my ability to conduct structured security analyses using real-world methods.

