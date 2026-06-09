<div align="center">

<img src="https://zingocards.com/__l5e/assets-v1/e3d247a8-8924-4079-8518-5aafd03c4087/zingo-social-logo.png" alt="ZingoCards" width="220" />

# ZingoCards

### Anonymous Visa cards. No KYC. Funded with crypto. Issued in minutes.

[![Website](https://img.shields.io/badge/Website-zingocards.com-0EA5E9?style=for-the-badge)](https://zingocards.com)
[![API](https://img.shields.io/badge/API-v1-22C55E?style=for-the-badge)](https://zingocards.com/api-docs)
[![Support](https://img.shields.io/badge/Email-support%40zingocards.com-F59E0B?style=for-the-badge)](mailto:support@zingocards.com)

<br />

<img src="https://zingocards.com/__l5e/assets-v1/c9af5a97-238c-488c-9ed9-6df0e7b39a88/zingo-youtube-thumbnail.png" alt="ZingoCards preview" width="780" />

</div>

---

## Why ZingoCards

- **No KYC** — no ID, no selfie, no address. Just an email.
- **Crypto‑funded** — pay in BTC, ETH, SOL, USDC, USDT, BNB, XMR.
- **Visa accepted worldwide** — works anywhere Visa works, online and in‑store.
- **Instant request** — issued from **5 minutes**, up to 25h for the final stamp.
- **Flat $10 fee** — top up `$X`, get `$X − 10` spendable on the card.
- **2 active cards** per account. Burn anytime.

<br />

<div align="center">
  <img src="https://zingocards.com/__l5e/assets-v1/c9af5a97-238c-488c-9ed9-6df0e7b39a88/zingo-youtube-thumbnail.png" alt="ZingoCards card preview" width="640" />
</div>

---

## Get a card in 3 steps

1. **Sign in** with your email at [zingocards.com](https://zingocards.com) — a 6‑digit code arrives in your inbox.
2. **Choose an amount and coin** in your dashboard. Send the crypto to the deposit address.
3. **Card appears** in your dashboard with PAN, CVV and expiry as soon as it's minted.

---

## Developer API

Issue cards programmatically. Clean REST, JSON in / JSON out, bearer auth.

- **Base URL** — `https://zingocards.com/api/public/v1`
- **Auth** — `Authorization: Bearer zc_live_...`
- **Get your key** — Dashboard → **API Keys** → *Regenerate*
- **Rate limit** — 60 req/min per key, burst 120

### Endpoint — `POST /v1/cards`

Request issuance of a new virtual Visa. Max 2 active cards per account.

#### Request

```bash
curl -X POST https://zingocards.com/api/public/v1/cards \
  -H "Authorization: Bearer zc_live_xxxxxxxxxxxxxxxxxxxxxxxx" \
  -H "Content-Type: application/json" \
  -d '{
    "amount_usd": 100,
    "coin": "USDC"
  }'
