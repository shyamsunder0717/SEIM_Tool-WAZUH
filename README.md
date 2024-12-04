# SEIM Tool using WAZUH

## Overview
The SIEM Tool is an open-source Security Information and Event Management (SIEM) solution designed to provide real-time monitoring, detection, and response to cybersecurity threats. Built using the ELK stack (Elasticsearch, Logstash, Kibana) and Filebeat, this tool centralizes log collection and analysis, making it an ideal solution for small to medium-sized enterprises.

## Key Features
- **Log Ingestion**: Collect logs from multiple endpoints using Filebeat and Elastic Agent.
- **Log Analysis**: Utilize Elasticsearch for powerful search and analytics capabilities.
- **Visualization**: Create intuitive dashboards in Kibana for real-time data visualization.
- **Intelligent Threat Detection**: Integrate Elastic Defend for proactive threat detection and alerting.
- **Custom Dashboards**: Build personalized dashboards to monitor security incidents and system health.
- **Cost-Effective**: A fully functional SIEM solution without the high costs associated with commercial products.

## System Architecture
The architecture consists of two main components:
- **Desktop 1 (SIEM Server)**:
  - **Elasticsearch**: For indexing and storing log data.
  - **Kibana**: For visualizing and analyzing logs.
  - **Elastic Defend**: For enhanced threat detection capabilities.

- **Desktop 2 (Monitored Machine)**:
  - **Filebeat**: A lightweight shipper for collecting logs.
  - **Elastic Agent**: For gathering comprehensive security logs.

## Installation Instructions

### Prerequisites
- Kali Linux or any compatible Linux distribution.
- Java (for Elasticsearch).

### Step 1: Setting Up Elasticsearch and Kibana on Desktop 1
1. **Install Elasticsearch**:
   - Download and install Elasticsearch.
   - Configure `elasticsearch.yml` to allow access on port 9200.
   - Start the Elasticsearch service and verify it by accessing `http://<IP>:9200`.

2. **Install Kibana**:
   - Download and install Kibana.
   - Configure `kibana.yml` to connect to Elasticsearch on port 9200.
   - Start the Kibana service and access it via `http://<IP>:5601`.

### Step 2: Configuring Log Collection on Desktop 2
1. **Install Filebeat**:
   - Download and install Filebeat on Desktop 2.
   - Configure `filebeat.yml` to point to the Elasticsearch server on Desktop 1.
   - Enable the system module to collect basic system logs.

2. **Install Elastic Agent**:
   - Install the Elastic Agent to gather comprehensive security logs.

### Step 3: Integrating Elastic Defend for Threat Detection
1. **Enable Elastic Defend**:
   - Activate Elastic Defend in Kibana to monitor suspicious activities.
   - Configure alerts for specific threat patterns (e.g., Nmap scans).

### Step 4: Configuring the Dashboard
1. **Create Custom Dashboards**:
   - Use Kibana’s visualization tools to create charts, graphs, and tables.
   - Build a dashboard to monitor security incidents and alerts.

## Results
The RAS SIEM Tool successfully collects and visualizes logs in real-time, providing alerts for suspicious activities. The integration of Elastic Defend enhances the system's ability to detect threats effectively.

## Future Scope
- Implement machine learning techniques for advanced anomaly detection.
- Expand data sources for broader threat visibility.
- Improve user interface and visualization options in Kibana.
- Automate response actions upon alarm triggering.

## Contact
For inquiries or contributions, please contact:
- LinkedIn: https://linkedin.com/in/shyam-sunder-sharma-987245s


## References
- [Kavanagh, K., & Nicolett, M. (2020). Magic Quadrant for SIEM. Gartner.](https://www.gartner.com)
- [Splunk Inc. (2021). Splunk Enterprise Security.](https://www.splunk.com)
- [El Mrabet, Z., et al. (2022). "An Evaluation of the ELK Stack as an Open-Source SIEM Solution."](https://www.journalofinformationsecurity.com)
- [Martínez, R., & Medel, D. (2021). "Challenges in Implementing Open-Source SIEM Solutions: A Case Study on ELK Stack."](https://www.ijcybersecurity.com)

## License
This project is licensed under the MIT License - see the [LICENSE](
