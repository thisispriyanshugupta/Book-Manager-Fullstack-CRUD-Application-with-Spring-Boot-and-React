# Spring Boot CRUD Backend

## Project Overview

This is a demo Spring Boot application designed to manage books with basic CRUD (Create, Read, Update, Delete) operations. It uses PostgreSQL as the database and leverages various Spring Boot modules for a streamlined development experience.

## Technologies Used

- **Java**: 22.0.1
- **Spring Boot**: 3.3.2
- **PostgreSQL**: 16
- **Maven**: 3.9.8
- **Node.js**: v20.15.1
- **npm**: v10.7.0
- **Postman**: For API testing
- **IntelliJ IDEA**: For development

## Prerequisites

1. **Java Development Kit (JDK)**
   - Version: 22.0.1
   - [Download JDK 22](https://jdk.java.net/22/)

2. **PostgreSQL**
   - Version: 16
   - [Download PostgreSQL 16](https://www.postgresql.org/download/)

3. **Maven**
   - Version: 3.9.8
   - [Download Maven](https://maven.apache.org/download.cgi)

4. **Node.js and npm**
   - Version: v20.15.1 and npm v10.7.0
   - [Download Node.js](https://nodejs.org/)

5. **Postman**
   - [Download Postman](https://www.postman.com/downloads/)

6. **IntelliJ IDEA**
   - [Download IntelliJ IDEA](https://www.jetbrains.com/idea/download/)

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/your-repository.git
    cd your-repository
    ```

2. **Set Up the Database:**

   - Create a new PostgreSQL database named `bookdb`.
   - Update the `src/main/resources/application.properties` file with your PostgreSQL database credentials:

     ```properties
     spring.datasource.url=jdbc:postgresql://localhost:5432/bookdb
     spring.datasource.username=yourusername
     spring.datasource.password=yourpassword
     spring.jpa.hibernate.ddl-auto=update
     ```

3. **Build the Project:**

    ```bash
    mvn clean install
    ```

4. **Run the Application:**

    ```bash
    mvn spring-boot:run
    ```

   The application will start on port `8080` by default.

## Testing with Postman

Postman is a powerful tool for testing APIs. After starting your application, you can use Postman to test your API endpoints.

1. **Open Postman**: Launch Postman after installation.
2. **Create a New Request**: Click on `New` > `Request`.
3. **Set the Request Type**: Choose the HTTP method (GET, POST, PUT, DELETE) based on the API endpoint you want to test.
4. **Enter the URL**: For example, `http://localhost:8080/api/books`.
5. **Add Headers and Body**: Set headers (like `Content-Type: application/json`) and the request body if necessary.
6. **Send the Request**: Click `Send` and check the response.

## Developing with IntelliJ IDEA

1. **Open IntelliJ IDEA**: Launch IntelliJ IDEA after installation.
2. **Import the Project**:
   - Click on `File` > `Open`.
   - Select the `pom.xml` file from your project directory.
3. **Build and Run**:
   - Use the built-in Maven tool window to run Maven commands (`clean`, `install`, etc.).
   - You can run the application directly from IntelliJ by clicking the run configuration for Spring Boot.

## API Endpoints

- **GET /api/books**: Retrieve a list of all books.
- **GET /api/books/{id}**: Retrieve a book by ID.
- **POST /api/books**: Create a new book.
- **PUT /api/books/{id}**: Update an existing book.
- **DELETE /api/books/{id}**: Delete a book by ID.

### Sample API Requests

- **Create a Book:**

    ```bash
    curl -X POST http://localhost:8080/api/books \
    -H "Content-Type: application/json" \
    -d '{"title": "Book Title", "author": "Book Author"}'
    ```

- **Retrieve All Books:**

    ```bash
    curl -X GET http://localhost:8080/api/books
    ```

- **Retrieve a Book by ID:**

    ```bash
    curl -X GET http://localhost:8080/api/books/{id}
    ```

- **Update a Book:**

    ```bash
    curl -X PUT http://localhost:8080/api/books/{id} \
    -H "Content-Type: application/json" \
    -d '{"title": "Updated Title", "author": "Updated Author"}'
    ```

- **Delete a Book:**

    ```bash
    curl -X DELETE http://localhost:8080/api/books/{id}
    ```

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## Acknowledgements

- Spring Boot documentation
- PostgreSQL documentation
- Hibernate documentation
- Postman documentation
- IntelliJ IDEA documentation
