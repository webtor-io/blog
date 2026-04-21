---
name: whats-new
description: "Write a \"What's New\" blog post based on recent changes across webtor-io repos"
user-invocable: true
allowed-tools: Bash, Read, Write, Edit, Glob, Grep, WebFetch, Agent, AskUserQuestion
---

Write a new "What's New" blog post for the Webtor blog by researching recent changes across webtor-io GitHub repositories.

## Step 1: Find the last post date

Find the most recent post in the "What's new" series:

```bash
grep -rl 'series: "What'\''s new"' content/en/post/*/index.md | xargs grep '^date:' | sort -t: -k3 | tail -1
```

Extract the date — all repo research starts from this date.

## Step 2: Research changes

Fetch commits since the last post date from the key user-facing repos:

```bash
for repo in web-ui torrent-http-proxy torrent-web-seeder content-transcoder embed-sdk-js vault nginx-vod magnet2torrent srt2vtt video-info torrent-store rest-api chrome-ext content-enhancer image-transformer; do
  echo "=== $repo ==="
  gh api "repos/webtor-io/$repo/commits?since=<DATE>T00:00:00Z&per_page=30" \
    -q '.[] | "\(.sha[0:7]) \(.commit.message | split("\n")[0])"' 2>/dev/null
done
```

For repos with interesting changes, fetch full commit messages to understand details:

```bash
gh api "repos/webtor-io/<repo>/commits?since=<DATE>T00:00:00Z&per_page=30" \
  -q '.[] | "\(.sha[0:7]) \(.commit.message)"'
```

## Step 3: Identify user-facing themes

Group changes into themes that matter to regular users. Think from the user's perspective:
- What can they do now that they couldn't before?
- What works better now?
- What annoyance is gone?

**Ignore** purely internal refactors that don't change the user experience.

**Lead with the most exciting feature** — put the biggest user-facing change first in the post.

## Step 4: Show the user what you found

Before writing, present the list of themes you identified and ask the user:
- Is anything missing or inaccurate?
- Should the priority/ordering change?
- Any corrections about how features actually work?

**Do NOT write the post until the user confirms the plan.**

## Step 5: Write the post (EN + RU)

Create both language versions:
- `content/en/post/<slug>/index.md`
- `content/ru/post/<slug>/index.md`

### Frontmatter template

```yaml
---
title: "<title>"
date: <current datetime ISO 8601 +03:00>
slug: "<slug>"
series: "What's new"          # EN
series: "Что нового"          # RU
translationKey: "<slug>"
titleEmoji: "<relevant emoji>"
---
```

`translationKey` must be identical in both files.

### Tone of voice (from CLAUDE.md)

- **Simple language** — no jargon, no implementation details. Describe what changed for the user, not how it was built
- **Short and direct** — short sentences, no filler
- **Conversational** — like a friend sharing good news
- **Show the benefit** — "4K streams play smoothly now", not "increased buffer size from 256K to 4MB"
- **Use examples** — show what the user would actually type or see
- **No self-congratulation** — don't say "we're excited to announce"
- **Russian version reads naturally** — not a translation from English, uses native phrasing

### Structure

- Short intro (1 sentence summarizing the update)
- Feature sections (biggest first, H2 each)
- Optional "Improved Stability" section at the end for backend fixes — keep it brief and user-facing
- End with "Thanks for using Webtor. More coming soon." / "Спасибо, что пользуетесь Webtor. Скоро будет ещё."

## Step 6: Verify

Build Hugo and confirm no errors:

```bash
hugo --quiet
```

Start the dev server and show the user the links to preview:

```bash
hugo server &
```

Then provide EN and RU preview URLs.
