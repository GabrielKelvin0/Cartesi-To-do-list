# Cartesi-To-do-list
A to do list built on Blockchain 
(link unavailable)

Cartesi Rollups Task Manager

*Overview*

This project utilizes the Cartesi Rollups library to manage tasks on the Cartesi Rollups network. It provides functionalities to add, retrieve, and mark tasks complete.

*Installation*

```
bash
npm install @cartesi/rollups
```

*Usage*

*Adding Tasks*

```
const task = { /* task data */ };
await addTask(task);
```

*Retrieving Tasks*

```
const tasks = await getTasks();
```

*Marking Tasks Complete*

```
const taskId = /* task ID */;
await markTaskComplete(taskId);
```

*Functions*

*addTask(task)*

Adds a new task to the Cartesi Rollups network.

- `task`: Object containing task data

*getTasks()*

Retrieves a list of tasks from the Cartesi Rollups network.

- Returns: Array of task objects

*markTaskComplete(taskId)*

Marks a task as complete on the Cartesi Rollups network.

- `taskId`: ID of the task to mark complete

*Code*

```
const { HttpBackend } = require('@cartesi/rollups/http');

async function addTask(task) {
  // Logic to validate and format task data
  const voucherData = { /* Prepare voucher data with task details */ };
  await HttpBackend.addVoucher(voucherData);
}

async function getTasks() {
  const reportData = { /* Define report data to retrieve task information */ };
  const reportResponse = await HttpBackend.addReport(reportData);
  // Parse report response to extract task data
}

async function markTaskComplete(taskId) {
  // Logic to identify and prepare voucher data for marking task complete
  const voucherData = { /* Include taskId and completion status */ };
  await HttpBackend.addVoucher(voucherData);
}

// Run a loop to simulate user interaction
while (true) {
  // Simulate user adding, retrieving, or marking tasks complete
  // Call appropriate functions based on user input
}
```

*Note*

This project assumes you have already set up the Cartesi Rollups network credentials.

