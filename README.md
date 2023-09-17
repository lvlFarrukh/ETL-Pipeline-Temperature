## ETL Using Shell Scripting

Welcome to the ETL Using Shell Scripting GitHub repository. This repository provides a practical example and implementation of an ETL (Extract, Transform, Load) pipeline using Bash scripting. After watching the accompanying video, you will have the knowledge to:

- Describe how shell scripting can be used to implement an ETL pipeline.
- Explain how ETL scripts or tasks can be scheduled using cron jobs.

### Project Overview

Imagine a scenario where you've been tasked with reporting the hourly average, minimum, and maximum temperatures from a remote sensor. This sensor supplies temperature data on demand, and the results need to be fed to a dashboard every minute. You have access to APIs that read the temperature, print it to standard output, and load the stats to a repository accessible to a reporting tool.

### Workflow

Here's an outline of how this task can be achieved using Bash scripting:

1. **Extraction**: Obtain a current temperature reading from the sensor using the 'get_temp' API. Append the reading to a log file, 'temperature.log'. Keep only the most recent hour of readings.

2. **Transformation**: Call a program, for example, a Python script called 'get_stats.py', which calculates temperature statistics from the 60-minute log. Load the resulting stats into the reporting system using the 'load_stats' API.

3. **Scheduling**: Schedule your ETL workflow to run every minute by creating a shell script named 'Temperature_ETL.sh' and setting up a cron job.

### Usage

To use this repository, follow these steps:

1. Create the 'Temperature_ETL.sh' shell script.
2. Open the script in a text editor and add the necessary commands as outlined in the comments.
3. Ensure that you've written the 'get_stats.py' Python script as described.
4. Set permissions to make your shell script executable.
5. Schedule your ETL job using a cron job, running it every minute of every day.

By exploring this repository and watching the video, you'll learn how to build ETL pipelines with basic Bash scripts and schedule ETL jobs efficiently. Start enhancing your data processing capabilities today!
