✅ 1. Open your project folder (devopsproject)

In terminal (VS Code):

cd devopsproject
✅ 2. Initialize Git
git init
✅ 3. Add all files
git add .
✅ 4. Commit
git commit -m "Initial commit"
✅ 5. Create repo in GitHub

Go to GitHub

Click New Repository

Name: devops-project (or anything)

✅ 6. Connect your project

Copy repo link and run:

git remote add origin https://github.com/JayashangavM/devops-project.git
✅ 7. Push your code
git branch -M main
git push -u origin main

👉 Version control using GitHub is the process of tracking and managing 
changes in project files using Git and storing them in a remote repository on GitHub.

🚀 FULL DOCKER DEPLOY (STEP BY STEP)
connect EC2 with pem file :
cd downloads
paste your pem file 

1️⃣ Update system
sudo apt update
2️⃣ Install Docker
sudo apt install docker.io -y
3️⃣ Start Docker
sudo systemctl start docker
sudo systemctl enable docker
4️⃣ Install Git
sudo apt install git -y
5️⃣ Clone your project
git clone https://github.com/JayashangavM/devops-project.git
6️⃣ Go to project folder
cd devops-project
7️⃣ Create Dockerfile
nano Dockerfile

👉 Paste this inside:

FROM nginx:latest
COPY file.html /usr/share/nginx/html/index.html

👉 Save:

CTRL + X
Y
Enter
8️⃣ Build Docker image
sudo docker build -t devops-project .

9️⃣ Run container
sudo docker run -d -p 80:80 devops-project

🔟 Check container
sudo docker ps

http://13.61.105.238/
