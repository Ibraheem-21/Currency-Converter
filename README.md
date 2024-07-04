# Currency Converter

## Overview

This is a simple Currency Converter program that uses the [Currency Converter API](https://www.currencyconverterapi.com/) to get the exchange rates and convert amounts from one currency to another. The program is written in Python and provides a command-line interface for users to interact with.

## Features

- List all available currencies with their symbols and names.
- Convert an amount from one currency to another.
- Get the exchange rate between two currencies.

## Requirements

- Python 3.x
- `requests` library

## Setup

1. Clone the repository:

```bash
git clone https://github.com/yourusername/currency-converter.git
cd currency-converter
```

2. Install the required dependencies:

```bash
pip install requests
```

3. Update the `API_KEY` with your own API key from [Currency Converter API](https://www.currencyconverterapi.com/):

```python
API_KEY = "your_api_key_here"
```

## Usage

Run the program:

```bash
python currency_converter.py
```

### Commands

- **list**: Lists all available currencies with their symbols and names.
- **convert**: Converts an amount from one currency to another.
  - Prompts for the base currency, the amount, and the target currency.
- **rate**: Gets the exchange rate between two currencies.
  - Prompts for the base currency and the target currency.
- **q**: Quits the program.

## Example

```plaintext
Welcome to the Currency Converter!
Enter list to see a list of different currencies
Enter convert to convert from one currency to another
Enter rate to get the exchange rate of two currencies

Enter a command (q to quit): list
AED - United Arab Emirates Dirham - د.إ
AFN - Afghan Afghani - ؋
...

Enter a command (q to quit): convert
Enter a base currency: USD
Enter an amount in USD: 100
Enter a currency to convert to: EUR
100 USD is equal to 84.23 EUR

Enter a command (q to quit): rate
Enter a base currency: USD
Enter a currency to convert to: EUR
USD -> EUR = 0.8423
```

## Code Explanation

### Imports and Initialization

```python
from requests import get
from pprint import PrettyPrinter

BASE_URL = "https://free.currconv.com"
API_KEY = "your_api_key_here"

printer = PrettyPrinter()
```

### Function Definitions

- **get_currencies**: Fetches the list of available currencies from the API.
- **print_currencies**: Prints the list of currencies in a readable format.
- **exchange_rate**: Fetches the exchange rate between two currencies from the API.
- **convert**: Converts an amount from one currency to another using the exchange rate.
- **main**: The main function that provides the command-line interface for the user.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## Author

- **Your Name** - [yourusername](https://github.com/yourusername)

Feel free to open an issue if you have any questions or suggestions.
