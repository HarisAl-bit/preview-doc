# ✉️ Send Email – Volantis Pipeline

## Overview  
The **Send Email** action allows you to automatically send an email when your pipeline conditions are met. This is useful for sending alerts, reports, or any data-driven communication.

With **Send Email**, you can:  
- Send custom messages to one or multiple recipients.  
- Include dynamic data in your email body using `@field`.  
- Set trigger conditions to control when emails are sent.  
- Preview email output before sending.  
- Test-send emails manually.

---

## Configuration

![Send Email Configuration](/vdata/documentation/pipeline/action/action-config.webp)

| Section     | Property     | Description                                                                 | Example                  |
|-------------|--------------|-----------------------------------------------------------------------------|--------------------------|
| **Recipient** | Send To       | Enter one or more email addresses. Press `Enter` after each to add.         | `haris@volantis.io`      |
| **Message**   | Subject       | Subject line of the email.                                                  | `halo pak`               |
|               | Body          | Email message. You can use dynamic data fields with `@field`.               | `ini income bulanan kita @value` |
| **Trigger**   | Condition     | Set a logical condition to trigger the email. If left blank, it always sends. | `value >= 900000000`     |

---

## Preview and Test Send

![Send Email Configuration](/vdata/documentation/pipeline/action/action-preview.webp)

You can **preview** your email before activating the pipeline. This helps verify your setup before going live.

### What Happens in Preview/Test Mode:
- Email will be sent with subject prefixed by `[PREVIEW]`.
- All dynamic fields like `@value` will be replaced with sample data.
- The email will only be sent to the configured address(es) as a test.
