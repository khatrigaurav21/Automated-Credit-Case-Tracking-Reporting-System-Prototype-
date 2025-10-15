# HOWTO: Reproduce the Zapier + Google Sheets automation

## Prerequisites
- Zapier account
- Google account with Sheets access
- Copy of samples/sample-cases.csv

## Steps
1. Create a Google Sheet from samples/sample-cases.csv.
2. In Zapier, create a Zap:
   - Trigger: Google Sheets -> New or Updated Spreadsheet Row
   - Action: (optional) Filter/Formatter
   - Action: Email by Zapier or Slack -> Send Message
3. Test by adding a new row; verify the notification or summary email.

## Notes
- Keep column names stable to avoid Zap field mismatches.
- For weekly summaries, add a Schedule trigger and search/filter rows.

