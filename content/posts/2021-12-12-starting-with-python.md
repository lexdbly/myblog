---
title: "Send SMTP Email With Python"
date: 2020-12-12
tags:
    - python
    - smtplib
    - email
categories:
    - tech
keywords:
    - python
    - smtplib
    - send email
draft: false
---

```python
import smtplib
from email.mime.text import MIMEText
from email.mime.multipart import MIMEMultipart
from email.mime.base import MIMEBase
from email import encoders
import os.path

email = '<youremail>' #your email address to be used for SMTP service
password = '<yourpassword>' #your password
data = [
    {
        "to": "<recipientemail>", 
        "subject": "Test Subject 1",
        "message": "First recipient will receive this message",
        "attachments": [
            {"file_location": "somefile.pdf"},
            {"file_location": "someotherfile.pdf"},
            ],
    },
    {
        "to": "<recipientemail2>",
        "subject": "Test Subject 2",
        "message": "Second recipient will receive a different message",
        "attachments": [
            {"file_location": "adifferentfile.pdf"},
            {"file_location": "someinvoices.pdf"},
            ],
    }
]

# Connect and login to the email server
server = smtplib.SMTP('smtp.gmail.com', 587) #modify if email provider is different than gmail
server.starttls()
server.login(email, password)

# Loop over each email to send to
for each in range(len(data)):
    # Setup MIMEMultipart for each email address (if we don't do this, the emails will concatenate on each email sent)
    msg = MIMEMultipart()
    msg['From'] = email
    msg['To'] = data[each]['to']
    msg['Subject'] = data[each]['subject']
    message = data[each]['message']

    # Attach the message to the MIMEMultipart object
    msg.attach(MIMEText(message, 'plain'))
    # Attach the attachment file
    for attachment in range(len(data[each]['attachments'])):
        # Create the attachment file
        file_location = data[each]['attachments'][attachment]['file_location']
        filename = os.path.basename(file_location)
        fileitem = open(file_location, "rb")
        part = MIMEBase('application', 'octet-stream')
        part.set_payload(fileitem.read())
        encoders.encode_base64(part)
        part.add_header('Content-Disposition', f"attachment; filename= {filename}")
        msg.attach(part)

    # Send the email to this specific email address
    server.sendmail(email, data[each]['to'], msg.as_string()) 

# Quit the email server when everything is done
server.quit()
```