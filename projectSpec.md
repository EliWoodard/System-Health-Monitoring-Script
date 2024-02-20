# System Health Monitoring Script Specifications

## Objective

Develop a shell script that monitors and logs various system health metrics including CPU usage, disk space, memory usage, and network utilization. The script will alert the system administrator if certain thresholds are exceeded.

## Features

### CPU Usage Monitoring

- Monitor the CPU usage percentage.
- Log high CPU usage events and optionally send alerts if the usage exceeds 80% for more than a minute.

### Disk Space Monitoring

- Check and log the available disk space on all mounted drives.
- Send alerts if disk space falls below 20%.

### Memory Usage Monitoring

- Monitor and log system memory (RAM) usage.
- Alert if memory usage exceeds a predefined threshold, e.g., 90%.

### Running Processes Monitoring

- List and log currently running processes, focusing on high-resource-consuming processes.
- Identify and log any abnormal processes behavior.

### Network Utilization and Error Monitoring

- Monitor network traffic and error rates on network interfaces.
- Log significant network activity or errors.

### Automated Reporting

- Generate and log daily or hourly reports summarizing the system's health.
- Optionally, configure the script to email these reports to a system administrator.

## Implementation Details

- **Scheduling**: Utilize cron jobs for periodic monitoring.
- **Alerts and Notifications**: Implement conditional alerts using if-else statements based on the monitoring thresholds.
- **Data Processing**: Use text processing tools such as `grep`, `awk`, `sed`, and `cut` for extracting and processing monitoring data.
- **Configuration**: Allow threshold and reporting configurations through an external file or command-line arguments.

## Tools and Commands

- `df` for disk space, `free` for memory usage, `top` and `ps` for processes, `uptime` for system load, and `netstat` or `ss` for network statistics.
- `mail` for sending email notifications.

## Learning Goals

- Gain proficiency in shell scripting and system command utilities.
- Understand system health monitoring principles.
- Develop skills in automating tasks and creating cron jobs.
