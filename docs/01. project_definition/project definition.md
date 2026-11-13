# SAM — Service & Automotive Management

**Product Description:** Automotive Workshop Management System  
**Version:** 0.2  
**Status:** Draft  
**Project Type:** Web-based Workshop Management Application

---

## 1. Project Overview

SAM (Service & Automotive Management) is a web-based application designed to improve the administrative and operational management of automotive workshops.

The system will centralize workshop information, including customer records, vehicle information, diagnostic reports, service quotations, work orders, employee assignments, financial operations, and repair history.

SAM will initially focus on small and medium-sized automotive workshops, while maintaining an architecture that can support larger businesses.

The application will support multiple workshops through independent accounts, ensuring that each business has access only to its own information.

The initial reference business is a small professional automotive workshop specializing in general mechanics and transmission services, with approximately nine employees.

## 2. Problem Statement

Many automotive workshops rely on informal administrative processes, handwritten notes, personal memory, and disconnected communication methods.

These practices can create difficulties in:

- Maintaining organized customer and vehicle records.
- Tracking vehicle repair progress.
- Identifying employees responsible for specific repairs.
- Managing spare parts and inventory locations.
- Tracking tools and workshop equipment.
- Recording business expenses and income.
- Evaluating repair costs and profitability.
- Maintaining diagnostic and service history.

SAM aims to address these problems by providing a centralized platform for workshop administration and operational tracking.

## 3. General Objective

Develop a web-based management system that centralizes automotive workshop operations, improves administrative organization, and provides reliable information for business management and decision-making.

The system must support multiple independent workshops and provide role-based access to their employees.

## 4. Specific Objectives

- Centralize customer and vehicle information.
- Record vehicle complaints and diagnostic results.
- Generate service quotations and preliminary billing reports.
- Create and manage work orders.
- Assign repair activities to employees.
- Track repair progress, responsibilities, and working times.
- Maintain vehicle service and warranty history.
- Record income, expenses, payments, and outstanding balances.
- Generate administrative and financial reports.
- Support future inventory, payroll, and equipment management.
- Maintain independent data access for each registered workshop.

## 5. Reference Business Model

The initial reference workshop has the following characteristics:

**Business Type:** General automotive mechanics and transmission specialization.

**Approximate Staff:** Nine employees.

**Organizational Structure:**
- One receptionist or administrative employee.
- Two lead mechanics.
- Four mechanic assistants, with two assistants assigned to each lead mechanic.
- Two additional employees whose specific responsibilities will need to be validated.

**Services Offered:**
- General maintenance and tune-ups.
- Oil changes.
- Automotive electronics and electrical repairs.
- Suspension and steering repairs.
- Preventive and corrective engine maintenance.
- Preventive and corrective transmission maintenance.
- Transmission oil changes and complete transmission repairs.

This business model will serve as the initial reference for understanding operational requirements.

## 6. Target Users and Permissions

SAM will support multiple users within each registered workshop.

### 6.1 Workshop Owner

The owner will have full access to relevant workshop information, including:

- Financial information.
- Employee management.
- Work orders and repair progress.
- Customer and vehicle records.
- Operational and financial reports.
- Workshop configuration.

### 6.2 Receptionist / Administrator

The receptionist or administrative employee will be responsible for:

- Registering customers and vehicles.
- Recording initial vehicle information.
- Managing diagnostic appointments and records.
- Creating service quotations.
- Registering authorized work orders.
- Assigning repair activities.
- Managing administrative information.

Additional administrative responsibilities, including human resources and payroll, may be introduced in future versions.

### 6.3 Lead Mechanics

Lead mechanics will participate in repair management and supervision.

Their responsibilities and permissions will be defined in detail during the requirements analysis.

### 6.4 Mechanic Assistants

Mechanic assistants will have access to workshop activities and repair information.

They should be able to:

- View their assigned activities.
- View other workshop activities in read-only mode.
- Consult repair instructions and deadlines.
- Register work start and completion times.

Assistants will not be allowed to modify administrative information or other employees' assignments.

### 6.5 Activity Tracking

SAM will record relevant work events, particularly:

- Work start time.
- Work completion time.
- Assigned employee.
- Activity status.

The system will not require a detailed daily activity log for every employee.

Repair durations must be flexible because different jobs have significantly different completion times.

For example, an oil change may take approximately 20 minutes to one hour, while a complete transmission repair may take several weeks or months.

## 7. Core System Modules

### 7.1 Authentication and Workshop Management

- User registration and login.
- Workshop account creation.
- User association with a workshop.
- Role and permission management.
- Independent workshop data access.

