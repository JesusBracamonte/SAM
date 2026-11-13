# SAM — User Flows

**Document:** User Flows  
**Version:** 0.1  
**Status:** In Progress

This document describes the main workflows within SAM, including user actions, system responses, alternative paths, and possible errors.

The purpose is to define how the system should behave before starting implementation.

---

# 1. Authentication and Workshop Access

## 1.1 Overview

SAM uses a single account per workshop in its initial release.

The account belongs to the workshop rather than to an individual person. The workshop owner is registered as the responsible person, while the account credentials are shared by authorized workshop personnel, such as the owner and receptionist.

Individual user profiles and permissions are planned for future releases.

## 1.2 Workshop Registration

### Required Information

**Workshop Information**
- Workshop name.
- Owner's full name.
- Business address.
- Workshop phone number.
- Workshop contact email.
- Workshop specialization.

**Account Credentials**
- Username or login email.
- Password.
- Password confirmation.

### Main Flow

1. The user opens the SAM registration page.
2. The user enters the workshop information.
3. The user enters the account credentials.
4. The system validates all required fields.
5. The system checks whether the username or login email is already registered.
6. The system checks whether the workshop is already registered.
7. If all validations pass, the system securely processes the password.
8. The system creates the workshop account and stores the associated workshop information.
9. The system confirms successful registration.
10. The system redirects the user to the login page.

### Alternative Flows and Errors

- **Missing information:** The system identifies incomplete required fields and requests corrections.
- **Invalid information:** The system displays validation messages.
- **Duplicate credentials:** The system prevents registration if the username or login email is already associated with an account.
- **Duplicate workshop:** The system prevents registration if the workshop is identified as already registered.
- **Password mismatch:** The system requests matching passwords.
- **Registration failure:** The system displays an error and does not create an incomplete account.

## 1.3 Login

### Main Flow

1. The user opens the SAM login page.
2. The user enters the workshop username or login email.
3. The user enters the account password.
4. The system validates the credentials.
5. The system establishes an authenticated session.
6. The system redirects the user to the workshop dashboard.

### Alternative Flows and Errors

- **Incorrect credentials:** The system displays an authentication error.
- **Empty fields:** The system requests the missing information.
- **Inactive or disabled account:** The system denies access and displays an appropriate message.
- **Authentication service failure:** The system informs the user that login is temporarily unavailable.

## 1.4 Workshop Access

After successful authentication:

1. The system identifies the workshop associated with the account.
2. The system loads the workshop information.
3. The system displays the workshop dashboard.
4. The user can access the available administrative modules.

All workshop records must remain associated with their corresponding workshop account.

## 1.5 Logout

### Main Flow

1. The user selects the logout option.
2. The system terminates the authenticated session.
3. The system redirects the user to the login page.
4. The user must authenticate again to access the workshop dashboard.

## 1.6 Initial Release Limitations

The initial release will use the following access model:

- One account per workshop.
- One set of login credentials per workshop.
- Shared credentials for the owner and receptionist.
- No individual employee accounts.
- No profile selection.
- No individual user permissions.

Future releases may introduce multiple profiles within a workshop account, allowing individual access, roles, and permissions.

---

# 2. Customer Management

## 2.1 Overview

The Customer Management module allows the workshop administration to register, search, consult, and update customer information.

Each customer record must be associated with the workshop account.

A customer may own or bring multiple vehicles to the workshop. Therefore, customer information must be stored independently from vehicle information.

## 2.2 Customer Registration

### Main Flow

1. The administrator opens the Customer Management module.
2. The administrator selects the option to register a new customer.
3. The system displays the customer registration form.
4. The administrator enters the customer's information.
5. The system validates the required fields.
6. The system checks for possible existing customer records.
7. If no duplicate is identified, the system saves the customer record.
8. The system confirms successful registration.

### Alternative Flows and Errors

- **Missing information:** The system identifies incomplete required fields.
- **Invalid information:** The system displays validation messages.
- **Possible duplicate customer:** The system warns the administrator if a similar customer record already exists.
- **Registration failure:** The system displays an error and does not save an incomplete record.

## 2.3 Customer Search and Consultation

### Main Flow

1. The administrator opens the Customer Management module.
2. The administrator enters a search term, such as the customer's name or phone number.
3. The system searches the workshop's customer records.
4. The system displays matching results.
5. The administrator selects a customer.
6. The system displays the customer's information and associated vehicle records.
7. The administrator can access the customer's service history.

### Alternative Flows

- **No matching results:** The system informs the administrator that no customers were found.
- **Incomplete search:** The system allows the administrator to modify the search criteria.

## 2.4 Customer Information Update

### Main Flow

1. The administrator searches for and selects a customer.
2. The administrator selects the option to edit customer information.
3. The system displays the existing customer information.
4. The administrator modifies the necessary fields.
5. The system validates the changes.
6. The system saves the updated information.
7. The system confirms successful modification.

### Alternative Flows and Errors

- **Invalid information:** The system requests corrections.
- **Update failure:** The system informs the administrator that the changes could not be saved.

## 2.5 Customer History

The system must allow the administrator to consult the customer's historical information, including:

- Associated vehicles.
- Previous work orders.
- Diagnostic and repair history.
- Quotations and service records.

Historical records must remain available even if the customer's contact information is updated.

## 2.6 Initial Release Limitations

The initial release will focus on:

- Customer registration.
- Customer search.
- Customer information consultation and updates.
- Association between customers and vehicles.
- Access to historical service records.

Customer-facing accounts and portals are not included in the initial release.

---

**Document status:** Flows 1 and 2 documented. Pending 9 flows.

**Next flow:** Vehicle Management.