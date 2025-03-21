
```text

ai-log-analyzer/
├── collectors/                # Source-specific log collectors
│   ├── selinux_collector.py     # Collects and parses SELinux logs
│   ├── systemd_collector.py     # Collects systemd journal logs via journalctl
│   └── audit_collector.py       # Collects logs from auditd
│
├── parsers/                  # Parsing and normalization modules
│   └── log_parser.py            # Parses and normalizes raw logs into structured format
│
├── features/                 # Feature extraction logic
│   └── feature_extractor.py     # Extracts TF-IDF, metadata, semantic features from logs
│
├── models/                   # ML models for classification
│   └── ml_ensemble.py           # Implements Random Forest, GBDT, Logistic Regression
│
├── cli/                      # CLI interface
│   └── main.py                  # Entry point for CLI usage
│
├── utils/                    # Helper utilities
│   └── helpers.py               # Logging, config loading, etc.
│
├── config/                   # Config files and schemas
│   └── config.yaml              # Configuration for model paths, thresholds, etc.
│
├── tests/                    # Unit and integration tests
│   ├── test_collectors.py       # Tests for log collection scripts
│   └── test_models.py           # Tests for ML model inference
│
├── README.md                 # Project overview and instructions
└── setup.py                  # Installation script (optional if packaging)
```
