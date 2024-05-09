# CMP2804M Team Software Engineering - Doctors on Hand
_Local Project Setup Instructions_

Doctors on Hand is a service to allow people to efficiently find the best doctor for their symptoms.

## Presequities

- Node v (^20.0.0) and Node Package Manager (NPM)
- Java 21 SDK
- Git
- Docker (& Docker Compose)

We highly recommend [IntelliJ IDEA](https://www.jetbrains.com/idea/) as the IDE of choice for running this project.

---

## Setup: Backend

- Clone the Repository [TSE Server](https://github.com/TSE-Doctors-on-Hand/tse-server):

```bash
git clone https://github.com/TSE-Doctors-on-Hand/tse-server
```

- Build the Project using Gradle Buildtools:

```bash
./gradlew build
```
_(Alternatively, use the Gradle Menu in IntelliJ IDEA)_

- Start the Docker Containers
```bash
docker compose up -d
```
This will start both the `PostgresDB` and `tse-server` required for the project to start.

The backend will then be available at http://localhost:8080

### Notice
The project's base `.env` file is designed with the Docker Compose files present in the project. Edit at your own risk.

---

## Setup: Frontend

- Clone the Repository [TSE Website](https://github.com/TSE-Doctors-on-Hand/tse-website):
```bash
git clone https://github.com/TSE-Doctors-on-Hand/tse-website
```

- Install Node Dependencies:

```bash
npm i
```

- Run Development version of application:

```bash
npm run dev
```

The frontend will then be available at http://localhost:3000

## Initialising Fake Data

In order to initialize fake data for the program, please access the mock endpoint available at:

http://localhost:8080/api/admin/insert

This data is not designed for post-development usage.

