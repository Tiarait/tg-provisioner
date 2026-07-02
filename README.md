# tg-provisioner
> Idea. What if creating a Telegram group was as easy as running a single command?
> The goal is to make Telegram group provisioning effortless.

The goal is to combine a **userbot** (MTProto) with a regular **Telegram bot** to automate tasks that normally require manual work.

The envisioned workflow:
- create one or multiple Telegram groups
- apply predefined templates
  - name
  - avatar
  - description
  - permissions
  - pinned messages
- invite users or predefined teams
- invite the future owner
- transfer group ownership
- optionally leave the bot in the group for ongoing management

The userbot performs operations unavailable through the Bot API (such as creating groups and transferring ownership), while the bot handles configuration and future administration.

## Examples

- Client onboarding. Every new client gets a dedicated Telegram group. With a single command, a new group is created, configured from a template, your team is invited automatically.
- Communities at scale. Launch dozens or hundreds of Telegram communities with identical settings, branding, permissions, and moderation rules.
- Courses & cohorts. Every new course, batch, or cohort gets its own preconfigured discussion group with instructors, moderators, and students invited automatically.
- Internal teams. Automatically create project or department groups from templates whenever a new project starts.
- Events. Generate dedicated Telegram groups for conferences, hackathons, webinars, or workshops, complete with branding and moderators.

## Planned tech stack

- Python, FastAPI, async
- Telethon (MTProto / userbot), aiogram (Bot API)
- HTMX + Jinja2 (Web)
- SQLite (initially), PostgreSQL support later or MySQL


> The Telegram Bot API cannot create groups or transfer ownership. Those operations require MTProto, which is why this project combines a userbot with a regular bot.

## Why?

Setting up Telegram groups is surprisingly repetitive. Creating a group, configuring it, inviting members, assigning ownership, and repeating the same steps over and over doesn't scale.

This project aims to make Telegram group provisioning as simple as deploying infrastructure.

## Status

Currently just an idea.

If there's enough interest from the community, I'll build it.

