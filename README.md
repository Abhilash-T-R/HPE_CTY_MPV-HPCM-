# Monitoring Pipeline Visualization

## Overview

The **Monitoring Pipeline Visualization** project aims to reduce the complexity of debugging and understanding the HPCM (High Performance Computing Monitoring) pipeline for end-users and support teams. This solution provides a real-time monitoring system, offering clear visualizations of the status and data flow between different services in the pipeline.

## Key Features

- **Real-time Data Collection**: Scrapes data from various pipeline components like Mosquitto, Kafka, Logstash, and Opensearch.
- **Service Status Monitoring**: Tracks and displays the status and uptime of key services.
- **Data Flow Identification**: Identifies data flow between pipeline stages to pinpoint issues quickly.
- **Graphical Visualization**: Utilizes Grafana’s NodeGraph API to visualize the relationships and statuses of pipeline components.
- **Command-Line Interface (CLI)**: Provides a CLI for managing and controlling the pipeline monitoring system.
- **Data Logging**: Implements a logging mechanism to track warnings, errors, and info logs for easier troubleshooting.

  ## Screenshots

  ![image alt](https://github.com/Abhilash-T-R/HPE_CTY_MPV-HPCM-/blob/35134c72567b3c41b40ebe38596040c09549efdb/Screenshot%20(37).png)
  ![image alt](https://github.com/Abhilash-T-R/HPE_CTY_MPV-HPCM-/blob/036b3d0db409c87aff351770e0f5b0a93a453a68/Screenshot%20(38).png)

## Technologies Used

- **Programming Language**: Python
- **Operating System**: RedHat Enterprise Linux (RHEL)
- **Visualization**: Grafana with NodeGraph API Plugin
- **Services**: Apache Kafka, Mosquitto, Logstash, Opensearch

## Architecture

1. **Data Scraping**: Extracts status and uptime of services using the Python subprocess module and systemd services.
2. **Data Logging**: Logs information with a time-rotating handler to avoid overloading log files.
3. **Data Persistence**: Stores real-time metrics for Grafana visualization.
4. **Service Deployment**: Runs as a service named `monitor.service`, allowing automated startup using systemctl.
5. **Visualization**: Grafana’s NodeGraph is used to create a visual representation of the pipeline's data flow.

## Installation
### Prerequisites
- RedHat Enterprise Linux (RHEL) 9.4
- Python 3.11/3.12
- Kafka 3.7.0
- Logstash 8.13.0
- Opensearch 2.11.0
- Grafana 11.1.0

### Steps
1. Clone the repository:
   git clone <repo-url>
2. Install necessary dependencies:
   pip install -r requirements.txt
3. Start the service:
   sudo systemctl start monitor.service
4. Use the provided CLI to manage the monitoring service:
   monitor status      # Check the status of the monitoring service
   monitor enable      # Enable the monitoring service
   monitor disable     # Disable the monitoring service
   
Future Scope
Dashboard Expansion: Develop dashboards for additional pipelines.
Security Enhancements: Implement advanced security features for the monitoring system.
AI-driven Debugging: Enable automatic debugging and error identification using AI.
Performance Optimization: Improve system efficiency and reduce downtime.

Contributors
Akshay G
Chandana L
Chinmai H K
Abhilash T R
Srivarshini S
Raghul Vasudevan


This README file provides a concise description, usage instructions, and installation guidelines for the project.

