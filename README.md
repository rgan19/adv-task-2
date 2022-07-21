# Adv-Task 2


- Ensure that there is a rabbitmq server running with queue named `tasks` for this task-consumer deployment. 
- After running `consumer-deploy.yaml`,  type this into url: http://localhost:31289/swagger/index.html

- GET Request in swagger will read all tasks in rabbitmq `tasks` queue

Sample Response:
```
[
  {
    "taskID": 5,
    "customerID": 120,
    "description": "Task 5",
    "priority": "medium",
    "status": 0
  },
  {
    "taskID": 2,
    "customerID": 120,
    "description": "Task 2",
    "priority": "medium",
    "status": 1
  },
  {
    "taskID": 3,
    "customerID": 120,
    "description": "Task 3",
    "priority": "medium",
    "status": 2
  }
]

```

- For Qn5: SAGA, POST Request in swagger will add task to `task-processed` queue

- 4 status number types

| number | status     |   |   |   |
|---|---------------|---|---|---|
| 0 | "STARTED"     |   |   |   |
| 1 | "IN_PROGRESS" |   |   |   |
| 2 | "COMPLETED"   |   |   |   |
| 3 | "FAILED"      |   |   |   |

