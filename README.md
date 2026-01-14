# Circle - Full Stack Application

[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](graphs/commit-activity)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](CONTRIBUTING.md)

## 📋 Project Overview

**Circle** is a modern, full-stack monorepo application designed to provide a seamless social experience. It leverages a robust architecture comprising a high-performance backend and a dynamic, responsive frontend.

This repository serves as the **ROOT** monorepo, housing all sub-projects and shared resources necessary for the development, deployment, and maintenance of the Circle platform.

### Key Features
*   **Unified Monorepo Workflow**: Centralized management of frontend and backend codebases.
*   **Modern Tech Stack**: Built with TypeScript, React, Node.js, and Prisma.
*   **Scalable Architecture**: Designed for modularity and ease of extension.

---

## 🏗 Repository Structure Overview

This repository is organized as a monorepo, facilitating code sharing and unified versioning across different parts of the application.

```text
circle/
├── .git/                 # Git configuration
├── be-circle/            # Backend API (Node.js/Express, Prisma)
├── fe-circle/            # Frontend Application (React, Vite)
├── ARCHITECTURE.md       # System architecture documentation
├── CHANGELOG.md          # Version history
├── CODE_OF_CONDUCT.md    # Community standards
├── CONTRIBUTING.md       # Contribution guidelines
├── GOVERNANCE.md         # Project governance
├── LICENSE               # License information
├── README.md             # This file
├── ROADMAP.md            # Future plans
├── SECURITY.md           # Security policies
└── SUPPORT.md            # Support channels
```

---

## 📦 Sub-Projects Description

The Circle platform consists of the following primary sub-projects:

### 1. Backend (`be-circle`)
The server-side application responsible for API handling, database interactions, and authentication.
*   **Tech Stack**: Node.js, Express, TypeScript, Prisma, PostgreSQL, Redis, Cloudinary.
*   **Location**: [`./be-circle`](./be-circle/README.md)

### 2. Frontend (`fe-circle`)
The client-side application providing the user interface and user experience.
*   **Tech Stack**: React, Vite, TypeScript, Chakra UI, Redux Toolkit.
*   **Location**: [`./fe-circle`](./fe-circle/README.md)

---

## 🚀 Getting Started

To get a local copy of the project up and running, follow these simple steps.

### Prerequisites
*   Node.js (v18 or higher)
*   npm or yarn
*   PostgreSQL (Local or hosted instance)
*   Redis (Optional, for caching features)

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/your-username/circle.git
    cd circle
    ```

2.  **Install Dependencies**
    Refer to the individual sub-project READMEs for specific installation instructions.
    *   [Backend Setup Guide](./be-circle/README.md)
    *   [Frontend Setup Guide](./fe-circle/README.md)

---

## 📚 Documentation

This section serves as the **central navigation hub** for all project documentation. Please refer to the specific documents below for detailed information.

### Core Documentation
*   [**ARCHITECTURE.md**](./ARCHITECTURE.md) - Deep dive into the system design, boundaries, and communication.
*   [**ROADMAP.md**](./ROADMAP.md) - Future features and milestones.
*   [**CHANGELOG.md**](./CHANGELOG.md) - History of changes and versions.

### Community & Governance
*   [**GOVERNANCE.md**](./GOVERNANCE.md) - How the project is governed and decisions are made.
*   [**CONTRIBUTING.md**](./CONTRIBUTING.md) - Comprehensive guide for contributors.
*   [**CODE_OF_CONDUCT.md**](./CODE_OF_CONDUCT.md) - Standards for community behavior.

### Legal & Security
*   [**LICENSE**](./LICENSE) - The ISC License governing this software.
*   [**SECURITY.md**](./SECURITY.md) - Security policy and vulnerability reporting.
*   [**DISCLAIMER.md**](./DISCLAIMER.md) - Legal disclaimer and liability limitations.

### Support
*   [**SUPPORT.md**](./SUPPORT.md) - Where to find help and ask questions.

### Sub-Project Documentation
*   [**Backend Documentation**](./be-circle/README.md)
*   [**Frontend Documentation**](./fe-circle/README.md)

---

## 🤝 Contribution Flow

We welcome contributions! Please follow our standard process:
1.  Read the [Contribution Guidelines](./CONTRIBUTING.md).
2.  Check for open issues or open a new one to discuss a feature/bug.
3.  Fork the repository and create your branch (`git checkout -b feature/AmazingFeature`).
4.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
5.  Push to the branch (`git push origin feature/AmazingFeature`).
6.  Open a Pull Request.

---

## 🔐 Security

We take security seriously. If you discover a vulnerability, please do **NOT** open a public issue. Review our [Security Policy](./SECURITY.md) for instructions on how to report it safely.

---

## 📜 License

Distributed under the **ISC License**. See [`LICENSE`](./LICENSE) for more information.

---

## 👥 Maintainers

*   **Circle Team** - *Initial Work*

Project Link: [https://github.com/your-username/circle](https://github.com/your-username/circle)
