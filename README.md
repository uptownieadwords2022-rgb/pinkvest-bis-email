# Uptownie — "Back In Stock" Email

A complete, production-ready responsive HTML email for the **Pure Linen Waistcoat + Skirt Set** restock campaign.

**File:** [`uptownie-linen-coord-restock.html`](./uptownie-linen-coord-restock.html)

---

## The concept

Not a generic "back in stock" blast. The whole email is built around one feeling:

> *the outfit everyone was waiting for is finally back — and probably won't stay back for long.*

Voice: witty, playful, confident — your fashionable best friend texting you. Built for Indian women aged 20–35.

### Psychological flow
1. **Pattern interrupt** — "You asked. Then asked again."
2. **FOMO** — it sold out fast, the waitlist grew, you're seeing it first
3. **Product desire** — emotional benefits, not fabric specs
4. **Why everyone loves it** — scannable icon rows
5. **Social proof** — realistic, screenshot-worthy customer quotes
6. **Tasteful urgency** — "sold out before some people even opened the email"
7. **CTA** — primary + a dark, high-contrast secondary close

---

## Merge variables

Replace these before (or at) send. Klaviyo/Shopify will resolve them automatically if the names match your data.

| Variable | Purpose | Required |
|---|---|---|
| `{{first_name}}` | Personal greeting in the FOMO block | ✅ |
| `{{product_url}}` | Destination for **every** CTA + clickable image (used 6×) | ✅ |
| `{{hero_image}}` | Top hero image | ✅ |
| `{{product_image}}` | Mid-email lifestyle/detail image | ✅ |
| `{{logo}}` | Brand logo (header + footer) | ✅ |
| `{{instagram_url}}` `{{tiktok_url}}` `{{website_url}}` | Footer social links | optional |
| `{{company_address}}` | Legal sender address (CAN-SPAM / compliance) | recommended |
| `{{unsubscribe_url}}` `{{preferences_url}}` | Footer compliance links | ✅ for sending |

> In **Klaviyo** the conventions are usually `{{ first_name }}`, `{% unsubscribe %}`, etc. In **Shopify Email** they're `{{ customer.first_name }}` and the built-in unsubscribe link. Do a quick find/replace to match your platform's exact syntax.

### Recommended image sizes
- **Hero:** 1200 × 1500 px (2× of 600 × 750), JPG/PNG, < 200 KB
- **Product:** 1200 × 900 px (2× of 600 × 450)
- **Logo:** 300 px wide transparent PNG (renders at 150 px)

Every image already has descriptive **ALT text** and a styled fallback, so the email still reads well with images off.

---

## Design

- Mobile-first, **600 px** max width, fluid down to small screens
- Luxury-minimal aesthetic, generous white space, pill (rounded) buttons
- Serif display type (Georgia) + clean sans body (Helvetica/Arial) — web-safe, no external fonts
- Palette: background `#F8F6F2` · text `#222222` · accent `#B89B72` · button `#222222` / text `#FFFFFF`

## Technical

- Table-based layout, **all styling inline** (the only `<style>` block holds media queries + client resets, which cannot be inlined)
- No external CSS or web-font files
- Bulletproof VML buttons for Outlook (desktop) + standard anchor buttons elsewhere
- Hidden preheader with spacer so inbox preview text doesn't leak body copy
- ~24 KB — safely under Gmail's 102 KB clipping limit
- Tested patterns for **Gmail, Apple Mail, Outlook, Yahoo, Klaviyo, Shopify Email**

---

## Before you send — checklist
- [ ] Swap in real `{{product_url}}`, image URLs, and logo
- [ ] Confirm merge-tag syntax matches your ESP (Klaviyo vs Shopify)
- [ ] Set a subject line (suggestions below) + confirm the preheader
- [ ] Send a seed test to Gmail + Apple Mail + Outlook before the real send

### Subject line ideas
- It's back. You're early. 🤍
- The co-ord you kept stalking? Restocked.
- You asked. Repeatedly.
- Don't say we didn't warn you (it's back)
