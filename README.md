# Wave ISP VPS: Is the IP Residential or Just ISP-Announced? Which SixtyNet Tier Fits, and What It Costs (Full Plan Table)

A `wave isp vps` is a server whose public IPv4 address is announced by the Astound/Wave network, AS11404. SixtyNet sells machines on that network as a residential VPS line with four tiers from $25/month, and Astound/Wave is one of the carriers those tiers can be provisioned on. What follows covers how to tell the three companies called Wave apart, what an ISP-announced address actually does for you, the current prices in monthly and annual terms, and the restrictions that decide whether this is the right purchase at all.

## Three companies called "Wave", and only one is a network

The keyword pulls up two hosting brands that happen to be named Wave, plus the carrier most searchers actually want. They are not related.

| Name | What it is | Gives you a Wave-announced IP? |
| --- | --- | --- |
| Astound/Wave, AS11404 | The cable ISP network; Wave Broadband and RCN now sit under Astound Broadband | Yes. This is the network in the keyword |
| Wave Technologies | A Philippine host selling ordinary KVM VPS on RAID-10 SSD, no public price list on its page | No. Datacenter address |
| Wave Hosting | A Canadian/US host selling NVMe VPS on 1 Gbps ports with DDoS protection | No. Datacenter address |

Both hosting brands named Wave are conventional virtual servers. If your reason for searching is that you need an American address that a streaming platform or an account system reads as a home connection rather than a datacenter, neither of them is the product you were looking for.

