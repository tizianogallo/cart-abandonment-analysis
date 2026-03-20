# 💼 Business Case — Reducing Cart Abandonment

**Project:** Reducing Cart Abandonment at an Undisclosed E-Commerce Platform  
**Author:** Tiziano Gallo  

---

## 1. 📌 Executive Summary

Analysis of October 2019 behavioural event data identified a cart abandonment rate of **49.07%** — meaning nearly half of all sessions that added a product to cart never completed a purchase. Across the full October dataset of 573,098 cart sessions, this represents an estimated **$134M+ in potential lost revenue in a single month**.

Three targeted initiatives are proposed to address this:
1. **Guest Checkout** — remove the forced account creation barrier
2. **Automated Cart Recovery Emails** — re-engage abandoners at 30 min, 24hr and 48hr
3. **Checkout UX Improvements** — simplify the checkout flow and add a progress indicator

Combined, these initiatives are projected to recover **$13.4M–$26.8M per month** at a low implementation cost, delivering a strong ROI within the first month of launch.

---

## 2. 📊 Current State — The Problem in Numbers

| Metric | Value |
|---|---|
| Total cart sessions (Oct 2019) | 573,098 |
| Sessions that completed purchase | 291,861 |
| Sessions that abandoned cart | 281,237 |
| Overall cart abandonment rate | **49.07%** |
| Industry benchmark abandonment rate | ~70% |
| Abandoners who never returned | 64.9% (134,344 users) |
| Abandoners who self-recovered | 35.1% (72,614 users) |
| Median time from cart to purchase | 1.8 minutes |
| 90% of purchases occur within | 7.4 minutes of cart add |
| Estimated revenue lost (Oct 2019) | **$134M+** (extrapolated from 12% sample) |

### 🔍 Root Cause Analysis

Data analysis ruled out price and product category as drivers of abandonment:
- ❌ **Price is not the issue** — abandoned and purchased items have near-identical average prices across all categories
- ❌ **Category preference is not the issue** — buyers at all hours purchase the same product mix
- ✅ **Checkout friction is the issue** — the process map identified forced account creation, no progress indicator, and session expiry with no recovery as the primary pain points

---

## 3. 💡 Proposed Initiatives & Expected Impact

### 3.1 🛒 Initiative 1 — Guest Checkout

**The problem:** The current checkout forces users to create an account before purchasing. This is the single biggest drop-off point in the AS-IS process map.

**The solution:** Introduce a guest checkout option allowing users to complete a purchase without registering.

**Evidence:** 
- Industry data shows guest checkout reduces abandonment by 8–12% on average
- 64.9% of abandoners never return — removing this barrier gives them no reason to leave

**Projected impact:**

| Scenario | Recovery Rate | Monthly Sessions Recovered | Est. Revenue Recovered |
|---|---|---|---|
| Conservative | 5% of abandoned sessions | 14,062 | ~$6.7M |
| Moderate | 8% of abandoned sessions | 22,499 | ~$10.7M |
| Optimistic | 12% of abandoned sessions | 33,748 | ~$16.1M |

**Implementation cost:** Low — standard development sprint (1–2 weeks)  
**Payback period:** Immediate — revenue recovered from day 1 of launch

---

### 3.2 📧 Initiative 2 — Automated Cart Recovery Emails

**The problem:** No cart recovery mechanism currently exists. 64.9% of abandoners never return on their own.

**The solution:** Implement a 3-email recovery sequence triggered at 30 minutes, 24 hours and 48 hours after abandonment. Emails are personalised with the abandoned product and timed to the user's local timezone.

**Evidence:**
- 35.1% of abandoners already self-recover without any nudge — with a recovery email, this could realistically reach 45–50%
- 90% of purchases happen within 7.4 minutes of cart add — the 30-minute email catches users while intent is still fresh
- Peak conversion hours (5–9am UTC) map to Asian afternoon hours — timezone-aware scheduling maximises open rates

**Projected impact:**

| Email | Trigger | Expected Recovery Rate | Sessions Recovered |
|---|---|---|---|
| Email 1 | 30 min after abandonment | 8–12% of recipients | 22,499–33,748 |
| Email 2 | 24 hrs after abandonment | 3–5% of remaining | 6,750–11,249 |
| Email 3 | 48 hrs with discount | 2–3% of remaining | 4,500–6,750 |
| **Total** | | **13–20% recovery** | **33,749–51,747** |

