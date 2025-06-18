Payroll System

A web-based payroll management system designed for small to medium-sized enterprises (SMEs) in South Africa, ensuring compliance with 2025 South African Revenue Service (SARS) regulations. The system automates payroll processing, generates payslips, and produces SARS-compliant reports (EMP201, IRP5, EMP501) while providing secure access for administrators and employees.

Table of Contents





Overview



Features



Compliance



Technology Stack



Architecture



Development Plan



Installation



Contributing



License

Overview

This project aims to streamline payroll operations for South African businesses with up to 50 employees. It provides a secure, user-friendly platform for managing employee data, calculating payroll with automated tax deductions, and generating compliance reports for SARS. The system includes an admin dashboard for payroll management and an employee portal for self-service access to payslips and personal details.

The focus is on compliance with SARS regulations, ease of use, and scalability, with a modular design to support future enhancements like eFiling integration or multi-frequency payroll cycles.

Features





Employee Management: Add, update, and manage employee details (name, ID number, tax number, bank details, salary components).



Payroll Processing: Automate calculations for gross salary, PAYE, UIF, SDL, medical aid, pension, and net salary based on 2025 SARS tax rules.



Payslip Generation: Produce PDF payslips with detailed breakdowns, accessible via the employee portal.



SARS Reporting: Generate EMP201 (monthly), IRP5 (annual), and EMP501 (mid-year/annual) reports in PDF format for eFiling submission.



Employee Portal: Allow employees to view payslips, update bank details, and access payroll history.



Security: Role-based access (admin vs. employee), secure authentication, and data encryption.



Scalability: Support for future growth with a containerized deployment option.

Compliance

The system is designed to meet SARS payroll requirements for 2025:





PAYE: Deduct taxes per SARS tax tables, submitted monthly via EMP201 by the 7th.



UIF: 1% employee + 1% employer contribution, capped at R177.36/month.



SDL: 1% employer contribution if annual payroll exceeds R500,000.



ETI: Support Employment Tax Incentive for eligible employees (ages 18-29).



EMP501: Reconcile PAYE, UIF, and SDL mid-year (August) and annually (February).



Record Retention: Store payroll data for 5 years as mandated.



Registration: Requires company registration with SARS (EMP101) and Department of Labour for UIF.

A payroll specialist should be consulted to ensure full compliance, especially for ETI and tax table updates.

Technology Stack





Backend: Java 17, Spring Boot (MVC, Data JPA, Security)



Frontend: Thymeleaf, Bootstrap 5



Database: H2 (development), PostgreSQL (production)



PDF Generation: iText 7



Build Tool: Maven



Deployment: Docker, Docker Compose



Security: Spring Security with BCrypt password hashing

This stack ensures a robust, maintainable, and scalable system with widely supported tools.

Architecture

The system follows a layered architecture for modularity:





Presentation Layer: Thymeleaf templates with Bootstrap for server-side rendering.



Controller Layer: RESTful endpoints and Thymeleaf controllers for request handling.



Service Layer: Business logic for payroll calculations, tax deductions, and reporting.



Repository Layer: JPA repositories for database operations.



Data Layer: Entity-based schema with H2/PostgreSQL.



Security Layer: Role-based access and authentication.



Utility Layer: Tax calculation helpers.

This design supports separation of concerns and future extensions (e.g., REST API, batch processing).

Development Plan

Phase 1: Planning (1-2 weeks)





Gather requirements and confirm SARS compliance rules.



Design database schema and API endpoints.



Set up Git repository and development tools.

Phase 2: Backend Development (4-6 weeks)





Build core entities, repositories, and services.



Implement payroll and tax calculation logic.



Develop PDF report generation.



Configure authentication and authorization.

Phase 3: Frontend Development (3-4 weeks)





Create Thymeleaf templates for admin and employee interfaces.



Integrate responsive design with Bootstrap.



Ensure role-based UI visibility.

Phase 4: Testing (2-3 weeks)





Unit test payroll calculations and services.



Integration test database and API endpoints.



Validate SARS report formats.



Perform security and usability testing.

Phase 5: Deployment (1-2 weeks)





Containerize with Docker for staging/production.



Set up PostgreSQL and deploy to a cloud provider.



Document setup and usage for end-users.

Phase 6: Maintenance





Update tax tables annually per SARS.



Add features (e.g., eFiling API, leave tracking).



Monitor performance and security.

Installation

Prerequisites





Java 17



Maven



Docker (optional)



PostgreSQL (production)

Setup Plan





Clone the repository: git clone <repo-url>.



Configure application.properties for database settings.



Build with Maven: mvn clean package.



Run locally: java -jar target/payroll-system-0.0.1-SNAPSHOT.jar.



(Optional) Deploy with Docker: docker-compose up --build.

Detailed setup instructions will be provided upon implementation completion.

Contributing

Contributions are welcome! To contribute:





Fork the repository.



Create a feature branch: git checkout -b feature/your-feature.



Commit changes: git commit -m "Add your feature".



Push to the branch: git push origin feature/your-feature.



Open a pull request.

Please follow coding standards and include tests for new features.

License

This project is licensed under the MIT License. See LICENSE for details
