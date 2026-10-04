# residential proxies: how to choose billing, plan size and geo-targeting for scraping, multi-accounting and ad verification

Most people searching for residential proxies are not looking for a definition. They already know why they need one. What they want to know is why two providers quote wildly different numbers for what sounds like the same product, and what their monthly bill will actually look like once the project starts running.

There are only two things that really decide that answer. First, whether you are billed for traffic or for IPs. Second, whether the pool you bought into is clean enough to avoid endless retries. Everything else, including pool size marketing and "AI-powered rotation" language, is secondary.

To make this concrete, it helps to price out one real provider all the way down. 9Proxy sells 20M+ residential IPs across 90+ countries (a vendor-reported figure, not an audited one) and runs three separate product families: pay per IP with unlimited bandwidth, pay per GB, and bundles. That mix makes it a useful case study, because the same provider lets you compare billing models side by side instead of guessing.

## Why the price per GB is the wrong number to stare at

If you buy bandwidth, your cost is a function of page weight, and page weight is something you rarely control.

Take a modest job: 10,000 product pages, 500KB each. That is about 5GB. Now run the same pages through a real browser stack with JavaScript, fonts, images and retries, and the traffic can land three to five times higher. Suddenly you are paying for 15 to 25GB, plus every CAPTCHA page and block page that still counted as data.

Compare that to market entry rates. Decodo starts around $3.75/GB on a small pack, Oxylabs around $6/GB at a 5GB monthly commit, and Bright Data commonly quoted in the $4 to $10/GB band depending on volume and program. At those rates, a 20GB month is a $75 to $200 line item before you have written a single thing to disk.

The per-IP model attacks the same problem from a different angle. On 9Proxy's IP-based packages, one IP carries unlimited traffic for as long as it stays alive, which the documentation puts at a few hours up to around 24 hours depending on the IP. Your constraint stops being gigabytes and becomes concurrency and IP lifecycle. Ten thousand requests through one IP cost the same as a hundred.

That is not a free lunch. You get a fixed number of IPs, they are not infinitely long-lived, and if your workflow needs thousands of distinct exit points per hour, no per-IP package will rescue you. But for account-based work and long scraping sessions, the difference in bill shape is the whole story.

## 9Proxy's full plan lineup, priced at current rates

One thing to know before comparing price tables anywhere online: 9Proxy raised prices on its IP-based and bundle packages on 1 June 2026, its first adjustment since launching in 2023. GB-based (bandwidth) packages were left untouched. Plenty of review pages still publish the older numbers, which is why you will see $20 quoted for 100 IPs in one place and $24 in another. The figures below are the post-adjustment ones.

### Residential proxies by IP (unlimited bandwidth, unused IPs never expire)

