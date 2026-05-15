# 🚀 Laravel 12 Production Template

Production-ready Laravel 12 template using Docker, PHP 8.4, Nginx, custom `php.ini` and GitHub Actions CI/CD.

A clean and reusable starter project for modern Laravel applications with Dockerized development and automated deployment.

## ✨ Features

- ✅ Laravel 12
- ✅ PHP 8.4 (FPM)
- ✅ Dockerized environment
- ✅ Nginx configured for Laravel
- ✅ Custom `php.ini`
- ✅ GitHub Actions CI/CD
- ✅ Ready for production environments
- ✅ Organized Docker structure

---

## 📂 Project Structure

```txt
.
├── app/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── routes/
├── storage/
├── docker/
│   ├── nginx/
│   │   └── default.conf
│   ├── php/
│   │   ├── Dockerfile
│   │   └── php.ini
├── .github/
│   └── workflows/
│       └── deploy.yml
├── docker-compose.yml
├── .dockerignore
└── README.md


🐳 Running the Project with Docker
1. Clone repository
git clone

Enter the project:

cd laravel12-production-template
2. Configure environment

Copy .env:

cp .env.example .env
3. Build containers
docker compose up -d --build
4. Install dependencies

Access container:

docker exec -it laravel_app bash

Install Composer dependencies:

composer install
5. Generate application key
php artisan key:generate
6. Run migrations
php artisan migrate
7. Access application

Open browser:

http://localhost:8080

🐘 PHP Configuration

Custom PHP configuration file:

docker/php/php.ini

Example settings:

memory_limit=512M
upload_max_filesize=50M
post_max_size=50M
max_execution_time=300
date.timezone=America/Sao_Paulo
🌐 Nginx Configuration

Nginx configuration file:

docker/nginx/default.conf

Configured for:

Laravel public directory
PHP-FPM
URL rewrite support
Security rules
🔄 CI/CD with GitHub Actions

This template includes a simple CI/CD pipeline.

Workflow file:

.github/workflows/deploy.yml
Pipeline includes:
Install dependencies
Generate Laravel key
Run automated tests
SSH deployment
Docker rebuild
Database migration
Laravel optimization
🔐 GitHub Secrets

Configure the following repository secrets:

Secret	Description
SERVER_HOST	Server IP or domain
SERVER_USER	SSH user
SERVER_SSH_KEY	Private SSH key

Go to:

Settings → Secrets and variables → Actions
🛠 Useful Commands

Start containers:

docker compose up -d

Stop containers:

docker compose down

Rebuild containers:

docker compose up -d --build

Access app container:

docker exec -it laravel_app bash

Laravel optimize:

php artisan optimize

Clear cache:

php artisan optimize:clear
🚀 Future Improvements

This template can easily be extended with:

Redis
Queue Workers
Horizon
Supervisor
Multi-stage Docker builds
Zero-downtime deploy
Traefik or Nginx Proxy
Monitoring & Logs

📄 License

This project is open-sourced under the MIT license.

👨‍💻 Author

Made with ❤️ for Laravel developers.
