# Vicarius-vRx-Reports-Dashboard

Tested on Ubuntu Server 22.04 LTS

# VicariusVrxReports Setup Instructions

## Prerequisites 

### Review the following KB article to create a new API Key from your Vrx Dashboard
https://customer-portal.vicarius.io/getting-started-with-vrx-rest-api

### Your dashboard_id corresponds to the url you use to login to your dashboard
Example: organization in https://organization.vicarius.cloud/

# Installation Method 
## URL Download

### Download and unzip the file
Download the package to the asset that will host the docker containers
vRxReportsDashboard.tar (https://campaign.vicarius.io/hubfs/vrxReports/vicarius-vrx-reports.tar.gz)


Install unzip to unzip the file

```bash
mkdir vicarius-vrx-reports-dashboard
dc vicarius-vrx-reports-dashboard
wget https://campaign.vicarius.io/hubfs/vrxReports/vicarius-vrx-reports.tar.gz
tar -xvzf vicarius-vrx-reports.tar.gz
```

### Install Docker configure the containers
Install the Docker stack using the installDocker.sh script:

```bash
sudo chmod +x installDocker.sh
sudo ./installDocker.sh
```

### Initialize Docker Secrets 
Create docker secrets to stor your dashboard_id, api_key, postgres_user, postgres_password

```bash
sudo chmod +x initDocker.sh
sudo ./initDocker.sh
```

### Bulid and push Docker images to Registry 
Deploy the Docker stack using the buildPushDocker.sh script:
```bash
sudo chmod +x buildPushDocker.sh
sudo ./buildPushDocker.sh
```

### Deploy Containers 
Deploy the Docker stack using the redeployDocker.sh script:
```bash
sudo chmod +x redeployDocker.sh
sudo ./redeployDocker.sh
```




## Github Cloning the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/jordan-Vicarius/Vicarius-vRx-Reports-Dashboard.git
cd Vicarius-vRx-Reports-Dashboard
```

## Install Docker and Initialize docker swarm and docker registry

Install the Docker stack using the installDocker.sh script:

```bash
chmod +x installDocker.sh
./installDocker.sh
```


## Initialize Docker Container Configuration 

### Review the following KB article to create a new API Key from your Vrx Dashboard
https://customer-portal.vicarius.io/getting-started-with-vrx-rest-api

### Your dashboard_id corresponds to the url you use to login to your dashboard
Example: organization in https://organization.vicarius.cloud/


### Build images and push to registry

```bash
chmod +x initDocker.sh
./initDocker.sh
```
*In this step it will be required dashboard_id, api_key, postgres_user, postgres_password*


### Init the Docker Stack Configuration

Deploy the Docker stack using the buildPushDocker.sh script:

```bash
chmod +x buildPushDocker.sh
./buildPushDocker.sh
```

### Deploying the Docker Stack

Deploy the Docker stack using the redeployDocker.sh script:

```bash
chmod +x redeployDocker.sh
./redeployDocker.sh
```


*Ensure you are in the directory containing the `redeployDocker.sh` script.*

---

**Additional Notes:**
- Ensure your Docker and Docker Compose versions support `version: '3.7'` as specified in `docker-compose.yml`.
- Adjust volume paths in `docker-compose.yml` as needed based on your directory structure.
- Verify that `entrypoint.sh` and `crontab` are correctly configured for your application.

