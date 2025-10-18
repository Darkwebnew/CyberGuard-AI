# 🛡️ CyberGuard AI - AI-Powered Web Application Firewall

## 📝 Project Description

CyberGuard AI is an advanced, AI-powered Web Application Firewall (WAF) system designed to provide real-time protection against modern cybersecurity threats. This final-year project combines machine learning techniques with traditional security measures to detect and prevent common web vulnerabilities including SQL injection, XSS attacks, brute force attempts, and other malicious activities. The system features automated rule generation, comprehensive monitoring dashboards, and production-grade logging capabilities.

## 🏫 College/Team Information

| Attribute | Details |
|-----------|----------|
| **College** | Saveetha Engineering College |
| **Department** | Cyber Security |
| **Course/Semester** | Final Year Project (4th Year, 7th Semester) |
| **Team Members** | 3 |

### 👥 Team Composition

| Name | Roll Number | Role/Responsibility |
|------|-------------|--------------------|
| Pavithra M | 212222100032 | Dashboard & Visualization |
| Sriram V | 212222103002 | Lead Developer / AI Engine |
| Surothaaman R | 212222103003 | Nginx & Logging Integration |

## 🏗️ Architecture/Flow Diagram

```text
┌─────────────────────────────────────────────────────────────────┐
│                         CyberGuard AI                           │
│                    Production-Ready WAF System                  │
└─────────────────────────────────────────────────────────────────┘
                          ┌──────────┐
                          │  Users   │
                          └────┬─────┘
                               │
               ┌───────────────┴────────────────┐
               │                                │
        ┌──────▼────────┐              ┌───────▼────────┐
        │  Nginx Node 1 │              │  Nginx Node 2  │
        │ (Load Balancer│              │ (Load Balancer) │
        │   + WAF)      │              │    + WAF)       │
        └──────┬────────┘              └───────┬────────┘
               │                               │
        ┌──────▼────────┐              ┌───────▼────────┐
        │Protected App 1│              │Protected App 2 │
        │ (Port 8081)   │              │ (Port 8082)    │
        └───────────────┘              └────────────────┘

                    ┌─────────────────────┐
                    │    ML Engine        │
                    │ (Real-time Analysis │
                    │  & Rule Generation) │
                    └─────────────────────┘
                             ┌─┴─┐
                    ┌────────┴───▼────────┐
                    │  Monitoring Stack   │
                    │ Grafana + Loki +    │
                    │ Promtail (Port 3000)│
                    └─────────────────────┘
```

### System Flow Summary
1. **Traffic Reception**: Nginx nodes receive and load-balance incoming requests
2. **WAF Analysis**: Each request is analyzed by integrated WAF rules
3. **ML Processing**: Suspicious patterns are sent to ML engine for analysis
4. **Rule Generation**: ML engine generates dynamic rules for new threat patterns
5. **Logging & Monitoring**: All activities are logged and visualized through Grafana
6. **Protection**: Malicious requests are blocked; legitimate traffic is forwarded

## ✨ Features/Functionalities

- **🤖 Real-time ML-based Attack Detection**: Advanced machine learning algorithms for identifying novel attack patterns
- **⚡ Dynamic WAF Rule Generation**: Automatic creation of firewall rules based on detected threats
- **📊 Comprehensive Monitoring Dashboards**: Real-time visualization with Grafana integration
- **🧪 Simulated Attack Traffic Generation**: Built-in tools for testing and validation
- **📋 Production-grade Logging & Analytics**: Structured logging with Loki and Promtail
- **⚖️ Load Balancing**: Multi-node Nginx setup for high availability
- **🔄 Automated Response**: Immediate blocking of detected threats
- **📈 Performance Metrics**: System health and security metrics tracking
- **🛠️ Configurable Rules**: Customizable security policies and thresholds
- **🚨 Real-time Alerting**: Instant notifications for security events

## 🚀 Installation/Quick Start

### Prerequisites

```bash
# Required Software
- Docker & Docker Compose (Latest versions)
- Python 3.8+ (for ML engine)
- Git
- 8GB+ RAM recommended
- 20GB+ available disk space
```

### Step-by-Step Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Darkwebnew/cyberguard-ai.git
   cd cyberguard-ai
   ```

2. **Environment Setup**
   ```bash
   # Copy environment template
   cp .env.example .env
   
   # Edit configuration if needed
   nano .env
   ```

3. **Build and Start Services**
   ```bash
   # Build all containers
   docker-compose build
   
   # Start the complete stack
   docker-compose up -d
   ```

4. **Verify Installation**
   ```bash
   # Check all services are running
   docker-compose ps
   
   # View logs
   docker-compose logs -f
   ```

5. **Initial Configuration**
   ```bash
   # Initialize ML models (if needed)
   docker-compose exec ml-engine python setup.py
   ```

## 💻 Usage/Demo/Screenshots

### Access Points

- **Protected Applications**: http://localhost:8080 (Load-balanced access)
- **Monitoring Dashboard**: http://localhost:3000 (Grafana)
- **ML Engine API**: http://localhost:5000
- **Individual Apps**: http://localhost:8081, http://localhost:8082

### Basic Usage

1. **Access the Monitoring Dashboard**
   - Navigate to http://localhost:3000
   - Login with default credentials (admin/admin)
   - View real-time security metrics and alerts

2. **Test Protected Applications**
   - Visit http://localhost:8080
   - Normal traffic will be served from load-balanced backend
   - Malicious requests will be blocked and logged

3. **Generate Test Traffic**
   ```bash
   # Run attack simulation
   docker-compose exec ml-engine python simulate_attacks.py
   ```

### Sample Screenshots

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/14fc8e84-97fd-4fe8-9848-72f18cb030f5" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/97697285-60fe-48b5-951e-6aa3e39194b4" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/87c60407-c41a-4ca7-9a6a-9134f3c299e9" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/2e75f568-9413-4950-bd68-bc99a46e4e31" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/cd89edfb-c7b7-4c4c-9628-29fa7d5c4415" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/5f0bc69b-333b-48b8-851a-b6a8b52f5a09" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/c41ea319-9553-4e03-9e13-90e225277a0f" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/86060d48-922f-4c16-aaee-9f3cb532b96a" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/5dea4cb4-4d75-496e-a886-7304d49b5024" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/0be3f422-892b-45fb-80bb-032297f99916" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/fede5fea-8cbe-4676-bde7-302dd15faa2d" />

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/bc1f7550-cf6a-4b55-b809-f95aa6628e1d" />


## 📚 API Documentation

### ML Engine API Endpoints

For complete API documentation, refer to: [API.md](docs/api.md)

#### Key Endpoints:

- `POST /analyze` - Analyze request for threats
- `GET /rules` - Retrieve current WAF rules
- `POST /rules/generate` - Generate new rules
- `GET /stats` - Get system statistics
- `GET /health` - Health check endpoint

### Sample API Usage

```bash
# Analyze a request
curl -X POST http://localhost:5000/analyze \
  -H "Content-Type: application/json" \
  -d '{"request_data": "sample_request"}'

