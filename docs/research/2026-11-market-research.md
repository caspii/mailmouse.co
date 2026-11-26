# MailMouse market research — November 2026

Research date: 2026-11-26. Prices come from vendor pages and review sites as
indexed on that date. Some sources disagree; verify before quoting publicly.

## 1. Summary

- Every serious competitor charges **per member**. Volunteer groups dislike this
  because large lists are mostly passive readers. A **flat price per group** is
  the clearest pricing gap.
- The most understood pain is **"group email goes to spam."** Lists that forward
  mail "from" a member's own domain break DMARC (the check that proves who sent
  an email). Yahoo's strict DMARC policy (`p=reject`) makes this worse. A list
  that handles this by default can promise "lands in the inbox."
- The best-fit customers are **volunteer-run groups** (churches, residents'
  associations, sports clubs, alumni groups). Their members skew older, refuse
  chat apps, and the organiser changes often.
- A product angle nobody sells: **the list outlives the volunteer** (co-owners,
  handover, inactivity warnings).

## 2. Competitors and pricing

| Product | Free tier | Paid | Notes |
|---|---|---|---|
| Google Groups | Free | Free; Workspace needed for custom domains | Dated UI. Members need Google accounts for web features. Spam placement problems from DMARC alignment. Custom roles for "who can manage/view members" removed (no new ones from 2025-09-15; existing removed 2026-01-05). |
| Groups.io | ≤100 members | Premium from $20/mo ($220/yr), quoted as $0.04/member; Enterprise "custom", mirrors show $100/mo non-profit, $200/mo commercial + $0.10–0.20/member | Feature-heavy (calendar, wiki, polls, photos). US-hosted. 50% non-profit discount on Enterprise. Strong in amateur radio and open-source communities. |
| Gaggle Mail | Yes (cap unclear: 200 or 1,000 members, sources disagree) | Standard $10/mo minimum, Premium $20/mo minimum, $0.10 / $0.20 per member; Enterprise $349/mo annual | Most direct competitor. Runs a large set of SEO comparison pages ("2026 Comparison Guide" for every rival). |
| Simplelists | Trial only (1 month) | Single list from $9/mo (1 GB) or $90/yr; pay-as-you-go by data; unlimited plan priced by unique members | UK-based. Data-volume billing is hard to understand. |
| ImprovMX | 1 domain, 25 aliases, 500 emails/day | From about $50/yr | Aliases only. Free plan caps an alias at 5 recipients. No archive or moderation. |
| Forward Email | Forwarding only | Paid plans (price not confirmed) | Open source. Aliases with multiple recipients. |
| Mailman 3 | Free, self-hosted | Server cost + admin time | Needs a technical maintainer. |
| L-Soft LISTSERV | — | Enterprise licensing (not found) | Legacy, universities and government. |
| WhatsApp Communities / Discord / Slack | Free | — | The real substitute for younger groups. Older members often refuse to install them. |

### Pricing gap

All paid competitors scale cost with member count. A 400-person church list
with 30 active posters pays the same as 400 active people.

Recommended model to test (not yet public):

| Tier | Price | Limits |
|---|---|---|
| Free | €0 | 1 list, up to 25 members |
| Group | €5/month per list | up to 500 members |
| Organisation | €19/month | unlimited lists, shared admins |
| Non-profit | 50% off | proof of status |

The homepage states the *principle* (flat price per group, free for small
groups, never per member) without numbers until pricing is validated.

## 3. Deliverability as positioning

- Lists rewrite messages. When the visible From domain matches neither the SPF
  nor DKIM domain, DMARC fails and mail goes to spam or is rejected.
- Yahoo publishes `p=reject`, so Yahoo members posting to a list are a known
  failure case.
- Google's bulk sender rules (≈5,000+ messages/day to Gmail) require SPF, DKIM,
  DMARC and one-click unsubscribe, with removal within 48 hours.
- Standard fix: rewrite From to the list domain ("Jane via Book Club"), set
  Reply-To, sign with DKIM on the list domain, add ARC headers, and add
  `List-Unsubscribe` + `List-Unsubscribe-Post`.

Product requirement: MailMouse must do all of this by default. Marketing claim:
"Your group's emails land in the inbox, not spam."

## 4. Use cases

### Already on the site
Company teams, community groups, schools, research teams, non-profits.

### Missing — volunteer-run groups (highest willingness to pay)
- **Churches and faith groups.** Heavy listserv users. Older members. Prayer
  lists, rotas, announcements.
- **Residents' associations, HOAs (homeowners' associations), condo boards.**
  Need a private board list and an announce-only residents list.
- **Youth sports and parent groups.** One list per team per season. Coach
  changes every year.
- **Alumni and class reunions.** Personal emails that last decades. Activity
  spikes yearly.
- **Allotments, co-ops, choirs, amateur radio clubs.**

