# Cheap RDP VPS: Is Evoxt's $2.99 Plan Enough for Windows, Which Plan Fits Your Workload, and What to Confirm Before You Prepay (Full Plan Table)

Evoxt's cheapest plan that can actually carry a Windows desktop is **VM-1 at $5.99/month**: 1 vCPU, 2 GB RAM, 20 GB storage, 500 GB monthly transfer, weekly offsite backup included. The $2.99 VM-0.5 gets you 512 MB of RAM, which is not a machine anyone can drive through Remote Desktop.

The plan price is the easy part. Evoxt's Windows VPS page lists the same monthly figures as its standard pricing page, with no separate Windows licence line and no stated number of RDP users. Those two blanks decide what you really pay, so this piece goes through every plan, the RAM floor for Windows, per-workload picks, and the questions Evoxt's pages leave open.

> Most people shopping for a cheap RDP VPS here should start at **VM-1 ($5.99/month)** for a single Windows desktop, or **VM-2 ($11.99/month)** if the box will run a trading terminal or automation around the clock and you want 4 GB of RAM to work with. Skip VM-0.5 and VM-0.75 for Windows entirely.
>
> 👉 [Check Evoxt's current plan prices and deploy a Windows VM](https://bit.ly/EvoXt)

## Every Evoxt plan on the pricing page

All prices in USD per month, taken from Evoxt's pricing page. Every plan includes a weekly offsite backup at no cost, browser-based VNC console access, VM cloning and sub-accounts. Evoxt also sells prepaid terms from one month up to three years, and you can park credit on the account for future invoices.

| Plan | CPU / RAM | Storage | Monthly transfer | Price (USD/mo) | Deploy |
| --- | --- | --- | --- | --- | --- |
| VM-0.5 | 1 core / 512 MB | 5 GB | 250 GB | $2.99 | [Deploy VM-0.5](https://bit.ly/EvoXt) |
| VM-0.75 | 1 core / 1 GB | 10 GB | 250 GB | $4.99 | [Deploy VM-0.75](https://bit.ly/EvoXt) |
| VM-1 | 1 core / 2 GB | 20 GB | 500 GB | $5.99 | [Deploy VM-1](https://bit.ly/EvoXt) |
| VM-1.5 | 2 cores / 2 GB | 20 GB | 500 GB | $6.95 | [Deploy VM-1.5](https://bit.ly/EvoXt) |
| VM-2 | 2 cores / 4 GB | 30 GB | 1,000 GB | $11.99 | [Deploy VM-2](https://bit.ly/EvoXt) |
| VM-3 | 4 cores / 4 GB | 30 GB | 1,000 GB | $14.99 | [Deploy VM-3](https://bit.ly/EvoXt) |
| VM-4 | 4 cores / 8 GB | 60 GB | 2,000 GB | $23.99 | [Deploy VM-4](https://bit.ly/EvoXt) |
| VM-6 | 8 cores / 8 GB | 60 GB | 2,000 GB | $29.99 | [Deploy VM-6](https://bit.ly/EvoXt) |
| VM-8 | 8 cores / 16 GB | 80 GB | 3,000 GB | $47.99 | [Deploy VM-8](https://bit.ly/EvoXt) |
| VM-12 | 16 cores / 16 GB | 80 GB | 3,000 GB | $60.95 | [Deploy VM-12](https://bit.ly/EvoXt) |
| VM-16 | 16 cores / 32 GB | 100 GB | 5,000 GB | $95.99 | [Deploy VM-16](https://bit.ly/EvoXt) |

The headline spec across the range is clock speed: Evoxt lists every core as running up to 6.0 GHz. For the things people usually put on a cheap RDP VPS, a trading terminal, an accounting client, a bot that runs one thread and waits, single-core speed matters more than core count.

## What "cheap" turns into once Windows is on the box

Four costs sit outside the plan name, and only one of them is visible on Evoxt's pages.

**The Windows licence.** Nothing on Evoxt's Windows VPS page or pricing page charges separately for it. The Windows page repeats the same $2.99 to $95.99 ladder, so either the licence is inside the number or it appears in the cart at deploy. Ask support before you commit, because a per-vCPU licence fee can turn a $5.99 plan into a $12 plan. For scale, MassiveGRID publishes its licence add-on at $6.31 per vCPU on top of a $3.99 entry price.

**The number of people who can log in.** Windows Server normally allows two administrative sessions; anything past that needs RDP user licences, which MassiveGRID sells at $8.90 per user per month. Evoxt's pages state no session limit at all. One person is safe on any plan. If two or three people need to be on it at once, get the answer in writing first.

**Memory and disk.** 512 MB and 1 GB are Linux territory. Windows itself eats well past a gigabyte at idle, and a browser plus a desktop app will push 2 GB hard. Storage is the other squeeze: 20 GB on VM-1 is thin once Windows, updates and one or two applications are installed. VM-2 gives you 30 GB and 4 GB of RAM for $6 more.

**Add-ons.** The only extra price shown on the pricing page is an additional IP at $3/month. Evoxt says you can add individual resources without changing plans, but extra disk pricing isn't listed, so ask what a storage bump costs before you build around a 20 GB VM.

👉 [See Evoxt's current monthly price for VM-1 and what the cart adds](https://bit.ly/EvoXt)

## Picking a plan by what you'll actually run

**One person, a desktop and a browser.** VM-1 at $5.99 is the floor. VM-1.5 at $6.95 keeps the same 2 GB of RAM and 20 GB disk but doubles you to 2 cores for 96 cents more, which is the better buy if you'll run a browser with a dozen tabs next to your work app.

**A trading terminal or 24/7 automation.** VM-2 at $11.99. Two cores, 4 GB, 30 GB and 1,000 GB of transfer. MetaTrader with several charts and an expert advisor, or a scheduled browser automation script, fits here with room to spare. If the strategy is latency-sensitive, the region you deploy into matters more than the plan tier.

**Two or more people on separate sessions.** Start at VM-2 for headroom, move to VM-3 ($14.99, 4 cores) if both sessions are heavy. Sort out the session licensing question before you buy, not after.

**SQL, IIS or a line-of-business app.** VM-4 at $23.99 (4 cores, 8 GB, 60 GB) is the sensible entry, with VM-6 at $29.99 if the database and the web server share the box.

**Compiling, encoding, batch jobs.** VM-8 and up. The 6.0 GHz claim helps here too, but shared vCPU on a $47.99 plan won't hold peak clocks for hours the way a dedicated core would.

👉 [Start a VM-2 deployment on Evoxt](https://bit.ly/EvoXt)

## What Evoxt's pages don't answer

Windows version. The OS list says "Windows RDP" without naming Server 2019, 2022 or 2025 builds in the material available. If your software needs a specific build, ask before ordering.

Windows 10. Microsoft ended support on 14 October 2025 and it no longer receives security updates. Cheap Windows 10 RDP boxes are still sold elsewhere for software that was never validated on Windows 11, and that is the only reason to run one now.

Location. The plan table doesn't show datacenters, and RDP is latency-sensitive: a 200 ms round trip makes a desktop feel sticky. Third-party write-ups describe separate network tiers including an Asia-focused option, so confirm which region you're landing in at deploy.

Refunds. No money-back term appears on the pricing or Windows VPS pages. That alone is a reason to start monthly rather than prepay three years.

Third-party feedback. It isn't uniformly positive. A GitHub-hosted review roundup points to mixed Trustpilot scores, with complaints centred on IP blocks and abuse flags, and cites a disputed-refund thread on Reddit. If your workload involves proxies, scraping or high connection rates, monthly billing is the sensible first step.

👉 [Compare Evoxt's Windows plans before you prepay for a year](https://bit.ly/EvoXt)

## Two competitors, for price context only

| Provider | Windows/RDP entry | Licence and RDP users published? | Billing |
| --- | --- | --- | --- |
| Evoxt | VM-1, $5.99/mo, 2 GB RAM | No | Monthly up to 3 years, prepaid credit |
| MassiveGRID | $3.99/mo for 1 GB on a 180-day Windows Server evaluation; licence +$6.31/vCPU | Yes: two admin sessions included, extra users $8.90/user/mo | Monthly |
| LightNode | $7.71/mo, or $0.012/hour | Not in the entry pricing | Hourly or monthly |

MassiveGRID's $3.99 is the clearest illustration of the trap in this market: that number buys an evaluation build that must be activated within 10 days and runs 180 days before the machine shuts down hourly until a licence is added. Its Windows 11 Pro option starts at $4.79 with 2 GB RAM minimum on your own key. LightNode's advantage is the hourly meter, useful for a two-week project you don't want to pay a month for.

Evoxt's position is different: identical list prices across Linux and Windows, monthly-to-three-year prepay, and a free weekly offsite backup on every tier.

## Who shouldn't buy this

You need a documented licence and CALs before signing: Evoxt doesn't publish either, and a business that has to show compliance should buy where the paperwork is on the page.

You need hourly billing: Evoxt's shortest term is a month.

You need managed support, patching or monitoring: this is self-managed infrastructure.

You need long stretches of full-core CPU: shared vCPU plans at these prices aren't built for it.

You need a lot of disk: the largest plan tops out at 100 GB.

## FAQ

**Is the Windows licence included?**
Not stated on the Windows VPS page or the pricing page, which show the same monthly prices as the Linux tiers. Confirm the total in the cart or with support before paying.

**How many users can connect at once?**
Evoxt doesn't publish a session limit. Windows Server typically ships with two administrative sessions, and more requires RDP user licences.

**Is the $2.99 plan enough for Windows?**
No. 512 MB won't hold a Windows desktop plus an application. It's a fine small Linux box.

**Can I upgrade later?**
Yes. Evoxt says you can scale at any time and add individual resources without switching plans. An extra IP costs $3/month.

**How do I pay?**
Billing runs monthly up to three years, and account credit is applied to future invoices automatically.

**Do I get backups?**
A weekly offsite backup is included on every VM at no cost, alongside browser VNC access and cloning.

## Before you order

1. Ask support, in writing, whether the Windows licence is in the plan price or added at checkout, and what version you get.
2. Ask how many concurrent RDP sessions the plan allows.
3. Confirm the datacenter region and ping it from where you'll be working.
4. Check extra disk pricing if 20 or 30 GB looks tight.
5. Start on monthly billing. Move to a longer prepaid term only after the licence, session count and refund position are confirmed.

If you want the cheapest workable Windows desktop on Evoxt, that's VM-1. If the machine has to earn its keep running something all day, it's VM-2.

👉 [Pick a plan and deploy on Evoxt](https://bit.ly/EvoXt)
