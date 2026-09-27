# سوق المساعدين — Mosaiden Souq MCP

اسأل ذكاءك الاصطناعي المفضّل بالعربية، وهو يبحث في **سوق المساعدين** ([mosaiden.com](https://mosaiden.com)):
متاجر (منها جرير وإكسترا بكل الماركات)، إعلانات مبوّبة، قوائم المطاعم بالأسعار، وأكثر من 20 ألف فندق — ويقارن الأسعار ويعطيك رابط الطلب.

Ask your favourite AI in Arabic or English to search the Saudi marketplace **Mosaiden Souq**: stores (Jarir, eXtra and more),
classified ads, restaurant menus with prices, 20,000+ hotels across seven countries — with price comparison and order links.

| | |
|---|---|
| Public endpoint (no sign-in) | `https://mosaiden.com/mcp` |
| Account endpoint (OAuth 2.1) | `https://mosaiden.com/mcp/me` |
| Official MCP Registry | `com.mosaiden/souq` |
| Docs | https://mosaiden.com/ai-connect |
| Privacy & support | https://mosaiden.com/ai-connect/privacy |

## Install

**Gemini CLI**
```bash
gemini extensions install https://github.com/alkhadraa02/mosaiden-souq-mcp
```

**Qwen Code** (reads the same `gemini-extension.json`)
```bash
qwen extensions install alkhadraa02/mosaiden-souq-mcp
```

**Kimi Code** — inside Kimi Code:
```
/plugins install https://github.com/alkhadraa02/mosaiden-souq-mcp
```

**Claude Code**
```bash
claude plugin marketplace add alkhadraa02/mosaiden-souq-mcp
claude plugin install mosaiden-souq@mosaiden-souq
```

**Codex**
```bash
codex plugin marketplace add alkhadraa02/mosaiden-souq-mcp
```

**Claude.ai, ChatGPT, Grok** — add a custom connector with `https://mosaiden.com/mcp` (or `/mcp/me` to connect your account).
Step-by-step: https://mosaiden.com/ai-connect

## Tools

| Tool | What it does | Sign-in |
|---|---|---|
| `search_souq` | Search products, classified ads, stores, restaurants and meals | — |
| `compare_prices` | Phones & electronics across Jarir, eXtra and other stores, cheapest first | — |
| `search_restaurants` / `get_restaurant_menu` | Restaurants and official menus with SAR prices | — |
| `search_hotels` | Hotels in Saudi Arabia, UAE, Egypt, Bahrain, Kuwait, Oman, Jordan | — |
| `list_assistants` / `list_categories` | The marketplace's specialised assistants and ad categories | — |
| `search_assistants` | Find an assistant for a need: the marketplace's own plus live-checked MCP servers from other providers | — |
| `checkout_link` | Turn chosen store products into one cart link; the user reviews, adds with a tap and pays on mosaiden.com | — |
| `my_account` | Your plan, listings, stores and recent orders | `souq.read` |
| `publish_listing` / `add_store_product` | Publish an ad or a store product — preview first, publish only after you approve (subscribers) | `souq.publish` |

Results render as interactive cards in hosts that support MCP Apps. Ordering, booking and payment always happen on mosaiden.com —
the connector never asks for card details.

## License

MIT — this repository only contains install manifests; the service itself runs at mosaiden.com.
