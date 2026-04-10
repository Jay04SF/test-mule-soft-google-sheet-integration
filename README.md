# RnD Mulesoft Google Sheets

[medium artical for mulesoft to google sheet](https://medium.com/another-integration-blog/mulesoft-google-sheets-connector-acb698840102)

## google cloud doc
[google cloud apis and google enterprise api](https://docs.cloud.google.com/apis/docs/overview)

# limitation 

[google sheet](https://developers.google.com/workspace/sheets/api/limits)
[google drive](https://developers.google.com/workspace/drive/api/guides/limits)

# Google workspace
[google workspace docs](https://developers.google.com/workspace/guides/get-started)

# OAuth app created in google console.
- app name : test-mulesoft-google-sheet
- Created credentials with user data.

# [OAuth playground](https://developers.google.com/oauthplayground)

# OAuth scope details in google workspace.
[auth scope page link](https://developers.google.com/workspace/sheets/api/scopes)

# OAuth details
```
{
    "web": {
        "client_id": "624446005192-enr9mj1ht13jt9q22v0s2chfipli9sli.apps.googleusercontent.com",
        "project_id": "silent-hook-492909-v3",
        "auth_uri": "https://accounts.google.com/o/oauth2/auth",
        "token_uri": "https://oauth2.googleapis.com/token",
        "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
        "client_secret": "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",
        "redirect_uris": [
            "http://localhost:8081/api/google-sheets/oauth/callback"
        ],
        "javascript_origins": [
            "http://localhost:8081"
        ]
    }
}

```
# OAuth related doc 
[oAuth 2.0 doc for 4 to 5 weeks](https://support.google.com/cloud/answer/13463073?visit_id=639114100168951219-3706451065&rd=1)

# Email disscussion
```
Hi Jake and Ahmed,
As we are finalizing the solution, I wanted to document the current process based on my understanding. Could you please review the
steps below and add or correct anything I may have missed?
The goal is to ensure we are fully aligned before we move forward.
Step 1 — Deal Closure and Data Entry (Jake)
Jake closes the restaurant deal and fills out the onboarding fulfillment Google Sheet with all required vendor details such as location,
partner ID, contact information, hours, go-live date, and tax rate.
The same information is then manually re-entered into Salesforce on the Lead record.
At this stage, the data is entered twice — once in Google Sheets and once in Salesforce — and the sheet is emailed to Ahmed and
the operations team.
Step 2 — Welcome Email (Ahmed)
Ahmed prepares and schedules the welcome email using a template.
For each location, he updates the vendor owner’s name, removes non-applicable brands, duplicates and updates the menu/pricing
Google Sheet, and includes the new link in the email.
The email is typically scheduled for delivery at 1 PM EST.
Step 3 — Otter Submission (Ahmed)
Ahmed completes the Otter Google Form with partner and restaurant details, brand information, and creates a new vendor email ID.
The data flows into the Mothership sheet.
He then validates the entry in the Mothership and manually retrieves Brand Record IDs from Salesforce to populate the sheet before
finalizing submission.
Step 4 — DoorDash Tracker (Ahmed)
Ahmed updates the DoorDash tracker with location, brand, address, hours, menu link, business IDs, and bank details.
DoorDash populates store UUIDs in the sheet within 1–2 days. Ahmed typically waits 24–48 hours before using them due to possible
changes.
Step 5 — Uber Eats Tracker (Ahmed)
Ahmed updates the Uber Eats tracker with concept details, address, hours, courier instructions, tags, and partner ID.
Uber processes submissions weekly and returns UUIDs by the following Tuesday.
Step 6 — GrubHub Submission (Ahmed)
Ahmed fills out GrubHub’s Excel template with store and brand details, including a sequential store number he maintains.
He uploads the file via JotForm along with submission details.
GrubHub returns the file via email with store IDs populated. This process is fully manual and does not support Canadian locations.
Step 7 — Training Invite (Ahmed)
Ahmed creates a 1-hour Google Calendar invite using the go-live date and onboarding details, and includes all relevant stakeholders
and the vendor.
Step 8 — Salesforce Updates (Ahmed)
Once IDs are received from DoorDash, Uber Eats, and GrubHub, Ahmed manually updates the vendor Account record in Salesforce
with all platform IDs.
Please review and let me know if this accurately reflects your current process or if there are any additions or corrections needed.
Thanks,
Priya
```
