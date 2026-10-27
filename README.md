# AI Acceleration for Cursor

AI Acceleration brings the business context you've saved in your AI Acceleration account into your chats, so drafts start from your business instead of a blank page.

Your Context Cards hold who you are, how you write, how you like to work, and the guardrails you've set. In your AI Acceleration portal, you choose which cards, roadmaps, and onboarding sessions this connection can use. Cards, roadmaps, and sessions you haven't selected stay private.

## What you can do

- Read the Context Cards you connected, so listing copy, client follow-ups, and updates use your voice.
- Continue the onboarding started in your account: review your audit, answer the three starting questions, bring reviewed context from your existing AI, and complete your business profile. Your exact corrections and sources stay with the same selected business. You confirm the final profile in your portal.
- Get your About Me, Brand Voice, and Working Style files as Markdown, compiled from the facts you've approved.
- Write a listing description from the confirmed facts in your saved private listing, then save it to your account as a new private draft. You review that exact saved version in your portal before you use it.
- If you have a published learning roadmap, see its modules and your saved work, work through a module's next step, and get your roadmap PDF when one is in your portal library.

## Who it's for

Real estate professionals with an AI Acceleration account.

## What it won't do

- It doesn't send email or texts, post to social media, change a CRM, or publish anything.
- It doesn't value property, run a CMA, pull MLS data, or read photos or web pages.
- It can't approve facts or drafts for you. You approve them in your portal.
- It reads only what you connected, for your own account. Disconnect it anytime in your AI Acceleration portal, and its next request is refused.

You're responsible for everything you publish. Check every fact and every Fair Housing question before a draft goes public.

## Set it up

1. Sign in to your AI Acceleration portal at [students.aiacceleration.ai](https://students.aiacceleration.ai).
2. Open **Context Cards → Connect your AI** and choose **Cursor**. Tick the exact cards and roadmaps it may read, then select **Save access**. Nothing is selected until you tick it.
3. Install **AI Acceleration** from the Cursor Marketplace.
4. In Cursor, open the MCP settings, find AI Acceleration, and sign in with the account you use in the portal. Allow access.
5. Ask: "List my connected Context Cards. Read my Brand Voice card and tell me when it was last saved."

Try these next:

- Use my Context Cards to write a follow-up to a buyer who toured a home yesterday.
- Write a listing description in my voice from these facts: 3 bed, 2 bath, new roof, fenced yard.
- Continue the real estate onboarding I started in my AI Acceleration account.

## Configuration

There are no API keys to set and no variables to fill in.

- **Server:** `https://mcp.aiacceleration.ai/mcp/context-cards` (streamable HTTP).
- **Sign-in:** OAuth 2.0 with PKCE through your AI Acceleration account. The client ID in `mcp.json` is a public client ID. It has no secret.
- **Scopes:** `context-cards:read`, `learning:read`, `onboarding:read` and `onboarding:write` for the tools; `openid` and `offline_access` so Cursor can stay signed in without asking again.

The `onboarding:write` scope only lets your AI save onboarding answers and private listing drafts as drafts for your review. It can't approve them.

## Disconnect

Open **Context Cards → Connect your AI** in the portal and select **Disconnect access**. Its next request is refused. You can also remove the plugin from Cursor at any time.

## What's in this repository

| Path | What it is |
| --- | --- |
| `.cursor-plugin/plugin.json` | Plugin manifest |
| `mcp.json` | The AI Acceleration MCP server and its sign-in settings |
| `skills/get-started/SKILL.md` | How your AI continues your real estate onboarding |
| `skills/use-my-context/SKILL.md` | How your AI drafts from your connected Context Cards |
| `assets/logo.png` | Plugin logo (512 x 512 PNG) |

The server runs on AI Acceleration's own infrastructure. This repository holds the plugin files only.

## Links

- Tool reference: [aiacceleration.ai/connect-your-ai/tools](https://aiacceleration.ai/connect-your-ai/tools)
- Privacy: [aiacceleration.ai/privacy#ai-connections](https://aiacceleration.ai/privacy#ai-connections)
- Terms: [aiacceleration.ai/terms](https://aiacceleration.ai/terms)
- Support: [aiacceleration.ai/contact](https://aiacceleration.ai/contact) or support@aiacceleration.ai

Published by Build Things That Build Things, LLC (doing business as AI Acceleration).

## License

The files in this repository are released under the [MIT License](LICENSE).
