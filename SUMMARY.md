# Capstone Project Summary

## Terraform
- Created Terraform EC2 instance (Terraform workstation)
- Then launched Ansible workstation EC2 using Terraform
- Generated SSH key pair using ssh-keygen
- SSH into Ansible workstation

## Ansible
- Installed Ansible
- Created /etc/ansible/hosts
- Added localhost ansible_connection=local
- Installed httpd server using Ansible playbook

## Docker
- Created Flask API (app.py, requirements.txt, Dockerfile)
- Built a Docker image
- Pushed image to Docker Hub (muzaffar81/test-flask-app:v1)

## Kubernetes (Kops)
- Created Kops cluster
- Deployed Flask app as Pod + NodePort
- Created shared HostPath volume between httpd and nginx pods

## Helm
- Built Helm chart with deployment + service
- Installed Helm chart and tested service
