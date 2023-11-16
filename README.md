# Telegram Credit Card Scraper

## Introduction

This Python script utilizes the Telethon library to extract credit card information from messages in multiple Telegram groups. It monitors incoming messages in specified groups, identifies credit card details, and logs the information.

## Disclaimer

**Disclaimer:** This script is intended for educational and demonstrative purposes only. Unauthorized extraction of credit card information is illegal and unethical. Use this script responsibly and only on data for which you have explicit authorization. The author and OpenAI disclaim any responsibility for misuse or consequences resulting from the use of this script.

## Requirements

- Python 3.6 or higher
- Telethon library (`pip install telethon`)

## Configuration

Before running the script, replace the placeholder values with your own Telegram API credentials.

```python
# Replace these values with your own
api_id = 'your_api_id'
api_hash = 'your_api_hash'
```

### Getting Telegram API Credentials

1. Visit [Telegram's website](https://my.telegram.org/auth) and log in.
2. Create a new application to obtain the `api_id` and `api_hash`.

## Credit Card Extraction

The script uses regular expressions to search for credit card information in incoming messages. It identifies the credit card number, expiry month, expiry year, and CVV. Extracted information is displayed and written to a file (`cc.txt`).

### Extracted Information

- **cc_number**: Credit card number.
- **expiry_month**: Expiry month of the credit card.
- **expiry_year**: Expiry year of the credit card.
- **cvv**: CVV (Card Verification Value) of the credit card.

## Telegram Client Setup

The script connects to the Telegram servers using the Telethon library, requiring user authorization to access specified groups.

### Running the Script

1. Install the required libraries: `pip install telethon`.
2. Replace `your_api_id` and `your_api_hash` with your actual Telegram API credentials.
3. Replace the placeholder group IDs in the `group_entities` list with the actual IDs of the Telegram groups to monitor.
4. Run the script.

```bash
python script_name.py
```

### Authorization

If the user is not authorized, the script will prompt for the phone number and verification code.

## Output

Extracted credit card information is displayed on the console and appended to the `cc.txt` file in the following format:

```plaintext
credit_card_number|expiry_month|expiry_year|cvv
```

## Conclusion

This script is a demonstration of credit card information extraction from Telegram messages. Adhere to legal and ethical guidelines when using such tools. The script is provided as-is, and the user is responsible for any consequences resulting from its usage.

---
