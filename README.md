# AWS CloudSecurity Challenge Level 1
Hey, my name is David. I am excited to present to you a challenge to get familiar with AWS and its services.

In this github repo, I'll walk you through how to setup a 3 tier web architecture with nginx, wordpress and mysql as a standalone VM.

## How to setup a 3 tier web architecture with nginx, wordpress and mysql at AWS

## Prerequisite
1. setup aliases
```ruby
alias k=kubectl; alias tf="terraform"; alias tfa="terraform apply --auto-approve"; alias tfd="terraform destroy --auto-approve"; alias tfm="terraform init; terraform fmt; terraform validate; terraform plan"
```
2. https://developer.hashicorp.com/terraform/install
Install if running at cloudshell
```ruby
sudo yum install -y yum-utils shadow-utils; sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo; sudo yum -y install terraform
```
```bash
Comprehensive Hands-On Lab: AWS Logging Solution
Objectives
Gain a thorough understanding of AWS logging mechanisms.
Implement and automate logging strategies to monitor AWS resources and activities effectively.
Lab Steps
Enable AWS CloudTrail:

Go to the AWS CloudTrail console.
Create a new trail, ensuring that:
It is applied to all regions.
Management and data events are recorded.
Logs are stored in a dedicated S3 bucket.
Set up Log File Integrity validation for enhanced security.
Create an Amazon S3 Bucket for Log Storage:

Create an S3 bucket specifically for CloudTrail logs.
Configure bucket policies to restrict access to only authorized IAM roles or users.
Enable versioning and server-side encryption (SSE) on the bucket for added security and data integrity.
Configure Amazon CloudWatch Logs:

Set up a CloudWatch Logs group for log storage and monitoring.
Create a Log Stream within that group to capture CloudTrail logs.
Configure CloudTrail to send the log files to the CloudWatch Logs group. This involves setting up permissions correctly to allow CloudTrail to write to CloudWatch Logs.
Set Up Alerts Using CloudWatch Alarms:

Define metric filters in CloudWatch to monitor specific activities, such as:
Unusual console sign-in attempts.
Unauthorized API calls.
Create CloudWatch Alarms based on the filters to notify stakeholders (using Amazon SNS) when a threshold is reached (e.g., over a certain number of failed logins).
Utilize Amazon Kinesis Data Firehose (Optional):

For advanced log processing, set up Amazon Kinesis Data Firehose to stream logs from CloudWatch to a more robust analysis tool or storage solution (e.g., S3, Elasticsearch).
Choose a target for your Firehose stream and configure it to handle the logs appropriately.
Deploy AWS Lambda for Custom Log Processing:

Create an AWS Lambda function that automatically triggers on new log entries.
Implement logic in the Lambda function to:
Parse log entries for specific patterns.
Identify anomalies or potential threats.
Send alerts to a designated SNS topic or store findings in an S3 bucket for further analysis.
Implement Amazon GuardDuty:

Enable Amazon GuardDuty for your AWS account to enhance security monitoring.
Monitor findings from GuardDuty, which analyzes CloudTrail and other data sources for signs of malicious or unauthorized behavior.
Create an Incident Response Plan:

Define processes and procedures to respond to alerts generated from CloudWatch and GuardDuty.
Test the incident response with simulated threat scenarios, verifying that the logs record the response efficiently.
Review and Analyze Logs:

Use AWS Athena or Amazon QuickSight to query logs stored in S3 for deeper analysis.
Generate reports or dashboards based on the log data for visualization and insights.
Documentation:

Maintain comprehensive documentation of configurations, procedures, findings, and any unusual events detected during the logging activities.

```
