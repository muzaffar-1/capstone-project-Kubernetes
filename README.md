# 🚀 Kubernetes Capstone Project  
Design and implement an end-to-end cloud infrastructure automation and deployment pipeline using **Terraform, Ansible, Docker, and Kubernetes**.

This project demonstrates automation skills across DevOps tools and cloud platforms by provisioning infrastructure, configuring servers, building container images, and deploying applications on Kubernetes.

---

## 📌 **Project Overview**

This capstone project was completed in three major phases:

### **1️⃣ Infrastructure Automation — Terraform**
- Launched a **Terraform Workstation EC2** (Ubuntu, t2.micro)
- Installed and configured Terraform, AWS CLI
- Created SSH keypair (`ssh-keygen`)
- Using Terraform, created an **Ansible Workstation EC2** instance
- Logged into the Ansible instance via SSH

---

### **2️⃣ Configuration Management — Ansible**
- Installed **Ansible** on the Ansible workstation
- Created an inventory file at:/etc/ansible/hosts
- with:
localhost ansible_connection=local
- Created an Ansible playbook to install **Apache HTTPD**  
- Verified installation using:curl http://localhost
- - Generated HTML output using Ansible automation

---

### **3️⃣ Containerization — Docker**
- Created a directory with:
- `Dockerfile`
- `requirements.txt`
- `app.py` (Python Flask API)
- Built Docker image: docker build -t muzaffar81/test-flask-app:v1 .
- Logged into Docker Hub and pushed image:docker push muzaffar81/test-flask-app:v1
- 
---

### **4️⃣ Kubernetes — Kops Cluster**
- Created a Kubernetes cluster using **Kops**
- Connected via jump server
- Created a pod using the Flask Docker image
- Exposed via NodePort: kubectl expose pod flask-pod --type=NodePort --port=5000
- - Accessed the app using:  http://<worker-node-external-ip>:<nodeport>

---

### **5️⃣ Shared Volume Task**
Created two pods: **httpd** and **nginx**, both mounting the same **hostPath volume**:

- Shared directory on node: `/data/myshared`
- Mount path inside pods: `/myshared`

Verified by writing in `httpd` pod and reading from `nginx` pod.

---

### **6️⃣ Helm Chart**
Created a full Helm chart with the structure:

mychart/
│-- Chart.yaml
│-- values.yaml
│-- charts/
│-- templates/
│-- deployment.yaml
└-- service.yaml
Installed using: helm install muzaffar-chart .
Verified using: kubectl get all

---

## 📸 **Screenshots**

### **Docker Hub Repository**
screenshots/docker image.PNG(docker-image.PNG)

### **Helm Chart Output**
(helm-chart.png)

### **Ansible Apache Installation**
(httppd.png)

### **Flask App on Kubernetes**
(pod-accessed.png)

### **Shared Volume Output**
(shared-volume-pods.png)

---

## 🛠️ **Tools & Technologies**

| Tool | Purpose |
|------|---------|
| **Terraform** | Infrastructure provisioning |
| **Ansible** | Configuration management |
| **Docker** | Containerization |
| **Docker Hub** | Image registry |
| **Kops** | Kubernetes cluster creation |
| **Kubernetes** | Application deployment |
| **Helm** | Application packaging |

---

## 🧪 **How to Run This Project**

### **Terraform**
terraform init
terraform validate
terraform plan
terraform apply -auto-approve


### **Ansible**


sudo apt install ansible -y
ansible-playbook install-httpd.yml


### **Docker**


docker build -t <your-image> .
docker push <your-image>


### **Kubernetes**


kubectl apply -f pod.yaml
kubectl expose pod flask-pod --type=NodePort --port=5000


### **Helm**


helm install <name> .


---

## 🎯 **Conclusion**

This capstone project shows complete DevOps lifecycle automation:

- 🔧 Provisioning infrastructure with Terraform  
- ⚙ Configuring servers using Ansible  
- 📦 Building containerized applications  
- ☸ Deploying and managing workloads on Kubernetes  
- 🚀 Packaging applications with Helm  

It validates real-world, end-to-end DevOps engineering skills.

---

## 👤 **Author**
**Md Muzaffar Qureshi**  
DevOps | Cloud Engineer
