# internship-task4-serverless-cost-calculator
A simple Serverless Cost Calculator built using AWS Lambda and Python. The function accepts two numbers as input and returns their sum using serverless computing.
# Project 4 – The Serverless Logic

## Overview
This project demonstrates a simple Serverless Cost Calculator using AWS Lambda and Python.  
The function performs addition of two numbers without managing any server infrastructure.

The project shows how serverless computing helps reduce cost by running code only when triggered.

---

## Objective
- Create a serverless function using AWS Lambda
- Accept two numbers as input
- Return the sum as output
- Test the function using Lambda test events

---

## Tools & Technologies
- AWS Lambda
- Python 3.12
- JSON

---

## Lambda Function Code

```python
import json

def lambda_handler(event, context):

    num1 = event['num1']
    num2 = event['num2']

    result = num1 + num2

    return {
        'statusCode': 200,
        'body': json.dumps({
            'sum': result
        })
    }
