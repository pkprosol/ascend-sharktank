> **Moved. Do not edit this repo.**
> This page now lives in **[Quizzify/barracuda-tank](https://github.com/Quizzify/barracuda-tank)** as `sites/ascend/`, and is still served at https://ascend-sharktank.validationinstitute.com/ from that repo.
> Kept for history only; its Render service no longer builds from here.

# Barracuda Tank — ASCEND 2027

Static landing page for the Barracuda Tank at **ASCEND**, the conference for independent
benefits agencies and producers: **January 19, 2027**, inside ASCEND's Jan 18–21, 2027 program
at the San Diego Convention Center (attendascend.com).

Terms are Al Lewis's, 2026-10-23: "should look just like HBCH except $5000 entry fee,
$12,500 investment or $25,000 in Quizzify … conference date is January 19th. Judges can't be
named because they aren't set yet."

| | ASCEND 2027 | (Houston/HBCH, for reference) |
|---|---|---|
| Headline | $25,000 at stake | $50,000 at stake |
| Entry fee | $5,000 | $10,000 |
| Audience | 200 benefits advisors | 150–200 employers |
| Winner picks one | $12,500 investment / $5,000 cash / $25,000 Quizzify services (incl. ER Consent) | $25K / $10K / $50K |
| Judges | Four leading advisors (not yet named) | 3 employers + 1 consultant |
| Contestants | 5 | 5 |

## Wired

- **Stripe payment link** (entry fee, $5,000): `https://buy.stripe.com/9B69AUe1U3O52hJ5Pm57W0M`
  - Product `prod_VUp1UZVFIIc2Ul`, price `price_1UTpNAJlOcMZLcnPN2ZtfMyK`, Quizzify account `acct_18lgiuJlOcMZLcnP`.
  - Supersedes the $10,000 ASCEND-2026-Nashville link `plink_1TTVDcJlOcMZLcnPON0tS1TF`.
- Both "Reserve Your Spot" CTAs route to that link.
- `SPOTS_REMAINING` env var drives the scarcity counter (default `5`); `build.sh` substitutes it.

## Open

- Judging panel: four advisors, to be named here once set.
- Application deadline — recommend ~3 weeks out (mid-December 2026).
- Exact time slot within the Jan 19 program, and the room at the San Diego Convention Center.

## Deploy

Render static site `ascend-sharktank` (Quizzify workspace), auto-deploys on push to `main`.
Live at https://ascend-sharktank.validationinstitute.com
