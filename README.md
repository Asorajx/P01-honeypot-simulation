# P01 - Honeypot Simulation

A simulated SSH honeypot environment using Cowrie to capture and analyse unauthorised access attempts in a controlled virtual environment.

## Overview

This project simulates a honeypot environment to observe and analyse unauthorised SSH access attempts. The setup allows safe study of brute-force behaviour, command patterns, and attacker interaction without using a real-world environment.

## Goals

- Understand common brute-force and unauthorised access techniques
- Capture and analyse attacker behaviour and commands
- Gain hands-on experience with defensive security tools such as Cowrie

## Components

| Component | Purpose |
|---|---|
| Ubuntu 22.04 VM | Hosts Cowrie to capture and log attacker activity |
| Kali Linux VM | Acts as an attacker performing SSH login attempts |
| Cowrie | Provides an emulated SSH/Telnet environment and detailed logging |
| Hydra | Simulates SSH brute-force attacks |
| Oracle VirtualBox | Hosts the isolated virtual environment |

## Features

- Simulates an SSH/Telnet service using Cowrie
- Captures SSH brute-force attempts, including usernames and passwords
- Logs commands executed during attacker sessions
- Generates structured logs for analysing attacker behaviour

## Scope

### In Scope

- Setting up a Cowrie honeypot environment on Ubuntu
- Simulating SSH brute-force attacks from Kali Linux
- Capturing and logging attacker login attempts and commands
- Basic analysis of attacker behaviour using collected logs

### Out of Scope

- Custom scripts for automated attack simulation or log analysis
- Advanced malware analysis or payload execution
- SIEM integration or large-scale monitoring
- Real-world deployment
- Automated defensive responses

## Environment

The project was built using two virtual machines inside Oracle VirtualBox:

| System | Role |
|---|---|
| Ubuntu 22.04 | Honeypot host running Cowrie |
| Kali Linux | Attacker machine used for SSH testing |

Both virtual machines were configured using a Host-Only Adapter to maintain an isolated testing environment. :contentReference[oaicite:2]{index=2}

## Setup Summary

1. Configure Ubuntu and Kali Linux virtual machines
2. Install and configure Cowrie on Ubuntu
3. Set up isolated Host-Only networking
4. Simulate SSH attacks from Kali Linux
5. Analyse captured Cowrie logs

## Test Summary

| Test | Result | Main Findings |
|---|---|---|
| Automated Password Guessing Using Hydra | Passed | Rapid automated login attempts were captured by Cowrie |
| Manual Common-Credential Testing | Passed | Weak credentials such as `root/test` were accepted while tested admin and user credentials failed |
| Successful Login and Command Execution | Passed | Cowrie captured post-login commands and attacker interaction |

## Documentation

Full project report:

`P01-honeypot-simulation.pdf`
