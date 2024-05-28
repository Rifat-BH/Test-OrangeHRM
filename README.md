# Test Plan for OrangeHRM Admin Module
## Objectives
Verify that the Add, Edit, and Delete functionalities in the Admin module work as intended. <br/>
Ensure that user management actions perform correctly and data integrity is maintained.<br/>
Identify and fix any bugs related to these functionalities.<br/>
## Test Environment
Operating System: Windows 11. <br/>
Browser: Chrome <br/>
OrangeHRM Version: 5.2.1<br/>
## Test Cases
Feature: Add Admin User <br/>
#### Test Case 1.1: Add New Admin User
Preconditions: Admin user is logged in.<br/>
Steps:<br/>
Navigate to the Admin module.<br/>
Click on "User Management" -> "Users".<br/>
Click on the "Add" button.<br/>
Fill in the required details (e.g., Employee Name, Username, Password, User Role as Admin).<br/>
Click "Save".<br/>
Expected Result: New admin user is added and listed under the Users section.<br/>

#### Test Case 1.2: Validation for Required Fields<br/>
Preconditions: Admin user is logged in.<br/>
Steps:<br/>
Navigate to the Add User form.<br/>
Leave required fields (e.g., Username, Password) blank.<br/>
Click "Save".<br/>
Expected Result: Appropriate validation messages are displayed, and the user is not added.<br/>
Feature: Edit Admin User<br/>

#### Test Case 2.1: Edit Existing Admin User<br/>
Preconditions: Admin user is logged in, and at least one admin user exists.<br/>
Steps:<br/>
Navigate to the Admin module.<br/>
Click on "User Management" -> "Users".<br/>
Select an existing admin user from the list.<br/>
Click "Edit".<br/>
Modify the necessary details (e.g., change the Username).<br/>
Click "Save".<br/>
Expected Result: The admin user's details are updated and reflected in the Users list.<br/>

#### Test Case 2.2: Edit with Invalid Data<br/>
Preconditions: Admin user is logged in, and at least one admin user exists.<br/>
Steps:<br/>
Navigate to the Edit User form.<br/>
Modify the Username to an invalid format or duplicate existing username.<br/>
Click "Save".<br/>
Expected Result: Appropriate validation messages are displayed, and the user's details are not updated.<br/>
Feature: Delete Admin User<br/>

#### Test Case 3.1: Delete Admin User<br/>
Preconditions: Admin user is logged in, and at least one admin user exists.<br/>
Steps:<br/>
Navigate to the Admin module.<br/>
Click on "User Management" -> "Users".<br/>
Select an existing admin user from the list.<br/>
Click "Delete".<br/>
Confirm the deletion.<br/>
Expected Result: The selected admin user is removed from the list.<br/>

#### Test Case 3.2: Attempt to Delete a User with Dependencies<br/>
Preconditions: Admin user is logged in, and at least one admin user exists with dependent records.<br/>
Steps:<br/>
Navigate to the Admin module.<br/>
Click on "User Management" -> "Users".<br/>
Select an admin user with dependent records (e.g., assigned roles or projects).<br/>
Click "Delete".<br/>
Confirm the deletion.<br/>
Expected Result: The user should not be deleted, and an appropriate message indicating existing dependencies should be displayed.<br/>

## Testing Tools<br/>
Jmeter for Performance testing. <br/>
Manual testing for UI verification and user interaction.<br/>

## Reporting Issues<br/>
If you encounter any issues, please report them via the OrangeHRM issue tracker.<br/>

## Conclusion<br/>
This test plan ensures that the Add, Edit, and Delete functionalities in the OrangeHRM Admin module are thoroughly tested. Following these test cases will help maintain data integrity and ensure a seamless user management experience.<br/>