### 7.2 Customer Management

- Customer registration.
- Contact information.
- Customer vehicle records.
- Previous service history.
- Customer search and consultation.

### 7.3 Vehicle Management

- Vehicle make and model.
- Model year.
- VIN.
- Customer ownership.
- Reported problems.
- Diagnostic and repair history.
- Warranty history.

### 7.4 Diagnostic Management

The diagnostic process will begin with an initial vehicle intake record.

The system should support:

- Customer information.
- Vehicle information.
- Customer-reported problems.
- Visual inspection results.
- OBD-II diagnostic information.
- Searchable diagnostic checklists.
- Recommended repairs.
- Estimated repair costs.
- Diagnostic service charges.

The initial intake information must be maintained separately from the confirmed customer and work order records until the customer authorizes the proposed service.

### 7.5 Quotations and Preliminary Billing

After completing the diagnostic process, SAM should generate a preliminary report containing:

- Diagnostic findings.
- Recommended repairs.
- Required services.
- Estimated labor costs.
- Estimated parts and materials costs.
- Diagnostic charges.
- Total estimated amount.

The customer must be able to accept or reject the proposed work.

The diagnostic service may be charged independently, even when the customer decides not to proceed with the repairs.

### 7.6 Work Order Management

Once the customer authorizes the work:

- Confirm the customer and vehicle records.
- Generate a work order.
- Record the authorized services.
- Assign responsible employees.
- Register required activities.
- Track repair progress.
- Record working times.
- Register repair observations.
- Record completion and delivery.

### 7.7 Warranty Management

Completed repairs may enter a warranty period.

The system should support:

- Warranty registration.
- Associated vehicle and work order.
- Warranty start and expiration dates.
- Warranty status.
- Warranty-related repairs and observations.

Expired warranties should no longer appear in the active warranty section, but their records must remain in the database for historical consultation.

The warranty duration and applicable conditions will need to be configurable.

### 7.8 Financial Management

The financial module will eventually support:

- Income records.
- Expense records.
- Customer payments.
- Advance payments.
- Partial payments.
- Outstanding balances.
- Repair costs.
- Employee payroll.
- Financial reports.
- Repair profitability analysis.

The system should allow the owner to evaluate the relationship between repair complexity, costs, revenue, and profitability.

Electronic invoicing will initially be represented through a mock implementation. Real tax authority integrations will be considered separately because their requirements vary by country.

### 7.9 Reports and Statistics

SAM should generate useful administrative reports, including:

- Customer and vehicle records.
- Diagnostic reports.
- Service quotations.
- Work order reports.
- Repair progress reports.
- Income and expense summaries.
- Financial reports.

## 8. Initial Scope (MVP)

The first functional version will prioritize the essential administrative workflow.

The MVP should include:

1. Workshop and user registration.
2. Authentication and basic permissions.
3. Customer and vehicle registration.
4. Initial vehicle intake.
5. Diagnostic checklists and reports.
6. Service quotations.
7. Work order creation and management.
8. Employee assignment and repair progress tracking.
9. Basic income and expense registration.
10. Basic administrative and financial reports.

The primary objective is to provide a usable application that allows a workshop to register vehicles, maintain customer contact information, generate quotations, track authorized repairs, and consult basic financial information.

## 9. Future Features

The following features are considered potential future improvements:

- Advanced inventory management.
- Spare parts storage and location tracking.
- Tool and equipment management.
- Supplier management.
- Advanced employee and payroll management.
- Electronic invoicing integrations.
- Customer notifications.
- Customer-facing service status portal.
- Advanced financial analytics.
- Business performance projections.
- Subscription plans and commercial platform management.

These features are not mandatory for the initial MVP.

## 10. General System Considerations

SAM should be developed with the following principles:

- **Security:** Protect sensitive business and customer information.
- **Data Isolation:** Prevent unauthorized access between workshops.
- **Usability:** Provide a clear and intuitive interface.
- **Data Integrity:** Maintain consistent customer, vehicle, work order, and financial records.
- **Maintainability:** Keep the code organized and easy to modify.
- **Scalability:** Support future growth in users and functionality.
- **Historical Records:** Preserve completed repairs, financial transactions, and warranty information.

## 11. Development Approach

SAM will be developed incrementally.

Each module will follow a structured process:

1. Requirements analysis.
2. Technical research.
3. System design.
4. Implementation.
5. Testing.
6. Documentation.
7. Version control and review.

The project will also serve as a practical software engineering learning experience, applying programming, database design, web development, testing, documentation, and version control principles.

---

**End of Project Definition — Version 0.2**