# Reflection
### 1. Why is automation critical when managing hundreds of cloud servers?
Automation is important when managing hundreds of cloud servers because doing every task manually takes a lot of time and increases the chance of human error. A script can repeat the same steps consistently, such as creating a backup, checking files, or performing routine maintenance. Scheduling the script with cron also helps make sure that a task runs even when an administrator is not available to start it.

### 2. What are the dangers of automation?
However, automation can also be dangerous if it is not checked carefully. A wrong command or destructive typo could delete or change important files. If that script ran on 1,000 servers, the damage could spread quickly and affect many systems at once. To reduce this risk, administrators should review scripts, test them in a safe environment, limit permissions, keep backups, and monitor the results before using automation on production servers.

### 3. How did writing a Bash script differ from writing the Docker Compose file in Lab 6?
Writing a Bash script was different from creating a Docker Compose YAML file in Mission 6. Bash uses commands and shell syntax to carry out actions step by step, such as making a directory and compressing files. Docker Compose YAML describes the services and settings that make up an application environment. Both are useful for automation, but they solve different problems: Bash automates command-line tasks, while Compose defines how containers and related services run together.

### 4. How has your understanding of cloud computing changed from Lab 1 to Lab 9?
Across Laboratories 1 to 9, my understanding of cloud computing has grown from learning basic cloud concepts to seeing how infrastructure, deployment, operations, security, and automation work together. I learned that cloud services need to be configured, protected, monitored, and maintained, not just created. Automation connects these skills because it helps make routine work more repeatable and efficient.

### 5. Which cloud computing role did you enjoy most, and why?
The role I enjoyed most was the **Cloud Automation Engineer** because it showed how a small script can reduce repetitive work and help prevent missed tasks. I also learned that automation should not be trusted blindly. It needs testing, clear documentation, and regular checks to make sure it is doing the correct job.
