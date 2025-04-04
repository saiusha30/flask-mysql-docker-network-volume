🌟 Flask + MySQL with Docker Compose
This project is a basic Flask web application connected to a MySQL database, all running inside Docker containers using Docker Compose.

It’s great for learning how to:

Connect a Flask app to MySQL using environment variables

Use Docker volumes and networks

Organize a simple containerized project

🗂 Project Structure
bash
Copy
Edit
docker_project/
├── docker-compose.yml     # Runs both Flask and MySQL
├── .env                   # Environment variables
└── web/
    ├── app.py             # Flask app
    └── Dockerfile         # Flask Docker image
🚀 Getting Started
✅ Step 1: Clone the Repository
bash
Copy
Edit
git clone git@github.com:saiusha30/flask-mysql-docker-network-volume.git
cd docker_project
✅ Step 2: Create a .env File
env
Copy
Edit
DB_HOST=db
DB_USER=root
DB_PASSWORD=rootpass
DB_NAME=testdb
MYSQL_ROOT_PASSWORD=rootpass
MYSQL_DATABASE=testdb
This file stores your database settings used by both services.

✅ Step 3: Run the App
bash
Copy
Edit
docker-compose up -d --build
Flask runs on http://localhost:5000

MySQL runs in the background (no direct web interface)

🧪 What Happens
Flask starts in a container and connects to the db container using environment variables.

MySQL stores its data in a named Docker volume (db_data).

Flask displays available MySQL tables when you visit the homepage.

🛑 Stop & Clean Up
bash
Copy
Edit
docker-compose down -v
This will stop the containers and remove the MySQL data volume.

🙌 Final Notes
This setup is great for learning, small projects, or as a starting point.

You can extend it by adding:

More Flask routes

API endpoints

Frontend integration

User auth
usha parvathina


