# Veriphone MCP Server

## Overview

Veriphone is a phone number verification service that enables you to parse, format, and validate phone numbers globally. The server provides accurate, fast, and reliable validation for phone numbers across all countries and regions.

### Key Features

- **Global Phone Number Validation:** Instantly determine if a phone number is valid, with support for all countries.
- **Number Formatting:** Convert valid phone numbers to standard international or local formats.
- **Automatic Country Detection:** Automatically sets a default country based on the requester's IP address.
- **Carrier and Region Identification:** Detect a phone number's type (e.g., mobile, landline) and carrier, wherever available.

## Tools Provided

### 1. Verify

- **Description:** This tool performs global phone number verification.
- **Parameters:**
  - **default_country**: The default country in a 2-letter ISO format (e.g., US, RU). Optional; if not provided, the country is inferred from the phone number prefix or the requestor’s IP address.
  - **phone**: The phone number to verify.

### 2. Example

- **Description:** This tool returns an example phone number for any specified country and phone type.
- **Parameters:**
  - **country_code**: The example number's country in a 2-letter ISO format (e.g., US, RU). Optional; if absent or invalid, the country is inferred from the requestor’s IP address.
  - **type**: The type of example number to return. Options include fixed_line, mobile, premium_rate, shared_cost, toll_free, and voip. Defaults to mobile if not specified.

## How It Works

Veriphone is built on a REST-based architecture, using JSON for data interchange. It provides a set of stateless endpoints that can be called via standard HTTP requests. The server responds with HTTP responses containing JSON payloads, detailing the validation results or example phone numbers.

### Authentication

Veriphone requires authentication to ensure secure access to its services. Ensure proper authentication of requests by following standard authentication protocols.

### Error Handling

Veriphone uses standard HTTP status codes to indicate request outcomes:

- **200**: Success
- **400**: Bad request due to missing required parameters
- **401**: Unauthorized request
- **403**: Forbidden, possibly due to exceeding usage quotas or overdue payments
- **500**: Internal server error, indicating an issue on the server side

## Conclusion

The Veriphone MCP server is an essential tool for developers and learners who need efficient and reliable phone number validation services. It offers comprehensive tools to validate, format, and retrieve example phone numbers for global use, making it an invaluable asset for web development and telecommunications applications.