---

copyright:
  years: 2019
lastupdated: "2019-11-22"

subcollection: cloud-databases

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:codeblock: .codeblock}
{:tip: .tip}

# Responsibilities for {{site.data.keyword.databases-for}}
{: #responsibilities-cloud-databases}

Learn about the management responsibilities and terms and conditions that you have when you use {{site.data.keyword.cloud}} {{site.data.keyword.databases-for}}. For a high-level view of the service types in {{site.data.keyword.cloud_notm}} and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for {{site.data.keyword.cloud_notm}} offerings](/docs/overview?topic=overview-shared-responsibilities).
{:shortdesc}

Review the following sections for the specific responsibilities for you and for {{site.data.keyword.IBM_notm}} when you use {{site.data.keyword.databases-for}}. For the overall terms of use, see [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms).

## Incident and operations management
{: #incident-and-ops-responsibilities}

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Backups and restore| {{site.data.keyword.databases-for}} is responsible for taking automatic daily backups, monitoring the state of customer backups.| The Customer is responsible for restoration, timeliness, and validity of backups. |
|Monitoring| {{site.data.keyword.databases-for}} is responsible for hosting monitoring and health services. | The Customer is responsible for integrating with the Monitoring service, Activity Tracker, or Logging service. |
|High Availability| {{site.data.keyword.databases-for}} is responsible for deploying databases across availability zones in a Multi-Zone Region (MZR), or across hosts in a Single-Zone Region (SZR), as well as storing backups in cross-region Cloud Object Store instances. {{site.data.keyword.databases-for}} provides replication, fail-over features, and infrastructure maintenance/updates. High availability varies based on each database type, please refer to database specific documentation for details. | The Customer is responsible for designing application logic to retry connections caused by temporary connection failures (during regular database maintenance and updates).|
|Database performance | {{site.data.keyword.databases-for}} is responsible for hosting and maintaining database infrastructure. | The Customer is responsible for the data model and performance, including tuning the data model, queries, and scaling the database as appropriate for application needs. |
{: caption="Table 1. Responsibilities for incident and operations" caption-side="top"}

## Change management
{: #change-management-responsibilities}

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Scaling| {{site.data.keyword.databases-for}} is responsible for scaling infrastructure to meet customer requests. | The Customer is responsible for choosing, monitoring, and scaling disk, memory, and CPU core allocation for their deployments via UI or API. |
|Major version upgrades| {{site.data.keyword.databases-for}} is responsible for providing availability and tooling for database major version upgrades. | The Customer is responsible for executing major database version upgrades. |
{: caption="Table 2. Responsibilities for change management" caption-side="top"}

## Security and regulation compliance
{: #security-responsibilities}

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Encryption| {{site.data.keyword.databases-for}} is responsible for the encryption of data on disk, in motion, and in backups. | The Customer is responsible for choosing and managing appropriate additional security features. If using Key Protect and Bring Your Own Key (BYOK), the customer is responsible for managing Key Protect authorizations and keys. |
|Security| {{site.data.keyword.databases-for}} is responsible for ensuring the security of data on disk and data in motion within our infrastructure. | The Customer is responsible for managing {{site.data.keyword.cloud_notm}} passwords and database passwords, and keeping passwords secure. The Customer is also responsible for configuring appropriate network security/isolation (ex. IP whitelisting, private endpoints). |
{: caption="Table 4. Responsibilities for security and regulation compliance" caption-side="top"}

## Disaster recovery
{: #disaster-recovery-responsibilities}

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Backups|{{site.data.keyword.databases-for}} is responsible for automatic backups and storing them in cross-region Cloud Object Store instances. | The Customer is responsible for testing the validity and restore time of the backups. |
|Read-only replicas, {{site.data.keyword.databases-for-postgresql}} ONLY| {{site.data.keyword.databases-for-postgresql}} is responsible for providing the capability of deploying read-only replicas across regions (with the exception of replicating data outside of `eu-de`). | The Customer is responsible for provisioning, configuring, monitoring, and promoting read-only replicas. |
{: caption="Table 5. Responsibilities for disaster recovery" caption-side="top"}

