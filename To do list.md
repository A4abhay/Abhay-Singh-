<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ToDo List</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
        }

        button {
            padding: 5px 10px;
            margin-top: 10px;
        }

        ul {
            list-style-type: none;
        }

        li {
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>My To-Do List</h1>
        <input type="text" id="taskInput" placeholder="Enter a task...">
        <button onclick="addTask()">Add Task</button>
        <ul id="taskList"></ul>
    </div>

    <script>
        function addTask() {
            var taskInput = document.getElementById("taskInput");
            var taskList = document.getElementById("taskList");

            if (taskInput.value === "") {
                alert("Please enter a task!");
                return;
            }

            var li = document.createElement("li");
            li.textContent = taskInput.value;

            taskList.appendChild(li);

            taskInput.value = "";
        }
    </script>
</body>
</html>
