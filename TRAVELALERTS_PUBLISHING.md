# Travel Alerts.ke Publishing Runbook

Apply whenever asked to publish or share an approved Travel Alerts.ke post. Read alongside CHATGPT.md and TRAVELALERTS_RESEARCH.md; the editorial approval gate and no-paid-calls-without-authorization rule remain in force.

1. Reuse approved copy and the exact existing flyer from the conversation or connected media library. Do not redo research or artwork for a publishing-only request.
2. Check connected publishing identities and existing publication history before asking for account details. Known X identity: @travelalertss. Known Telegram publishing bot: @Africanalertbot; destination channel: @TravelAlertsKe. Verify live identity and destination permissions before posting. These are identifiers, not secret credentials.
3. Check limits, credits, permissions, image compatibility, and duplicate history. A quota failure is not a disconnected account. Do not upgrade or spend credits without authorization.
4. Before publishing or scheduling on any platform, obtain explicit editor approval of the exact text, intended platform and destination account or channel. For a post with an attachment, reuse the approved asset. Follow any further tool-specific confirmation requirement. Research and draft review alone do not authorize release.
5. For Telegram, use the verified channel username directly; do not ask again simply because recent-chat discovery is empty. Telegram bot update discovery is not a channel roster.
6. Use idempotency keys when available; verify each published message ID or URL. Report separately for every platform: published with link, blocked with precise reason, or not attempted.
7. If one connector is blocked, inspect already-connected alternatives before asking the user to reconnect, but do not bypass payment or platform authorization.
8. Keep the final status concise. Never claim a post is live without platform confirmation. Never expose API keys or tokens.

## X via Buffer

Use ChatGPT → Composio → Buffer → **@travelalertss**. The route was tested successfully on 16 November 2026. Recheck the connection on each run.

1. For an approved X post, **first discover Composio's Buffer actions**; do not default to direct X/Twitter, Hermoso, SocialClaw or Metricool merely because those connectors are visible. A missing direct Composio X connection does **not** imply Buffer's X channel is unavailable.
2. Check Buffer's current active connection with `BUFFER_GET_ACCOUNT_CONTEXT`. Select the **connected, unlocked Twitter/X channel named travelalertss** by the channel ID returned **in that run**; never assume an old channel ID is still valid.
3. Check recent `BUFFER_LIST_POSTS` for that channel and compare the proposed story/text against already sent or scheduled posts to prevent duplication. Apply the editorial story-level deduplication gate as well.
4. Require explicit editor approval of the exact text and intended account before public publishing. Respect existing_only spending; check and seek approval for any new paid usage, upgrades or limits. Do not assume approval of research authorizes publication.
5. On approval, use Composio's `BUFFER_PUBLISH_POSTS` with the verified `channel_ids`, `text` and `delivery_mode: "share_now"`. Do not schedule or cross-post unless separately approved.
6. Inspect the actual tool response: report **published** only if the intended channel returns `status: "sent"` (and no relevant failure); otherwise report queued, failed or uncertain accurately. Save or reference the post ID, timestamp and platform when available; never invent an X permalink.
7. If Buffer is disconnected, locked, unavailable or fails, explain the specific blocker. Only then consider another publishing provider after checking its connection, costs and limits. Hermoso's Free plan hit its monthly publishing limit on 16 November 2026, so it is not the default fallback; recheck current status before any future use.

## Spending

Use existing access at KES 0 by default. Obtain specific approval before any new paid usage.

Current operational note (17 Nov 2026): Hermoso Telegram posting was blocked by the free-plan monthly post limit despite a working bot connection. Recheck the limit at each attempt; this is not a permanent account state.
