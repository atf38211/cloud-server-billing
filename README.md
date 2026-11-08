# Best Cloud Based Server: What Should You Pay, When Does Hourly Billing Cost More Than Monthly, and Which Plan Fits Your Workload? (Full Plan Tables)

A workable cloud server costs €3 to $6 a month at the entry level. UpCloud's Starter tier lists €3/month for 1 GB RAM, one vCPU and 10 GB of storage; Kamatera appears at $4.00/month and IONOS at $5.76/month in a frequently updated provider roundup, which is where both publish a starting figure. Everything above that entry point comes down to three things: how the provider bills you, what a trial does when it expires, and whether the product you picked is a server at all.

This guide works through all three, puts Spin Servers' fixed-resource plans next to the hourly clouds so you can see where the price curve bends, and finishes with selection rules you can apply to your own workload.

> **If you only want the short version:** one small site or API fits in the €3–$8 bracket and you should pick the cheapest plan that gives you root and a snapshot option. If you want 4 to 16 vCPU, root access and 8 to 15 TB of monthly transfer at a flat rate, Spin Servers publishes **$39.00/month** for its 6 vCPU / 8 GB KVM plan. 👉 [See the current Spin Servers VPS and dedicated plan list](https://bit.ly/Spinservers)

## Spin Servers' current plans and where they sit on the price curve

Spin Servers sells two product lines that buyers lump together as "cloud": KVM virtual servers it markets as Simple Application Servers for websites, development and everyday applications, and bare-metal dedicated servers in Dallas and San Jose. Every virtual plan includes RAID-10 SSD storage, a 1 Gbps port, one IPv4 address, one IPv6 address and 8 to 15 TB of monthly transfer.

| Plan | vCPU / RAM | Storage | Transfer / port | Price (USD/mo) | Order |
| --- | --- | --- | --- | --- | --- |
| 4 vCPU | 4 / 4 GB DDR4 | 80 GB RAID-10 SSD | 8 TB, 1 Gbps | On order page | [Check live price](https://bit.ly/Spinservers) |
| 6 vCPU | 6 / 8 GB DDR4 | 120 GB RAID-10 SSD | 8 TB, 1 Gbps | **$39.00** | [Check live price](https://bit.ly/Spinservers) |
| 8 vCPU | 8 / 8 GB DDR4 | 160 GB RAID-10 SSD | 10 TB, 1 Gbps | On order page | [Check live price](https://bit.ly/Spinservers) |
| 12 vCPU | 12 / 12 GB DDR4 | 160 GB RAID-10 SSD | 10 TB, 1 Gbps | On order page | [Check live price](https://bit.ly/Spinservers) |
| 16 vCPU (Intel Xeon) | 16 / 16 GB DDR4 | 320 GB RAID-10 SSD | 15 TB, 1 Gbps | On order page | [Check live price](https://bit.ly/Spinservers) |

Only the 6 vCPU tier carried a public starting price when I checked; the other four quote on the order page, and the figure moves with location and term. All five are billed monthly, and all five ship with SMTP port 25 closed by default, which matters more than it sounds and gets its own section below.

The dedicated list is organised by location. Dallas carries one ready-to-go build that auto-provisions; San Jose carries seven configurations, all with instant provisioning.

| Location | CPU | RAM | Storage | Network | Order |
| --- | --- | --- | --- | --- | --- |
| Dallas, TX | Xeon E3-1280 v5, 4C/8T, 3.7 GHz turbo | 32 GB DDR4 ECC | 1 TB M.2 NVMe | 10 Gbps, 30 TB, 1 IPv4 | [Check live price](https://bit.ly/Spinservers) |
| San Jose, CA | 12C/24T, 2.6 GHz base | 64 GB DDR3 ECC | 240 GB SSD | 2 × 10 Gbps, 30 TB | [Check live price](https://bit.ly/Spinservers) |
| San Jose, CA | 4C/8T, 3.7 GHz base | 32 GB DDR4 ECC | 1 TB M.2 NVMe | 2 × 10 Gbps, 30 TB | [Check live price](https://bit.ly/Spinservers) |
| San Jose, CA | 16C/32T, 1.8 GHz base | 64 GB DDR4 ECC | 1.6 TB SSD | 2 × 10 Gbps, 30 TB | [Check live price](https://bit.ly/Spinservers) |
| San Jose, CA | 16C/32T, 1.8 GHz base | 64 GB DDR4 ECC | 1.6 TB NVMe | 2 × 10 Gbps, 30 TB, 1 IPv4 | [Check live price](https://bit.ly/Spinservers) |
| San Jose, CA | 24C/48T, 1.8 GHz base | 64 GB DDR4 ECC | 1.6 TB SSD | 2 × 10 Gbps, 30 TB | [Check live price](https://bit.ly/Spinservers) |
| San Jose, CA | 16C/32T, 1.8 GHz base | 256 GB DDR4 ECC | 2 × 1.6 TB SSD, hardware RAID | 2 × 10 Gbps, 30 TB | [Check live price](https://bit.ly/Spinservers) |
| San Jose, CA | 32C/64T, 2.1 GHz base | 512 GB DDR4 ECC | 2 × 3.84 TB SSD, battery-backed RAID | 2 × 10 Gbps, 30 TB, 1 IPv4 | [Check live price](https://bit.ly/Spinservers) |

Spin Servers doesn't print a price on every dedicated configuration card, and its listing warns that pricing varies with location, hardware and availability. Third-party reviews published in October 2026 put the entry build at $79/month for the Dallas E3-1280 v5 machine, with two higher tiers quoted at $149 (dual Xeon E5-2630L v3, 256 GB DDR4, 2 × 1.6 TB SSD in RAID-1, 20 TB transfer) and $679 (quad E5-4640 v2, 768 GB DDR3, 8 × 2 TB SSD in RAID-10, 40 TB transfer). Those numbers come from review sites, not from Spin Servers' own price list, so confirm the live quote for the exact chassis you order.

One detail explains the pricing. A review describes Spin Servers as vertically integrated with a used enterprise hardware trading business, which is how mid-2010s Xeons end up at $79–$149 with dual 10 Gbps ports and 30 TB of transfer included. You get cheap cores, generous bandwidth and full IPMI console access. You don't get this year's silicon, and the same reviews note that month-to-month service generally carries no refund policy, so the cancellation date becomes your refund policy.

## Cloud hosting, cloud servers and managed platforms are three different purchases

The phrase "cloud based server" covers at least three products with almost nothing in common, and mainstream rankings blur them. One widely read provider list places HostGator ($4.95/month, 50–450 GB NVMe, unlimited domains, 75+ one-click installers) and DreamHost ($8.99/month, OpenStack and Ceph underneath, 30-second launches) in the same table as Kamatera, which hands you root on a custom image and an API. Hostinger sits there too at $7.19/month with LiteSpeed, a built-in CDN and up to 300 sites per isolated server. The price columns look comparable; the products do not.

Before paying, answer four questions about the plan on offer: do you get SSH as root, can you choose the OS image, can you attach block storage later, and what happens to snapshots. UpCloud includes daily snapshots retained for 24 hours on its General Purpose, High CPU and High Memory plans, with paid retention at 7, 30 or 365 days. That is a server feature. A managed WordPress plan at a similar price gives you a control panel and a site limit instead, and you cannot install a kernel module or run a database version the host hasn't approved.

## Where a cheap cloud based server bill actually comes from

The billing model decides the second and third invoice. UpCloud's Cloud Native plans charge CPU and memory only while the server is powered on, but storage and public IP addresses bill continuously because they stay allocated. Its Starter and Premium plans bill 24/7/365 until you delete the instance. A cluster that idles every night looks cheap on the compute line and less cheap once the volumes and IPs are counted.

Kamatera runs both models side by side. Monthly servers are prepaid for the configuration you chose, with prorated charges for upgrades made later. Hourly servers bill differently depending on whether the machine is powered on or off, and billing stops when you terminate rather than when you power down.

Trials have their own terms, and the summaries usually leave them out. Kamatera's 30-day trial requires a valid credit card, allows one server with a configuration costing up to $100, and includes 1 TB of traffic counting both inbound and outbound. Stay inside those limits and the card isn't charged; do nothing and billing starts when the trial ends. Cloudways takes the opposite approach with a three-day trial that doesn't ask for a card, which is a shorter window with less friction.

Renewal structure is the third variable. Tencent Cloud's Lighthouse ran an April 2026 promotion with a 4 vCPU / 4 GB plan at 38 CNY for the first year on a first order, plus a 2 vCPU / 2 GB plan at 99 CNY with same-price renewal allowed once, making two years 198 CNY. Those were limited-time, first-order prices and shouldn't be read as current, but the shape is everywhere: a first-year number that isn't the ongoing number. Work out first year plus two renewals before you commit to anything.

On the fixed-resource side the arithmetic is simpler. Spin Servers bills month to month with no setup fee and no annual contract, so the $39.00 on the 6 vCPU plan is the number you pay again next month. 👉 [Check how Spin Servers prices its monthly KVM plans](https://bit.ly/Spinservers)

## Reading uptime promises: 99.9% is roughly eight hours a year

| Promise | Downtime per year | Where it appears |
| --- | --- | --- |
| 99.9% | ~8 h 46 min | Kamatera's product page; Hetzner's SLA with defined credits |
| 99.99% | ~53 min | UpCloud's Starter tier |
| 99.999% | ~5 min | UpCloud's platform SLA |
| 99.9999% | ~32 s | Hostwinds' advertised guarantee |

Two things matter beyond the headline figure. First, whether the promise covers the platform or your individual instance: UpCloud advertises 99.999% for the platform while its Starter plans carry 99.99%, and a single VM can't outperform the host it sits on. Second, whether there are credit terms attached. Hetzner publishes an SLA with clearly defined credits in the event of a malfunction; an uptime badge with no remedy clause is a marketing line. Kamatera's 99.9% comes from its own product page, which is the number to trust over the 99.95% repeated in third-party roundups.

## Limits that decide fit before price does

**Port 25 is closed on every Spin Servers VPS.** The company closes SMTP by default to limit IP abuse, requires a support ticket with a justification to open it, and reserves the right to refuse. If your application sends mail directly rather than through a relay, budget an afternoon for that ticket or pick an external SMTP service.

**Inventory isn't guaranteed.** Hetzner's shared cloud plans showed "Currently not available" on the page I checked, leaving the dedicated-vCPU line as the orderable option. Its regions are Germany (Falkenstein, Nuremberg), Finland (Helsinki), the US (Hillsboro, Ashburn) and Singapore.

**Old silicon is cheap for a reason.** The E3-1280 v5 and E5-2630L v3 are mid-2010s server chips, and one San Jose configuration still uses DDR3. They handle web serving, VPNs and game servers well, which is what Spin Servers lists them for. Per-core throughput won't match a current-generation cloud instance; UpCloud quotes a Geekbench improvement of more than 37% for a 2 vCPU / 4 GB plan running on 5th-gen AMD EPYC.

**Compliance work stays with you.** Spin Servers advertises PCI-compliant facilities, and a review points out that managed PCI compliance services aren't part of the package. The building is certified; the paperwork is yours.

## Matching the plan to the job

- **One blog, a portfolio site or a staging box** under 2 GB of RAM: the cheapest entry VM you can find, €3 to $6, and no reason to pay more.
- **A production API that needs root, custom images and snapshots**: an IaaS VM with documented snapshot retention, not a managed hosting plan with a similar sticker price.
- **A workload that only runs during business hours**: a plan billed per powered-on hour, with storage and IP charges added back in.
- **Anything that sends email**: check the port 25 policy before you migrate, not after.
- **Several machines that need to talk privately**: Spin Servers includes VPC networking with Layer 2 connectivity between its servers at no extra cost, which is cheaper than paying a managed-cloud premium for the same topology.
- **Heavy sustained transfer**: 30 TB a month averages about 93 Mbit/s, so a 10 Gbps port is burst headroom rather than a monthly allowance. The allowance is what you'll hit first.

## FAQ

**What's the difference between cloud hosting and a cloud server?**
Cloud hosting usually means a managed slice of a web stack with a control panel and site limits. A cloud server gives you root access, your own OS image and an API. The first is easier to run; the second is the only one where you control the kernel and the database version.

**Is hourly billing cheaper than monthly?**
Only if the machine is off for a meaningful part of the month. Kamatera's hourly servers bill according to power state, and UpCloud's Cloud Native plans stop charging for CPU and memory when powered off while storage and IPs keep billing. A server that runs all month is usually cheaper on a monthly plan.

**Will a free trial start charging me automatically?**
With Kamatera, yes: the 30-day trial needs a card, covers one server up to a $100 configuration and 1 TB of traffic, and converts to paid billing if you don't terminate before it ends.

**Do I need a 10 Gbps port?**
Only if you push past roughly 1 Gbps for real. Monthly transfer allowances usually run out long before port speed does.

## Before you order

Two checks save most of the surprises. Confirm the billing model and the cancellation terms in writing, because "powered off" and "not billed" are different states at more than one provider, and month-to-month plans often skip refunds entirely. Then confirm the two physical constraints: the datacenter location relative to your users and your compliance obligations, and whether port 25 is open if anything on the box sends mail.

If your workload is a small site, stay in the entry bracket and spend the difference on backups. If it's 4 to 16 vCPU with real transfer volume and you'd rather pay a flat monthly rate than model storage and egress line items, the 6 vCPU plan at $39.00 is the natural starting point. 👉 [See Spin Servers' current VPS and dedicated configurations](https://bit.ly/Spinservers)
