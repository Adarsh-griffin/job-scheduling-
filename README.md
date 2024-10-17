This code implements a simple job scheduling system in C++. 

### Class Definitions

1. *Job Class*:
   - Represents a single job with three attributes:
     - jobID: An integer identifier for the job.
     - jobName: A string representing the name of the job.
     - status: A string indicating the current status of the job, which can be "Pending", "Processing", or "Completed".
   - The constructor initializes the jobID, jobName, and sets the initial status to "Pending".

2. *JobScheduler Class*:
   - Manages the job queue and job statuses.
   - Contains three data structures:
     - jobQueue: A queue to hold jobs waiting to be processed.
     - completedJobs: A stack to store jobs that have been completed.
     - allJobs: A vector to maintain all jobs and their statuses for tracking.

### Methods of JobScheduler

- *addJob*: Adds a new job to the jobQueue and allJobs. It outputs a message confirming the job's addition.

- *processJobs*: Processes jobs in the jobQueue:
  - If the queue is empty, it outputs a message.
  - Otherwise, it processes each job by:
    - Changing its status to "Processing".
    - Simulating job completion by changing its status to "Completed" and pushing it onto the completedJobs stack.

- *displayCompletedJobs*: Displays all jobs that have been completed by popping jobs from the completedJobs stack and printing their details.

- *displayPendingJobs*: Iterates through allJobs and displays jobs with the status "Pending".

- *displayAllJobs*: Displays the details of all jobs stored in allJobs, including their current status.

### Main Function

- Provides a simple text-based user interface for interacting with the JobScheduler:
  - Users can choose to add jobs, process them, and display pending or completed jobs, or see all jobs.
  - The loop continues until the user selects the option to exit.

### Example Workflow

1. *Add Job*: The user enters a job ID and name, which is then added to the system.
2. *Process Jobs*: The system processes jobs in the order they were added, updating their statuses accordingly.
3. *Display Jobs*: The user can view pending jobs, completed jobs, or all jobs at any time.

### Key Concepts Used

- *Data Structures*: Utilizes a queue for FIFO job processing and a stack for LIFO completed job tracking.
- *Object-Oriented Programming*: Encapsulates job-related functionality within classes, promoting modularity.
- *User Input Handling*: Uses standard input/output for user interaction.

Overall, this code provides a straightforward implementation of a job scheduling system, demonstrating basic C++ programming concepts like classes, data structures, and user input handling.
