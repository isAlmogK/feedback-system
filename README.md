

# Deploy the update
This guide provides step-by-step instructions on how to update the Fider application running on a DigitalOcean droplet using Docker Compose.

## Prerequisites
Access to DigitalOcean Dashboard: Ensure you have access to the DigitalOcean account where the droplet is hosted.
Docker & Docker Compose: Docker and Docker Compose should already be installed on the droplet.
Steps to Update Fider
## 1. Log into the Droplet
Open your DigitalOcean Dashboard.

Go to Droplets and find the droplet running Fider.

Click on the droplet’s name to open its details.

Click on Console in the top-right corner of the droplet’s page. This opens a console window where you can access the droplet directly.

You are now connected to your droplet.

## 2. Navigate to the Fider Directory
Once connected, navigate to the directory where Fider is set up. This is typically located in /var/fider.
```bash
cd /var/fider
```
This directory contains your docker-compose.yml file and other necessary settings for running Fider.

## 3. Pull the Latest Docker Image
Pull the latest version of the Docker image to ensure your application has the most recent updates.

```bash
docker compose pull
```
Note: This command only downloads the latest image but doesn’t restart the application yet.

## 4. Restart Fider with the New Image
After pulling the updated image, restart Fider to apply the changes. This command will update and start the container in the background:

```bash
docker compose up -d
```
The -d option ensures Fider runs in "detached mode," meaning it operates in the background.

## 5. Verify the Update
To confirm that Fider has successfully updated and is running, check the status of the Docker containers:

```bash
docker compose ps
```
You should see Fider listed as "Up" if it’s running correctly.


