# Cloud Agent Deployment - OpenClaw on AWS EC2

## Overview
This is the cloud gateway running on AWS EC2 (t3.small) as a failover/backup to the local gateway.

## Instance Details
- **Instance ID:** i-0547b6d8cc5dc5556
- **Type:** t3.small
- **URL:** ws://52.91.192.10:18789
- **Region:** us-east-1

## Setup (done)
- OpenClaw installed on EC2
- Running via systemd or similar
- Models: MiniMax → OpenRouter

## Access
- SSH: `ssh -i ~/.ssh/your-key.pem ec2-user@52.91.192.10`
- Both gateways sync via GitHub (openclaw-brain repo)

## Failover
- Local gateway (ws://127.0.0.1:18789) is primary
- Cloud gateway (ws://52.91.192.10:18789) is backup
- If local dies → requests route to cloud
- Both sync state via GitHub
