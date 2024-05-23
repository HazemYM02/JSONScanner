
# JASON Scanner

## Overview
The `JASONScanner` is a Python class designed to tokenize a given text into specific categories based on pre-defined regular expressions. This scanner is particularly useful for identifying components such as numbers, identifiers, operators, and various types of brackets and symbols in a programming or configuration language.

## Features
- **Tokenization:** Converts strings into a series of tokens based on type, such as numbers, identifiers, and operators.
- **Customizable Token Specification:** Easily modifiable regular expressions to fit different or additional token types.
- **Error Handling:** Provides basic error handling for unrecognized characters.

## Usage
To use the `JASONScanner`, follow these steps:
1. **Instantiate the Scanner with Text:**
   Create an instance of `JASONScanner` by passing the string you want to tokenize.
2. **Tokenize the Text:**
   Call the `tokenize()` method to process the text. The method returns a list of tokens.

## Example
Here's a simple example to demonstrate how to use the `JASONScanner`:

```python
# Sample code to tokenize
code = """
Integer x;
Set x = 1;
"""

# Instantiate the scanner with the provided code
scanner = JASONScanner(code)

# Tokenize the code and print the tokens
tokens = scanner.tokenize()
print(tokens)
```

## Token Definition
Tokens are defined in the scanner using regular expressions. Here is the list of token types and their corresponding patterns:

- **Num:** Matches integers and decimal numbers.
- **Identifier:** Matches identifiers that start with a letter or underscore, followed by any word character.
- **OP:** Matches arithmetic and assignment operators.
- **OpenBrace, ClosedBrace:** Matches open `{` and close `}` braces.
- **OpenBracket, ClosedBracket:** Matches open `(` and close `)` brackets.
- **Semicolon:** Matches semicolons `;`.
- **Space:** Matches spaces and tabs. (Note: These are currently not skipped in the token output)
- **NewLine:** Matches newline characters. (Note: These are currently not skipped in the token output)
- **Other:** Matches any other character.

## Contributing
Contributions to improve the functionality or extend the types of tokens that can be recognized are welcome.
