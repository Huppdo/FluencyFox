# Tandem: next-quarter plan

October 17, 2026 · Dominic

## Summary

Recommendation: allocate next quarter's capacity to sync reliability, SSO for Brightwell Logistics, teammate invite prompts and mobile onboarding. These four items, plus 1 week to scope an AI assistant v1, use 30 of 36 engineer-weeks, leaving 6 weeks of contingency against the ±25% estimate range. Calendar sync, the AI task assistant, Gantt view and dark mode are deferred. Each has supporting demand, but none currently has evidence comparable to the sync-related churn and support data or Brightwell's written $180k commitment.

## What the data says

- **Sync is the main problem.** Sync tickets have nearly quadrupled since the July offline-mode launch, and sync is the top reason teams give for cancelling.
- **Churn is rising.** Monthly paid churn went from 3.1% in Q1 to 4.4% last month.
- **New teams struggle on mobile and when they work alone.** Mobile signups activate at half the web rate or less, and teams that invite teammates early keep paying much longer.
- **Only one ask has revenue attached.** Brightwell's $180k-a-year contract depends on SSO shipping by quarter end.

## Prioritized Plan

| Order | Item | Eng-weeks | If +25% | Running total | Why it's in |
| --- | --- | --- | --- | --- | --- |
| 1 | A. Sync reliability fix | 12 | 15 | 12 | Largest support and churn signal. Starts week 1. |
| 1 | E. SSO (SAML) | 6 | 7.5 | 18 | Brightwell's $180k depends on it, with a hard date. Starts week 1, in parallel with A. |
| 2 | C. Teammate invite prompts | 3 | 3.75 | 21 | Lowest-cost test of the teammate-invite gap above. |
| 3 | B. Mobile onboarding redesign | 8 | 10 | 29 | Targets the mobile activation gap above. |
| 4 | F. AI assistant v1 scoping | 1 | 1.25 | 30 | Committed in the CEO message: engineering input to scope a narrow v1. The full build stays in Skipped Work. |
|  | **Reserve** | **6** |  | **36** | Covers overruns. At +25% the planned items take 37.5 weeks, so B is the first to shrink. |
| Potential | D. Calendar sync (scoping) | From reserve |  |  | Only if the reserve is unused at week 8. The full build stays in Skipped Work. |

The order follows risk and deadline. Mobile onboarding goes last because it is the item to cut or shrink if A or E run over.

A few questions still need answers before this plan is committed (see Outstanding Questions).

## Skipped Work

The 29 requested weeks in the plan plus 44 deferred is the full 73 requested. Items are compared by estimated paid-plan votes, since paying teams are the ones at risk.

| Item | Eng-weeks | Paid votes (est.) | Why it waits |
| --- | --- | --- | --- |
| D. Calendar sync | 10 | ~800 | The strongest deferred case: 18% of exit-survey answers and the most paid demand on the board. Swapping it for B would cut the reserve to 4 weeks. It may also touch the sync layer we are rewriting; Engineering to confirm. First in line for next quarter. Scoping is also listed as a potential use of the reserve in the Prioritized Plan. |
| F. AI task assistant v1 | 16 | ~150 | 44% of capacity. No customer or revenue commitment, and weak demand evidence (see Outstanding Questions). We scope a narrow v1 this quarter instead, using 1 engineer-week in the plan (see Message to the CEO). |
| H. Gantt / timeline view | 14 | ~280 | No churn or support signal behind it, and it costs more than SSO and invite prompts combined. |
| G. Dark mode | 4 | ~190 | Most votes on the board (2,140), but 9% of voters pay and it appears in no churn data. It would use more than half the reserve. |

## Success Metrics

| Metric | Baseline | Target | When |
| --- | --- | --- | --- |
| Sync tickets per month | 520 | 200 or fewer (pre-July was 140) | 8 weeks after the sync fix ships |
| Brightwell contract signed | Not signed | Signed, $180k a year | End of next quarter |
| Mobile week-1 activation (iOS and Android) | 20% (3,260 of 16,000) | 26% | 30 days after onboarding ships |

