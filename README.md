<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Task Manager</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        #taskInput, #taskList {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <h1>Task Manager</h1>
    <input type="text" id="taskInput" placeholder="Add a new task">
    <button onclick="addTask()">Add Task</button>
    <ul id="taskList"></ul>

    <script>
        function addTask() {
            var taskInput = document.getElementById('taskInput');
            var taskList = document.getElementById('taskList');

            if (taskInput.value !== '') {
                var taskItem = document.createElement('li');
                taskItem.textContent = taskInput.value;
                taskList.appendChild(taskItem);
                taskInput.value = '';
            }
        }
    </script>
</body>
</html>
