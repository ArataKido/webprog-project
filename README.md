# Project Documentation

## Project Description
Project is a website created for an IT company that includes various features such as job cases, blog, and a contact form. The website is written in Django and is containerized using Docker.

## Features
The Shiddy Project website includes the following features:
- Job cases: A section that displays various projects or jobs completed by the IT company.
- Blog: A section that allows the IT company to create and publish blog posts.
- Contact form: A form that allows visitors to contact the IT company.
- Navigation menu: A navigation menu that allows visitors to easily navigate the website.
- Search bar: A search bar that allows visitors to search for blog posts or job cases.
- Cases: A section that allows users to look up cases which was made by company
- Portfolio: A section which shows what kind of projects were done by company and its stack.
- Docker: Docker provides quite much  security benefits for the website, and  one of the primary benefits is a isolation. Isolation helps to limit the impact of potential security vulnrabilities that may exist in the application. Docker containers provide a way to isolate the application from the host system and other containers that are running on the same machine. Additionally  docker facilitates horizontal scaling, which allows the website to prevent denial-of-service (DoS) attacks. Finally, Docker provides a number of built-in security features, such as secure default settings/user namespaces/seccomp profiles. This functionality  helps to reduce potential security risks and provide an additional layer of protection for the website.





## Dependencies
The following third-party dependencies are required to run the project:
- asgiref==3.5.2
- django-ckeditor==6.5.0
- django-js-asset==2.0.0
- Django==4.1
- Pillow==9.2.0
- setuptools==65.3.0
- sqlparse==0.4.2
- wheel==0.37.1
- gunicorn==20.1.0
- psycopg2-binary==2.9.5
- pytils==0.4.1


## Installation
To set up the project on a local development environment, follow these steps:

1. Clone the repository(if you don't have it locally): `git clone https://github.com/ArataKido/shiddy_project.git
2. Navigate to the project directory: `cd shiddy_project`
3. Install the required dependencies: `pip install -r requirements.txt`
4. Start the Docker containers: `docker compose up -d`
5. Apply the database migrations: `docker compose exec web python manage.py migrate`
6. Create a superuser account: `docker compose exec web python manage.py createsuperuser`
7. Access the website at `http://localhost:8000/`

## Configuration
The following environment variables need to be set in the `.env` file:
- `SECRET_KEY`: A secret key used for secure cryptographic signing.
- `DEBUG`: A boolean value indicating whether debug mode is enabled.
- `DB_NAME`: The name of the PostgreSQL database used for the project.
- `DB_USER`: The username used to connect to the database.
- `DB_PASSWORD`: The password used to connect to the database.
- `DB_HOST`: The hostname of the database container.
- `DB_PORT`: The port number used to connect to the database.

## Deployment
To deploy the website to a production environment, follow these steps:

1. Clone the repository: `git clone https://github.com/ArataKido/shiddy_project.git`
2. Create a `.env` file in the root directory with the following environment variables (replace with your own values):

```
SECRET_KEY=your_secret_key
DEBUG=False
DB_NAME=your_database_name
DB_USER=your_database_user
DB_PASSWORD=your_database_password
DB_HOST=your_database_host
DB_PORT=your_database_port
```
3. Modify the `docker-compose.yml` file to set the appropriate production values for environment variables and database settings.
4. Build the Docker container: `docker-compose build`
5. Start the Docker container: `docker-compose up -d`
6. Access the website at `http://your_server_address/`

## Contribution Guidelines
Contributions are not allowed!