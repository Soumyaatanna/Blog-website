# Spring Boot Blog Application

## Project Overview
This Spring Boot Blog Application is a comprehensive project designed to enhance your development skills using Java Spring Boot. The application allows users to create and manage blog posts with features like user authentication, post creation, editing, and deletion. It is built using Spring Data JPA for database interactions, H2 Database for in-memory data storage, Thymeleaf for server-side rendering, Spring Security for user authentication and authorization, and follows the Model View Controller (MVC) architecture.

## Features
- **User Registration and Authentication**: Secure user registration and login functionality.
- **Blog Post Management**: 
  - Create, read, update, and delete blog posts.
  - View a list of all blog posts.
  - View individual blog post details.
- **User Roles**:
  - Admin: Full access to create, edit, delete posts.
  - User: Access to view posts and create comments.
- **Secure Handling of User Data and Authentication**: Implemented using Spring Security.

## Technologies Used
- **Spring Boot**: Core framework for building the application.
- **Spring Data JPA**: For database interactions.
- **H2 Database**: In-memory database for development and testing.
- **Thymeleaf**: Template engine for rendering views.
- **Spring Security**: For authentication and authorization.
- **MVC Architecture**: For structuring the application.

## Setup and Installation

### Prerequisites
- Java JDK (version 11 or higher)
- Maven
- IDE (e.g., IntelliJ IDEA, Eclipse)

### Project Setup
1. Clone the repository:
    ```sh
    git clone https://github.com/YourUsername/SpringBootBlog.git
    cd SpringBootBlog
    ```

2. Open the project in your IDE.

3. Build the project using Maven:
    ```sh
    mvn clean install
    ```

### Backend Configuration
1. Configure the `application.properties` file with your H2 database settings:
    ```properties
    spring.datasource.url=jdbc:h2:mem:blogdb
    spring.datasource.driverClassName=org.h2.Driver
    spring.datasource.username=sa
    spring.datasource.password=password
    spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
    spring.h2.console.enabled=true
    spring.h2.console.path=/h2-console
    spring.jpa.hibernate.ddl-auto=update
    ```

2. Run the Spring Boot application:
    ```sh
    mvn spring-boot:run
    ```

### Frontend Setup
- Thymeleaf templates are used for rendering views. No separate frontend setup is required.

## Database Setup
- The H2 database will be automatically configured and initialized by Spring Boot. You can access the H2 console at `/h2-console` for database management.

## API Endpoints

### User Authentication
- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/signin` - Authenticate a user

### Blog Post Management
- `POST /api/posts` - Create a new blog post (admin only)
- `GET /api/posts` - Retrieve all blog posts
- `GET /api/posts/{id}` - Retrieve a specific blog post by ID
- `PUT /api/posts/{id}` - Update a blog post (admin only)
- `DELETE /api/posts/{id}` - Delete a blog post (admin only)

## Security
- User authentication and authorization are implemented using Spring Security.
- Passwords are securely hashed and stored in the database.

## Testing and Debugging
- Thoroughly tested both frontend and backend functionalities.
- Used browser developer tools and backend logs for debugging.

## Contributing
- Feel free to open issues or submit pull requests for improvements and new features.

## License
This project is licensed under the MIT License.

## Contact
For any questions or support, please contact [Your Name].
