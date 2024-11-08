# atlas-mongo-backup-restore

This script is applicable to Atlasmongo Database. I was not able to find any scripts which did end to end so thought of writing my own. Might help others.....

Many fintech companies face an audit requirement to perform comprehensive backup and restore of their data sources every six months. This routine ensures data integrity by checking for corruption and providing evidence of data reliability, but it frequently consumes a significant amount of DevOps time. Because this task only arises biannually, it’s often overlooked until auditors request the required documentation and proof of process.

To address this need efficiently, the script will automate this process by creating a new cluster and restoring data from a prior snapshot (specifically, the n-1 snapshot) in the new cluster environment. After restoring the snapshot, it will automatically validate the integrity of the data, identifying any discrepancies or corruption. Once validation is complete, the script will remove the temporary cluster, providing a streamlined solution that reduces manual intervention. This automation frees up DevOps resources, ensures consistency, and meets audit requirements with minimal effort.

By implementing this solution, DevOps teams can stay audit-ready, maintain data integrity standards, and reduce the risk of last-minute efforts to meet compliance requirements.

Future Improvement: 

The script needs to run as cron job every six months 
Script can be further integarted with ticket systems which can automatically take eveidences and create the tickets 
All secrets can be passed via env variables via CI/CD