| Package | Price | Effective cost per IP | Buy |
| --- | --- | --- | --- |
| 100 IPs | $24 | $0.24/IP | [Start with the 100 IP package](https://bit.ly/9-Proxy) |
| 500 IPs | $72 | $0.144/IP | [Grab the 500 IP package](https://bit.ly/9-Proxy) |
| 1,000 IPs + 500 bonus IPs | $126 | $0.084/IP | [Get 1,500 IPs for the price band of 1,000](https://bit.ly/9-Proxy) |
| 2,500 IPs | $210 | $0.084/IP | [Choose the 2,500 IP package](https://bit.ly/9-Proxy) |
| 5,000 IPs | $360 | $0.072/IP | [Scale to the 5,000 IP package](https://bit.ly/9-Proxy) |
| 15,000 IPs | $720 | $0.048/IP | [Order the 15,000 IP package](https://bit.ly/9-Proxy) |
| 25,000 IPs | $863 | $0.035/IP | [Buy the 25,000 IP package](https://bit.ly/9-Proxy) |
| 50,000 IPs | $1,438 | $0.029/IP | [Take the 50,000 IP package](https://bit.ly/9-Proxy) |
| 100,000 IPs (business) | $2,300 | $0.023/IP | [Open the 100,000 IP business package](https://bit.ly/9-Proxy) |
| 200,000 IPs (business) | $4,140 | $0.021/IP | [Look at the 200,000 IP business package](https://bit.ly/9-Proxy) |
| 500,000 IPs (business) | $8,625 | $0.018/IP | [Enquire about the 500,000 IP package](https://bit.ly/9-Proxy) |

### Residential proxies by GB (180-day validity, unlimited endpoints)

| Package | Price | Effective cost per GB | Validity | Buy |
| --- | --- | --- | --- | --- |
| 5 GB | $15 | $3.00/GB | 180 days | [Test the network with 5 GB](https://bit.ly/9-Proxy) |
| 50 GB + 5 bonus GB | $105 | $2.10/GB | 180 days | [Buy the 50 GB pack](https://bit.ly/9-Proxy) |
| 100 GB | $150 | $1.50/GB | 180 days | [Order the 100 GB pack](https://bit.ly/9-Proxy) |
| 200 GB | $200 | $1.00/GB | 180 days | [Take the 200 GB pack](https://bit.ly/9-Proxy) |
| 1,000 GB | $800 | $0.80/GB | 180 days | [Get the 1,000 GB pack](https://bit.ly/9-Proxy) |
| 2,000 GB | $1,500 | $0.75/GB | 180 days | [Scale into 2,000 GB](https://bit.ly/9-Proxy) |
| 3,000 GB (enterprise) | $2,160 | $0.72/GB | No expiry | [Ask about the 3,000 GB enterprise pack](https://bit.ly/9-Proxy) |
| 6,000 GB (enterprise) | $4,200 | $0.70/GB | No expiry | [Review the 6,000 GB enterprise pack](https://bit.ly/9-Proxy) |
| 10,000 GB (enterprise) | $6,800 | $0.68/GB | No expiry | [Contact sales for the 10,000 GB pack](https://bit.ly/9-Proxy) |

### Bundle packages (IPs plus traffic in one purchase)

| Bundle | What's inside | Price | Buy |
| --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | [Get the Starter bundle](https://bit.ly/9-Proxy) |
| Popular | 1,500 IPs + 50 GB | $180 | [Get the Popular bundle](https://bit.ly/9-Proxy) |
| Pro | 5,000 IPs + 500 GB | $720 | [Get the Pro bundle](https://bit.ly/9-Proxy) |

Bundle traffic is valid for 180 days, same as the standalone GB packs. The bundles also carry a built-in discount rather than a coupon: 9Proxy's own billing documentation shows an order summary where the Pro bundle lists at $860 and $140 comes off at checkout. Whether that exact figure appears in your cart is worth checking, but the pattern is that the bundle pricing is already discounted against buying IPs and GB separately.

## Which model fits which job

**Account-based work, social profiles, sneaker or marketplaces.** Pay per IP. You want the same exit point across a long session, and you do not want a data counter quietly draining while a logged-in profile sits open. Sessions of several hours up to roughly a day line up with how people actually run these workflows.

**High-rotation scraping, SERP checks, price monitoring, ad verification.** Pay per GB. You burn little traffic per request but need a fresh exit point constantly, and GB packs generate unlimited endpoints with rotating or sticky sessions. This is also the friendlier option on infrastructure: IP-based packages require the desktop app with local port forwarding, while GB-based works straight from the dashboard using username/password credentials or an IP whitelist.

**Agencies juggling several clients.** Bundles. One purchase covers the stable IPs one client needs and the flexible traffic another one burns, without maintaining two balances.

## Targeting: country is the easy part, and often not enough

9Proxy advertises targeting down to country, state, city, ZIP code and ISP level. The useful part is the last two. City-level targeting is what makes a local ranking check or a geo-priced product page show you real data instead of a national average. ISP-level targeting matters when you are building profiles that need to look internally consistent, because an IP registered to a cable provider in one city paired with a browser timezone from another is a fingerprint mismatch waiting to be flagged.

Two practical checks before you buy big: resolve a sample of IPs with an IP lookup service to confirm they actually report as residential and belong to the ISP you asked for, and run the same query from a few target cities to confirm the page content really changes. Advertised granularity and delivered granularity are not always the same thing across providers.

## What independent testing shows

Vendor-published success rates are claims, not results. Third-party tests are more useful, even when imperfect.

A 2026 Geekflare review ran 300 sequential requests through 9Proxy's rotating residential IPs against a major e-commerce site sitting behind Cloudflare. Results: 293 passes (97.7%), 5 CAPTCHA challenges (1.7%) that all came from a single IP range and cleared once traffic rotated away, 2 hard blocks (0.6%), and an average response time of 0.63 seconds. The same test pattern through a datacenter pool produced a 34% block rate on the first pass, which is the comparison that explains why residential IPs cost more.

A separate write-up from ProxyBros in late 2025 reported roughly 99.5% success across US, DE, UK, BR and IN over a week of mixed work, with about 0.6 second average response and connection-level errors dropping around 35% once auto-refresh was enabled. Treat that one with more caution: it reads like a sponsored review, and it also makes the fair point that pool-size claims should never be the deciding factor.

Directory coverage is more moderate. ProxyLook's 2026 comparison pages score 9Proxy around 3.9 out of 5, list a 20M+ residential pool and a 97% success rate, and describe it as a budget option built on per-IP pricing with unlimited bandwidth. Two of those three sources carry affiliate links, which is worth remembering when a number looks unusually clean.

## The fine print that actually affects your bill

- **Expiry.** Unused IPs on the IP-based plans never expire. GB balances are valid for 180 days, except on the 3,000GB and larger enterprise packs, where they do not expire at all. If your project runs in bursts, that difference matters more than the per-GB rate.
- **Rotation.** IP-based plans do not rotate naturally. You rotate by running the company's Auto Rotation on selected ports at intervals you set, and Auto-Refresh replaces IPs that drop offline (the vendor says within about 60 seconds). GB plans rotate per request by default, or hold a sticky session you define.
- **Failed IPs.** 9Proxy advertises a 60-second window in which an IP that does not work after forwarding can be swapped or credited. Confirm the current terms with support before you rely on it at volume.
- **IP reuse.** The Today List lets you reuse any proxy from the previous 24 hours at no extra cost. The company estimates this cuts effective spend by roughly 20 to 30% on recurring tasks, which is a meaningful number if your jobs hit the same targets daily.
- **Payment.** Cards, crypto (USDT, BTC, ETH, LTC, DOGE among others), local payment methods, Alipay, Apple Pay and Google Pay are all listed. Partner materials advertise a 5% bonus IP credit for crypto payments and a 5% discount on referred sign-ups, which is how invite-code sign-up links work. Check what the checkout applies to your specific order rather than assuming.
- **Trial.** A limited trial for new users is advertised subject to availability. Ask support before buying a package if you want to test your actual targets rather than a demo endpoint.
- **Support.** 24/7 through the site chat, Telegram and email, with technical answers rather than scripted replies according to the reviewers who filed real tickets.

## Mistakes that cost money

Buying the largest tier first is the most expensive one. Start with 100 IPs or a 5GB pack, run your real targets for a few days, and see what your success rate and burn rate look like. Old price tables from 2025 will also mislead you on tier costs, so check the live pricing page rather than a comparison blog.

Paying per GB for browser-rendered scraping is the second. If your requests pull 2 to 5MB of JavaScript-heavy markup each, metered billing turns every retry into money, and failed requests still count.

Over-rotating is subtler. Changing the exit IP in the middle of a login sequence or a multi-step checkout is a fast way to look less like a person, not more. Use sticky sessions for anything with state and rotation for anything without.

And treating pool size as a quality metric is the oldest mistake in the category. Twenty million IPs means nothing if the ones assigned to your target city were blacklisted last week. Success rate against your actual target site is the only number worth optimizing.

## FAQ

**What is a residential proxy?** An IP address assigned by a consumer ISP to a real home connection, routed so your traffic exits through it. Sites see a household connection instead of a datacenter range, which reduces blocks and gives you the localized version of a page.

**How much do residential proxies cost?** Entry-level metered rates across the market sit roughly between $3 and $6 per GB, with enterprise providers quoted higher. 9Proxy starts at $3.00/GB on its smallest pack and drops to $0.68/GB at the 10,000GB tier, while per-IP pricing runs from $0.24 down to $0.018 per IP at the top business tier.

**Per-IP or per-GB?** Per-IP if you need stable identities, long sessions, or unpredictable traffic volume. Per-GB if you need constant rotation across many targets and modest traffic per request.

**Do the IPs expire?** Purchased IPs on IP-based plans do not expire, though any single IP stays active for a few hours up to around 24 hours. GB balances last 180 days unless you are on a large enterprise pack.

**Will it work with anti-detect browsers?** 9Proxy supports HTTP/HTTPS and SOCKS5, hands out credentials in the standard host:port:username:password format, and is listed as compatible with the usual anti-detect browsers and automation libraries.

If you want to see what your own workload costs before committing to a tier, 👉 [create a 9Proxy account and price out a small package](https://bit.ly/9-Proxy) — a 100 IP or 5GB start is enough to measure success rate on your targets, and you can scale from there once the numbers make sense.
