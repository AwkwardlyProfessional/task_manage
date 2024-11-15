# Answers to Technical Questions

## 1. How long did you spend on the coding test?

I spent about **X hours** on the coding test. Most of this time went into building the core features like user authentication, task management, and email notifications. I also spent time setting up the environment and testing everything to ensure it worked as expected. Debugging and refining the code to handle edge cases was another big part of the process.

---

## 2. What was the most useful feature that was added to the latest version of your chosen language? Please include a snippet of code that shows how you've used it.

One of the most useful features in **Python 3.10** is **Structural Pattern Matching** (PEP 634). It’s kind of like a more powerful version of switch-case statements, and it makes your code much cleaner and easier to read, especially when you're dealing with complex conditions or data.

Here's a quick example of how I’ve used it:

# #3. How would you track down a performance issue in production? Have you ever had to do this?
To track down a performance issue in production, I would follow these steps:

Monitor and Identify: First, I’d check the application logs or performance monitoring tools like New Relic or Datadog to identify the issue (e.g., slow API responses, high memory usage, etc.).

Replicate Locally: I’d try to reproduce the issue in a staging or local environment under similar load conditions. This helps isolate the problem without affecting real users.

Check Logs and Database Queries: I’d dive into the logs and database queries to look for anything unusual, such as long-running queries or errors that might be contributing to the issue.

Use Profiling Tools: I’d use profiling tools (like cProfile for Python) to identify slow functions or bottlenecks in the code. These tools help pinpoint exactly where the application is struggling.

Optimize and Test: Once I know where the issue is, I’d either optimize the code (e.g., refactor slow algorithms) or optimize the database (e.g., add indexes or refactor queries).

Continuous Monitoring: After making fixes, I’d continue monitoring to make sure the issue doesn’t pop up again.

I’ve had to debug performance issues in previous projects, especially when optimizing database queries or improving application response times during periods of high traffic.

# #4. If you had more time, what additional features or improvements would you consider adding to the task management application?
If I had more time, there are definitely a few features I’d love to add to enhance the task management application:

Task Deadline Notifications: It would be super helpful to send reminders via email or push notifications when a task is approaching its deadline.

User Roles & Permissions: I’d like to add different user roles (like admin, manager, user) so that certain people can manage tasks or settings for others.

Task Search and Filters: Adding the ability to search and filter tasks by date, priority, or status would really help users stay organized and find what they need quickly.

Recurring Tasks: Allowing users to set recurring tasks (like daily, weekly, or monthly) would make the app more useful for people with repetitive tasks.

Analytics and Task History: I’d add an option for users to view their task history and get insights into their productivity with charts and analytics.

Dark Mode: I’d add a dark mode option for a more comfortable user experience, especially for those who work late.

Real-Time Collaboration: It would be awesome to implement real-time updates, where users can collaborate on tasks in real-time, similar to how Google Docs works.

python
```def get_task_priority(priority):
    match priority:
        case 1:
            return "High priority"
        case 2 | 3:
            return "Medium priority"
        case 4 | 5:
            return "Low priority"
        case _:
            return "Unknown priority"
        
# Example usage
task_priority = 2
print(get_task_priority(task_priority))  # Output: Medium priority```
