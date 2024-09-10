# CPU Utilization Monitoring on AWS using CloudWatch

This project demonstrates how to monitor CPU utilization of EC2 instances on **AWS** using **Amazon CloudWatch**. It provides a step-by-step guide to set up CloudWatch alarms to monitor CPU usage and send notifications when certain thresholds are met.

## Features
- Real-time monitoring of CPU utilization on AWS EC2 instances.
- Set up custom CloudWatch alarms to trigger when CPU usage exceeds defined thresholds.
- Automatic notifications via Amazon SNS (Simple Notification Service) when alarms are triggered.

## Table of Contents
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Setup](#setup)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Architecture

The architecture of this project involves:
1. **Amazon EC2** instances: These are the virtual servers where your applications run.
2. **Amazon CloudWatch**: A monitoring service that tracks CPU utilization and other performance metrics.
3. **Amazon SNS**: Sends notifications (email, SMS, etc.) when CloudWatch alarms are triggered.

## Prerequisites

Before you begin, make sure you have the following:
- An active **AWS account**.
- At least one **EC2 instance** running in your AWS environment.
- Basic knowledge of AWS services, especially **EC2**, **CloudWatch**, and **SNS**.

## Installation

1. **Set up EC2 instances**:
   - Launch EC2 instances from the AWS Management Console.
   - Ensure they have the necessary permissions (CloudWatch permissions are required).

2. **Install AWS CLI** (optional):
   You can also configure and monitor resources using the AWS Command Line Interface (CLI). Install it by following the official AWS CLI installation guide [here](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).

3. **Configure AWS CLI** (if using CLI):
   ```bash
   aws configure
