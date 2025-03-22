Documentation for the project

I am a 2nd-year M.Tech student at IIT Bombay with expertise in developing Large Language Models (LLMs) from scratch and Natural Language Processing (NLP). I have worked extensively on AI-driven solutions and have prior experience in log classification systems. My technical background includes machine learning, deep learning, and anomaly detection applied to real-world system log analysis.

I am excited to contribute to this project, leveraging AI and hybrid techniques to enhance log intelligence, anomaly detection, and automated troubleshooting. Through this work, I aim to build an efficient, scalable, and intelligent log analysis system that can adapt to various security and monitoring use cases.

Basic Idea of the Project
This project implements a multi-layered log classification and anomaly detection framework that intelligently processes logs using three complementary approaches:

- Regular Expressions (Regex) – For predictable and structured log patterns.

- NLP based ML classifiers (BERT + ML model) – For more complex log structures with adequate labeled data.

- LLM-Based Log Analysis – For handling unstructured, unknown, and poorly labeled logs, leveraging the power of large-scale AI models.

Additionally, integrate real-time anomaly detection and severity ranking, ensuring that critical system issues are detected early and flagged for immediate attention.

12-Week Project Timeline (Brief Plan)

Phase 1: Research & Setup (Weeks 1-3) 
Week 1– Define project scope, select tools, and set up log aggregation (journalctl, syslog, dmesg, SELinux, auditd).  
Week 2 – Preprocess logs into structured format, filter noise, and store in a database.  
Week 3 – Perform exploratory data analysis (EDA), identify log patterns, and design classification strategy.  

Phase 2: Machine Learning & Model Training (Weeks 4-8)  
Week 4 – Implement regex-based classification for known log types.  
Week 5 – Train a BERT model for log classification and severity prediction.  
Week 6 – Integrate LLM for zero-shot classification of unknown logs.  
Week 7 – Implement anomaly detection using ML (Isolation Forest, Autoencoders).  
Week 8 – Develop severity ranking, real-time alerting, and correlation analysis.  

Phase 3: Deployment & Optimization (Weeks 9-12)  
Week 9 – Develop API for log classification, anomaly detection, and severity ranking.  
Week 10 – Deploy solution.  
Week 11 – Optimize performance, reduce false positives, and conduct stress testing.  
Week 12 – Final testing, documentation, and project review.  