Guardrail: monthly paid churn back to 3.6% (the Q2 level) or lower by the end of the quarter. Churn lags, so I won't judge the sync fix on it alone. For invite prompts I'll first set a baseline for the share of new teams inviting 2+ teammates in 14 days.

## Message to the CEO

> The AI assistant isn't in next quarter's build. Here's why.
>
> At 16 engineer-weeks it would take 44% of our capacity, while sync is costing us customers now. Sync tickets went from 140 to 520 a month, and 31% of cancelling teams named sync or lost changes as the main reason. An assistant built on unreliable sync won't keep anyone.
>
> The 68% figure came from 41 people on the AI waitlist. It shows interest from people who already opted in, not demand across our paying teams.
>
> This quarter I'll scope a narrow v1 with design and engineering and test it with paying teams, so we can start building at the top of next quarter.
>
> Can we talk this week? I need to know whether "this half" is a board commitment, and whether a smaller v1 would meet it.

## Outstanding Questions

Most of these come down to one request: a team-level extract from Data and Support with plan, dates, churn, survey responses and ticket history. None of them changes the order of the plan, but they decide how big the problem is and how we report results.

| What I don't trust | Why | How I'd check |
| --- | --- | --- |
| Funnel conversions | 976 paid conversions in 90 days on a base of 1,400 paying teams implies much faster growth than ARR shows. "Converted" may count users, not teams. | Ask Data how conversions are counted, and for starting teams, cancellations, downgrades and reactivations. |
| Retention split | It covers 1,400 teams, the same as all paying teams, but should only include teams that started paying 6–12 months ago. It is six-month survival, not monthly churn, and it shows correlation. | Pull the real 6–12 month cohort from the team extract. Treat invite prompts as a test. |
| Exit survey | 312 responses in 3 months, but last month's churn rate implies about 185 cancelled teams. There may be several responses per team. No team IDs. | Map responses to teams; count one answer per team. |
| Cause of the sync spike | The rise started with the July offline-mode launch. Timing is not proof. | Ask Support for tickets per active team, tagging changes and offline-mode use. Ask Engineering for incident data and a before-and-after comparison around the July release. |
| 4.4% churn | One month. A warning, not yet a trend. | Ask Finance or Data for a churn timeline: pricing, renewals, competitor moves, customer mix. |
| AI survey (68%) | 41 respondents, all on the AI waitlist. | Survey a random sample of paying teams. |
| Feature votes | All-time votes, mostly from free users. | Count distinct paying teams per request. |
| Estimates and staffing | ±25%, with no dependencies or staffing in the data. With several engineers on it, the 12-week sync fix may finish well inside the quarter. | Engineering breaks down A and E and maps dependencies, staffing and the critical path. |
| Brightwell's SSO requirements | The commitment is reported by Sales. Signed scope, deadline and identity provider are unconfirmed. | Sales confirms Brightwell's signed scope, deadline and SSO requirements, including which identity provider they use. |

## Assumptions

- **Capacity.** 36 engineer-weeks is net of on-call and maintenance, as the brief states.
- **Revenue per team.** $1,714 ($2.4M ÷ 1,400 paying teams). The brief rounds this to $1,700; the gap is under 1%.
- **Estimates.** Taken as given, at ±25%, with no dependencies between items.
- **Brightwell.** The $180k commitment holds as reported by the Head of Sales, and 6 weeks of SSO work meets their requirements.
- **Sync.** The fix is expected to reduce sync tickets and sync-related churn.
- **Paid votes.** Estimated as votes × share of voters on a paid plan, assuming that share applies evenly across votes.
- **AI scoping.** 1 engineer-week is my estimate; the data has none for scoping work.
- **Mobile activation target.** 26% is a judgment call; the data has no benchmark beyond the 44% web rate.

## Appendix: sources

- **Source data:** tandem_data.xlsx, six tabs (signup funnel, retention, churn and support, feature requests, stakeholder asks, engineering estimates). ARR, paying teams, price and capacity come from the FluencyFox assessment brief.
- **Dashboard:** [Tandem planning dashboard](https://claude.ai/artifact/42CRBMugQ25EjJH4Hm1SPX). Charts the workbook, with calculated conversion rates, estimated paid votes and data consistency checks. Private until shared.
