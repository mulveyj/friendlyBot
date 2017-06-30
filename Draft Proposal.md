[InsertNameHere] is intended to be a bot-style mobile app for managing expenses, billing and notes, 
with an additional browser interface for account and data management. It is aimed at sole traders or small businesses.

Its key design principles are: 
•	a simple, message-style user interface similar to WhatsApp.
•	capability to interpret natural language.
•	highly flexible and user-configurable.
•	thin client using minimal resource in the device.
•	secure, encrypted data transfer, and authenticated login.
•	fast download and setup.

Some Basic Use Cases

Use Case 1 – Expense – access via phone app
1.	User enters “Spent £7.50 parking Manchester Piccadilly”.
2.	Server interprets input and writes to “Expenses” Collection or Table – username, amount, timestamp, description.
3.	Server renders acknowledgment to mobile app: ‘Recorded expense £7.50’.

Use Case 2 – Billing – access via phone app
1.	User enters “Bill Barclays £170 CPD course”.
2.	Server writes to “Billing” Collection or Table – username, amount, timestamp and description.
3.	Server renders acknowledgment to mobile app: ‘Recorded billing £170’.

Use Case 3 – Simple Note – access via phone app
1.	User enters “Renew newsletter sub, VAT return, make Joe’s tea”.
2.	Server writes to ‘Notes’ Collection or Table – username, timestamp, text.
3.	Server renders acknowledgment to app: “Note written to database”.

Use Case 4 – Query – access via browser
1.	User enters query data on form: ‘Expenses’, ‘From: 1/5/2017’, ‘To: 1/6/2017’.
2.	Tabulated result displayed on browser.
3.	User has option to export result to CSV.

Use Case 5 - Query - access via phone app
1. User enters natural language query: "expenses today?"
2. Server returns succint results message such as "3 items, £7.50 parking, £4.50 lunch, £6.20 stationery" or "Nothing found".

In addition, we envisage that the server will send messages to the mobile client after prolonged inactivity.
For example: "You have not entered any billing so far today. Do you need to?"

Priorities
We aim to introduce the functionality in order of priority: 
•	[Phase 1] single-user, simple note-taking capability (native app, html notes accessed via browser).
•	[Phase 1] simple expenses tracking (integration with native application based on MongoDB or SQL, exports CSV file for Excel or other spreadsheet).
•	[Phase 1] automated expense reports and mobile reminders.
•	[Phase 2] natural language processing.
•	[Phase 2] native timesheet app for recording work and billing.
•	[Phase 2] multi-users, authentication and security.

Potential extensions:
•	[Phase 3] option of integrating notes with EverNote.
•	[Phase 3] post items to Google Calendar as reminders.
•	[Phase 3] integration with Sage or Quickbooks.
•	[Phase 4] Photo recognition of receipts.

Technology
•	Mobile app front end: React Native, target operating system to be decided.
•	Browser front end: React.
•	Database holding user account data, Note objects, Expense objects, Billing objects, Mongo or SQL to be decided.
•	Integration with a 3rd party API for natural language processing, eg Google Natural Language, wit.ai, textrazor etc.
•	Node server, REST API, Express etc.

Team: Adie Williams, Emilia Ponomareva, Sally Newell, Joe Mulvey, Sina Kabki.
Visit our project management site: https://trello.com/b/uL7nJFkB/projectkim
