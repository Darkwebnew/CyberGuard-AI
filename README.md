# 🛡️ CyberGuard AI - AI-Powered Web Application Firewall
## 📝 Project Description
CyberGuard AI is an advanced, AI-powered Web Application Firewall (WAF) system designed to provide real-time protection against modern cybersecurity threats. This final-year project combines machine learning techniques with traditional security measures to detect and prevent common web vulnerabilities including SQL injection, XSS attacks, brute force attempts, and other malicious activities. The system features automated rule generation, comprehensive monitoring dashboards, and production-grade logging capabilities.

## 🏫 College/Team Information
| Attribute | Details |
|-----------|---------|
| **College** | Saveetha Engineering College |
| **Department** | Cyber Security |
| **Course/Semester** | Final Year Project (4th Year, 7th Semester) |
| **Team Members** | 3 |

### 👥 Team Composition
| Name | Roll Number | Role/Responsibility |
|------|-------------|---------------------|
| Pavithra M | 212222100032 | Dashboard & Visualization |
| Sriram V | 212222103002 | Lead Developer / AI Engine |
| Surothaaman R | 212222103003 | Nginx & Logging Integration |

## 🏗️ Architecture/Flow Diagram
```
text
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
```

## 📄 License
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
```
text
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

## 👥 Contributors
[AI-Powered Heart MRI Classification Contributors](https://github.com/Darkwebnew/AI-Powered-Heart-MRI-Classification-for-Clinical-Decision-Support#-contributors)  
Thanks to all the amazing contributors who make this project better every day.

- [Darkwebnew](https://github.com/Darkwebnew/)
- [22008686](https://github.com/22008686)
- [surothaaman](https://github.com/surothaaman)
