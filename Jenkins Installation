Jenkins Installation Guide for CI/CD Pipeline

Step 1: Pull Jenkins Docker Image
---------------------------------
docker pull jenkins/jenkins:lts

Step 2: Run Jenkins Container
-----------------------------
docker run \
  -u root \
  -d \
  -p 8080:8080 \
  -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  --name jenkins \
  jenkins/jenkins:lts

Step 3: Unlock Jenkins
----------------------
1. Open your browser and go to http://localhost:8080
2. Get the initial admin password using:
   docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
