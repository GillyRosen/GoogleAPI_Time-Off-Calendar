# Google Sheets to Calendar Shift Scheduler

This Google Apps Script automatically creates calendar events for shifts listed in a Google Sheet. It helps automate the process of scheduling "Out of office" time based on approved requests.

## How it Works

The script reads shift data (start time, end time, employee name, etc.) from a Google Sheet. It then checks an associated Google Calendar for existing events. If an event for a shift doesn't exist, the script creates a new calendar event with the appropriate details.

## Instructions

1. **Copy the code:** Copy the provided `scheduleShifts()` function into your Google Apps Script editor.
2. **Update Sheet Name:** Change `"FormResponses"` in the script to the actual name of your sheet containing the shift data.
3. **Set Calendar ID:** Replace `"YOUR_CALENDAR_ID"` with the ID of your Google Calendar.
4. **Adjust Data Range:** Update the `getRange()` function accordingly.
5. **Customize Event Title:** Modify the `title` variable if you want a different format for your calendar event titles.
6. **Run the script:**  In the Apps Script editor, click the "Run" button (you might need to authorize the script).

## Spreadsheet Format

The script expects the shift data in your Google Sheet to be organized in columns. Make sure the following information is included in the specified columns:

* **Column C:** Start time of the shift
* **Column D:** End time of the shift
* **Column E:** Employee name (or other identifier used in the event title)
* **Column I:** Request number
* **Column J:** Approval status (must be "Complete" for the script to create an event)

You can adjust the column numbers in the script if your data is organized differently.

## Notes

* The script skips creating events for shifts that already exist in the calendar.
* The script assumes the approval status is in a column where "Complete" indicates an approved shift.
* Make sure the Google Calendar you use has the correct time zone settings.
* You can uodate the code using ChatGPT giving your data (ranges and description of the table, etc).
