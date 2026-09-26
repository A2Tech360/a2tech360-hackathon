# IBM setup guide

<p align="right"><img src="../assets/ibm.png" width="160"><br><a href="https://ibm.biz/a2tech360">ibm.biz/a2tech360</a></p>

Start at **[ibm.biz/a2tech360](https://ibm.biz/a2tech360)**. That's IBM's hackathon site for this event: registration, education, tutorials, labs, team formation, and your team's IBM Cloud account.

Competing for **Best of IBM**? Use one or more of the tools below and say how in your Devpost write-up. None of them is required individually; use what serves your project.

The full IBM guide is here too: [A2Tech360 Hackathon Guide 2026 (PDF)](official/A2Tech360_Hackathon_Guide_2026.pdf).

## 1. Register and get your team's cloud account

1. Go to [ibm.biz/a2tech360](https://ibm.biz/a2tech360) and click **Register or sign in with IBMid**. Use an IBMid tied to your university or company email (or create one).
2. Form your team on the IBM site (see [Form your team](#form-your-team-on-the-ibm-platform) below).
3. Follow the **"Complete the hackathon"** page instructions to request a pre-configured IBM Cloud account for your team.
4. Every teammate gets an email from IBM Cloud. Click **Join now**, review your info, accept the Account notice, click **Join Account**, then **Continue** to authenticate.
5. You'll land on the IBM Cloud dashboard.

> **Already have a personal IBM Cloud account on the same email?** You might land in it. Switch to the hackathon account (`xxxxxxx – watsonx`) from the account dropdown at the top right.

**Submissions are due Sunday, Sept 27 at 12:00 PM.** When hacking opens, the **Complete the hackathon** page has step-by-step instructions for accounts, what to create, and how to submit on the IBM platform.

### Form your team on the IBM platform

Everyone on the team must be registered. Each person can be on only one team and submit one project. Teams can be **1–5 people**; solo is fine.

**Team Lead** (whoever creates the team is Lead and manages the submission):
1. **My Team → Create a Team.** Enter a name (4–64 characters). Optional: team image and "About your team."
2. Click **Create Team**.
3. Invite teammates: **Team Members** → enter their email → **Invite**, or **Invite Members** → search → **Invite**.
4. Need people? Use **Find Members (AI Assisted)** to describe your team and get matches.

**Joining a team:**
1. **My Team → Join a Team**, pick a team, click the **+** on an open spot, and send a short message to the Team Lead. Or use **Find a Team (AI Assisted)**.
2. Once the Lead accepts, you're on the team.

Leave any time with the red **Leave team** link. Plan to talk with your team outside the IBM site (Discord works).

### Education tab (learn fast)

- **Meet IBM Bob:** "Meet Bob: An AI-Powered IDE for Modern Software Development" (about 9 min) and "Tech Talk and Demo: Build with Bob" (about 21 min). IBM SkillsBuild: [skillsbuild.org/adult-learners](https://skillsbuild.org/adult-learners) · [Bob courses](https://skillsbuild.org/learning-catalog?q=Bob&topic=ai)
- **watsonx.ai:** overview (about 6 min) and Prompt Lab overview (about 3 min)
- **Agents:** Lab: Implement a ReAct Design Pattern with IBM Granite (guided project, about 30 min)
- **watsonx Orchestrate:** Get to know Orchestrate (about 6 min), Beginner's guide to multi-agent orchestration (about 7 min), AI agents for the enterprise (video, about 35 min), ADK guide for Python agents (about 1 hour, optional)

### IBM judging rubric (25 points)

| Criterion | Points | Ask yourself |
|---|---|---|
| Completeness and feasibility | 5 | Is the proof of concept complete, with IBM technology clearly applied? |
| Creativity and innovation | 5 | Is the approach original and differentiated? |
| Design and usability | 5 | Could real users adopt it quickly? |
| Effectiveness and efficiency | 5 | Does it address a real priority, measurably, with room to scale? |
| Michigan impact | 5 | Does it keep value, jobs, and opportunity in Michigan? |

Final score is the average of the judges' scores.

### Credits and limits

- Each provisioned account gets **$100 in credits** for watsonx.ai and Code Engine.
- Model inference: 1,000 tokens = 1 RU at $0.0001. Notebook runtimes: $1.02 per capacity unit hour.
- Email alerts at **25%, 50%, and 80%**. At **100%, the account is deactivated within an hour.**
- **Accounts are deactivated after the hackathon.** Export anything you want to keep (see the end of this page).
- Out of scope for this event: Agent Studio (Beta), deploying on IBM Cloud/watsonx.ai, bring your own model, fine-tuning, Cloud Object Storage.

## 2. IBM Bob (featured AI tool)

IBM's AI productivity assistant. Free trial: **40 Bobcoins for 30 days.**

1. Start the trial: https://bob.ibm.com/trial?utm_source=hack-michigan
2. Create or log in to your IBM account and verify your email with the 7-digit code.
3. Wait about 5 minutes for the confirmation email, then download Bob.
4. Track usage in the admin portal: https://bob.ibm.com/admin/

**Tips:** spend early Bobcoins validating your idea, coordinate who on your team is signed in so you don't double-spend on the same prompts, and save useful prompts and outputs locally.

## 3. watsonx.ai + IBM Granite

Foundation model studio with Prompt Lab and API/SDK access.

1. Log in at https://dataplatform.cloud.ibm.com/wx/home?context=wx with your IBM Cloud email.
2. Confirm the account is `xxxxxxx – watsonx` and the region is **Dallas**.
3. Click **Open Prompt Lab**. To switch models: AI Model dropdown → View all foundation models → search "granite".

**Programmatic access** (needed to call watsonx from Jac or Python):

1. On the watsonx.ai home page, scroll to **Developer access**.
2. Select **Project or space → watsonx Challenge Sandbox** to get your **project ID**.
3. Copy the **endpoint URL** (Dallas: `https://us-south.ml.cloud.ibm.com`).
4. Click **Create API key**, choose "Disable the leaked key", and store it securely. Never commit it to GitHub.
5. In Prompt Lab, the **View code** icon (top right) gives you cURL, Node.js, and Python snippets.

IAM token for raw API calls (valid about 60 minutes):

```bash
curl -X POST https://iam.cloud.ibm.com/identity/token \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -d "grant_type=urn:ibm:params:oauth:grant-type:apikey&apikey=$WATSONX_APIKEY"
```

Capabilities: [chat](https://www.ibm.com/watsonx/developer/capabilities/chat), [tool calling](https://www.ibm.com/watsonx/developer/capabilities/tool-calling), [text generation](https://www.ibm.com/watsonx/developer/capabilities/text-generation), [embeddings](https://www.ibm.com/watsonx/developer/capabilities/embeddings), [rerank](https://www.ibm.com/watsonx/developer/capabilities/text-rerank), [text extraction](https://www.ibm.com/watsonx/developer/capabilities/text-extraction), [time series](https://www.ibm.com/watsonx/developer/capabilities/time-series)

Samples: [AI stylist with Granite](https://www.ibm.com/think/tutorials/build-ai-stylist-with-granite-python-watsonx-ai) · [Agentic framework with CrewAI](https://developer.ibm.com/articles/build-an-agentic-framework-crewai/)

## 4. watsonx Orchestrate (agents)

Build, configure, and deploy AI agents and agentic workflows, with no code or with the Agent Development Kit (ADK).

**Open it:** IBM Cloud → Navigation menu → Resource list → AI / Machine Learning → **watsonx-Hackathon Orchestrate** → Launch watsonx Orchestrate.

Start here:
- [Develop agents with no code](https://developer.ibm.com/tutorials/develop-agents-no-code-watsonx-orchestrate/)
- [Agentic workflows with no code](https://developer.ibm.com/tutorials/agentic-workflows-watsonx-orchestrate-no-code/)
- [Getting started with the ADK](https://developer.ibm.com/tutorials/getting-started-with-watsonx-orchestrate/)
- [Connect MCP tools with the ADK](https://developer.ibm.com/tutorials/connect-mcp-tools-watsonx-orchestrate-adk/)
- [Multi-agent orchestration learning path](https://developer.ibm.com/learningpaths/watsonx-orchestrate-multiagent-orchestration/)
- [Embed agents in your web app](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agents-using-agent-in-embedded-chat)
- [Demos](https://www.ibm.com/products/watsonx-orchestrate/demos)

Out of scope: Build with AI (Preview).

## 5. Open source: Granite + BeeAI

Run Granite locally, no cloud account needed (32 GB RAM and a GPU recommended).

- [Granite on Hugging Face](https://huggingface.co/ibm-granite) · [Granite with Ollama](https://www.ibm.com/granite/docs/#run-locally-with-ollama)
- [Granite docs](https://www.ibm.com/granite/docs/) · [Cookbooks](https://www.ibm.com/granite/docs/use-cases/all-cookbooks/) · [Workshop](https://ibm.github.io/granite-workshop/)
- [BeeAI agent framework (Python)](https://github.com/i-am-bee/beeai-framework/tree/main/python) · [(TypeScript)](https://github.com/i-am-bee/beeai-framework/tree/main/typescript)

## 6. Cloudant (database)

Managed JSON document database (Lite plan: 1 GB, 20 reads/s, 10 writes/s).

- Open: Resource list → Databases → your Cloudant instance
- Credentials: Service credentials → New credential → copy URL and API key
- [Getting started](https://cloud.ibm.com/docs/Cloudant?topic=Cloudant-getting-started-with-cloudant) · [Python SDK](https://github.com/IBM/cloudant-python-sdk) · [Node SDK](https://github.com/IBM/cloudant-node-sdk) · [Query](https://cloud.ibm.com/docs/Cloudant?topic=Cloudant-query)

## 7. Code Engine (deploy)

Serverless containers, apps, jobs, and functions; it can build images straight from your source code.

- Open: Resource list → **watsonx-Hackathon Code Engine**
- [Deploy an app](https://cloud.ibm.com/docs/codeengine?topic=codeengine-deploy-app) · [Build from source](https://cloud.ibm.com/docs/codeengine?topic=codeengine-build-app-tutorial) · [CLI](https://cloud.ibm.com/docs/codeengine?topic=codeengine-cli) · [Samples](https://github.com/IBM/CodeEngine)

## Data rules

- Bring your own data, and make sure it's compliant.
- Public website data is OK if the terms allow commercial use. Keep a list of sources.
- **No** confidential data, client data, personal information, or data obtained from social media.

## Before you leave: export your work

IBM Cloud accounts are deactivated at the end of the hackathon.

- **Prompt Lab:** Save work → Save as → Prompt session.
- **Export a project:** project Overview → Export or import project → Export project → choose assets → remove sensitive info → Continue export.
- Commit everything else to your GitHub repo (without API keys).

Questions? Come to the **Local Impact sponsor workshop (IBM, Google, Baz) at 3:00 PM Saturday** or ask in [Discord](https://discord.gg/Av2JKhVyA) **#ask-an-organizer**.
