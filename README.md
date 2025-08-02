# task-manager
 The Workforce Management (workforcemgmt) module is an API that helps managers create, assign, and track tasks for their employees
# Task Manager - Spring Boot Project

This is a simple Task Management system built using Spring Boot.

## Features
- Create Tasks
- Reassign Tasks (old one is marked as CANCELLED)
- Fetch Tasks by Date Range (excludes CANCELLED tasks)

## How to Run

### Prerequisites
- Java 17+
- Maven

### Steps
1. Unzip the project.
2. Open terminal and run:
   ```bash
   ./mvnw spring-boot:run
   ```
   Or open in IntelliJ and run `TaskManagerApplication.java`.

## API Endpoints

### Create Task
`POST /tasks`
```json
{
  "title": "Follow up with client",
  "assignee": "John",
  "date": "2025-08-02"
}
```

### Reassign Task
`POST /tasks/reassign/{taskId}?newAssignee=Alice`

### Fetch Tasks by Date Range (Excludes CANCELLED)
`GET /tasks?assignee=Alice&start=2025-08-01&end=2025-08-10`

---

## License
MIT
