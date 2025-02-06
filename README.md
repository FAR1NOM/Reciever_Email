First code (no real email connection)
This variant doesn't connect
to a real email server, but uses stubs (placeholders) to simulate operation.

🔸 Highlights:
✔ Interface on Tkinter: email and password fields, Connect, Scan Messages buttons, list of messages, text field for attachments.
✔ Connect - just shows "Connected to email server" message, but doesn't do actual authorization.
✔ Scan Messages - adds fake messages (Message 1, 2, 3) to the list.
✔ Download and Open - shows message ID when double-clicking on an email (but does not download it).
✔ Mark as Read - allows you to mark an e-mail as read (changes background color in the list).

📌 Conclusion:
This code only imitates an email client, but does not interact with real mail.

🔹 Second code (with connection to email via IMAP)
This variant connects to the mail server via IMAP and receives real emails.

🔸 Highlights:
✔ EmailClient (class to work with IMAP)

Connects to the mail server (imap.gmail.com, IMAP4 SSL).
Authorizes with login and password (you need to replace YOUR_EMAIL, YOUR_PASSWORD).
Retrieves list of last 10 emails (fetch_topics).
Fetches attachments (fetch_attachments).
Downloads a specific file (download).
✔ AppBackendUI (GUI)

Works the same way as in the first code, but now interacts with EmailClient.
Scan Messages retrieves actual email subjects.
Download and Open allows you to download attachments from emails.
