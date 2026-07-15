# Urban Scooter QA Engineering Project

This repository documents the final project developed during a QA Engineer bootcamp. It showcases a complete QA engineering workflow covering requirements analysis, test planning, test execution, defect reporting, and evidence collection for the Urban Scooter application.

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

## QA Engineering Focus

This project reflects core QA engineering practices such as:

- Requirements review and traceability
- Test case and checklist design
- Functional and UI validation
- Boundary value and equivalence partition testing
- Test execution and evidence documentation
- Bug reporting and defect analysis

## Conclusion

This repository serves as a practical QA portfolio that demonstrates the end-to-end documentation and execution process of testing activities for a real-world application scenario.
