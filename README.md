## Screenshot
![](https://raw.githubusercontent.com/zhulinn/blog/hexo/source/uploads/post_pics/spring-angular/cart.png)

## Features
- REST API
- Docker
- Docker Compose
- JWT authentication
- Cookie based visitors' shopping cart
- Persistent customers' shopping cart
- Cart & order management
- Checkout
- Catalogue
- Order management
- Pagination
## Technology Stacks
**Backend**
  - Java 11
  - Spring Boot 2.2
  - Spring Security
  - JWT Authentication
  - Spring Data JPA
  - Hibernate
  - PostgreSQL
  - Maven
Note: The backend API url is configured in `src/environments/environment.ts` of the frontend project. It is `localhost:8080/api` by default.


## Database Schema

![](https://raw.githubusercontent.com/zhulinn/blog/hexo/source/uploads/post_pics/spring-angular/db.png)

## How to  Run

  1. Install [PostgreSQL](https://www.postgresql.org/download/) 
  2. Configure datasource in `application.yml`.
  3. `cd backend`.
  4. Run `mvn install`.
  5. Run `mvn spring-boot:run`.
  6. Spring Boot will import mock data into database by executing `import.sql` automatically.
  7. The backend server is running on [localhost:8080]().

#### Run in Docker
You can build the image and run the container with Docker. 
1. Build backend project
```bash
cd backend
mvn package
```
2. Build fontend project
```bash
cd frontend
npm install
ng build --prod
```
3. Build images and run containers
```bash
docker-compose up --build
```