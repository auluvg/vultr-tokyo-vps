# tokyo vps: Vultr Plans From $3.50/mo, Hourly Billing Explained, and When Tokyo's Cheaper Hosts Win

Anyone searching for a "tokyo vps" is usually after one of two things: a server that answers users in Japan, Korea, Taiwan, or Hong Kong with low latency, or a Japanese IP for games, bots, and apps that behave differently depending on where requests come from. The results you'll hit are mostly small specialists — OliveVPS, Host4Fun, NovaVPS, EDIS Global, JUSTG — waving $3 to $5 entry plans. Vultr plays in a different league: a large cloud with a Tokyo (NRT) region, shared-CPU plans from **$3.50/mo**, and one feature none of those five offer — billing by the hour.

The honest short version: if you're keeping a 1 GB box running 24/7 all year, a specialist usually costs less. OliveVPS charges $3.99/mo for a dedicated vCPU, 1 GB RAM, and free DDoS protection; Vultr's 1 GB plan is $5/mo, with DDoS protection sold separately. If you need a server for a weekend event, want to spin machines up and destroy them without emailing support, or care about snapshots, a full API, and 30-plus regions under one login, Vultr is the better fit.

> **Quick picks**
> - Most people: **Vultr Cloud Compute 1 GB — $5/mo** (1 vCPU, 25 GB SSD, 1 TB transfer). 👉 [See Vultr's current cloud compute plans and prices](https://www.vultr.com/products/cloud-compute/?ref=7268283)
> - Tightest always-on budget: OliveVPS Starter ($3.99/mo, Linux only) or Host4Fun (from $3/mo) — both bill monthly.
> - Short-lived projects: Vultr. Hourly billing means a two-day test costs literal pennies.
>
> New Vultr accounts also get a signup credit (currently $100, valid 30 days), so you can measure real latency from Tokyo to your users before spending anything.

## Vultr's Tokyo VPS plans and prices

Vultr runs its full shared-CPU Cloud Compute line in Tokyo and charges the same price there as in every other region on its list — there's no Japan surcharge to worry about. Here's the line as it currently stands:

| Plan | vCPU / RAM | Storage | Transfer | Monthly | Deploy |
| --- | --- | --- | --- | --- | --- |
| 512 MB | 1 vCPU / 512 MB | 10 GB SSD | 0.5 TB | $3.50 | [ Deploy 512 MB](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| 1 GB | 1 vCPU / 1 GB | 25 GB SSD | 1 TB | $5 | [ Deploy 1 GB](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| 2 GB | 1 vCPU / 2 GB | 55 GB SSD | 2 TB | $10 | [ Deploy 2 GB](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| 4 GB | 2 vCPU / 4 GB | 80 GB SSD | 3 TB | $20 | [ Deploy 4 GB](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| 8 GB | 2 vCPU / 8 GB | 160 GB SSD | 4 TB | $40 | [ Deploy 8 GB](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| 16 GB | 4 vCPU / 16 GB | 320 GB SSD | 5 TB | $80 | [ Deploy 16 GB](https://www.vultr.com/products/cloud-compute/?ref=7268283) |

A few things worth knowing before you pick a row:

- Every plan includes one IPv4 address (geolocated in Japan) plus a free IPv6 /64 allocation.
- Custom ISO uploads are supported, so unusual operating system choices are possible.
- Provisioning is automated — instances usually run within about a minute of deploying.
- Vultr also sells a High Frequency line (3 GHz-class cores with NVMe storage, from $6/mo) and a High Performance line. Regional availability shifts as those roll out, so check the Tokyo option in the deploy menu or 👉 [scan the full pricing page](https://www.vultr.com/pricing/?ref=7268283) before committing to a tier.

## What latency to expect from a Tokyo VPS

Tokyo is the best-connected city in East Asia, and the numbers hold up across benchmarks published independently by several Tokyo hosts. Typical round-trip times from a server in Tokyo:

| Route | Typical RTT |
| --- | --- |
| Local Tokyo | 1–3 ms |
| Osaka | ~5 ms |
| Seoul | ~30 ms |
| Taipei | ~35 ms |
| Hong Kong | ~35–50 ms |
| Singapore | ~70 ms |
| Sydney | ~95–110 ms |
| Los Angeles | ~110 ms |

These are typical published figures for Tokyo-hosted servers in general — your actual route depends on your users' ISPs, not just the datacenter. One honest caveat: unlike EDIS or OliveVPS, Vultr doesn't publish its own Tokyo speed-test tables on a marketing page. Since the entry instance costs less than a cent an hour to run, the cheapest way to get real numbers is to deploy one and ping it from your own network.

## Hourly billing: the feature the cheap specialists don't have

Vultr meters every instance by the hour and caps the bill at the plan's monthly price. The $5 plan works out to roughly $0.007/hour, so a server that runs 48 hours over a weekend costs about $0.33. Destroy it and billing stops; let it run a full month and you never pay more than $5.

None of the five Tokyo specialists in this niche do this. OliveVPS, Host4Fun, NovaVPS, EDIS Global, and JUSTG all bill monthly or annually (EDIS throws in a free month on annual terms; JUSTG discounts yearly prepay). That's fine — often cheaper, in fact — if the server lives 24/7. For a match-night game server, a two-week test, a CI runner that only needs to exist during builds, or a relay you'll tear down after an event, monthly billing means paying for weeks you never use. Hourly billing also pairs with Vultr's multi-region model: you can run the same plan in Seoul, Osaka, or Singapore simultaneously, test which one your users feel first, and delete the losers — no migration tickets, no 30-day location-switch cooldowns like JUSTG's plan. 👉 [Deploy a Tokyo instance on hourly billing](https://www.vultr.com/products/cloud-compute/?ref=7268283) if that workflow matches what you're building.

## The costs that don't show up in the plan price

Sticker price is only part of the bill. Four line items to know about:

- **Automatic backups add 20%** to the instance price — the $5 plan becomes $6/mo with backups enabled. Snapshots, stored separately, run about $0.05/GB per month.
- **DDoS protection is a paid add-on**, listed at $10/mo per instance. Several Tokyo rivals bundle it free: OliveVPS includes it on every plan, and NovaVPS advertises included L3/L4 filtering (UDP game floods covered, though it's no L7 WAF). If your workload attracts floods — public game servers especially — price this in.
- **Transfer overage runs $0.01/GB** once you pass your quota; inbound traffic is free. OliveVPS overages cost $0.005/GB, half the rate, though its plans also start cheaper.
- **Vultr is a KYC'd cloud.** You pay by card, PayPal, Alipay, or wire, and the account is tied to your identity. If anonymous signup is the actual requirement — a real reason some people hunt for crypto-only Tokyo hosts — NovaVPS is the one in this comparison built around no-KYC payments (USDT, Monero, and more). Vultr won't work for that use case.

None of this makes Vultr expensive — a $5 plan with backups is still $6 for 1 GB and 1 TB of monthly transfer — but it does change which provider is genuinely cheapest for your situation.

## Vultr vs Tokyo's cheap VPS specialists

The comparison only means something with real numbers side by side. Everything below comes straight from each provider's current Tokyo plan page:

| Host | Cheapest Tokyo plan | Entry specs | What they're known for |
| --- | --- | --- | --- |
| Vultr | $5/mo (hourly billing) | 1 vCPU, 1 GB, 25 GB SSD, 1 TB | Hourly billing, API/Terraform, 30+ regions |
| OliveVPS | $3.99/mo | 1 dedicated vCPU, 1 GB, 25 GB NVMe, 1 TB @ 1 Gbps | Free DDoS, Equinix TY11 in Ariake, Linux-only entry tier |
| Host4Fun | from $3/mo | config varies | JPIX peering, Ryzen nodes, crypto and cards |
| NovaVPS | $5.49/mo list ($3 with a $50+ prepay) | 1 vCPU, 2 GB, 40 GB NVMe, unmetered 1 Gbps | No-KYC signup, crypto-only billing, ~60s deploys |
| JUSTG | $19.99/mo | 1 core, 512 MB, 10 GB SSD, 500 GB @ 500 Mbps | Native Japanese IPv4; tested unlocks for ChatGPT, Claude, Netflix, Disney+ (Oct 2026) |
| EDIS Global | from €7.99/mo | 4 GB tier: 2 vCPU, 45 GB SSD, 4 TB at €21.99 | Equinix TY8 in Shinagawa, 2×10 Gbps uplinks, ~9 Gbps published local speed test (Sep 2026), free month on annual |

Where the specialists genuinely win:

- **Pure 24/7 monthly cost.** OliveVPS Starter does the same job as Vultr's $5 plan for $3.99 with DDoS protection included.
- **IP reputation games.** JUSTG tests its Japanese IPs against Netflix, Disney+, and the major AI services and publishes the results; Vultr makes no unlock promises of any kind, and whether a given service treats its Tokyo IPs the way you want is something you'd verify yourself.
- **Privacy.** NovaVPS's token-only signup and Monero support exist for a reason Vultr can't replicate.
- **Raw bandwidth.** EDIS's Tokyo plans ride 2×10 Gbps uplinks in Equinix TY8, and their published speed test to a local Tokyo node hit roughly 9 Gbps in September 2026.

Where Vultr wins: billing granularity, automation (full API, CLI, Terraform support), snapshots and instant redeployment, and one account that covers Tokyo plus every other region you might later need. If your project outgrows Japan, nothing gets rebuilt — you just deploy in a new zone.

## Which Vultr Tokyo plan fits your workload

- **512 MB ($3.50)** — lightweight proxies, status pages, tiny bots. Tight; don't run a database here.
- **1 GB ($5)** — the default for a small website, a Telegram or Discord bot, or a low-population Minecraft server for friends.
- **2 GB ($10)** — WordPress with a real database, small web apps, WireGuard for a household.
- **4 GB ($20)** — busier game servers, small PostgreSQL instances, Docker stacks with a few containers.
- **8–16 GB ($40–$80)** — app backends and multi-service deployments. At this size, also price EDIS's 4 GB tier (€21.99, with those 10 Gbps uplinks) if bandwidth matters more to you than hourly billing.

One Windows note: the specialists bundle licensing — OliveVPS includes Windows from its $7.99 Pro tier up, and EDIS points Windows Server users at its 2-vCPU plans. On Vultr you install Windows yourself through the ISO library and handle licensing your own way. More work, more control.

## Before you order: three quick checks

1. **Pick Tokyo (NRT) in the region dropdown at deploy.** Vultr won't put you there automatically, and a Tokyo VPS only delivers the numbers above if the box actually sits in Japan.
2. **Decide on backups at deploy time.** The checkbox adds 20% to the bill; retrofitting is possible, but it's easier to choose upfront.
3. **Use the trial-credit month to measure latency** from your users' networks to the instance. Ping, traceroute, and one real weekend of traffic will tell you more than any benchmark table — and with hourly billing, that test costs roughly nothing.

If you're keeping the server for years and want the lowest possible invoice, one of the $3–$4 specialists will win on price alone. For everything else — projects that start and stop, workloads that might move regions, anyone who'd rather use an API than a support ticket — 👉 [start with Vultr's 1 GB Tokyo plan and scale (or destroy) from there](https://www.vultr.com/products/cloud-compute/?ref=7268283).
