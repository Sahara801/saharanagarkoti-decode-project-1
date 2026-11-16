# Project 1: Zero-Shot & Few-Shot Data Extraction

## 1. Overview

This project focuses on extracting structured information from unstructured customer complaint emails using Prompt Engineering.

The objective is to design a prompt that instructs an AI model to identify specific details from an email and return them in a valid JSON format.

## 2. Objectives

- Extract relevant information from customer emails.
- Use clear delimiters to separate instructions from input data.
- Apply few-shot prompting using input/output examples.
- Generate structured JSON responses.
- Handle missing information using `null` values.

## 3. Prompting Techniques Used

- **Clear Instructions:** Defined the AI's role as a data extraction engine.
- **Delimiter Usage:** Used `###` to separate the email content from the instructions.
- **Few-Shot Prompting:** Included two input/output examples to demonstrate the expected response format.
- **Structured Output:** Required plain-text JSON without additional explanations.
- **Missing Value Handling:** Instructed the model to return `null` when information is unavailable.

## 4. Information Extracted

The prompt extracts the following fields:

| Field | Description |
|---|---|
| `customer_name` | Name of the customer |
| `order_number` | Customer's order number |
| `complaint_type` | Category of the complaint |
| `severity_level` | Complaint severity from 1 to 5 |
| `contact_phone` | Customer's contact number or null |

## 5. Project Structure

```text
Project-1/
│
├── README.md
├── prompt.txt
│
├── examples/
│   └── test-email-01.txt
│
├── outputs/
│   └── test-output-01.json
│
└── screenshots/
    └── Decode-project1.png
```

## 6. Example Input

```text
Subject: WORST SERVICE EVER

Hi, I'm Anita Gurung. I was charged twice for order C5590 and nobody has replied in 5 days. Unacceptable. Fix it today or I'm disputing with my bank. - Anita
```

## 7. Expected JSON Output

```json
{
  "customer_name": "Anita Gurung",
  "order_number": "C5590",
  "complaint_type": "billing",
  "severity_level": 4,
  "contact_phone": null
}
```

*Note: The output above is an expected example. The actual output should match the response generated when testing the prompt.*

## 8. Screenshot

![DecodeLabs Project 1](screenshots/Decode-project1.png)

## 9. Conclusion

This project demonstrates how clear instructions, delimiters, and few-shot examples can guide an AI model to extract structured information from customer complaint emails.

It also provides practical experience in designing prompts for consistent JSON output and handling missing information.

## 10. Skills Practiced

- Prompt Engineering
- Zero-Shot and Few-Shot Prompting
- Data Extraction
- Delimiter Usage
- JSON Formatting
- Structured Output Generation
