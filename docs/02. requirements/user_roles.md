# SAM — User Roles and Permissions

**Document:** User Roles and Permissions  
**Version:** 0.1  
**Status:** Draft

## 1. Purpose

This document defines the user roles within SAM and establishes their responsibilities and access permissions.

The goal is to ensure that only authorized personnel can manage workshop information and operations through the system.

## 2. User Roles

SAM will initially support two user roles:

### 2.1 Owner

The Owner is the person who owns the workshop and has full control over its SAM account.

**Responsibilities:**
- Manage workshop information and configuration.
- Create, edit, deactivate, and manage administrator accounts.
- Access and manage customer and vehicle records.
- Manage diagnostics, quotations, and work orders.
- Assign work orders to mechanics and assistants.
- Manage employee information.
- Manage inventory records.
- Access financial records, income, expenses, and reports.
- Access all system information and administrative functions.

**Access level:** Full access.

### 2.2 Administrator

The Administrator is authorized by the Owner to manage the workshop through SAM.

**Responsibilities:**
- Manage customer and vehicle records.
- Register diagnostic results and generate reports.
- Create and manage quotations.
- Create, update, and monitor work orders.
- Assign work orders to mechanics and assistants.
- Manage employee information.
- Register and update inventory.
- Record income and expenses.
- Consult operational and financial reports.

**Access level:** Administrative access to workshop operations.

The Owner retains ultimate control over the workshop account and administrator management.

## 3. Employees Without System Accounts

Mechanics and assistants will not have individual accounts or direct access to SAM.

Their work will be managed through traditional workshop procedures.

**Responsibilities:**
- Receive work orders and instructions from the Owner or Administrator.
- Perform assigned mechanical tasks.
- Report progress, delays, or issues to the person responsible for managing the work order.

The Owner or Administrator will be responsible for updating work order information in SAM.

## 4. Permission Principles

SAM will follow these principles:

- Only the Owner and authorized Administrators can access the system.
- Employees without system accounts cannot modify workshop records.
- Administrative actions must be performed by an authorized user.
- The Owner maintains full control over the workshop account.
- Workshop information must remain isolated from other workshops using SAM.

## 5. Future Considerations

The permission system may be expanded in future versions to support:

- More granular administrator permissions.
- Different administrative access levels.
- Employee accounts with limited access.
- Employee activity tracking through the system.

These features are not part of the initial scope unless explicitly added to the project requirements.

--- 
** End of User Roles and Permissions Version 0.1**