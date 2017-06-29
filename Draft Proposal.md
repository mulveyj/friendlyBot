[InsertNameHere] is intended to be a bot-style iPhone app for managing expenses, billing and notes, 
with an additional browser interface for account and data management. It is aimed at sole traders, partnerships or 
small businesses with fewer than 10 employees. 

Its key design principles are: 
•	a simple message-style user interface similar to WhatsApp.
•	capability to interpret natural language.
•	highly flexible and user-configurable.
•	thin client using minimal resource in the device.
•	secure, encrypted data transfer.
•	fast download and setup.

Some Basic Use Cases

Use Case 1 – Expense – access via phone app
1.	User enters “Spent £7.50 parking Manchester Piccadilly”.
2.	POST text to server.
3.	Handler routes to natural language API.
4.	Parsed return flags keyword “spent” and money amount £7.50, routes to ‘expense’ handler.
5.	Server writes to “Expenses” Collection or Table – username, amount, timestamp, description.
6.	Server renders acknowledgment to app: ‘Recorded expense £7.50’.

Use Case 2 – Billing – access via phone app
1.	User enters “Bill Barclays £170 CPD course”.
2.	POST text to server.
3.	Handler routes to natural language API.
4.	Parsed return flags keyword “Bill”, and amount, routes to ‘billing’ handler.
5.	Server writes to “Billing” Collection or Table – username, amount, timestamp and description.
6.	Server renders acknowledgment to app: ‘Recorded billing £170’.

Use Case 3 – Simple Note – access via phone app
1.	User enters “Renew newsletter sub, VAT return, make Joe’s tea”
2.	POST text to server.
3.	Handler routes to natural language API.
4.	Parsed return contains no keywords indicating expense or billing, default handler is ‘note’.
5.	Server writes to ‘Notes’ Collection or Table – username, timestamp, text.
6.	Server renders acknowledgment to app: “Note written to database”.

Use Case 4 – Query – access via browser
1.	User enters query data on form: ‘Expenses’, ‘From: 1/5/2017’, ‘To: 1/6/2017’.
2.	GET request to server.
3.	Handler queries DB, returns result to browser.
4.	Option to export result to CSV.

Priorities
We aim to introduce the functionality in order of priority: 
•	[Phase 1] simple note-taking capability (native app, html notes accessed via browser).
•	[Phase 1] simple expenses tracking (integration with native application based on MongoDB or SQL, exports CSV file for Excel or other spreadsheet).
•	[Phase 1] automated expense reports.
•	[Phase 2] natural language processing.
•	[Phase 2] native timesheet app for recording work and billing.
•	[Phase 2] authentication and security.

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
•	Node server, REST API.
