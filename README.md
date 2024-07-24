# Replace Special Characters With Dashes

This Salesforce Apex utility class provides functionality to sanitize input text by replacing special characters with dashes, except for hyphens which are retained. The class is designed to be used in Salesforce processes where such text manipulations are needed, especially in formatting fields for consistent data entry or storage.

## Features

- **Invocable Method**: The class includes a Salesforce invocable method, allowing it to be called from Salesforce Flow, Process Builder, or API. This method, `replaceSpecialChars`, takes a list of request objects, each containing `inputText`, and returns each with `outputText` where special characters are replaced by dashes.
- **Handling of Various Inputs**: The method can handle strings with alphanumeric characters, special characters, and even null or empty strings effectively.

## Usage

To use this method in a Salesforce process, you need to pass a list of request objects to `replaceSpecialChars`. Each request object should have an `inputText` attribute that you want to sanitize.

## Apex Test Class

The accompanying test class, `ReplaceSpecialCharactersWithDashesTest`, provides comprehensive test coverage for this utility class:
- **Test Cases**: It includes tests for strings with various characters, including alphanumeric, special characters, mixed cases, and null or empty strings.
- **Assertions**: Each test verifies that the output is as expected, ensuring that only special characters are replaced by dashes and that null or empty inputs are handled gracefully.

## Example Test Scenarios

1. **Standard Input**: Verifies that strings like "Hello, World!" are converted to "Hello--World-".
2. **Alphanumeric Only**: Confirms that strings like "1234567890" remain unchanged.
3. **Mixed Special Characters**: Checks that strings with various non-hyphen special characters are sanitized properly.
4. **Empty String**: Ensures that an empty input returns an empty response.
5. **Null Input Handling**: Tests that a null input results in a null output.

This utility and its tests ensure robust text handling in your Salesforce applications, enhancing data integrity and usability across your platform.
