# InvoiceProcessingBot

A UiPath bot that automates invoice data entry by extracting data (e.g., Invoice Number, Amount) from PDF invoices and submitting it to a Google Form.

## Purpose
This bot saves IT teams 2–5 hours/month on manual data entry by automating the process of extracting invoice data from PDFs and submitting it to a Google Form for record-keeping.

## Requirements
- UiPath Studio (Community Edition or higher) to open and run the project.
- A paid UiPath license (e.g., Pro or Enterprise) is required for commercial production use.
- A PDF invoice file (e.g., test.pdf) for input.
- A Google Form URL to submit the extracted data (configured in Main.xaml).

## Setup Instructions
1. Clone or download this repository from GitHub.
2. Open UiPath Studio and load the project from the `InvoiceProcessingBot` folder.
3. Update the Google Form URL in `Main.xaml`:
   - Open `Main.xaml`, locate the "Use Application/Browser" activity, and set the URL to your Google Form (e.g., https://docs.google.com/forms/d/e/yourform).
4. Place a test PDF invoice (e.g., test.pdf) in the project folder.
5. Run the bot in UiPath Studio to process the PDF and submit the data.

## Usage
- The bot extracts key fields (Invoice Number, Amount) from the PDF using UiPath’s “Read PDF Text” activity.
- It submits the data to a Google Form using browser automation.
- Check the Google Form responses to verify the submission (e.g., Invoice Number: INV123, Amount: $5,000).

## Limitations
- Currently supports PDFs with a specific layout (e.g., Invoice Number and Amount in fixed positions). Update the extraction logic in `Main.xaml` for different PDF formats.
- Requires manual updates to the Google Form URL if the form changes.

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/baconj/RPA/blob/main/LICENSE) file in the main repository for details.
