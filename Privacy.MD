# Crvvi Privacy Policy

_Last updated: May 4, 2026_

Crvvi is a meal-planning app that uses AI to generate weekly dinner plans and pre-build a grocery cart at your retailer.

## What we collect

When you use Crvvi we collect and store the following:

- **Account state.** A household profile that holds your saved meals, scheduled week, and store selection. No name or email is collected unless you sign in with a third-party identity provider (currently optional Sign in with Apple).
- **Plan inputs.** The constraints you type into the planner (meal count, dietary preferences, budget, dislikes, free-text notes).
- **Saved meals.** Recipes you save to your library and the linked grocery SKUs you've chosen.
- **Store selection.** The retailer location you've picked (e.g. a Kroger store ID).
- **Kroger account tokens** (only if you connect Kroger). We store an OAuth access token + refresh token so the app can push items into your authenticated Kroger cart on your behalf. Tokens are scoped to `cart.basic:write` and `profile.compact`.

We do **not** collect: location, contacts, advertising identifier, photos, or microphone data.

## How we use it

- **AI plan generation.** Your plan inputs and the titles of your saved meals (no email, no identity, no payment info) are sent to **Anthropic** (anthropic.com) so their Claude model can generate a meal plan. Anthropic retains the request per their API data-handling policy. We do not train models on your data.
- **Grocery resolution.** Ingredient names from generated plans are sent to **Kroger** to look up real Kroger SKUs at your selected store.
- **Cart push.** When you tap "Send to Kroger cart," we use your stored Kroger tokens to add items to your authenticated Kroger cart. We do not handle payment.

## Who we share data with

- **Anthropic** (AI provider) — plan inputs and saved-meal titles only.
- **Kroger** (retailer) — ingredient names and SKU IDs for resolution; OAuth-scoped cart writes when you push.
- **Supabase** (database hosting) — all persisted data.
- **Apple** — only if you choose Sign in with Apple. Apple receives an authentication challenge; we receive the resulting identity token.

We do not sell, rent, or share data with advertisers.

## Your rights

- **Access:** request a copy of the data tied to your household by emailing the address below.
- **Deletion:** delete your account and all associated data inside the app at **Settings → Delete Account**. This removes your household, saved meals, scheduled week, store selection, and Kroger tokens from our database immediately. If you used Sign in with Apple, we also revoke the Apple identity token.

## Children

Crvvi is not directed at children under 13. We do not knowingly collect data from children.

## Security

Data in transit is HTTPS/TLS. The database is hosted by Supabase with Row-Level Security and access scoped to the application's service role. Kroger OAuth tokens are encrypted at rest by Supabase.

## Contact

Questions about this policy or your data: ahaddad2545@gmail.com

## Changes

We'll update this page when policies change. The "last updated" date at the top tracks the most recent revision.
