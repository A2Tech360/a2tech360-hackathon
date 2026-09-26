# Baz AI code review

[Baz](https://baz.co) is an AI code reviewer, and it's **installed on the [A2Tech360 GitHub org](https://github.com/A2Tech360)** for this hackathon. Every pull request opened in an org repo gets an automatic review: likely bugs, risky changes, and suggestions, right in the PR.

Baz is part of the **Local Impact track** build requirements, and every team can use it.

## Set up (2 minutes)

Baz is **already installed** on the A2Tech360 org. No invite or setup needed: it starts reviewing as soon as your project repo exists.

1. **Create your team repo in the org.** New repository → Owner: **A2Tech360** → name it after your project → **Public** (Devpost requires a public repo). Add your teammates as collaborators.
2. **Open pull requests** as you build (see below).

> Already started a repo under your own account? You can [transfer it](https://docs.github.com/en/repositories/creating-and-managing-repositories/transferring-a-repository) to the A2Tech360 org, or ask for help in [Discord](https://discord.gg/Av2JKhVyA) **#ask-an-organizer**.

## Work in pull requests

```bash
git checkout -b feature/walker-recommendations
# ...build...
git add . && git commit -m "Add recommendation walker"
git push -u origin feature/walker-recommendations
```

Then open a pull request into `main`. Baz reviews it automatically.

- **Read the comments, fix what matters, push again.** Baz re-reviews new commits.
- **Keep PRs small.** One feature or fix per PR gets you faster, sharper reviews.
- **Merge often.** Don't let branches drift overnight; `main` should always be demo-able.
- **Reply to Baz** in the PR thread if a suggestion doesn't fit; you're in charge.

## Why this helps you win

- Fewer demo-breaking bugs at 11:59 AM Sunday.
- A clean, timestamped commit and PR history. Judges check that code was written during hacking hours.
- Better code quality counts toward **technical execution** in judging.

## Resources

- Baz docs: https://docs.baz.co
- Baz on GitHub Marketplace: https://github.com/marketplace/baz-review
- Questions: **#ask-an-organizer** on [Discord](https://discord.gg/Av2JKhVyA)