# Get current rules
curl http://localhost:5000/rules
```

## 🌐 Local Services & Ports

| Service | Port | URL | Description |
|---------|------|-----|-------------|
| **Load Balancer** | 8080 | http://localhost:8080 | Main application access point |
| **Protected App 1** | 8081 | http://localhost:8081 | Backend application instance 1 |
| **Protected App 2** | 8082 | http://localhost:8082 | Backend application instance 2 |
| **Grafana Dashboard** | 3000 | http://localhost:3000 | Monitoring & visualization |
| **ML Engine API** | 5000 | http://localhost:5000 | Machine learning analysis |
| **Loki (Logs)** | 3100 | http://localhost:3100 | Log aggregation service |
| **Promtail** | 9080 | http://localhost:9080 | Log collection agent |
| **Nginx Status** | 8080/nginx_status | http://localhost:8080/nginx_status | Nginx metrics |

## 🧪 Testing/Demo Commands

### Security Testing

```bash
# Run comprehensive security test suite
docker-compose exec ml-engine python test_security.py

# Test SQL injection detection
curl "http://localhost:8080/search?q=1' OR '1'='1"

# Test XSS detection
curl "http://localhost:8080/comment" -d "content=<script>alert('xss')</script>"

# Test brute force protection
for i in {1..20}; do curl -X POST http://localhost:8080/login -d "user=admin&pass=wrong$i"; done
```

### Performance Testing

```bash
# Load testing with Apache Bench
ab -n 1000 -c 10 http://localhost:8080/

# Monitor system performance
docker stats

# Check ML engine response times
curl -w "%{time_total}" http://localhost:5000/health
```

### Attack Simulation

```bash
# Run automated attack simulation
docker-compose exec ml-engine python simulate_attacks.py --mode comprehensive

# Generate custom attack patterns
docker-compose exec ml-engine python generate_attacks.py --type sql_injection --count 50

# Test rule generation
docker-compose exec ml-engine python test_rule_generation.py
```

### Log Analysis

```bash
# View real-time attack logs
docker-compose logs -f nginx | grep "ATTACK"

# Check ML engine decisions
docker-compose logs -f ml-engine | grep "THREAT_DETECTED"

# Analyze Grafana metrics
curl http://localhost:3100/loki/api/v1/query?query={job="nginx"}
```

## 🔮 Future Scope/Limitations

### Future Enhancements

- **🌍 Multi-region Deployment**: Support for distributed WAF nodes across regions
- **🔗 API Gateway Integration**: Enhanced API security with rate limiting and authentication
- **📱 Mobile Dashboard**: Native mobile app for security monitoring
- **🤝 Third-party Integrations**: SIEM integration with Splunk, ELK Stack
- **🧠 Advanced ML Models**: Deep learning models for zero-day attack detection
- **⚡ Real-time Training**: Online learning capabilities for adaptive threat detection
- **🔐 SSL/TLS Termination**: Built-in certificate management and encryption
- **📊 Custom Reporting**: Automated security reports and compliance dashboards

### Current Limitations

- **🔄 Single-node ML Engine**: ML processing limited to single instance (scaling planned)
- **💾 Local Storage**: Logs stored locally (cloud storage integration planned)
- **🌐 IPv4 Only**: IPv6 support not yet implemented
- **📈 Basic Analytics**: Advanced threat intelligence features under development
- **🔧 Manual Configuration**: Some advanced settings require manual configuration
- **⚠️ Beta Status**: System is in beta phase, not recommended for critical production use
- **📚 Documentation**: Some advanced features lack comprehensive documentation

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
- **Scikit-learn Community** - Machine learning algorithms and methodologies
- **Docker Community** - Containerization and orchestration guidance

### Open Source Libraries
- **Flask** - Web framework for ML engine API
- **pandas** - Data processing and analysis
- **numpy** - Numerical computing
- **Grafana** - Monitoring and alerting platform
- **Loki & Promtail** - Log aggregation and collection
- **Docker & Docker Compose** - Containerization platform

### Security Research
- **OWASP Foundation** - Web application security guidelines
- **CVE Database** - Vulnerability research and threat intelligence
- **Security Research Papers** - Machine learning in cybersecurity applications

---

*Built with ❤️ by Team CyberGuard AI - Saveetha Engineering College*

*Final Year Project 2024 | Department of Cyber Security*
