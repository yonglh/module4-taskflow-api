# Taskflow API from Module 3

A Spring Boot REST API for managing tasks. Tasks are stored in memory, so they are cleared when the application restarts.

## How the code is organized

- `TaskflowApiApplication` starts the Spring Boot application and provides the `ChatClient` used for AI summaries.
- `model/Task` defines a task with an ID, title, and completed status.
- `repository/TaskRepository` stores tasks in a `HashMap` and assigns IDs to new tasks.
- `service/TaskService` implements task operations and builds the prompt for task summaries.
- `controller/TaskController` exposes the HTTP endpoints under `/api/tasks`.

## API endpoints

| Method | Path | Description |
| --- | --- | --- |
| `GET` | `/api/tasks` | List all tasks |
| `GET` | `/api/tasks/{id}` | Get a task by ID |
| `POST` | `/api/tasks` | Create a task |
| `PUT` | `/api/tasks/{id}` | Replace a task’s title and completed status |
| `PUT` | `/api/tasks/{id}/complete` | Mark a task as complete |
| `DELETE` | `/api/tasks/{id}` | Delete a task |
| `GET` | `/api/tasks/summary` | Generate a plain-text AI summary of the tasks |

Task JSON has this shape:

```json
{
  "id": 1,
  "title": "Prepare assignment",
  "completed": false
}
```
# Module 4 Assignment
## Render Live Application URL
https://module4-taskflow-api-2aus.onrender.com/api/tasks

## Render Dashboard Screenshots
![Render dashboard](screenshots/Render-Dashboard1.jpg)
![Render dashboard](screenshots/Render-Dashboard2.jpg)

# Sketch Goal Option 1
Add CI Pipeline using GitHub Action

## GitHub Action Pipeline Run Link
https://github.com/yonglh/module4-taskflow-api/actions/runs/42165743481

## Docker Hub Image Link
https://hub.docker.com/repository/docker/yonglh/module4-taskflow-api/tags
