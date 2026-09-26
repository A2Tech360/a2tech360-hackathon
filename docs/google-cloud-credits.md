# Claim your Google Cloud credits

Every hacker can claim **$25 in Google Cloud credits**, courtesy of the Google Developer Groups North America team (250 vouchers).

> ⚠️ **Claim them during the event.** Vouchers expire when the event ends and can't be saved for later. Budget 10–15 minutes.
>
> ⚠️ **Not compatible with Google AI Studio billing.** Use the credits on Google Cloud services, such as Gemini on Vertex AI.

**You'll need:** a personal `@gmail.com` account (not a school or work account) and your phone for verification.

## Step 1: Join the Google Group

You must be a member of the group before you can claim.

- Group email: `a2tech360-hackathon@googlegroups.com`
- Join here: **https://groups.google.com/g/a2tech360-hackathon**

<img src="../assets/google-group.png" width="160"><br>https://groups.google.com/g/a2tech360-hackathon

## Step 2: Claim your credits

Open **https://g.dev/credits/a2tech360-hackathon-2** (the **CLAIM** button appears once the event starts).

<img src="../assets/google-credits.png" width="160"><br>https://g.dev/credits/a2tech360-hackathon-2

1. **Scan the QR code** or open the link above.
2. **Sign in and join the Google Developer Program.** Use your personal Gmail account.
3. **Claim your badge and verify.** Complete the mobile verification step.
4. **Wait for billing.** Give it 2–5 minutes while your billing account is created.
5. **Open a new browser window** signed in with the same `@gmail.com` account.
6. **Create a new Google Cloud project** at [console.cloud.google.com](https://console.cloud.google.com/projectcreate).
7. **Confirm the project uses the credits billing account** (Billing → Account management).

📺 Video walkthrough: https://www.youtube.com/watch?v=noshGMsPzEg
📄 One-pager: [google-how-to-claim-event-credits.pdf](../assets/google-how-to-claim-event-credits.pdf)

## Troubleshooting

| Error | Fix |
|---|---|
| **CRED-101** Workspace account error | Switch your browser login to a personal `@gmail.com` account. A private or incognito window helps. |
| **CRED-103** Verification issues | Refresh the page, retry the security challenge, or switch your phone to mobile data. |
| No CLAIM button | Make sure you joined the Google Group with the same Gmail account, then refresh. |
| Anything else | Ask in **#ask-an-organizer** on Discord or find an organizer. |

## Using the credits with your project

- **Gemini on Vertex AI:** enable the Vertex AI API in your project, then authenticate locally with `gcloud auth application-default login`.
- **Deploy:** Cloud Run is a quick way to host an API or web app.
- **Data:** Firestore or Cloud SQL for app state.
- **Watch your spend:** $25 goes a long way at hackathon scale, but set a [budget alert](https://console.cloud.google.com/billing/budgets) and shut down anything you're not using.

Competing for **Best of Google**? Make sure your Devpost write-up says which Google services you used and how.
