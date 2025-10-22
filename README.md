# 🛡️ CyberGuard AI - AI-Powered Web Application Firewall

A comprehensive, enterprise-grade Web Application Firewall powered by AI/ML for real-time threat detection and automated response.

## 🌟 Project Overview

CyberGuard AI is an intelligent Web Application Firewall designed to protect web applications from sophisticated cyber threats using advanced machine learning algorithms. This Final Year Project combines traditional WAF capabilities with AI-driven threat intelligence for superior protection.

### Key Features

-  **AI-Powered Threat Detection** - Machine learning models for pattern recognition
-  **Real-Time Monitoring** - Continuous traffic analysis and anomaly detection  
-  **Automated Response** - Intelligent blocking and rate limiting
-  **Comprehensive Logging** - Detailed audit trails with ELK Stack integration
-  **Load Balancing** - Nginx-based request distribution
-  **Scalable Architecture** - Docker-based containerized deployment

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        Internet                             │
└───────────────────────┬─────────────────────────────────────┘
                        │
                        ▼
            ┌───────────────────────┐
            │   Nginx Load Balancer │
            │   (Reverse Proxy)     │
            └───────────┬───────────┘
                        │
         ┌──────────────┼──────────────┐
         │              │              │
         ▼              ▼              ▼
    ┌────────┐    ┌────────┐    ┌────────┐
    │WAF Node│    │WAF Node│    │WAF Node│
    │   1    │    │   2    │    │   3    │
    └────┬───┘    └────┬───┘    └────┬───┘
         │             │             │
         └─────────────┼─────────────┘
                       │
         ┌─────────────┴─────────────┐
         │                           │
         ▼                           ▼
    ┌─────────────┐          ┌─────────────┐
    │Protected App 1│              │Protected App 2 │
    └─────────────┘          └─────────────┘
```

## 🚀 Quick Start

### Prerequisites

- Docker Engine 20.10+
- Docker Compose 2.0+
- Python 3.8+
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/Darkwebnew/CyberGuard-AI.git
cd CyberGuard-AI

# Set up environment variables
cp .env.example .env

# Build and start services
docker-compose up -d

# Verify deployment
docker-compose ps
```

## 📊 Features in Detail

### 1. Machine Learning Detection Engine

- **Anomaly Detection**: Statistical analysis of traffic patterns
- **Pattern Recognition**: Trained on OWASP Top 10 vulnerabilities
- **Behavioral Analysis**: User and session-based threat scoring

### 2. Attack Mitigation

Protection against:
- SQL Injection
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- DDoS attacks
- Brute force attempts
- Path traversal
- Remote Code Execution (RCE)

### 3. Monitoring & Analytics

- Real-time dashboards (Grafana)
- Log aggregation (Elasticsearch, Logstash, Kibana)
- Alert management
- Threat intelligence feeds

## 🛠️ Technology Stack

### Core Components

- **WAF Engine**: ModSecurity + custom rules
- **ML Framework**: TensorFlow, scikit-learn
- **Web Server**: Nginx
- **Backend**: Python (Flask/FastAPI)
- **Database**: PostgreSQL, Redis

### Monitoring & Logging

- **Metrics**: Prometheus
- **Visualization**: Grafana
- **Logging**: ELK Stack (Elasticsearch, Logstash, Kibana)

### DevOps

- **Containerization**: Docker
- **Orchestration**: Docker Compose
- **CI/CD**: GitHub Actions

## 📁 Project Structure

```
CyberGuard-AI/
├── waf/                  # WAF engine and rules
├── ml-models/            # Machine learning models
├── api/                  # REST API endpoints
├── dashboard/            # Monitoring dashboard
├── config/               # Configuration files
├── docker/               # Docker configuration
├── docs/                 # Documentation
├── scripts/              # Utility scripts
└── tests/                # Test suites
```

## 🔧 Configuration

### Basic WAF Configuration

```yaml
# config/waf.yaml
waf:
  mode: detection  # detection | blocking
  anomaly_threshold: 5
  paranoia_level: 2
  request_body_limit: 128kb
  
ml_engine:
  model: random_forest
  confidence_threshold: 0.85
  auto_retrain: true
```

### Environment Variables

```bash
WAF_MODE=blocking
DB_HOST=postgres
DB_PORT=5432
REDIS_HOST=redis
REDIS_PORT=6379
LOG_LEVEL=INFO
```

## 📈 Performance

- **Latency**: < 10ms additional latency
- **Throughput**: 10,000+ requests/second
- **Accuracy**: 98% threat detection rate
- **False Positives**: < 0.5%

## 🧪 Testing

```bash
# Run unit tests
python -m pytest tests/unit

# Run integration tests
python -m pytest tests/integration

# Security testing
python scripts/security_scan.py
```

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```text
MIT License

Copyright (c) 2024 CyberGuard AI Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

## 🙏 Acknowledgments/References

### Academic Support

- **Saveetha Engineering College** - Institutional support and resources
- **Department of Cyber Security Faculty** - Technical guidance and project mentorship
- **Project Advisors** - Continuous feedback and direction

### Technical References

- **ModSecurity** - WAF rule syntax and implementation patterns
- **Nginx Documentation** - Load balancing and reverse proxy configuration
- **Grafana Labs** - Monitoring and visualization best practices
- **Elastic Stack** - Log aggregation and collection
- **Docker & Docker Compose** - Containerization platform

### Security Research

- **OWASP Foundation** - Web application security guidelines
- **CVE Database** - Vulnerability research and threat intelligence
- **Security Research Papers** - Machine learning in cybersecurity applications

---

*Built with ❤️ by Team CyberGuard AI - Saveetha Engineering College*

*Final Year Project 2024 | Department of Cyber Security*

## 👥 Contributors

<div align="center">

### Lead Contributor

<table>
<tr>
<td align="center">
<a href="https://github.com/Darkwebnew">
<img src="https://github.com/Darkwebnew.png" width="100" style="border-radius:50%;" alt="Darkwebnew"/>
<br />
<sub><b>Darkwebnew</b></sub>
</a>
<br />
<b>🎯 Lead Maintainer & Project Initiator</b>
</td>
</tr>
</table>

### Project Team

<table>
<tr>
<td align="center" width="150">
<a href="https://github.com/Darkwebnew">
<img src="https://github.com/Darkwebnew.png" width="80" style="border-radius:50%;" alt="Darkwebnew"/>
<br />
<sub><b>Darkwebnew</b></sub>
</a>
</td>
<td align="center" width="150">
<a href="https://github.com/22008686">
<img src="https://github.com/22008686.png" width="80" style="border-radius:50%;" alt="22008686"/>
<br />
<sub><b>22008686</b></sub>
</a>
</td>
<td align="center" width="150">
<a href="https://github.com/surothaaman">
<img src="https://github.com/surothaaman.png" width="80" style="border-radius:50%;" alt="surothaaman"/>
<br />
<sub><b>surothaaman</b></sub>
</a>
</td>
</tr>
</table>

<br />

*Thanks to all contributors for their dedication and expertise in making this project a success.*

</div>
