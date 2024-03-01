# Metabase Configuration

Run the metabaseInstallation.sh script 

## Metabase Setup
Navigate to = http://your_host:4000

* Select "Lets get started"
* Select your language 
* Create a user
* Add your data
** Select the PostgreSQL option
** Display Name: vRx-Reports
** Host: appdb
** Port: 5432
** Database name: <your dashboard id> # If your dashboard is https://example.vicarius.cloud. your dashboard_id is example
** Username: <user created during the initDocker script>
** Password: <password created during the initDocker script>
* Complete the setup






# VicariusVrxReports Setup Instructions

## Prerequisites 

### Review the following KB article to create a new API Key from your Vrx Dashboard
https://customer-portal.vicarius.io/getting-started-with-vrx-rest-api

### Your dashboard_id corresponds to the url you use to login to your dashboard
Example: organization in https://organization.vicarius.cloud/

# Installation Method 
## Method 1: URL Download

### Download and unzip the file
Download the package to the asset that will host the docker containers
vRxReportsDashboard.tar (https://campaign.vicarius.io/hubfs/vrxReports/vicarius-vrx-reports.tar.gz)


Install unzip to unzip the file

```bash
mkdir vicarius-vrx-reports-dashboard
cd vicarius-vrx-reports-dashboard
wget https://campaign.vicarius.io/hubfs/vrxReports/vicarius-vrx-reports.tar.gz
tar -xvzf vicarius-vrx-reports.tar.gz
```