### Missing — professional
- **Agencies and freelancers.** One list per client project; archive at the end.
- **Boards of directors, councils.** Confidential, auditable archive.
- **Shared role addresses for tiny businesses** (`bookings@`, `orders@`) without
  paying for Google Workspace.
- **Customer advisory boards, beta-tester groups.**
- **Deal teams** across several companies (real estate, legal, construction).

### Missing — temporary
- Weddings, group trips, conferences, funerals. A list for six weeks, then gone.

## 5. Left-field ideas (ranked)

1. **The list outlives the volunteer.** Two owners minimum, inactivity warning,
   formal handover. Every club has lost a list when a secretary left.
2. **AI digest mode.** Per member: every email, or one weekly summary
   ("3 decisions, 1 question for you, meeting moved to Tuesday").
3. **Ask the archive.** Email `ask@yourgroup` a question; get an answer from
   past list emails, with a link to the source.
4. **Reply-to-vote.** "Reply 1 for Saturday, 2 for Sunday." MailMouse tallies and
   sends one result. Polls and RSVPs (event replies) without links.
5. **Bridge between generations.** Email members and WhatsApp/Telegram members
   see the same conversation.
6. **Expiring lists.** "Wedding guests — ends 1 August." Fits the privacy story
   and spreads the product to every guest.
7. **Join by QR code.** A noticeboard poster for churches, cafés, community
   centres.
8. **Paid membership lists.** Collect annual dues via Stripe; lapsed members are
   removed automatically.
9. **Duty rotas for role addresses.** `onduty@` reaches whoever is on this week.
10. **Translated delivery.** Each member receives the message in their language.
11. **Paper fallback.** Members without email get a printed letter by post.

## 6. Keyword data (Ahrefs, US, 2026-11-26)

| Keyword | Volume | KD | Traffic potential |
|---|---|---|---|
| listserv | 4,900 | 45 | 1,200 |
| distribution list | 1,200 | 0 | 500 |
| email distribution list | 1,000 | 2 | 800 |
| reply all | 900 | 7 | 1,000 |
| group email | 400 | 62 | 3,100 |
| mailing list service | 400 | 59 | 600 |
| how to create an email list | 300 | 8 | 600 |
| how to create a group email | 250 | 1 | 3,700 |
| church mailing list | 200 | 0 | 150 |
| email group | 200 | 33 | 3,100 |
| google groups alternative | 150 | 0 | 80 |
| how to make a group email | 150 | 2 | 6,500 |
| hoa communication | 150 | 0 | 80 |
| church email list | 100 | 0 | 150 |
| church email | 100 | 1 | 10 |
| group email address | 100 | 5 | 6,300 |
| email distribution list gmail | 60 | 2 | 1,000 |
| parent email list | 40 | 0 | 0 |
| how to create an email distribution list | 30 | 0 | 400 |
| groups.io alternative | 20 | — | — |
| free group email service | 20 | 49 | 24,000 |
| hoa email list | 10 | — | — |
| club email | 10 | — | — |
| google groups emails going to spam | 0 | — | — |
| listserv alternative | 0 | — | — |

KD = Ahrefs keyword difficulty (0–100). Traffic potential = traffic the #1 page
gets from all its keywords.

Takeaways:
- "Distribution list" terms are large and almost uncontested (KD 0–2).
- Church terms combine to ~400/month at KD 0–1.
- "hoa communication" is 150/month at KD 0.
- Spam-folder searches are phrased many ways; the exact phrase has no volume.
  Write the page for positioning and internal linking, not for search traffic.

## 7. Sources

- Groups.io plans: https://groups.io/helpcenter/manual/ownersgettingstarted/gs_owners/own_gs_step2.htm
- Groups.io compare / pricing: https://groups.io/static/compare , https://groups.io/static/pricing
- Gaggle Mail pricing: https://www.gaggle.email/pricing
- Gaggle subscription types: https://help.gaggle.email/article/290-whats-the-difference-between-the-types-of-subscriptions
- Simplelists products: https://www.simplelists.com/products/
- ImprovMX pricing: https://www.improvmx.com/pricing
- ImprovMX multi-recipient aliases: https://improvmx.com/guides/redirecting-alias-to-multiple-addresses
- Google Groups member-management changes: https://support.google.com/a/answer/16339383
- Workspace Updates, June 2025: https://workspaceupdates.googleblog.com/2025/06/upcoming-changes-for-who-can-manage-and-who-can-view-custom-roles-in-google-groups.html
- Why Google Group emails go to spam (Suped): https://www.suped.com/learn/email-deliverability/why-are-google-group-emails-going-to-spam-and-what-are-the-alternatives
- Google email sender guidelines: https://support.google.com/mail/answer/81126
- Help Scout, Google Groups alternatives: https://helpscout.com/blog/google-groups-alternatives
