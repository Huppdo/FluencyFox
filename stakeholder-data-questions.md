# Data questions before we commit to next quarter's plan

## Ask now: what goes in the quarter

These four decide which big items fit in the 36 engineer-weeks.

1. **Brightwell.** Is the $180k commitment signed, and what is the exact deadline? Do they need anything beyond SSO, such as a security review, user provisioning, or audit logs? Anything extra changes the 6-week estimate.
2. **AI assistant.** Is "this half" a board commitment or a goal? How many weeks of the half are left? Would a smaller first version meet it? The full version takes 16 of our 36 weeks.
3. **Team shape.** How many engineers make up the 36 weeks, and how many work on web vs. mobile? The sync fix is 12 weeks of work in a 13-week quarter, so how many people can work on it at once?
4. **Dependencies.** Does calendar sync depend on the sync fix? Do the mobile onboarding redesign and the invite prompts change the same screens? This decides the order we build in.

## Data checks

A few numbers in `tandem_data.xlsx` don't line up, and they decide how big the churn problem is.

5. **Conversions vs. paying teams.** The funnel shows 976 conversions to paid in 90 days, but there are only 1,400 paying teams in total. Is "converted" counting users or teams? How many paying teams did we gain, net, last quarter?
6. **Retention vs. churn.** The retention data implies about 9% monthly churn. The churn tab says 3.1% to 4.4%. Which is right, and is churn counted by teams or by revenue?
7. **Exit survey.** 312 people answered in 3 months, but only about 150 to 185 paid teams cancelled. Does the survey include free teams, or several people per team? What do paid teams alone say?
8. **Sync tickets.** How many paying teams filed sync tickets, and how many of them later cancelled?

### Next round

9. **Ticket growth.** Sync tickets rose from 140 to 520 a month. How much of that rise comes from user growth or more people using offline mode? Did ticket categories or tagging change in July?
10. **Root cause.** Has Engineering confirmed that conflict handling causes the sync problems? Could the July offline-mode release be part of it?
11. **Last month's churn.** The 4.4% is one month of data. Did anything else happen that month, such as a price change, a competitor launch, or a batch of renewals?

### Third round

12. **Mobile signups.** Only 18% to 22% of mobile signups become active users in their first week, compared with 44% on web. Are many mobile signups people who were invited to an existing team, rather than people starting a new team? Invited people may never create 3 tasks, so they would pull the mobile rate down.
13. **Invited teammates.** Does the signup count include people who joined through an invite? If so, the same people appear in both the signup numbers and the invite numbers.
