# Task Management Backend

This is the backend API for a NooroTask, a task management application, built with Node.js, Express, and Prisma.

## Setup

1.  **Clone the repository:**

    ```bash
    git clone <your-backend-repository-url>
    cd <your-backend-directory>
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Set up environment variables:**

    * Create a `.env` file in the root directory.
    * Add the following variables:

        ```dotenv
        DATABASE_URL="postgresql://user:password@host:port/database?schema=public"
        ```

        Replace `user`, `password`, `host`, `port`, and `database` with your PostgreSQL database credentials.

4.  **Initialize the database with Prisma:**

    * Generate the Prisma client:

        ```bash
        npx prisma generate
        ```

    * Run database migrations:

        ```bash
        npx prisma migrate dev --name init
        ```

        This will create the necessary tables in your database.

5.  **Start the server:**

    ```bash
    npm run dev
    ```

    The server will start at `http://localhost:3001`.

## API Endpoints

* `GET /tasks`: Get all tasks.
* `GET /tasks/:id`: Get a single task by ID.
* `POST /tasks`: Create a new task.
* `PUT /tasks/:id`: Update a task by ID.
* `DELETE /tasks/:id`: Delete a task by ID.

## Technologies Used

* Node.js
* Express.js
* Prisma
* PostgreSQL