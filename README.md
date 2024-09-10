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

## Setup
Step 1: Create a CloudWatch Alarm for CPU Utilization
Go to the AWS Management Console.
Navigate to CloudWatch.
Click on Alarms → Create Alarm.
Select the EC2 instance(s) you want to monitor.
Choose CPU Utilization as the metric and set a threshold (e.g., greater than 80%).
Configure Actions to send notifications via SNS when the alarm is triggered.
Review and create the alarm.
Step 2: Set Up Amazon SNS for Notifications
Go to the SNS dashboard.
Create a new topic (e.g., CPUAlerts).
Subscribe to the topic with your email address or phone number.
Associate the SNS topic with your CloudWatch alarm.
Step 3: Testing the Setup
.Trigger the Alarm: Run a CPU-intensive task on your EC2 instance to test the alarm.
.Receive Notifications: When the CPU utilization exceeds the threshold, CloudWatch will trigger the alarm, and you will receive a notification via SNS.


## Usage
Monitoring: The CPU utilization metrics can be viewed in real-time from the CloudWatch dashboard.
Alarms: Alarms will trigger notifications when the CPU usage exceeds the configured threshold, allowing you to take immediate action.
Notifications: SNS will send an email or SMS notification to the specified recipient when alarms are activated.
