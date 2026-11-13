# SAM — Functional Requirements

**Document Version:** 0.2  
**Status:** Draft  
**Project:** Service & Automotive Management

## 1. Authentication and Workshop Management

- **FR-001:** The system shall allow workshop owners to create an account.
- **FR-002:** The system shall allow registered owners and administrators to log in and log out.
- **FR-003:** The system shall associate each workshop with its own users and information.
- **FR-004:** The owner shall be able to manage workshop administrators.
- **FR-005:** Only owners and authorized administrators shall have access to the system's management functions.
- **FR-006:** The system shall isolate each workshop's information from other workshops.

## 2. Customer Management

- **FR-007:** The system shall allow authorized users to register customers.
- **FR-008:** The system shall store customer contact information, including name and phone number.
- **FR-009:** The system shall allow users to search for customers.
- **FR-010:** The system shall display a customer's vehicle and service history.

## 3. Vehicle Management

- **FR-011:** The system shall allow authorized users to register vehicles.
- **FR-012:** Vehicle records shall include make, model, year, VIN, and owner.
- **FR-013:** The system shall allow users to search for registered vehicles.
- **FR-014:** The system shall preserve a vehicle's service history.

## 4. Vehicle Intake and Diagnostics

- **FR-015:** The initial vehicle intake shall be performed outside the system using the workshop's physical process.
- **FR-016:** The system shall not create customer, vehicle, or intake records before the customer authorizes the repair process.
- **FR-017:** If the customer rejects the proposed repair after diagnosis, no customer, vehicle, or work order record shall be created in SAM.
- **FR-018:** The workshop shall be able to charge for the diagnostic service independently of whether the customer authorizes the repair.
- **FR-019:** Diagnostic checklists and reports for rejected repairs shall be handled outside SAM during the initial version.
- **FR-020:** Once the customer authorizes the repair, authorized users shall be able to register the customer, vehicle, and relevant diagnostic information in SAM.

## 5. Service Catalog and Quotations

- **FR-021:** The system shall allow authorized users to manage a catalog of workshop services.
- **FR-022:** Service records shall include a name, description, and configurable price.
- **FR-023:** The system shall allow authorized users to create quotations for customers.
- **FR-024:** Quotations shall support separate cost items such as labor, parts, materials, and diagnostics.
- **FR-025:** The system shall allow authorized users to record whether a quotation was accepted or rejected.
- **FR-026:** The system shall preserve quotations associated with registered work orders.

## 6. Work Orders

- **FR-027:** The system shall allow authorized users to create work orders after the customer authorizes the repair.
- **FR-028:** Each work order shall be associated with a customer, vehicle, and quotation when applicable.
- **FR-029:** Authorized users shall be able to assign work orders to workshop employees.
- **FR-030:** The system shall allow authorized users to consult and update work order progress.
- **FR-031:** Work orders shall support the following statuses: pending, in progress, paused, completed, and delivered.
- **FR-032:** Authorized users shall be able to pause and resume a work order.
- **FR-033:** When pausing a work order, the user shall select a reason from a predefined list.
- **FR-034:** The system shall preserve the work order's status history.
- **FR-035:** The system shall allow authorized users to record relevant observations about a work order.
- **FR-036:** The system shall allow authorized users to register when a vehicle is delivered to the customer.

## 7. Employee and Activity Management

- **FR-037:** Only the owner and authorized administrators shall manage employee assignments through SAM.
- **FR-038:** Mechanics and assistants shall not require individual system accounts in the initial version.
- **FR-039:** Mechanics and assistants shall receive their assigned work orders through the workshop's traditional communication process.
- **FR-040:** Mechanics and assistants shall not create, edit, pause, or complete work orders directly in SAM.
- **FR-041:** Employee supervision and day-to-day activity control shall remain outside the system during the initial version.

## 8. Warranty Management

- **FR-042:** The system shall allow authorized users to register warranties associated with completed work.
- **FR-043:** Warranty records shall include the relevant work order and warranty conditions.
- **FR-044:** The system shall allow authorized users to consult active warranties.
- **FR-045:** Expired warranties shall no longer appear in the active warranty view, but their records shall remain available historically.

## 9. Financial Management

- **FR-046:** The system shall allow authorized users to register workshop income.
- **FR-047:** The system shall allow authorized users to register workshop expenses.
- **FR-048:** Financial records shall be associated with relevant work orders when applicable.
- **FR-049:** The system shall allow authorized users to consult income and expense records.
- **FR-050:** The system shall generate basic income and expense reports.
- **FR-051:** The system shall provide a basic overview of workshop expenses.
- **FR-052:** The system shall allow authorized users to consult the financial results of individual work orders when the required information is available.

## 10. Inventory Management

- **FR-053:** The system shall allow authorized users to register inventory items.
- **FR-054:** Inventory records shall include item name, description, quantity, and basic cost information.
- **FR-055:** The system shall allow authorized users to update inventory quantities.
- **FR-056:** The system shall allow users to search and consult inventory records.

## 11. Reports

- **FR-057:** The system shall generate basic operational reports about work orders.
- **FR-058:** The system shall generate basic financial reports about income and expenses.
- **FR-059:** The system shall allow authorized users to consult historical customer, vehicle, and work order information.

## 12. Out of Scope for the Initial Version

The following features are not included in the initial version:

- Direct mechanic and assistant access to SAM.
- Employee time tracking and payroll management.
- Advanced inventory management, including warehouse locations and stock automation.
- Tool and equipment tracking.
- Supplier management.
- Customer portal and direct customer access.
- Automated customer notifications.
- Real electronic invoicing or tax authority integrations.
- Workshop subscription and billing management.
- Advanced business analytics.
**End of Functional Requirements — Version 0.2**