> **The short version.** For an IPv4 announced by Astound/Wave, price out SixtyNet's residential line: four tiers from $25 to $165 per month, Astound/Wave offered as a carrier option next to AT&T Mobility and Cox, and ports 80/443 closed on every residential plan. If you only want cheap CPU and don't care whose ASN the address sits on, an ISP line is the wrong purchase and a datacenter plan will cost less.
> 👉 [Check SixtyNet's current residential tiers and carrier options](https://sixtynet.net/aff.php?aff=39)

## SixtyNet's residential tiers and what they cost

Four tiers, billed monthly or annually, with the annual option knocking 13–16% off the monthly rate.

| Plan | vCPU · RAM · NVMe | Traffic / network | Monthly | Annual | Order |
| --- | --- | --- | --- | --- | --- |
| Residential-STARTER | 2 core · 2 GB · 40 GB (12,500 IOPS) | 5 TB · 2G premium | $25 | $260 (−13%) | [Order STARTER](https://sixtynet.net/aff.php?aff=39) |
| Residential-MICRO | 4 core · 4 GB · 80 GB (12,500 IOPS) | 10 TB · 4G premium | $45 | $460 (−15%) | [Order MICRO](https://sixtynet.net/aff.php?aff=39) |
| Residential-MEDIUM | 8 core · 8 GB · 160 GB (25,000 IOPS) | 20 TB · 10G premium | $85 | $860 (−16%) | [Order MEDIUM](https://sixtynet.net/aff.php?aff=39) |
| Residential-LARGE | 16 core · 16 GB · 320 GB (25,000 IOPS) | 40 TB · 10G premium | $165 | $1,660 (−16%) | [Order LARGE](https://sixtynet.net/aff.php?aff=39) |

The annual column is where the real cost sits. Paying month to month for a year costs $300, $540, $1,020 and $1,980 on the four tiers; the annual prices above save $40, $80, $160 and $320 respectively. That works out at roughly $21.67, $38.33, $71.67 and $138.33 per month equivalent.

Three details apply to every row in that table.

- **Ports 80 and 443 are closed.** The product page states it directly: residential IP products do not open 80 and 443 for IP risk-control reasons. A public website on a residential address is not an option here, at any tier.
- **The tier name doesn't fix the carrier.** Astound/Wave is an option inside the residential line, not a separate plan code. The residential store link on the cart page sits under an AT&T Mobility catalogue, and third-party reviews have covered Astound/Wave and Cox builds of the same line. Which carrier you get is a checkout question.
- **Stock is the variable you can't plan around.** The cart has listed all four residential tiers as 0 available, so check availability before scheduling a migration.

Expect a carrier surcharge. Reviews published in October 2025 reported a $5/month add-on for the Astound IP and the same for Cox, charged on top of the single-ISP price. Treat those figures as reported rather than current, and read the cart total before paying.

The same price list carries three other lines, none of which give you a Wave address:

- **LAX series** (datacenter IP, DDoS protection, 80/443 open): STARTER $200/yr, MICRO $400/yr, MEDIUM $800/yr, LARGE $1,600/yr, plus Storage-500G at $400/yr and Storage-1TB at $700/yr. List prices run about 17% higher.
- **Irvine Pro** (AS9929 route optimised for China, residential IP, whitelist-only access): STARTER from $350/yr, list $420.
- **China Unicom Premium** (AS9929, free BGP session, 100M base port with 3× burst, 95th percentile billing): $2,500/yr, list $3,000.

👉 [See the full SixtyNet price list and current stock](https://sixtynet.net/aff.php?aff=39)

## What a Wave ISP VPS actually gives you

A server has two independent properties. Compute is CPU, memory, disk, operating system and admin access. Network identity is the public IPv4 and the network announcing it through BGP. An ISP VPS is a complete KVM machine plus one dedicated IPv4 announced by a carrier network. It is still a server: you get root, you install what you want, you run it persistently.

The part that trips people up is the word residential. One US provider that sells the same Astound/Wave AS11404 route describes its Seattle product as an ISP VPS with a dedicated Astound ISP IPv4, and states plainly that it is not sold as a residential connection, a rotating residential proxy or a shared NAT exit. SixtyNet labels its equivalent line "Residential IP". Both describe a dedicated address announced by a carrier network, but the marketing vocabulary differs, and only one of them claims residential status. Read the exact wording on the product you're buying rather than assuming the categories are interchangeable.

AS11404 is the identifier for the Astound/Wave network. Public IP databases and destination services may use ASN ownership, WHOIS records, routing data, address history and their own signals when they evaluate a connection, so an address announced by an ISP network can be treated differently from one announced by a cloud provider. It is not a pass. Each destination sets its own rules, weighing device and browser signals, account history, payment details and behaviour. An ISP-announced address is context, not a bypass.

Classifications also drift. Providers update their databases and individual addresses build their own history, so the only claim worth making is narrow: at the time of service, this dedicated IPv4 is announced by the named ISP network.

## The "10 Gbps" figure belongs to the host, not to your VM

In ISP VPS listings, a 10 Gbps figure usually describes the symmetrical uplink available to the physical host. It is a host route, not a reservation for each virtual machine on that host. Actual throughput depends on the remote endpoint, the route between you, protocol behaviour, how busy the node is and what your workload is doing. SixtyNet labels its tiers 2G, 4G and 10G premium network rather than quoting a host uplink, which makes the same point differently: the tier label describes the port class, not a guaranteed speed test result.

A third-party test of the Astound build in October 2025 noted the line advertises 10 Gbps while measuring closer to 1 Gbps. Single-thread speed tests tell you about one route at one moment. If a specific throughput number matters for your application, measure it against your actual destination after deployment.

## Known limits, from official pages and third-party tests

- **Ports 80 and 443 closed** on all residential tiers, per the official product page.
- **No IPv6** on the Astound and Cox builds tested in October 2025.
- **PING blocked** on those same builds, according to the published reviews.
- **I/O around 178–188 MB/s**, well below what the NVMe spec suggests; the reviewers attributed it to official limits.
- **CPU model not published.** The listings say AMD EPYC 7002 series without naming the SKU. CPU performance in the same tests was rated good despite the weak disk numbers.
- **Traffic allowance is generous**, 5 TB at the entry tier up to 40 TB at the top, which is unusual at these prices.
- **The tests are dated.** October 2025 results describe the Cox and Astound builds as they were then; specs, routing and policy can change without notice.

The combination of AMD EPYC 7002, KVM, BBR enabled by default and no IPv6 turns up across Astound-based residential products from more than one seller, including a Los Angeles Astound dual-ISP offering reviewed in July 2026 with the same CPU family, BBR and no IPv6. That consistency is useful when you're comparing listings: it suggests a common upstream shape rather than one provider's quirk.

## How other Astound/Wave routes are sold

Two other sellers are worth knowing about, purely as reference points on price and packaging.

**Blossom Host** runs two separate ISP routes rather than one pool. Seattle is Astound/Wave AS11404 with a 10 Gbps symmetrical host route and SSD-only storage, on the west coast. Washington, DC is Verizon FiOS Business at 1 Gbps with an NVMe root disk plus a SATA HDD data disk. Plans start at $19/month across four metros, Windows Server 2022, Windows 11 and Tiny11 are included at no extra licence cost, payment runs through Stripe with 3D Secure, BTC/LTC or Zelle, and prepaying takes 5% off at three months, 10% at six and 15% at twelve. Their own page calls the Seattle product an ISP VPS rather than a residential one, which is the labelling distinction above in practice.

The trade-off is straightforward. SixtyNet sells residential-labelled IPs with large traffic allowances and closed web ports; Blossom sells an ISP-labelled address on a west-coast host route without the residential claim. Same carrier, different product category.

## Which tier to pick, and two things to confirm first

- **You need an Astound/Wave-announced IPv4 for streaming, account environments or region-sensitive logins.** Take the smallest residential tier whose traffic allowance covers you. Residential-STARTER at $25/month or $260/year gives 2 cores, 2 GB and 5 TB, which is enough for a single always-on environment. Move up only if you're running several streams or hitting the traffic cap.
- **You want to host a public website.** Residential is disqualified by the port policy. Take a LAX plan instead, where 80 and 443 are open and DDoS protection is included; $200/year buys 2 cores, 2 GB and 5 TB there.
- **You want a Windows desktop or a batch of always-on scripts and don't care about the ASN.** A datacenter VPS does the same job for less. The ISP premium buys network identity, nothing else.
- **You want the whole physical box.** Look at bare metal from whichever provider lists it; virtualisation is the wrong layer for that workload.

Before you pay, confirm two things in writing: which carrier the tier will actually be provisioned on, and whether a surcharge applies for the Astound/Wave address specifically. Then check stock, because the residential tiers sell out and restock in bursts.

👉 [Start with SixtyNet's residential line and confirm carrier and stock at checkout](https://sixtynet.net/aff.php?aff=39)
