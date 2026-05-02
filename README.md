📌 Overview :

This project implements a Process Monitor and Memory Log Scheduler in Python.

It monitors running system processes and logs details such as process ID, name, user, and memory usage at regular intervals.
The logging mechanism helps in analyzing system performance and tracking resource consumption.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🏗️ Architecture Diagram :

            +----------------------+
            |      User Input      |
            | (Directory, Time)    |
            +----------+-----------+
                       |
                       v
            +----------------------+
            |   Scheduler Module   |
            |   (schedule lib)     |
            +----------+-----------+
                       |
                       v
            +----------------------+
            |  Process Monitor     |
            |   (psutil lib)       |
            +----------+-----------+
                       |
                       v
            +----------------------+
            |  Process Collection  |
            | (PID, Name, Memory)  |
            +----------+-----------+
                       |
                       v
            +----------------------+
            |   Log File Writer    |
            |  (Directory Based)   |
            +----------------------+

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

⚙️ Features :

📊 Monitors running processes
🧠 Captures memory usage (VMS)
⏱️ Scheduled execution (interval-based)
📁 Automatic log file creation
📂 Directory-based log storage
❌ Handles process access exceptions

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

▶️ Command :
  python ProcessMonitorMemoryLogScheduler.py <DirectoryPath> <TimeIntervalInMinutes>

Example :
  python ProcessMonitorMemoryLogScheduler.py Logs 5

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🔄 Workflow :

Accept directory path and time interval
Initialize scheduler
Collect process information using psutil
Write process data into log file
Repeat at specified interval

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📚 Libraries Used :

Library   Purpose
os        Directory handling
psutil    Process monitoring
time      Timestamp handling
schedule  Task scheduling
sys       Command-line arguments

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🧠 Functions & Their Usage :

ProcessDisplay()
  Collects process information
  Creates log file
  Writes process details

main()
  Handles command-line arguments
  Schedules periodic execution

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📊 Logged Information :

Process ID (PID)
Process Name
Username
Memory Usage (Virtual Memory Size)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📊 Sample Log Output :

Process Logger : Mon Oct 10 12-30-45 2025

{'pid': 1234, 'name': 'python', 'username': 'user', 'vms': 45.23}
{'pid': 5678, 'name': 'chrome', 'username': 'user', 'vms': 150.67}

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

⚠️ Limitations :

Depends on psutil library
No GUI (CLI-based only)
Logs may grow large over time
No real-time visualization

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🔮 Future Enhancements :

📊 Add real-time dashboard
📈 Graph-based visualization
🧵 Multi-threaded logging
📧 Email alerts for high memory usage
🗃️ Log compression & rotation

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

👨‍💻 Author :

Pratik Chavan

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
