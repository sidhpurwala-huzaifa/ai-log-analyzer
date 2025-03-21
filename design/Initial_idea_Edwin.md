# AI-Powered Log Triage System for Fedora

## Executive Summary
This project proposes an efficient, lightweight AI-powered log triage system designed specifically for Fedora. It aggregates logs from various system sources, normalizes their formats, and employs machine learning models to classify and prioritize security events. The solution ensures minimal resource consumption, making it ideal for standard laptop environments.



## System Architecture Overview
The architecture follows a structured pipeline comprising four core components:

1. **Log Collection & Normalization**:
   - Sources: SELinux, systemd journal, audit logs
   - Convert logs into unified JSON format with standardized metadata.

2. **Feature Extraction**:
   - Extract features like keywords, numerical patterns, timestamps, IP addresses, and contextual data from logs.

3. **Classification & Prioritization**:
   - Classify logs using ML models into severity levels (Critical, Warning, Info).
   - Provide confidence scores for classification.

4. **Presentation Layer**:
   - Present prioritized alerts via CLI with optional email or system notifications.
  

![Screenshot 2025-03-20 at 11 36 44 PM](https://github.com/user-attachments/assets/8c1eb57d-dc54-4304-adac-634be5a06e5b)
## Detailed System Architecture

### Log Ingestion & Aggregation
- **Data Sources**: SELinux, systemd journal, audit logs.
- **Methods**: Python, Bash scripts, systemd-journald API, auditd.
- **Preprocessing**:
  - Structured JSON/CSV format.
  - Metadata extraction (timestamps, process names, IP addresses, error codes).

### Log Processing (Parsing & Filtering)
- Regular expressions (Regex), NLP feature extraction.
- Deduplication and noise reduction.

### AI Classification & Prioritization
- **Primary Models**: Traditional ML (Random Forest, Gradient Boosting Decision Trees, Logistic Regression).
- **Alternative Models**: Lightweight Transformers (DistilBERT, TinyBERT).
- **Output**:
  - Severity labels (Critical, Warning, Info).
  - Classification confidence scores.

### Output & Notifications
- CLI-based prioritized alerts.
- Optional email, Slack, or system notifications.

### Data Persistence
- Optional storage in SQLite/PostgreSQL or in-memory processing for real-time analysis.

## AI Model Selection & Rationale

### Primary Recommendation: Lightweight ML Ensemble
- Models: Random Forest, GBDT, Logistic Regression.
- Advantages:
  - Low memory (~50MB), rapid inference.
  - High interpretability.
- Resources:
  - Memory: ~50MB
  - CPU: Single-core minimal usage
  - Storage: <100MB

### Alternative Approach: Small Language Model (SLM)
- Models: DistilBERT, TinyBERT, ALBERT.
- Optimization: Quantization, distillation, pruning.
- Resources:
  - Memory: ~100-200MB
  - CPU: Single/Multi-core (multi-core recommended)

### Implementation Strategy
- **Phase 1**: Traditional ML ensemble for baseline performance.
- **Phase 2**: Evaluation on real Fedora log data.
- **Phase 3 (Optional)**: Integrate optimized SLMs for improved accuracy.

## Training Data Acquisition & Preparation
- **Sources**:
  - MITRE ATT&CK, CVE reports, synthetic attack-pattern logs, Fedora system logs.
- **Labeling**:
  - Rule-based labeling, semi-supervised learning, human validation.
- **Feature Engineering**:
  - TF-IDF text vectors, metadata features, security-specific event detection.

## Technical Implementation Details

### Log Parsing & Normalization
- Python modules (journalctl, auditd, SELinux handlers).
- Regex extraction, unified JSON schema.

### ML Pipeline
- scikit-learn for traditional ML models.
- HuggingFace Transformers (optional).

### Performance Optimization
- Batch processing, incremental learning, caching frequent patterns.

### Packaging & Deployment
- RPM compliant packaging for Fedora.
- Minimal external dependencies.
- Integration with systemd for background operation.

## Evaluation Strategy

### Performance Metrics
- Precision, recall, F1-score.
- False positive/negative rates.
- Throughput (logs/sec).

### Resource Utilization
- Memory usage profiling.
- CPU utilization metrics.
- Storage analysis for models and log data.

## High-Level Project Goals

1. **Log Aggregation & Normalization**
   - Collect and structure logs from Fedora systems.

2. **AI-based Classification & Prioritization**
   - Classify and prioritize logs based on severity.

3. **RPM Packaging & Deployment**
   - Create Fedora-compatible RPM packages.

4. **CLI / Minimal UI**
   - Develop a user-friendly CLI or minimal GUI for real-time monitoring.

5. **Documentation & Testing**
   - Comprehensive guides, unit and integration testing, performance evaluations.

## Documentation & Community Involvement
- User Guide (Installation, Configuration, Usage).
- Developer Guide (Code Structure, Contribution Guidelines).
- Active participation through GitHub.

## Conclusion & Next Steps
This structured plan provides clear guidance for implementing the Fedora AI-powered log triage system. Next steps involve refining based on mentor feedback, developing a proof-of-concept, and iteratively improving through GitHub community collaboration.

