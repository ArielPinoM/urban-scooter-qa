# Urban Scooter QA Engineering Project

Comprehensive manual testing project for a scooter rental application, covering web, mobile, and API layers with structured defect reporting.

## Objective

To validate the functional and design quality of the Urban Scooter application across its three layers — web frontend, mobile frontend, and backend API — by designing and executing structured tests, documenting defects, and collecting evidence in a professional QA workflow.

## Problem Statement

The application exhibited numerous functional, validation, and documentation bugs that compromised user experience and data integrity. A systematic testing approach was required to identify, report, and track these issues through to resolution.

## Key Learnings & Achievements

- Designed test cases and checklists directly from business requirements and Figma prototypes.
- Executed functional and UI tests across multiple browsers, screen resolutions, and a physical mobile device.
- Performed API testing using Postman, including database verification via SQL.
- Logged over 70 detailed bug reports in Jira with full traceability and evidence.
- Built a clean, well-organized repository structure suitable for a professional QA portfolio.

## Skills

**Testing & Analysis**
- Requirements review and traceability
- Test case and checklist design (functional and UI)
- Boundary value and equivalence partitioning
- API testing with Postman
- Database validation through SQL queries
- Cross-browser and cross-device testing
- Design validation against Figma references

**Documentation & Process**
- Defect tracking and management in Jira
- Test evidence collection and organization
- Test run reporting and progress tracking
- Professional repository documentation with Markdown
- Version control with Git and GitHub

## Tech Stack

- **Testing tools:** Postman, Figma (design reference), Jira (defect tracking)
- **Browsers:** Chrome 85+, Opera 71+
- **Devices:** Samsung Galaxy S23+, Android Emulator (Pixel 6)
- **Documentation:** Markdown, Git/GitHub

## Project Overview

The project is structured around four main areas:

1. Web application testing
2. Mobile application testing
3. API testing
4. Bug reporting and defect tracking

This portfolio demonstrates practical QA activities performed across different layers of the application and reflects a hands-on approach to manual testing, test design, and quality assurance documentation.

## 1. Urban Scooter Web Application

The web application requirements are documented in [docs/requirements/brd-web-app.md](docs/requirements/brd-web-app.md).

### Web Testing Artifacts

- A mind map for the two order forms was created in [docs/test-planning/web-app/order-form-mind-map.png](docs/test-planning/web-app/order-form-mind-map.png)
- Test data for the order forms is available in [docs/test-planning/web-app/order-form-test-data.md](docs/test-planning/web-app/order-form-test-data.md)
- A checklist for the "Order Status" screen was created and executed in [docs/testing/checklists/web-app/order-status-checklist.md](docs/testing/checklists/web-app/order-status-checklist.md)
- A checklist for the "Place Order" flow was created and executed in [docs/testing/checklists/web-app/place-order-checklist.md](docs/testing/checklists/web-app/place-order-checklist.md)

### Web UI Design Testing

The place-order checklist also includes UI and design validation based on the Figma design reference:

- Figma Web Design: https://www.figma.com/design/r070o8mwcFMhl5ulm8sjfE/Urban-Scooter-WEB?node-id=0-1&p=f&t=t0wpu9yBF7mcZ74x-0

## 2. Urban Scooter Mobile Application

The mobile application requirements are documented in [docs/requirements/brd-mobile-app.md](docs/requirements/brd-mobile-app.md).

### Mobile Testing Artifacts

- Functional and UI/design test cases were designed and stored in [docs/test-planning/mobile-app/](docs/test-planning/mobile-app/)
- The Figma reference used for design-based test cases is:
  - Figma Mobile Design: https://www.figma.com/design/oTS67jtkFRFA2GOkUOVfu1/Urban-Scooter-mobile?node-id=0-1&t=dJIZHaz7dAtFVqp9-1
- Test execution results and evidence are available in:
  - [docs/testing/test-runs/mobile-app/test-run-design-mobile.md](docs/testing/test-runs/mobile-app/test-run-design-mobile.md)
  - [docs/testing/test-runs/mobile-app/test-run-functional-mobile.md](docs/testing/test-runs/mobile-app/test-run-functional-mobile.md)

## 3. Urban Scooter API Testing

The backend requirements are documented in [docs/requirements/brd-backend.md](docs/requirements/brd-backend.md), and the API documentation is available in [docs/requirements/api-doc.md](docs/requirements/api-doc.md).

### API Testing Artifacts

- Boundary Value Analysis (BVA) and Equivalence Partitioning (EP) for courier creation are documented in [docs/test-planning/api/courier-test-data.md](docs/test-planning/api/courier-test-data.md)
- An API checklist was designed and executed in [docs/testing/checklists/back-end/courier-checklist.md](docs/testing/checklists/back-end/courier-checklist.md)

## 4. Bug Reports and Defect Tracking

All bug reports generated during the project are collected in [docs/testing/bug-reports/](docs/testing/bug-reports/).

The repository includes defect documentation from US-1 through US-71, covering issues identified during web, mobile, and API testing.

## Test Execution Summary

| Layer       | Tests Designed | Tests Executed | Passed | Failed | Skipped | Pass Rate |
|-------------|----------------|----------------|--------|--------|---------|-----------|
| Web App     | 215            | 328*           | 240    | 39     | 49      | 73.2%     |
| Mobile App  | 27             | 27             | 16     | 3      | 8       | 59.3%     |
| Backend API | 72             | 72             | 34     | 38     | 0       | 47.2%     |
| **Total**   | **314**        | **427**        | **290** | **80** | **57**   | **67.9%** |

*Several web test cases were executed across multiple browsers and resolutions, increasing execution count.

**Coverage:** All critical user flows across web, mobile, and API layers, including positive and negative scenarios, UI validation, and backend data integrity.

---

*This repository serves as a practical QA portfolio demonstrating the end-to-end testing process of a real-world application.*
