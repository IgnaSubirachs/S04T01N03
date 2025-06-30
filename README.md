# Postman Environment Test – Maven & Gradle Projects

## Description

This exercise consists of testing two Spring Boot REST API projects using Postman:

- A Maven-based project (port: `9000`)
- A Gradle-based project (port: `9001`)

You are required to configure two separate **Postman environments**, one for each project, using variables for `server` and `port`. After that, execute at least one API request from each environment and capture the result.

---

## Objectives

- Create two Postman environments:
  - `Maven Project`
  - `Gradle Project`
- Each environment must include:
  - `server` = `http://localhost`
  - `port` = `9000` (Maven) or `9001` (Gradle)
- Use variables in the request URL, for example:
  ```
  {{server}}:{{port}}/HelloWorld/elmeunom
  ```

---

## How to Run the Projects

1. Open both Maven and Gradle projects in Eclipse.
2. Run both applications simultaneously:
   - Maven project will start on `http://localhost:9000`
   - Gradle project will start on `http://localhost:9001`
3. Verify that each project is responding to the `/HelloWorld/{name}` endpoint.

---

## How to Configure Postman

### 1. Create Environment for Maven

- Name: `Maven Project`
- Variables:
  - `server` → `http://localhost`
  - `port` → `9000`

### 2. Create Environment for Gradle

- Name: `Gradle Project`
- Variables:
  - `server` → `http://localhost`
  - `port` → `9001`

### 3. Send Request from Postman

Use the following request URL:
```
{{server}}:{{port}}/HelloWorld/elmeunom
```

> Replace `elmeunom` with your name.

---

## Deliverables

You must submit the following files:

1. `maven-environment.json` – exported Postman environment for Maven
2. `gradle-environment.json` – exported Postman environment for Gradle
3. `screenshot-maven.png` – capture of a successful request using the Maven environment
4. `screenshot-gradle.png` – capture of a successful request using the Gradle environment

---

## Example Output

If the `/HelloWorld/elmeunom` endpoint is working correctly, you should receive a response like:

```json
{
  "message": "Hello, elmeunom!"
}
```

---

## Notes

- Make sure both applications are running when testing from Postman.
- Use the `Manage Environments` section in Postman to import/export the environments.
- Screenshots must clearly show the environment in use and the response from the API.
