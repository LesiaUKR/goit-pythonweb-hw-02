## Task 2

Clone a FastAPI application, configure and run it in a Docker container, and check the application's functionality and database connection.

### Step-by-Step Instructions

1. Clone the repository at https://github.com/GoIT-Python-Web/Computer-Systems-hw02 using git clone and navigate to the cloned directory.

2. Create a Dockerfile with instructions to build the Docker image for the application.

3. Write a docker-compose.yaml file with the configuration for the application and PostgreSQL.

4. Use Docker Compose to build the environment and the docker-compose up command to launch the environment.

💡 Hint: Modify the SQLALCHEMY_DATABASE_URL connection string found in conf/db.py. Instead of localhost, insert the PostgreSQL service name from your docker-compose.yaml.

#### Example:

```python
SQLALCHEMY_DATABASE_URL = f"postgresql+psycopg2://postgres:567234@localhost:5432/hw02"
```

When using Docker Compose, each service (container) has its own network, and they usually can’t communicate via localhost. Instead, use the service name as the hostname.

5. Verify the application’s functionality and the database’s availability.
   💡 Hint:

After running the container with the application, the browser view should appear as follows:

![Container](./assets/task_example_1.jpg)
If correctly configured in docker-compose.yaml, pressing the “Check DB” button should display the following:

![Container](./assets/task_example_2.jpg)

If you see a red error box instead of “Welcome to FastAPI!”, it means docker-compose.yaml is incorrectly configured.

### Acceptance Criteria

- The repository is cloned, and a Dockerfile for building the application’s Docker image is created.
- A docker-compose.yaml file is written with configuration for the application and PostgreSQL.
- Docker Compose and the docker-compose up command are used to build and run the environment.
- The application is functional, and the database is accessible, as confirmed by pressing the “Check DB” button.

----

# TASK RESULTS

![Step 1](./assets/Screenshot_4.png)

![Step 2](./assets/Screenshot_3.png)

![Step 3](./assets/Screenshot_1.png)

![Step 4](./assets/Screenshot_2.png)