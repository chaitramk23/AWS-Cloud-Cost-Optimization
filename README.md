# AWS-Cloud-Cost-Optimization
AWS cloud cost optimization often starts with identifying and managing stale or unused resources. These resources can accumulate quickly and increase costs unnecessarily. Here’s how you can identify and handle stale resources effectively:
# Identifying Stale EBS Snapshots
In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.
# Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
