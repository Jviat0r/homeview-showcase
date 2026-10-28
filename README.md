# HomeView

A home search site built just for the Washington, DC metro. It answers the questions that actually decide a DMV move, which the national sites answer generically or not at all: what this home will really cost each month in its own county, how far the walk to Metro is, how long the drive to work is, and whether it's cheaper than renting nearby.

**Live demo:** https://homeview-dev.pages.dev
**Source:** private, available on request

## Why I built it

I'm from the DMV, and the national home sites treat it like anywhere else. Property tax, Virginia's car tax, DC's homestead deduction and each county's recording taxes all change what a home really costs each month. I wanted a search that knew those rules.

## What it does

- **Map search.** Price pins and clusters on an interactive map of MD, VA and DC with Metrorail stations. Filters for price, beds and baths, home type, size, HOA, days on market, walk to Metro, commute time, assigned school and deals. Every search is a shareable URL.
- **True monthly cost.** The payment with the home's own jurisdiction: 2026 property tax rates, DC's homestead deduction, Virginia car tax after each county's relief, HOA, PMI and insurance.
- **Cash to close.** Every recording tax with the share the buyer usually pays, including DC's and Maryland's first-time buyer breaks.
- **Rent vs. buy.** Similar rentals nearby against the true monthly cost.
- **Walk to Metro and commute.** Walking minutes to the nearest station along real streets, and drive times to 8 DMV work centers.
- **Deal radar.** Flags homes priced 20%+ under comparable homes nearby, fresh price cuts, and homes sitting 90+ days after a cut, and always says what it compared against.
- **School zones**, saved homes and searches, compare, a mortgage hub, rentals mode, dark mode, mobile layout and an offline shell.

## The hard parts

- **Getting the tax math right.** Each jurisdiction has its own rates, deductions and recording rules. Every rate comes from the jurisdiction's official source for 2026, checked against published worked examples where the county has them, and the tests pin those numbers.
- **Walk times for thousands of homes.** A build script routes about 5,000 homes to their nearest Metro station along streets (not as the crow flies) ahead of time, so the site stays a fast static app with no backend.
- **Keeping it fast.** It's prerendered with performance budgets checked in CI, so the map and listings load quickly on a phone.

## Built with

React 19, TypeScript (strict), Vite, React Router, MapLibre GL, Vitest with 88 test files, GitHub Actions CI, and Cloudflare Pages hosting.

## Status

A working portfolio project with a snapshot of about 1,900 homes for sale and 4,000 rentals across 8 DMV markets. The listing data is a one-time sample for the demo, not a live feed. The source is private. If you're reviewing my work for a role, ask me and I'll walk you through it.
