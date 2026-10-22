# isys2001-finance-assistant
# Deekshi's Finance — Student Budget and Savings Assistant

## Project Overview

Deekshi's Finance is a Python-based student budgeting assistant designed to help students understand their spending habits. Users can upload a CSV file containing their transactions and ask questions about their spending. The application analyses spending by category and uses Google's Gemini API to provide budgeting advice.

## Features

- Upload transaction data using CSV files.
- Analyse spending by category.
- Process transaction data using pandas.
- Ask budgeting questions and receive AI-generated answers using Google's Gemini API.
- Use an interactive interface built with Gradio.
- Validate uploaded data and handle common errors.
- Access the API key securely through Google Colab Secrets.

## Technologies Used

- Python — main programming language.
- pandas — loading and processing CSV transaction data.
- requests — sending HTTP requests to the Gemini API.
- Google Gemini API — generating budgeting advice.
- Gradio — building the interactive user interface.
- Google Colab — developing and running the notebook.

## CSV File Format

The uploaded CSV must contain two columns: `category` and `amount`.

Example:

| category | amount |
|---|---:|
| Rent | 700 |
| Groceries | 250 |
| Transport | 100 |
| Groceries | 50 |
| Shopping | 150 |

Amounts must be valid, non-negative numbers, and every transaction must have a category.

## How to Run the Application

1. Open `ISYS2001_Finance_Assistant.ipynb` in Google Colab.
2. Make sure the required libraries are available.
3. Open the Secrets panel in Google Colab.
4. Add your Gemini API key as a secret named `GEMINI_API_KEY`.
5. Enable notebook access for the secret.
6. Run the notebook cells in order.
7. Run the Gradio application cell.
8. Upload a CSV file containing transaction data.
9. Enter a budgeting question and submit it to receive a response.


## Testing

The project includes basic calculations and spending analysis using sample transaction data. Assertion-based tests should be run to check that calculations produce the expected results.

Additional tests should cover invalid amounts, missing CSV columns, missing categories and other invalid inputs.

## Limitations

- The current sample data contains spending categories and amounts but does not automatically provide the user's income.
- Remaining income and savings-goal progress are not fully integrated into the current combined interface.
- Budgeting advice depends on the accuracy of the uploaded transaction data.
- Gemini responses may vary and should not be treated as professional financial advice.

## Future Improvements

- Add income and savings-goal inputs.
- Calculate remaining income and savings progress.
- Add charts to visualise spending patterns.
- Improve chat history and follow-up questions.
- Expand automated testing and input validation.
