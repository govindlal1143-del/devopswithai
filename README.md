# 🚀 DevOps Engineer Portfolio

<div align="center">

![DevOps Banner](https://img.shields.io/badge/DevOps-Engineer-0A66C2?style=for-the-badge&logo=devdotto&logoColor=white)
![Workshop](https://img.shields.io/badge/Cloud_Train-DevOps_Workshop-00C4CC?style=for-the-badge)
![Projects](https://img.shields.io/badge/Mini_Projects-12-orange?style=for-the-badge)
![Capstone](https://img.shields.io/badge/Capstone_Project-1-red?style=for-the-badge)
![Tests](https://img.shields.io/badge/Practice_Tests-10-green?style=for-the-badge)

**Trained at [Cloud Train](https://www.thecloudtrain.com) | 7-Day Intensive DevOps Workshop**

*Bridging the gap between Development and Operations through automation, containerization, and continuous delivery.*

</div>

---

## 👨‍💻 About Me

I have completed an intensive **7-Day DevOps Workshop** by **Cloud Train**, where I gained hands-on experience with industry-standard DevOps tools and practices. This portfolio showcases everything I learned, built, and practiced during the workshop — including **12 Mini Projects**, **1 Capstone Project**, and **10 Practice Tests**.

---

## 🛠️ Tech Stack & Skills

<div align="center">

| Category | Tools |
|----------|-------|
| **Version Control** | ![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white) |
| **CI/CD** | ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white) |
| **Containerization** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white) |
| **Configuration Mgmt** | ![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat&logo=ansible&logoColor=white) |
| **Orchestration** | ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white) |
| **Monitoring** | ![Nagios](https://img.shields.io/badge/Nagios-Monitoring-2C3E50?style=flat) |

</div>

---

## 🗂️ Repository Structure

```
devops-portfolio/
│
├── mini-projects/
│   ├── 01-git-branching-workflow/
│   ├── 02-github-repo-setup/
│   ├── 03-jenkins-freestyle-job/
│   ├── 04-jenkins-pipeline-github/
│   ├── 05-docker-custom-image/
│   ├── 06-dockerhub-push-pull/
│   ├── 07-docker-compose-app/
│   ├── 08-ansible-server-setup/
│   ├── 09-ansible-playbook-webserver/
│   ├── 10-kubernetes-deployment/
│   ├── 11-kubernetes-services-ingress/
│   └── 12-nagios-monitoring-setup/
│
├── capstone-project/
│   └── full-cicd-pipeline/
│
├── practice-tests/
│   ├── test-01-devops-basics.md
│   ├── test-02-git-github.md
│   ├── test-03-jenkins-ci.md
│   ├── test-04-docker-basics.md
│   ├── test-05-docker-advanced.md
│   ├── test-06-ansible.md
│   ├── test-07-kubernetes-basics.md
│   ├── test-08-kubernetes-advanced.md
│   ├── test-09-nagios-monitoring.md
│   └── test-10-devops-scenario.md
│
└── README.md
```

---

## 🔬 12 Mini Projects

---

### 🟦 Mini Project 1 — Git Branching Workflow
**Tool:** Git  
**Objective:** Understand how teams work with branches in real projects

**What I Did:**
- Created a new Git repository
- Created `main`, `develop`, and `feature` branches
- Made changes on the `feature` branch
- Merged `feature` → `develop` → `main`
- Resolved a merge conflict manually

**Commands Used:**
```bash
git init
git checkout -b develop
git checkout -b feature/login-page
# make changes
git add .
git commit -m "Added login page feature"
git checkout develop
git merge feature/login-page
git checkout main
git merge develop
```

---

### 🟦 Mini Project 2 — GitHub Remote Repository Setup
**Tool:** Git + GitHub  
**Objective:** Push a local project to GitHub and manage it remotely

**What I Did:**
- Created a new repo on GitHub
- Connected local project using `git remote`
- Pushed code and created Pull Requests (PRs)
- Reviewed and merged PR

**Commands Used:**
```bash
git remote add origin https://github.com/YOUR-USERNAME/repo-name.git
git branch -M main
git push -u origin main
git pull origin main
```

---

### 🟦 Mini Project 3 — Jenkins Freestyle Job
**Tool:** Jenkins  
**Objective:** Create a basic Jenkins job that runs a shell script

**What I Did:**
- Installed Jenkins on a Linux server
- Created a Freestyle Job
- Added a build step to execute a shell script
- Triggered the job manually and observed console output

**Sample Shell Script in Jenkins:**
```bash
echo "Hello from Jenkins!"
echo "Build Number: $BUILD_NUMBER"
date
```

---

### 🟦 Mini Project 4 — Jenkins Pipeline with GitHub Integration
**Tool:** Jenkins + GitHub  
**Objective:** Automatically trigger Jenkins build when code is pushed to GitHub

**What I Did:**
- Configured GitHub Webhook to trigger Jenkins
- Created a Jenkins Pipeline job
- Pulled code from GitHub on every push
- Ran build and test steps automatically

**Jenkinsfile:**
```groovy
pipeline {
    agent any
    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/YOUR-USERNAME/your-repo.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'echo Build Success'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo Tests Passed'
            }
        }
    }
}
```

---

### 🟦 Mini Project 5 — Build a Custom Docker Image
**Tool:** Docker  
**Objective:** Create a custom Docker image using a Dockerfile

**What I Did:**
- Wrote a `Dockerfile` for a simple web application
- Built the image using `docker build`
- Ran a container from the image
- Accessed the app on the browser via `localhost`

**Dockerfile:**
```dockerfile
FROM ubuntu:20.04
RUN apt-get update && apt-get install -y apache2
COPY index.html /var/www/html/
EXPOSE 80
CMD ["apache2ctl", "-D", "FOREGROUND"]
```

**Commands Used:**
```bash
docker build -t my-web-app .
docker run -d -p 8080:80 my-web-app
docker ps
```

---

### 🟦 Mini Project 6 — Push & Pull Docker Image to Docker Hub
**Tool:** Docker + Docker Hub  
**Objective:** Share Docker images using Docker Hub registry

**What I Did:**
- Created a Docker Hub account
- Tagged a Docker image
- Pushed image to Docker Hub
- Pulled the image on a different server and ran it

**Commands Used:**
```bash
docker login
docker tag my-web-app YOUR-DOCKERHUB-USERNAME/my-web-app:v1
docker push YOUR-DOCKERHUB-USERNAME/my-web-app:v1
docker pull YOUR-DOCKERHUB-USERNAME/my-web-app:v1
docker run -d -p 8080:80 YOUR-DOCKERHUB-USERNAME/my-web-app:v1
```

---

### 🟦 Mini Project 7 — Multi-Container App with Docker Compose
**Tool:** Docker + Docker Compose  
**Objective:** Run multiple containers together (e.g., web app + database)

**What I Did:**
- Wrote a `docker-compose.yml` file
- Launched a web app + MySQL database together
- Verified containers communicate with each other

**docker-compose.yml:**
```yaml
version: '3'
services:
  webapp:
    image: nginx
    ports:
      - "8080:80"
    depends_on:
      - database

  database:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: rootpass
      MYSQL_DATABASE: mydb
    ports:
      - "3306:3306"
```

**Commands Used:**
```bash
docker-compose up -d
docker-compose ps
docker-compose down
```

---

### 🟦 Mini Project 8 — Ansible Server Setup (Master-Slave)
**Tool:** Ansible  
**Objective:** Set up Ansible control node and connect managed nodes

**What I Did:**
- Configured SSH key-based authentication between master and slave
- Created Ansible inventory file
- Tested connection using `ansible ping`

**Inventory File (`/etc/ansible/hosts`):**
```ini
[webservers]
192.168.1.10
192.168.1.11

[dbservers]
192.168.1.20
```

**Commands Used:**
```bash
# Generate SSH key
ssh-keygen

# Copy key to managed nodes
ssh-copy-id user@192.168.1.10

# Test connection
ansible all -m ping
```

---

### 🟦 Mini Project 9 — Ansible Playbook to Install & Configure Apache
**Tool:** Ansible  
**Objective:** Automate web server installation using a Playbook

**What I Did:**
- Wrote an Ansible Playbook to install Apache on multiple servers
- Started the Apache service automatically
- Deployed a custom HTML page using Ansible

**Playbook (`install_apache.yml`):**
```yaml
---
- name: Install and Configure Apache
  hosts: webservers
  become: yes
  tasks:
    - name: Install Apache
      apt:
        name: apache2
        state: present
        update_cache: yes

    - name: Start Apache Service
      service:
        name: apache2
        state: started
        enabled: yes

    - name: Copy HTML file
      copy:
        src: index.html
        dest: /var/www/html/index.html
```

**Commands Used:**
```bash
ansible-playbook install_apache.yml
ansible-playbook install_apache.yml --check   # dry run
```

---

### 🟦 Mini Project 10 — Deploy App on Kubernetes Cluster
**Tool:** Kubernetes  
**Objective:** Deploy a containerized application on Kubernetes using YAML

**What I Did:**
- Set up a Kubernetes cluster (Minikube)
- Wrote a Deployment YAML file
- Deployed a web app with 3 replicas
- Scaled the deployment up and down

**deployment.yaml:**
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: webapp-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: webapp
  template:
    metadata:
      labels:
        app: webapp
    spec:
      containers:
      - name: webapp
        image: nginx:latest
        ports:
        - containerPort: 80
```

**Commands Used:**
```bash
kubectl apply -f deployment.yaml
kubectl get deployments
kubectl get pods
kubectl scale deployment webapp-deployment --replicas=5
kubectl delete -f deployment.yaml
```

---

### 🟦 Mini Project 11 — Kubernetes Services & Ingress
**Tool:** Kubernetes  
**Objective:** Expose the deployed app to the outside world using Services and Ingress

**What I Did:**
- Created a NodePort Service to expose the app
- Configured an Ingress resource for HTTP routing
- Accessed the app via browser using the Ingress host

**service.yaml:**
```yaml
apiVersion: v1
kind: Service
metadata:
  name: webapp-service
spec:
  type: NodePort
  selector:
    app: webapp
  ports:
    - protocol: TCP
      port: 80
      targetPort: 80
      nodePort: 30001
```

**ingress.yaml:**
```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: webapp-ingress
spec:
  rules:
  - host: myapp.local
    http:
      paths:
      - path: /
        pathType: Prefix
        backend:
          service:
            name: webapp-service
            port:
              number: 80
```

---

### 🟦 Mini Project 12 — Nagios Monitoring Setup
**Tool:** Nagios  
**Objective:** Monitor server health — CPU, memory, disk, and services

**What I Did:**
- Installed Nagios on a monitoring server
- Added a remote host to monitor
- Installed Nagios Plugins (NRPE) on the monitored server
- Set up alerts for CPU usage > 80% and disk usage > 90%

**Sample Nagios Host Config:**
```cfg
define host {
    use             linux-server
    host_name       web-server-01
    alias           Web Server 01
    address         192.168.1.10
    max_check_attempts  5
    check_period        24x7
    notification_interval  30
    notification_period  24x7
}
```

**Commands Used:**
```bash
# Install Nagios Plugins
sudo apt-get install nagios-plugins

# Check disk usage manually
/usr/lib/nagios/plugins/check_disk -w 20% -c 10% -p /

# Restart Nagios after config changes
sudo systemctl restart nagios
```

---

## 🏆 CAPSTONE PROJECT — Full DevOps CI/CD Pipeline

> **"End-to-End Automated DevOps Pipeline: Code to Production"**

### 📌 Project Overview

This capstone project combines **all 7 tools** learned in the workshop into one complete, automated pipeline. A developer pushes code to GitHub, and it automatically gets built, tested, containerized, deployed to Kubernetes, and monitored — without any manual steps.

---

### 🗺️ Architecture Diagram

```
Developer
    │
    ▼
GitHub (Push Code)
    │
    ▼ Webhook Trigger
Jenkins CI Server
    │
    ├── Stage 1: Pull Code from GitHub
    ├── Stage 2: Build & Test Application
    ├── Stage 3: Build Docker Image
    ├── Stage 4: Push Image to Docker Hub
    └── Stage 5: Deploy to Kubernetes Cluster
                      │
                      ▼
              Kubernetes Cluster
              (3 Replicas Running)
                      │
                      ▼
              Nagios Monitoring
              (Health Alerts Active)
```

---

### 🧱 Tools Used

| Tool | Role in Pipeline |
|------|-----------------|
| **Git + GitHub** | Source code management + webhook trigger |
| **Jenkins** | Automation server — orchestrates the full pipeline |
| **Docker** | Builds and packages the app into a container image |
| **Docker Hub** | Stores the Docker image as a registry |
| **Ansible** | Configures Kubernetes nodes (server setup) |
| **Kubernetes** | Deploys and manages the containerized application |
| **Nagios** | Monitors the server and app health continuously |

---

### 📋 Step-by-Step Implementation

#### ✅ Step 1 — Set Up GitHub Repository
```bash
git init my-devops-app
cd my-devops-app
git remote add origin https://github.com/YOUR-USERNAME/my-devops-app.git
```

#### ✅ Step 2 — Write Your Application
Create a simple `index.html` or any app file:
```html


DevOps App

  🚀 Deployed via Full DevOps CI/CD Pipeline!
  GitHub → Jenkins → Docker → Kubernetes


```

#### ✅ Step 3 — Write the Dockerfile
```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

#### ✅ Step 4 — Write the Full Jenkinsfile (CI/CD Pipeline)
```groovy
pipeline {
    agent any

    environment {
        DOCKERHUB_USER = 'your-dockerhub-username'
        IMAGE_NAME = 'my-devops-app'
        IMAGE_TAG = "v${BUILD_NUMBER}"
    }

    stages {

        stage('Stage 1: Clone Code from GitHub') {
            steps {
                echo '🔄 Pulling latest code from GitHub...'
                git branch: 'main',
                    url: 'https://github.com/YOUR-USERNAME/my-devops-app.git'
            }
        }

        stage('Stage 2: Build & Test') {
            steps {
                echo '🔨 Building the application...'
                sh 'echo Build completed successfully'
                echo '✅ Running tests...'
                sh 'echo All tests passed'
            }
        }

        stage('Stage 3: Build Docker Image') {
            steps {
                echo '🐳 Building Docker Image...'
                sh "docker build -t ${DOCKERHUB_USER}/${IMAGE_NAME}:${IMAGE_TAG} ."
                sh "docker tag ${DOCKERHUB_USER}/${IMAGE_NAME}:${IMAGE_TAG} ${DOCKERHUB_USER}/${IMAGE_NAME}:latest"
            }
        }

        stage('Stage 4: Push Image to Docker Hub') {
            steps {
                echo '📤 Pushing Docker Image to Docker Hub...'
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-credentials',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {
                    sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
                    sh "docker push ${DOCKERHUB_USER}/${IMAGE_NAME}:${IMAGE_TAG}"
                    sh "docker push ${DOCKERHUB_USER}/${IMAGE_NAME}:latest"
                }
            }
        }

        stage('Stage 5: Deploy to Kubernetes') {
            steps {
                echo '☸️ Deploying to Kubernetes Cluster...'
                sh 'kubectl apply -f k8s/deployment.yaml'
                sh 'kubectl apply -f k8s/service.yaml'
                sh "kubectl set image deployment/devops-app devops-app=${DOCKERHUB_USER}/${IMAGE_NAME}:${IMAGE_TAG}"
                sh 'kubectl rollout status deployment/devops-app'
            }
        }

    }

    post {
        success {
            echo '🎉 Pipeline completed successfully! App is live on Kubernetes.'
        }
        failure {
            echo '❌ Pipeline failed. Check the logs above.'
        }
    }
}
```

#### ✅ Step 5 — Kubernetes Deployment YAML (`k8s/deployment.yaml`)
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: devops-app
  labels:
    app: devops-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: devops-app
  template:
    metadata:
      labels:
        app: devops-app
    spec:
      containers:
      - name: devops-app
        image: your-dockerhub-username/my-devops-app:latest
        ports:
        - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
  name: devops-app-service
spec:
  type: NodePort
  selector:
    app: devops-app
  ports:
    - protocol: TCP
      port: 80
      targetPort: 80
      nodePort: 30080
```

#### ✅ Step 6 — Configure Nagios Monitoring
- Add the Kubernetes nodes to Nagios
- Monitor CPU, memory, disk usage
- Set up email alerts for failures

---

### 🎯 Capstone Project Outcome

✅ Code pushed to GitHub automatically triggers the entire pipeline  
✅ App is built, tested, and containerized without manual steps  
✅ Docker image versioned and stored on Docker Hub  
✅ Application deployed across 3 Kubernetes replicas  
✅ Nagios monitors the infrastructure 24/7  
✅ Any failure sends an alert immediately  

---

## 📝 10 Practice Tests

> Use these to test your knowledge after each day of the workshop!

---

### 📋 Practice Test 1 — DevOps Basics

1. What is the difference between Waterfall and Agile models?
2. Define DevOps. What problem does it solve?
3. List the 8 phases of the DevOps Lifecycle.
4. Name 5 popular DevOps tools and their purpose.
5. What is Continuous Integration? What is Continuous Deployment?
6. What is the difference between CI and CD?
7. What is a DevOps pipeline?
8. Why is collaboration important in DevOps culture?
9. What is "Infrastructure as Code"?
10. Name 3 benefits of adopting DevOps in an organization.

---

### 📋 Practice Test 2 — Git & GitHub

1. What is Version Control? Why is it important?
2. What is the difference between Git and GitHub?
3. What does `git init` do?
4. What is the difference between `git add` and `git commit`?
5. How do you check which branch you are currently on?
6. What is a merge conflict? How do you resolve it?
7. What is the difference between `git pull` and `git fetch`?
8. How do you create and switch to a new branch in one command?
9. What does `git log` show you?
10. What is the purpose of a `.gitignore` file?

<details>
<summary>✅ Click to see Answers</summary>

1. Version Control tracks changes in files over time, allowing rollback and collaboration.
2. Git is the tool (runs locally); GitHub is a cloud platform to host Git repositories.
3. `git init` initializes a new Git repository in the current directory.
4. `git add` stages changes; `git commit` saves staged changes to history.
5. `git branch` or `git status`
6. A merge conflict happens when two branches modify the same line. Resolve by editing the file manually and committing.
7. `git pull` fetches AND merges; `git fetch` only downloads without merging.
8. `git checkout -b branch-name`
9. `git log` shows the commit history.
10. `.gitignore` tells Git which files/folders to ignore (e.g., passwords, temp files).

</details>

---

### 📋 Practice Test 3 — Jenkins & CI/CD

1. What is Continuous Integration?
2. What is the role of Jenkins in DevOps?
3. What is a Jenkins Pipeline?
4. What is the difference between a Freestyle Job and a Pipeline Job in Jenkins?
5. What is a `Jenkinsfile`?
6. What does the `agent any` directive mean in a Jenkinsfile?
7. What are Jenkins Stages and Steps?
8. How do you trigger a Jenkins build automatically when code is pushed to GitHub?
9. What is a Jenkins Plugin? Name 2 examples.
10. What does the `post` block in a Jenkinsfile do?

<details>
<summary>✅ Click to see Answers</summary>

1. CI is the practice of frequently merging code changes and automatically building/testing them.
2. Jenkins automates the build, test, and deployment process.
3. A Jenkins Pipeline is a set of automated steps defined in a `Jenkinsfile`.
4. Freestyle Jobs are simple GUI-based; Pipeline Jobs use code (Jenkinsfile) for complex workflows.
5. A `Jenkinsfile` is a text file that defines the Jenkins Pipeline as code.
6. `agent any` means Jenkins can run the pipeline on any available agent/node.
7. Stages are major phases (Build, Test, Deploy); Steps are individual commands within a stage.
8. Configure a GitHub Webhook pointing to Jenkins URL.
9. Plugins extend Jenkins features. Examples: Git Plugin, Docker Plugin.
10. The `post` block runs actions after the pipeline finishes (e.g., send email on success/failure).

</details>

---

### 📋 Practice Test 4 — Docker Basics

1. What is the difference between Virtualization and Containerization?
2. What is Docker?
3. What is a Docker Image?
4. What is a Docker Container?
5. What is the difference between a Docker Image and a Docker Container?
6. What command is used to list all running containers?
7. How do you stop a running container?
8. What is Docker Hub?
9. What does the `docker pull` command do?
10. What is the purpose of `EXPOSE` in a Dockerfile?

<details>
<summary>✅ Click to see Answers</summary>

1. Virtualization creates full VMs with OS; Containerization shares the host OS kernel — lighter and faster.
2. Docker is a platform to build, ship, and run containers.
3. A Docker Image is a read-only template used to create containers.
4. A Docker Container is a running instance of a Docker Image.
5. An Image is static (like a blueprint); a Container is a running instance of that blueprint.
6. `docker ps`
7. `docker stop <container-id>`
8. Docker Hub is a public registry to store and share Docker images.
9. `docker pull` downloads an image from Docker Hub.
10. `EXPOSE` documents which port the container listens on (it does not publish the port).

</details>

---

### 📋 Practice Test 5 — Docker Advanced

1. What is a Dockerfile?
2. What does `FROM` instruction mean in a Dockerfile?
3. What is the difference between `RUN` and `CMD` in a Dockerfile?
4. How do you build a Docker image from a Dockerfile?
5. How do you tag a Docker image?
6. How do you push a Docker image to Docker Hub?
7. What is Docker Compose?
8. What is the command to start services defined in docker-compose.yml?
9. What is a Docker Volume? Why is it used?
10. What is the difference between `docker stop` and `docker kill`?

<details>
<summary>✅ Click to see Answers</summary>

1. A Dockerfile is a script of instructions to build a Docker image.
2. `FROM` specifies the base image to start from.
3. `RUN` executes commands during image build; `CMD` defines the default command when the container starts.
4. `docker build -t image-name .`
5. `docker tag image-name username/image-name:tag`
6. `docker push username/image-name:tag`
7. Docker Compose is a tool to define and run multi-container Docker applications.
8. `docker-compose up -d`
9. A Docker Volume persists data outside the container lifecycle — used for databases, logs, etc.
10. `docker stop` sends SIGTERM (graceful shutdown); `docker kill` sends SIGKILL (immediate stop).

</details>

---

### 📋 Practice Test 6 — Ansible

1. What is Ansible? What is it used for?
2. What is "agentless" in Ansible?
3. What is an Ansible Inventory file?
4. What is an Ansible Playbook?
5. What language are Ansible Playbooks written in?
6. What is an Ansible Module? Give 2 examples.
7. What does `become: yes` mean in a Playbook?
8. How do you run an Ansible Playbook?
9. What is an Ansible Role?
10. What does `ansible all -m ping` do?

<details>
<summary>✅ Click to see Answers</summary>

1. Ansible is an open-source automation tool used for configuration management, app deployment, and task automation.
2. Agentless means Ansible doesn't need any software installed on managed nodes — it uses SSH.
3. Inventory file lists all the managed nodes (servers) Ansible controls.
4. An Ansible Playbook is a YAML file with a list of tasks to be executed on managed nodes.
5. YAML
6. Ansible Modules are reusable units of code. Examples: `apt` (install packages), `service` (manage services).
7. `become: yes` allows the task to run with sudo/root privileges.
8. `ansible-playbook playbook.yml`
9. Ansible Roles are a way to organize playbooks into reusable, structured components.
10. It tests SSH connectivity to all nodes in the inventory — if successful, returns "pong".

</details>

---

### 📋 Practice Test 7 — Kubernetes Basics

1. What is Kubernetes?
2. What problem does Kubernetes solve?
3. What is a Pod in Kubernetes?
4. What is a Node in Kubernetes?
5. What is the difference between a Master Node and a Worker Node?
6. What is a Deployment in Kubernetes?
7. How do you check all running Pods?
8. What is `kubectl`?
9. What does `kubectl apply -f file.yaml` do?
10. What is Minikube?

<details>
<summary>✅ Click to see Answers</summary>

1. Kubernetes (K8s) is an open-source container orchestration platform.
2. It automates deployment, scaling, and management of containerized applications.
3. A Pod is the smallest deployable unit in Kubernetes — it wraps one or more containers.
4. A Node is a physical or virtual machine in the Kubernetes cluster.
5. Master Node manages the cluster (API Server, Scheduler, etcd); Worker Nodes run the actual app containers.
6. A Deployment defines the desired state for Pods — number of replicas, image, etc.
7. `kubectl get pods`
8. `kubectl` is the command-line tool to interact with a Kubernetes cluster.
9. It creates or updates resources defined in the YAML file.
10. Minikube is a tool to run a single-node Kubernetes cluster locally for learning and testing.

</details>

---

### 📋 Practice Test 8 — Kubernetes Advanced

1. What is a Kubernetes Service? Why is it needed?
2. What are the types of Kubernetes Services?
3. What is a ClusterIP Service?
4. What is a NodePort Service?
5. What is a LoadBalancer Service?
6. What is Kubernetes Ingress?
7. What is a ConfigMap in Kubernetes?
8. What is a Secret in Kubernetes?
9. How do you scale a Deployment to 5 replicas?
10. What is a Kubernetes Namespace?

<details>
<summary>✅ Click to see Answers</summary>

1. A Service provides a stable IP/DNS to access Pods, even as Pods restart.
2. ClusterIP, NodePort, LoadBalancer, ExternalName.
3. ClusterIP exposes the service only within the cluster.
4. NodePort exposes the service on a static port on each Node's IP.
5. LoadBalancer provisions an external cloud load balancer to expose the service publicly.
6. Ingress manages external HTTP/HTTPS access to services, typically with routing rules.
7. ConfigMap stores non-sensitive configuration data as key-value pairs.
8. Secret stores sensitive data (passwords, tokens) in base64-encoded form.
9. `kubectl scale deployment <name> --replicas=5`
10. A Namespace is a way to divide cluster resources between multiple users or teams.

</details>

---

### 📋 Practice Test 9 — Nagios Monitoring

1. What is Continuous Monitoring in DevOps?
2. What is Nagios?
3. What is the Nagios Architecture?
4. What are Nagios Plugins?
5. How does Nagios check a remote host?
6. What is NRPE in Nagios?
7. What is the difference between Active and Passive checks in Nagios?
8. What does a "CRITICAL" state mean in Nagios?
9. How do you add a new host to monitor in Nagios?
10. What are notification contacts in Nagios?

<details>
<summary>✅ Click to see Answers</summary>

1. Continuous Monitoring tracks the health and performance of infrastructure and apps in real time.
2. Nagios is an open-source monitoring tool for systems, networks, and infrastructure.
3. Nagios has a core server that runs checks and plugins, and a web UI to view results.
4. Nagios Plugins are scripts/binaries that perform the actual checks (disk, CPU, etc.).
5. Nagios uses NRPE (Nagios Remote Plugin Executor) to run checks on remote hosts.
6. NRPE is a Nagios agent installed on remote hosts to allow Nagios to run plugins locally on those hosts.
7. Active checks: Nagios initiates the check. Passive checks: external source sends results to Nagios.
8. CRITICAL means the service/host has crossed the critical threshold (e.g., disk 95% full).
9. Create a `.cfg` file in the Nagios config directory with `define host{}` block and restart Nagios.
10. Notification contacts are people/email addresses that Nagios alerts when a problem is detected.

</details>

---

### 📋 Practice Test 10 — DevOps Scenario-Based Questions

1. A developer pushes bad code and the build fails. How does Jenkins notify the team?
2. Your Docker container keeps crashing. What steps do you take to debug it?
3. A Kubernetes Pod is stuck in `CrashLoopBackOff`. What do you check first?
4. You need to deploy the same web server config to 50 servers. Which tool do you use?
5. How would you roll back a bad Kubernetes deployment to the previous version?
6. Your disk is 95% full on a server. How would Nagios alert you?
7. A Jenkins build was successful but the app is not working on the server. What could be wrong?
8. How do you ensure zero downtime during a Kubernetes deployment update?
9. Your Docker image is 2GB. How do you reduce its size?
10. Describe the full DevOps pipeline from a developer pushing code to users seeing the change.

<details>
<summary>✅ Click to see Answers</summary>

1. Jenkins uses the `post` block with email/Slack notifications on failure.
2. Check logs with `docker logs <container-id>`, then inspect with `docker inspect`.
3. Check Pod logs: `kubectl logs <pod-name>` and `kubectl describe pod <pod-name>`.
4. Ansible — write a Playbook to configure all 50 servers at once.
5. `kubectl rollout undo deployment/<deployment-name>`
6. Nagios has a disk check plugin set with warning/critical thresholds — it sends an email alert.
7. The deployment may have succeeded but the app config, environment variables, or DB connection could be wrong.
8. Use Rolling Updates in Kubernetes — it replaces Pods one at a time without downtime.
9. Use a smaller base image (like `alpine`), remove unnecessary packages, and use multi-stage builds.
10. Developer pushes code → GitHub triggers Jenkins webhook → Jenkins builds & tests → Docker image created → Image pushed to Docker Hub → Kubernetes pulls and deploys → Nagios monitors — users see the update live.

</details>

---

## 📈 DevOps Lifecycle — How It All Connects

```
Plan → Code (Git/GitHub) → Build (Jenkins) → Test (Jenkins)
  → Package (Docker) → Deploy (Kubernetes) → Monitor (Nagios)
       ↑                                              |
       └──────────── Feedback Loop ──────────────────┘
```

---

## 📜 Workshop Details

- **Workshop:** Cloud Train — DevOps Workshop (7 Days)
- **Platform:** [www.thecloudtrain.com](https://www.thecloudtrain.com)
- **Topics Covered:** DevOps, Git/GitHub, Jenkins, Docker, Ansible, Kubernetes, Nagios
- **Mini Projects Completed:** 12
- **Capstone Project:** Full CI/CD Pipeline
- **Practice Tests:** 10

---

## 📬 Connect With Me

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your@email.com)

</div>

---

<div align="center">

⭐ **If you found this helpful, please star this repository!** ⭐

*Built with ❤️ after completing the Cloud Train DevOps Workshop*

</div>
