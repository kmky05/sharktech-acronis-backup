# online server backup: How Sharktech's $4/Month Acronis Plan Works, Which Billing Cycle Actually Costs Less, and Who Should Skip It

Anyone searching for online server backup is usually trying to answer one question: if my server dies tonight, how fast can I get it back, and what will protecting it cost every month? The short version for this article: Sharktech sells a hosted Acronis Cyber Protect backup service starting at **$4/month with 200 GB of storage included**, billed per GB beyond that, protectable across Windows, Linux, macOS, and virtualized workloads. This article walks through what you actually get, the full price breakdown across all four billing cycles (including a catch in the overage math that most coverage of this service gets wrong), how it stacks up against buying Acronis directly, and which situations it doesn't fit.

> **Quick pick:** For most people running one to a handful of servers, the 200 GB monthly plan at $4.00/month with $0.02/GB overage is the sensible entry point — month-to-month, no long commitment, and you can resize storage anytime in the portal. 👉 [configure the 200 GB monthly plan in Sharktech's portal](https://portal.sharktech.net/cart.php?a=add&pid=648&configoption%5B1862%5D=200&configoption%5B1863%5D=0&billingcycle=monthly&aff=1626)

## What Sharktech's online server backup actually is

Sharktech's backup product is a resold and hosted version of **Acronis Cyber Protect**, the same backup-and-security platform that enterprise IT teams use directly. Sharktech runs it on its own infrastructure and sells it as a storage-based add-on service rather than a per-device license. The official product page describes it as protection for "physical servers, virtual machines and cloud workloads" across supported Windows, Linux, and macOS systems, with application and database protection depending on workload support and the license tier you select.

A few things matter about this arrangement:

- You get genuine Acronis, with the invoice showing Acronis Cyber Protect — relevant if compliance requirements or client contracts name the platform.
- Storage is billed **per GB**, not per server. Backing up five small machines into 200 GB costs the same as backing up one larger one into the same space.
- The Acronis web console is separate from any server control panel. You register machines, set schedules, and manage retention from one dashboard regardless of how many systems you protect.
- Sharktech's technical team provides 24/7 support on the service.

Sharktech itself is a hosting and DDoS-protection provider founded in 2003, with data centers you can pick from at checkout: Los Angeles, Las Vegas, Denver, Chicago, and Amsterdam. If your servers are also hosted with Sharktech, backup traffic between your machines and the backup target stays within one provider's network, and both services fall under the same support team.

## Full pricing: every billing cycle Sharktech currently offers

There are no tiered packages to compare — it's a single configurable product (Acronis Cloud Backup) with four billing cycles, each built on the same base: 200 GB of Cloud Backup & Protection storage. Beyond that you pay an overage rate per extra GB, and File Sync & Share is a separate optional add-on billed per GB. The official product page states plans "start at $4/month" with the final recurring price confirmed in the customer portal at checkout.

| Billing cycle | Price | Included storage | Overage (per extra GB) | File Sync & Share add-on | Order |
| --- | --- | --- | --- | --- | --- |
| Monthly | $4.00/mo | 200 GB | $0.02/GB | $0.03/GB/mo | [ order monthly](https://portal.sharktech.net/cart.php?a=add&pid=648&configoption%5B1862%5D=200&configoption%5B1863%5D=0&billingcycle=monthly&aff=1626) |
| Quarterly | $8.00/qtr | 200 GB | $0.04/GB | $0.06/GB/qtr | [ order quarterly](https://portal.sharktech.net/cart.php?a=add&pid=648&configoption%5B1862%5D=200&configoption%5B1863%5D=0&billingcycle=quarterly&aff=1626) |
| Semi-annual | $12.00/6mo | 200 GB | $0.06/GB | $0.12/GB/6mo | [ order semi-annual](https://portal.sharktech.net/cart.php?a=add&pid=648&configoption%5B1862%5D=200&configoption%5B1863%5D=0&billingcycle=semiannually&aff=1626) |
| Annual | $24.00/yr | 200 GB | $0.12/GB | $0.24/GB/yr | [ order annual](https://portal.sharktech.net/cart.php?a=add&pid=648&configoption%5B1862%5D=200&configoption%5B1863%5D=0&billingcycle=annually&aff=1626) |

Location (one of the five data centers above) and both storage sliders are chosen on the same configuration page before checkout.

### The overage math most articles get wrong

Here's the increment worth pausing on. The monthly plan's $0.02/GB gets headlined as the "lowest overage rate," and it is — per month. But that rate recurs every month, which annualizes to **$0.24 per extra GB per year**. The annual plan's listed $0.12/GB applies to the year, and the semi-annual rate works out the same ($0.06 twice a year). Quarterly annualizes to $0.16/GB.

Run a realistic example: a dataset that settles at 2 TB (about 1,848 GB over the included 200 GB).

- Monthly: $4 + (1,848 × $0.02) = $40.96/month, or roughly $491/year
- Annual: $24 + (1,848 × $0.12) = $245.76/year, about $20.48/month

The annual plan costs half as much at that size. The monthly plan only makes sense when you value flexibility, expect your storage to shrink, or want to test the service before committing. One honest caveat: the listed rates are per billing cycle, and the exact behavior of overage metering should be confirmed against the live total the cart shows before you pay — which is easy to do, because the configuration page displays your running price as you adjust storage. 👉 [open the cart, set your real storage figure, and see the live total](https://portal.sharktech.net/cart.php?a=add&pid=648&configoption%5B1862%5D=200&configoption%5B1863%5D=0&billingcycle=monthly&aff=1626)

### What happens if you skip File Sync & Share

Nothing. It's an optional add-on that turns part of your backup storage into a Dropbox-style synced and shareable drive. If you only want server backups, leave the slider at zero and you pay nothing for it. Managed-server customers commonly skip it; resellers and MSPs who bundle file sharing for clients tend to enable it.

## What you get beyond raw storage

The Acronis platform underneath is where this service earns its keep, and it covers several failure modes that simpler file-backup tools don't:

1. **Granular restore.** Recover a single deleted file, a set of folders, or an entire machine from the same backup chain. This matters more than it sounds: one widely shared account on Reddit describes a 400 GB restore through a control-panel backup tool that spent over five hours just zipping the files before the download kept failing, forcing the user to pull data in 50–80 GB batches. Being able to mount a recovery point and grab exactly what you need avoids that mess entirely.
2. **Bare-metal recovery to different hardware.** A dead server can be restored onto dissimilar hardware without first reinstalling the OS — the difference between hours and days of downtime when the original machine is unrecoverable.
3. **Anti-ransomware protection.** Acronis's Active Protection monitors processes and blocks suspicious encryption behavior before files get scrambled, and backups can be scanned for malware before you restore, so you don't reinfect the machine from your own safety copy.
4. **Schedules and retention you control.** You choose when backups run and how long recovery points are kept, per machine.
5. **Encryption and access controls** built into the platform; additional security and disaster-recovery features depend on the selected license.
6. **Storage-side deduplication and compression**, which is partly why per-GB pricing can stay low — identical blocks across machines and retention points don't each consume billable space.

One practical limitation the official page states plainly: recovery time depends on data size and the restore method you pick, and Sharktech recommends making recovery testing part of your regular operations. A backup you've never test-restored is a hope, not a plan.

## How it compares with the alternatives

Against **buying Acronis directly**: the direct channel licenses per workload (per server, VM, or workstation) and sells security, DR, and other modules as separate SKUs. PCMag's review of Acronis Cyber Protect 17 — which scored it Editors' Choice at 4.5/5 — lists cloud storage tiers from 250 GB at $229/year up to 5 TB at $3,309/year on top of licensing. For a single-server owner, Sharktech's $24/year annual plan with 200 GB included sits far below that entry point, which is the core argument for buying through a hosting partner. The trade-off is that direct Acronis gives you the vendor relationship and the full add-on catalog; Sharktech gives you flat storage pricing and one bundled tier.

Against **Veeam- or MSP-style hosted backup**: Veeam focuses purely on backup and relies on third-party tools for threat detection, while Acronis integrates an anti-malware layer into the same agent and console. That integration is included in what Sharktech resells rather than priced as a separate product.

Against **doing it yourself** (scripts to object storage, external drives, cPanel backups): you keep the lowest possible bill but own every failure mode — retention, encryption, verification, and the restore-path problems described above. The $4 entry price exists precisely because the "I'll set up a cron job and an S3 bucket" approach tends to stay on the to-do list until the day it's needed.

## Who this fits, and who should look elsewhere

Reasonable fit:

- You run **1–10 machines** (dedicated servers, VPSes, or a mix with some VMs) and want off-site backup with ransomware protection for single-digit dollars per month.
- Your servers are already with Sharktech, and you'd rather have backup and compute under one provider and one support number.
- You need real Acronis on the invoice for compliance or client-facing reasons but don't want per-workload quoting.

Poor fit, stated plainly:

- **Multi-hundred-TB archives with custom multi-region retention policies.** The storage slider caps at 100,000 GB per configuration, and there's no indication of multi-region replication within one order. Hyperscale buyers belong with enterprise backup vendors or public-cloud object storage.
- **Anyone who needs managed, hands-on backup administration.** This is a self-service add-on. Sharktech's engineers answer questions 24/7, but someone on your side owns the schedules, retention, and restore tests.
- **Buyers who require a refund guarantee.** Sharktech doesn't prominently publish a money-back policy for this service, and third-party review profiles (a small Trustpilot sample around 3.5) mention the absence of refund guarantees among complaints. Treat the monthly plan as your de facto trial period and confirm terms with support before a large annual prepay.

## Setting it up, step by step

The order itself takes a few minutes:

1. Open the Acronis Cloud Backup configuration page and pick a data center location (Los Angeles, Las Vegas, Denver, Chicago, or Amsterdam). Choosing one geographically distant from your servers is the whole point of off-site backup.
2. Set the **Cloud Backup & Protection** slider. The default configuration is 200 GB; estimate your total protected dataset after compression, then round up.
3. Set **Files Sync & Share** to 0 unless you specifically want the file-sharing add-on.
4. Pick a billing cycle — start monthly if you're unsure, per the overage math above.
5. Confirm the itemized total at checkout. The product page explicitly warns that optional services may be priced separately, so check each line before paying.

After checkout, the work shifts to the Acronis web console: install the agent on each machine, register it, define backup schedules and retention, and then — this is the step everyone skips — run a test restore of a few files. The console also shows backup status, activity, reports, and storage consumption, and flags failed jobs, which is where you'll notice if a dataset quietly outgrows your allocation. 👉 [set up Acronis Cloud Backup with 200 GB included](https://portal.sharktech.net/cart.php?a=add&pid=648&configoption%5B1862%5D=200&configoption%5B1863%5D=0&billingcycle=monthly&aff=1626)

## FAQ

**Does the 200 GB count compressed or raw data?** The plan includes 200 GB of billable backup storage, and Acronis applies deduplication and compression on the storage side, so raw data typically consumes less space than its on-disk size. The console's storage-usage view shows your actual consumption.

**Is File Sync & Share included in the base price?** No. It's a separate per-GB add-on that defaults to 0 GB in the cart and only costs money if you enable it.

**Can I protect servers not hosted by Sharktech?** The product page places no restriction on where protected machines live — the Acronis agents cover supported Windows, Linux, macOS, and virtualized systems anywhere — though the same-network advantage only applies to Sharktech-hosted servers.

**Can I change storage or billing cycle later?** Storage is a slider on the same configuration, so you can adjust capacity in the customer portal; switching billing cycles means starting the service on the new cycle. Confirm specifics with Sharktech's 24/7 support before making changes mid-term.

## The bottom line before you order

If you're protecting a single busy server whose backups land around 250–300 GB, the **annual plan at $24/year** is the cheapest route as long as you've confirmed the overage behavior at your data size. If storage needs are still moving, or this is your first proper backup setup, **monthly at $4** keeps the exit door open for the price of two coffees. If you're in the multi-TB, multi-region, custom-retention territory, this product was never aimed at you, and forcing it will end in frustration.

Whatever you pick, set the storage slider to your real estimated dataset first — the cart shows the exact recurring total before you commit. 👉 [start with the 200 GB plan and check your configured price](https://portal.sharktech.net/cart.php?a=add&pid=648&configoption%5B1862%5D=200&configoption%5B1863%5D=0&billingcycle=monthly&aff=1626)
