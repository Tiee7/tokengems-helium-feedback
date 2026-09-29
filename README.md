# TokenGems × Helium HNT: evidence-based product feedback

**Observed:** 2026-09-29 17:03–17:15 Beijing time (UTC+8)  
**Scope:** public, no-cost browser flows on [TokenGems](https://tokengems.ai/), [Helium](https://www.helium.com/), and [Helium's HNT documentation](https://docs.helium.com/tokens/hnt-token/).  
**Author:** Tiee, with AI-assisted browser exploration. No token purchase, trade, deposit, wallet transaction, or security scan was performed.

## Why this project

The [TokenGems feedback bounty](https://superteam.fun/earn/listing/try-a-solana-project-and-give-useful-feedback-tokengems) asks entrants to explore a Solana project and publish a specific, useful take on its TokenGems page. Helium is a fitting subject: TokenGems has a [Solana HNT page](https://tokengems.ai/tokens/solana/helium-network-token-hntyVP6YFm1Hg25TN9WGLqM12b8TQmcknKrdu1oxWux), and [Helium's own documentation](https://docs.helium.com/tokens/hnt-token/) confirms the Solana migration and the same HNT mint address. The product's public site makes it possible to review the learn-about-HNT path without buying anything.

This is an **independent experience report, not a contest entry**. The listing's current data marks it `HUMAN_ONLY`; [Superteam's agent rules](https://superteam.fun/earn/agents) accept agent submissions only for `AGENT_ALLOWED` or `AGENT_ONLY` listings. No TokenGems contribution or Superteam submission was posted by the agent. A human entrant should independently check the observations and follow the contest's identity and authorship rules.

## Most useful finding: the HNT buy/sell path ends at a 404

From the [Helium HNT page](https://www.helium.com/hnt), the “Earn, Buy, or Sell HNT” section explains the two routes. Its **Buy or sell HNT** button opens a new tab at this exact URL:

```text
https://www.helium.com/plushttps://www.coinbase.com/en-pt/price/helium
```

That URL displays **“Page Not Found”** on Helium's site. The link appears to combine Helium's `/plus` path with a full Coinbase URL. I verified both the anchor's `href` and the destination reached by clicking the visible button; I did not visit a checkout or make a purchase.

| Reproduction | Observed | Expected |
| --- | --- | --- |
| Open `https://www.helium.com/hnt`, scroll to “Earn, Buy, or Sell HNT”, click **Buy or sell HNT**. | A new tab opens the combined URL above and shows “Page Not Found”. | A working, clearly labeled destination for learning how to buy or sell HNT, with any country restrictions explained. |

This is the point where an interested reader tries to act on the HNT explanation. A dead end there undercuts the page's otherwise clear account of how carrier data use, HNT burns, and deployer rewards relate. The smallest fix is to replace the button target with the intended valid URL and check it in a normal browser. If the destination varies by region, a maintained choice page would be clearer than a country-specific deep link.

Evidence: [visible HNT action](evidence/helium-buy-link-visible.png) · [result after clicking](evidence/helium-broken-destination.png).

## Experience log

These observations describe the exact path taken. A visible element is not evidence that its underlying action works unless the action was tested.

| Step | What I observed | Status |
| --- | --- | --- |
| 1. Read the bounty | One to three contributions, each on a different Solana project; the strongest one is judged for specificity, exploration, and usefulness. No purchase or token ownership is required. The listing data gave a deadline of **2026-10-17 06:59:59 UTC** (14:59:59 Beijing time) and a winner-announcement date of **2026-10-24 06:59:59 UTC**. It is `HUMAN_ONLY`. | Verified from the live listing and its embedded data. |
| 2. Open TokenGems | Home page offered search, categories, leaderboard, launches, latest posts, and a market map. An existing authenticated browser session was present. I completed its previously empty username and bio with the Tiee identity; no new wallet signature was requested during this review. | Verified UI; authentication method was not independently tested. |
| 3. Search “Helium” | The header search opens a modal with chain/category and other filters. The text search returned HNT and MOBILE on Solana, plus an unrelated meme token whose symbol is “Helium”. Chain badges and full names distinguish them. | Verified result list; no claim about search ranking quality. |
| 4. Open the HNT TokenGems page | The page displayed the Solana logo, HNT mint `hntyVP6YFm1Hg25TN9WGLqM12b8TQmcknKrdu1oxWux`, a link to Helium's website, token statistics, community sentiment, Insights/Trade/Followers tabs, and existing posts. The mint matches [Helium's documentation](https://docs.helium.com/tokens/hnt-token/). | Verified identity and navigation. Market figures are time-sensitive snapshots, not independently audited. |
| 5. Inspect the post composer | Clicking **Post** on the HNT page opened a composer prefilled with `$HNT is a gem!`. It was editable. I closed it without posting. For a constructive review, the writer should replace the positive template with the actual observation rather than imply endorsement. | Verified draft UI; publish action untested. |
| 6. Inspect TokenGems Trade | The HNT Trade tab loaded an embedded frame. I did not connect a trading wallet, request a quote, or execute a trade. | Navigation verified; trading untested. |
| 7. Visit Helium | TokenGems' project link led to Helium's official site. The homepage explains a people-deployed wireless network and links to HNT and Helium World. I rejected optional cookies. | Verified public pages. |
| 8. Review HNT | The HNT page describes coverage deployment, carrier offload, HNT burning, and deployer rewards. The “Earn” button points to Helium Plus. The adjacent buy/sell action failed as detailed above. | Page and broken action verified. No purchase attempted. |
| 9. Read tokenomics | After scrolling the counters into view, the page showed **223M HNT** hard cap and a **$9K** daily burn-rate figure during this visit. The initial page snapshot showed zero placeholders before the animated counters entered view, so those placeholders are **not** reported as a bug. | Visible figures verified at one moment; underlying calculation not audited. |
| 10. Cross-check the docs | Helium's HNT docs identify Solana migration on 2023-04-18 and the HNT mint. They explain HNT-to-Data-Credit burn-and-mint mechanics and a roughly 223M maximum after early under-issuance. | Read-only cross-check. |
| 11. Attempt Helium World | The “Explore the Network” link reached `https://world.helium.com/`, but this browser remained on a Vercel security checkpoint. I did not bypass it or infer that the map itself is broken. | Blocked; map features unverified. |

## Additional, lower-priority notes

1. **Tokenomics copy context.** The subtitle under “The Tokenomics” says “And phone users are left with coverage gaps.” That sentence fits the earlier “The Problem” section but does not explain the supply, halving, or burn figures immediately below it. A one-sentence summary of the burn-and-mint mechanism would connect the heading to the chart and counters. [Heading screenshot](evidence/helium-tokenomics-heading.png).
2. **Documentation table clarity, as a question.** The [Max Supply section](https://docs.helium.com/tokens/hnt-token/#max-supply) says the maximum fell to about 223M after roughly 17M in early under-issuance, while the nearby target-emission table still lists 225M HNT at the start of 2027 and repeats year numbers 7 and 8 for 2027 and 2028. The table may be an unadjusted theoretical schedule; labeling it that way, adding the adjusted series, and correcting row numbering would help readers reconcile it with the hard-cap statement. I did **not** verify current on-chain supply or assert that the token itself exceeds its cap.
3. **Good part of the journey.** The HNT page gives a readable causal chain from deployment to carrier use, HNT burn, and deployer reward. TokenGems makes the project discoverable by name and links the token to its official website and community discussion. The broken action matters because it occurs after these useful explanations.

## Evidence and limits

- Browser: Chromium-based Ego browser, normal public-page interaction. Times are Beijing time (UTC+8). Screenshots show only public Helium pages; no wallet address, account secret, or transaction details are published.
- [HNT buy/sell button](evidence/helium-buy-link-visible.png), [404 after click](evidence/helium-broken-destination.png), [tokenomics heading](evidence/helium-tokenomics-heading.png), [loaded tokenomics metrics](evidence/helium-tokenomics-metrics.png).
- No token purchase, deposit, swap, wallet signing, authenticated Helium action, security scan, or attempt to bypass the Helium World checkpoint.
- No prize, sale, receivable, or revenue has been earned by producing this report.
