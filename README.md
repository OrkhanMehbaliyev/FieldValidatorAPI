# Practising Delegates in C#

FieldValidatorAPI is a C# library designed to provide common validation functions for form fields. It includes various delegate-based validation methods to ensure the integrity of user inputs, such as required field validation, string length validation, date format validation, pattern matching, and field comparison.

## Features

- **Required Field Validation**: Checks if a field is not empty.
- **String Length Validation**: Ensures a string falls within a specified length range.
- **Date Validation**: Validates whether a string represents a valid date.
- **Pattern Matching**: Uses regex to verify if a string matches a specified pattern.
- **Field Comparison**: Compares two field values for equality.

## Usage

To use the validation functions, reference `CommonFieldValidatorFunctions` and call the required delegate.

### Example Usage

```csharp
using System;
using FieldValidatorAPI;

class Program
{
    static void Main()
    {
        // Required field validation
        bool isRequiredValid = CommonFieldValidatorFunctions.RequiredFieldValidDel("Hello");
        Console.WriteLine($"Required Valid: {isRequiredValid}");

        // String length validation
        bool isLengthValid = CommonFieldValidatorFunctions.StringFieldLengthValidDel("Hello", 3, 10);
        Console.WriteLine($"String Length Valid: {isLengthValid}");

        // Date validation
        DateTime validDate;
        bool isDateValid = CommonFieldValidatorFunctions.DateFieldValidDel("2025-01-31", out validDate);
        Console.WriteLine($"Date Valid: {isDateValid}, Parsed Date: {validDate}");

        // Pattern matching validation
        bool isPatternValid = CommonFieldValidatorFunctions.FieldPatternValidDel("test@example.com", "^[^@\s]+@[^@\s]+\.[^@\s]+$");
        Console.WriteLine($"Pattern Match Valid: {isPatternValid}");

        // Field comparison validation
        bool isFieldsEqual = CommonFieldValidatorFunctions.FieldsComparisonValidDel("password123", "password123");
        Console.WriteLine($"Fields Comparison Valid: {isFieldsEqual}");
    }
}
```

## Installation

1. Clone the repository or download the `FieldValidatorAPI.cs` file.
2. Include it in your C# project.
3. Use the `CommonFieldValidatorFunctions` class to perform validation.



