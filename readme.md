# Things I have learned from this course

Reflecting on the course, I've gained valuable insights and skills that are instrumental in modern software development:

1. Docker: I acquired proficiency in Docker, a powerful tool for containerization. Docker's ability to encapsulate applications and their dependencies has significantly enhanced my understanding of deployment processes.

2. Git: Strengthening my Git proficiency has been pivotal for version control management. Effectively utilizing branching, merging, and collaboration features has streamlined codebase management and facilitated smoother teamwork.

3. Nginx: Understanding Nginx's role as a high-performance web server and reverse proxy has broadened my knowledge of server-side technologies, contributing to more efficient web application deployments.

4. Testing Using Python: Employing Python testing frameworks like PyTest has instilled confidence in my code quality. Writing comprehensive test suites and automating test execution have become integral parts of my development workflow.

5. Python: Furthering my Python skills has enabled me to develop robust, maintainable codebases. Leveraging Python's versatility across web development, data analysis, and automation has been invaluable in various project contexts.

6. GitHub Actions: Implementing automated workflows with GitHub Actions has revolutionized my development process. Integrating continuous integration and deployment pipelines directly into version control has enhanced project efficiency and reliability.

7. APIs: Exploring API development principles has deepened my understanding of inter-service communication. Designing and consuming APIs effectively has been essential for building scalable, interconnected systems.

8. Dockerhub: Utilizing DockerHub for image management has simplified the sharing and distribution of containerized applications. Managing Docker images and versioning has become more streamlined and organized.

9. Minio: Incorporating Minio for object storage management has introduced me to scalable, self-hosted storage solutions. Leveraging Minio's compatibility with Amazon S3 APIs has facilitated efficient data storage and retrieval.

10. REPL: Engaging with REPL environments has provided an interactive platform for code experimentation and rapid prototyping. Immediate feedback and iterative development cycles have accelerated learning and problem-solving processes.

Each of these areas has contributed significantly to my professional development and equipped me with the skills necessary to thrive in contemporary software engineering environments.


# User Management Repository Overview

## Introduction
The User Management repository is a comprehensive solution for managing user information within an application. This repository provides functionalities for user authentication, CRUD operations on user data, and integration with external storage using Minio. With its modular design and adherence to best practices, the repository offers a robust foundation for building user-centric applications.

## Repository Structure
The repository follows a structured layout to facilitate ease of navigation and maintainability. Here's an overview of the directory structure:

- **app/**: Contains the main application code, including routers, schemas, services, and utilities.
- **tests/**: Houses the test suite for the application, ensuring reliable code quality and functionality.
- **settings/**: Stores configuration files and settings for the application.
- **requirements.txt**: Lists all dependencies required to run the application.

## Components
### 1. Main Application
The main application code is housed within the `app/` directory. It leverages the FastAPI framework to create a robust API for managing user data. Key components include:

- **Routers**: Defines API endpoints for user management functionalities.
- **Schemas**: Contains Pydantic models for data validation and serialization.
- **Services**: Implements business logic for user-related operations.
- **Utilities**: Provides helper functions and utilities to streamline application development.

### 2. Tests
The `tests/` directory hosts the test suite for the application. It includes unit tests, integration tests, and end-to-end tests to ensure the reliability and functionality of the codebase.

### 3. Minio Integration
The repository features integration with Minio, an open-source object storage solution. Minio is used for storing and managing user-uploaded files such as profile pictures. Key aspects of Minio integration include:

- **Purpose**: Minio enhances the application by providing scalable and reliable storage for user-generated content.
- **Integration**: Minio is seamlessly integrated into the application, allowing users to upload and retrieve files with ease.
- **Configuration**: Configuration settings for Minio are stored in the `settings/` directory, ensuring flexibility and ease of management.
- **Usage**: Developers can utilize Minio's features to store and retrieve files securely within the application.

### 4. Additional Functionality
The repository may include additional functionalities such as authentication mechanisms, email services integration, and logging capabilities. These features enhance the overall functionality and usability of the application.

# Issues faced

1. Production.yml file: By changing the github username and docker image name, and also by adding GITHUB_USERNAME and GITHUB_TOKEN helped in resolving the issues that were causing the github actions to fail.

link: https://github.com/lovkyasushya/user_management/pull/2/files

2. Creating auth_routes.py: 
I've created a new file named auth_routes.py to improve code organization and maintainability. In user_routes.py, we focus on managing routes related to user profile functionalities, such as creating, updating, retrieving, and deleting user profiles. On the other hand, auth_routes.py is dedicated to handling routes related to authentication tasks, including login, logout, and password management. 

link: https://github.com/lovkyasushya/user_management/pull/6/files

3. Duplicate email and nickname issues: In this particular issue, I observed that some test cases were erroneously passing despite the presence of failures, particularly concerning error code 400. Additionally, I identified issues related to duplicate emails and nicknames. To address these issues, I introduced new routes in user_routes.py and made necessary modifications in user_service.py, common.py, test_users_api.py, and test_user_service.py. 

link: https://github.com/lovkyasushya/user_management/pull/11/files

4. Locked and unverified users issues: Several issues arose regarding the verification process for new and locked users. To address these issues, I made updates to the code in both user_routes.py and user_service.py. Additionally, I expanded the test coverage by adding new test cases in test_users_api.py to thoroughly validate the verification process for new users. 

link: https://github.com/lovkyasushya/user_management/pull/13/files

5. Password Validation: I made enhancements to the code in user_schemas.py to enforce strict validation rules for passwords. Additionally, I incorporated new lines of code into user_routes.py to accommodate these changes. Furthermore, I expanded the test suite by including additional test cases in both test_user_api.py and test_user_schemas.py to thoroughly validate the password validation functionality.

link: https://github.com/lovkyasushya/user_management/pull/21/files

6. Resolving errors in email: Changed the order of few lines of code and added few test cases beacause the user verification structure was not in order. 

link: https://github.com/lovkyasushya/user_management/pull/4/files

## New Feature: Upload pictures using Minio.
To enable users to upload and update their profile pictures, I implemented a new API endpoint. This endpoint allows users to upload their profile pictures, which are securely stored in Minio. Additionally, I updated the user profile API endpoints to include the profile picture URL. When displaying user profiles, the application retrieves the profile picture URL from Minio. These enhancements ensure that users can personalize their accounts with profile pictures while maintaining security and efficiency.

link: https://github.com/lovkyasushya/user_management/pull/18/files

## Test cases
I have added 16 test cases in total. All these cases are added to reolve the issues that I have faced and to test if the issues got resolved or not. The above links that I have provided shows us the cases.

# Dockerhub link 
The docker image is being saved in the dockerhub and the project is working well. Below are the link and image of my Dockerhub repositories.

link: https://hub.docker.com/repositories/lovkyasushya

Image: ![Screenshot (2)](https://github.com/lovkyasushya/user_management/assets/158232938/e7395ff8-e343-4f08-b7d1-a6301d3861e4)


These competencies assure me that I am prepared to tackle complex software projects, collaborate effectively within elite teams, and stay ahead of evolving technologies. They position me as a formidable contender for various roles in the tech industry, spanning from software development to systems engineering and more. Each skill not only amplifies my technical prowess but also underscores my commitment to ongoing growth and enhancement—essential attributes for progressing in a technology-centric career.
