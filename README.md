# Project Idea: AI-Powered Log Triage and Security Alert Aggregator for Fedora

## Difficulty Level:
Easy

## Type:
1 person, full-time, 350 hours (12 weeks)

## Technology Stack:
- **Languages:** Python, Bash
- **Libraries/Frameworks:** Scikit-learn, PyTorch, TensorFlow
- **Security Technologies:** SELinux, systemd journal, audit logs
- **Machine Learning/NLP:** Basic ML techniques, Natural Language Processing (NLP)
- **System Technologies:** Fedora, RPM packaging

## Mentor:
**Huzaifa Sidhpurwala**  
Email: [huzaifas@redhat.com](mailto:huzaifas@redhat.com)

---

## **Project Description:**

### Overview:
The aim of this project is to develop an **AI-powered log triage and security alert aggregator** tool for Fedora systems. The tool will automate the parsing, classification, and prioritization of security-related logs, sourced from various log systems such as SELinux, systemd journal, and audit logs. The tool will use machine learning (ML) and natural language processing (NLP) techniques to help administrators quickly identify critical security events while minimizing noise from non-essential log entries.

### Problem Statement:
System administrators often deal with large volumes of log data from different sources. Identifying security incidents within these logs manually is time-consuming and prone to errors. There is a need for an automated tool that can triage logs and flag security-related issues effectively and efficiently.

### Solution:
This project will focus on:
1. **Log Aggregation:** Collecting logs from various sources, such as SELinux, systemd journal, and audit logs.
2. **Log Classification:** Using basic machine learning and NLP techniques to classify logs into categories (e.g., security alerts, information, warnings).
3. **Log Prioritization:** Applying heuristics or models to assign priority levels to the logs, helping administrators focus on the most critical issues first.
4. **Plugin-based Architecture:** Implementing a plugin-based structure for different log types, where each log source has its own "collector" plugin that gathers the logs in a standardized format.
5. **Deployment as an RPM package:** The final tool will be packaged as an RPM, making it easy to install on Fedora systems.

### Key Features:
- **Plugin-based structure:** Each log type (e.g., SELinux logs, audit logs, systemd journal) will have a corresponding plugin. This will allow the addition of new log sources in the future without requiring a complete redesign.
- **AI and ML-powered log classification:** The system will use machine learning models to classify logs, helping to identify potential security threats.
- **Prioritization of security alerts:** The system will be able to prioritize logs based on severity, reducing the time required to identify critical alerts.
- **Real-time log analysis:** Logs will be parsed and analyzed in real-time, providing immediate feedback to administrators.
- **CLI Interface/Basic UI:** A command-line interface or a simple UI will be provided to interact with the tool and review logs.
  
---

## **Deliverables:**

1. **Source Code Repository:**
   - A publicly accessible GitHub/GitLab repository that contains all scripts, models, and integration logic for the project. This will include:
     - Python scripts for log collection, parsing, classification, and prioritization.
     - Model training code (using scikit-learn, PyTorch, or TensorFlow).
     - Any other utilities or scripts related to the project.
   
2. **Packaged RPM:**
   - A Fedora-compliant RPM package that can be easily installed on Fedora systems.
   - The RPM will include the tool and its dependencies, making installation and deployment simple for users.
   
3. **Documentation:**
   - Concise user and developer documentation:
     - **Installation Instructions:** Guide for installing the tool on Fedora using RPM.
     - **Usage Instructions:** How to use the tool from the CLI or UI.
     - **Configuration Instructions:** How to configure log collectors and prioritize alerts.
     - **Development Guidelines:** Instructions for contributors on how to add new plugins or extend functionality.
   
4. **Demonstration/Prototype:**
   - A working prototype (CLI or simple UI) that demonstrates the following:
     - Collection of logs from various sources.
     - Classification of logs based on type.
     - Prioritization of logs based on severity or risk.
   
5. **Testing & Evaluation Results:**
   - A set of unit and integration tests to verify the functionality of the tool.
   - Evaluation reports on the performance of the classification models, including:
     - Accuracy, precision, recall, and F1 score metrics for model evaluation.
     - Benchmarking results on the tool’s performance in terms of speed, resource usage, and effectiveness in identifying security threats.

---

## **Proposed Architecture:**

1. **Log Collector Plugins:**
   - The tool will support different log sources (SELinux, systemd journal, audit logs, etc.) using plugins. Each log source will have a dedicated "collector" plugin. The plugin will be written in YAML (or another suitable configuration format), and it will manage the collection and parsing of logs from that source.
   
2. **Log Classification Module:**
   - The logs will be processed using machine learning models. These models will be trained to classify logs into categories (e.g., alerts, information, warning, critical).
   - NLP techniques will be used to parse and understand the text-based logs.
   
3. **Log Prioritization Module:**
   - Logs will be assigned a priority level based on their classification and a set of predefined rules or ML-based heuristics (e.g., based on frequency, historical patterns, or severity).
   
4. **CLI or Basic UI:**
   - A command-line interface (CLI) or a simple web-based UI will display the classified and prioritized logs in real-time.
   
5. **Packaging & Deployment:**
   - The tool will be packaged as an RPM, making it easy to install on Fedora systems. The packaging will include all dependencies and configuration files necessary for deployment.

---

## **Timeline:**

### Week 1-2:
- **Research and Planning:** Understand the requirements for different log sources (SELinux, systemd journal, audit logs).
- **Design Log Collector Plugin Architecture:** Develop a plugin-based architecture and begin the implementation of the first log collector plugin.
  
### Week 3-4:
- **Develop Initial Log Collection:** Implement log collection for SELinux logs and basic parsing functionality.
- **Start Working on Log Classification:** Begin exploring ML/NLP techniques for basic classification of logs.
  
### Week 5-6:
- **Integrate Log Classification with Collection:** Begin integrating machine learning models for log classification and categorization.
- **Extend Log Collection to More Sources:** Add support for systemd journal and audit logs.
  
### Week 7-8:
- **Develop Log Prioritization System:** Start implementing the prioritization logic, based on severity or predefined rules.
- **Testing and Debugging:** Ensure that the collection, classification, and prioritization modules work as expected.
  
### Week 9-10:
- **UI/CLI Interface Development:** Develop a simple CLI or web-based interface for interacting with the tool.
- **Testing and Evaluation:** Begin writing unit tests and evaluating the performance of the tool.
  
### Week 11-12:
- **Documentation:** Finalize user and developer documentation.
- **Final Testing & Packaging:** Package the tool as an RPM, finalize testing, and prepare for deployment.
- **Evaluation Report:** Prepare the final evaluation report, including benchmarks and performance evaluation.

---

## **Conclusion:**
The proposed AI-powered log triage and security alert aggregator for Fedora aims to automate the process of log collection, classification, and prioritization using machine learning and natural language processing techniques. The plugin-based architecture will make the tool flexible and extendable, while the end result will be a user-friendly tool that enhances system administrators' ability to quickly identify critical security events.