**Estimated revenue recovered:** $16.1M–$24.7M per month  
**Implementation cost:** Low — email service provider integration (1 sprint)  
**Payback period:** Immediate

---

### 3.3 ✨ Initiative 3 — Checkout UX Improvements

**The problem:** The current checkout has no progress indicator, too many steps, and no exit-intent mechanism.

**The solution:** Streamline checkout to 3 steps, add a progress bar, and implement an exit-intent popup.

**Evidence:**
- Converted sessions average **7.5 events** vs 4.4 for abandoned — engaged users convert, disengaged users don't
- A simpler, clearer checkout keeps users engaged longer
- Industry data shows progress indicators reduce abandonment by 3–5%

**Projected impact:**

| Scenario | Recovery Rate | Sessions Recovered | Est. Revenue Recovered |
|---|---|---|---|
| Conservative | 3% of abandoned sessions | 8,437 | ~$4.0M |
| Moderate | 5% of abandoned sessions | 14,062 | ~$6.7M |

**Implementation cost:** Medium — UX design + development (2–3 sprints)  
**Payback period:** < 1 month

---

## 4. 📈 Combined ROI Summary

| Initiative | Est. Monthly Revenue Recovered | Implementation Cost | Payback Period |
|---|---|---|---|
| 🛒 Guest Checkout | $6.7M–$16.1M | Low | Immediate |
| 📧 Cart Recovery Emails | $16.1M–$24.7M | Low | Immediate |
| ✨ Checkout UX | $4.0M–$6.7M | Medium | < 1 month |
| **Total** | **$26.8M–$47.5M/month** | **Low–Medium** | **< 1 month** |

> ⚠️ *Note: Revenue estimates are based on average product prices from the dataset and industry-standard recovery rates. Actual results will vary based on platform traffic, email open rates, and implementation quality. A/B testing is recommended post-launch to validate projections.*

---

## 5. 🎯 Priority Recommendation

Implement in the following order based on effort vs impact:

| Priority | Initiative | Effort | Impact | Recommendation |
|---|---|---|---|---|
| 1 | 📧 Cart Recovery Emails | Low | Very High | Implement immediately |
| 2 | 🛒 Guest Checkout | Low | High | Implement in Sprint 1 |
| 3 | ✨ Checkout UX | Medium | Medium | Implement in Sprint 2–3 |

**Start with recovery emails** — they require no changes to the checkout flow, can be implemented in days, and target the 281,237 sessions already being lost every month.

---

## 6. 📏 Success Metrics & KPIs

| KPI | Baseline (Oct 2019) | 3-Month Target | 6-Month Target |
|---|---|---|---|
| Cart abandonment rate | 49.07% | < 44% | < 40% |
| Cart recovery rate | 0% | 8–12% | 13–20% |
| Guest checkout adoption | 0% | > 25% | > 40% |
| Checkout completion rate | 50.93% | > 56% | > 60% |
| Revenue per session | TBD | +10% | +20% |

---

## 7. ⚠️ Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Recovery emails marked as spam | Medium | Medium | Use reputable ESP, honour unsubscribes immediately |
| Guest checkout reduces account signups | Medium | Low | Offer post-purchase account creation |
| UX changes break existing checkout | Low | High | Thorough QA and staged rollout |
| Revenue projections not met | Medium | Medium | A/B test each initiative before full rollout |

---

## 8. ✅ Recommended Next Steps

1. **Week 1–2:** Procure email service provider and begin recovery email sequence build
2. **Week 2–3:** Development sprint for guest checkout implementation
3. **Week 4–6:** UX design and development for checkout flow improvements
4. **Week 6:** Launch recovery emails and guest checkout simultaneously
5. **Week 8:** First performance review — compare abandonment rate vs baseline
6. **Week 12:** Full ROI assessment and decision on UX rollout

---

*⬅️ Previous: [Power BI Dashboard ←](../5_dashboard/)*  
*⬅️ Back to: [README ←](../README.md)*
