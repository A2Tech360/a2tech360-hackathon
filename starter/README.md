# Jac + Jaseci resources

Everything you need to start building with Jac, collected from the [JacHacks A2Tech hacker guide](https://jachacks.org/a2tech-guide) and the official Jac docs. No prior Jac experience needed.

> **The one hard rule:** at least **40% of your code must be Jac**.

## From the JacHacks team

| Resource | What it's for | Link |
|---|---|---|
| **JacHacks A2Tech hacker guide** | Tracks, rules, submissions, packing list | [jachacks.org/a2tech-guide](https://jachacks.org/a2tech-guide) |
| **Jac workshop** | Zero to shipping on Jac, all levels welcome. Led by Jayanaka. | **Saturday 2:00–3:00 PM** |
| **Jac language docs** | Docs, tutorials, and everything you need to go from zero to shipping in Jac | [jaclang.org](https://jaclang.org) |
| **Jac-GPT** | An AI assistant that actually knows Jac | [jac-gpt.jaseci.org](https://jac-gpt.jaseci.org) |
| **Jaseci Discord Q&A bot** | Drop any Jac question in **#ninjaclaw-yap-room** and the bot answers | [discord.com/invite/6j3QNdtcN6](https://discord.com/invite/6j3QNdtcN6) |
| **JacHacks Discord** | Announcements, team matching, mentors. Ask in **#ask-an-organizer**. | [discord.gg/Av2JKhVyA](https://discord.gg/Av2JKhVyA) |
| **JacHammer** | Host your project so judges can try it (free "sandbox" tier) | [jachammer.ai](https://jachammer.ai) |
| **Star the Jac repo** | Required for your Devpost submission | [github.com/jaseci-labs/jac](https://github.com/jaseci-labs/jac) |
| **Jaseci source code** | The open-source Jaseci repo | [github.com/jaseci-labs/jaseci](https://github.com/jaseci-labs/jaseci) |
| **Jaseci** | Project home | [jaseci.org](https://jaseci.org) |
| **Devpost resources** | Links posted on the JacHacks Devpost | [jachacks-a2tech.devpost.com/resources](https://jachacks-a2tech.devpost.com/resources) |

## Quick start (from the official Jac docs)

These commands come from [docs.jaseci.org](https://docs.jaseci.org). Jac moves fast, so if anything differs, the docs and Jac-GPT win.

**Install** ([install guide](https://docs.jaseci.org/quick-guide/install/)):

```bash
curl -fsSL https://raw.githubusercontent.com/jaseci-labs/jaseci/main/scripts/install.sh | bash
```

Docker alternative: `docker pull jaseci/jaclang`. VS Code and Open VSX extensions are available.

**Hello world:** save as `hello.jac`, then run `jac hello.jac`.

```jac
with entry {
    print("Hello from Jac!");
}
```

**Full-stack app:** scaffold with `jac create example --kind web-app`, then serve locally with `jac start` (http://localhost:8000).

**AI functions with byLLM** ([AI quickstart](https://docs.jaseci.org/tutorials/ai/quickstart/)):

```jac
def translate2french(text: str) -> str by llm();
sem translate2french = "Translate the given text to French";

with entry {
    result = translate2french("Hello, how are you?");
    print(result);
}
```

Set your model provider's API key as an environment variable (for example `GOOGLE_API_KEY`), and pick a model with `import from byllm.lib { Model }` and `glob llm = Model(model_name="...")`, or in `jac.toml`. Never commit API keys.

## Learn more

- [Jac tour](https://docs.jaseci.org/quick-guide/): nodes, edges, walkers, and graph-based programming
- [AI guide](https://docs.jaseci.org/tutorials/ai/quickstart/): `by llm()`, model selection, and testing with mocks

## Using IBM and Google with Jac

- **IBM:** see [docs/ibm-setup.md](../docs/ibm-setup.md) for watsonx.ai (IBM Granite models via API), watsonx Orchestrate, IBM Bob, Cloudant, and Code Engine.
- **Google:** see [docs/google-cloud-credits.md](../docs/google-cloud-credits.md) to claim your credits for Gemini on Vertex AI and other Google Cloud services.
- **Baz:** create your project repo in the A2Tech360 GitHub org and open pull requests; Baz reviews them automatically. See [docs/baz-code-review.md](../docs/baz-code-review.md).
