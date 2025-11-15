## User Registration System
A Java Swing application that demonstrates the implementation of the Chain of Responsibility design pattern for user input validation. 
The system provides a graphical user interface (GUI) for registering users and validates multiple fields such as username, password, email, and phone number.

## Description
This project simulates a user registration system for an application, where user credentials are validated before registration is completed. 
It uses the Chain of Responsibility pattern to separate validation logic into multiple classes, each responsible for a single type of validation. 
This allows flexible, modular, and maintainable code.
- Chain of Responsibility Pattern: Each validator checks one specific field (username, password, email, or phone number) and passes the validation along the chain if the field is valid.
- Java Swing GUI: Provides an interactive form for users to input registration data. Displays validation results or errors in real-time.

## Features
- Input fields for Username, Password, Email, and Phone Number.
- Validation rules:
       - Username: At least 5 characters long.
       - Password: Minimum 8 characters with at least one uppercase letter, one lowercase letter, and one digit.
       - Email: Must follow standard email format.
       - Phone Number: Exactly 10 digits.
- Displays success message on valid registration.
- Shows error messages via dialog boxes for invalid inputs.
- Modular validators that can be extended or reordered easily.

## Structure
- UserRegistrationUI: Creates the Swing GUI and handles form submission. Initiates the validation chain.
- UserRegistration: Represents the user's registration data.
- Validator (Interface): Defines the structure for validators in the chain.
- UsernameValidator, PasswordValidator, EmailValidator, PhoneNumberValidator: Implements validation logic for each field.
- ValidationException: Custom exception thrown when validation fails.

