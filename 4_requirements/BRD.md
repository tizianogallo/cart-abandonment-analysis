# 📋 Business Requirements Document (BRD)

**Project:** Reducing Cart Abandonment at an Undisclosed E-Commerce Platform  
**Author:** Tiziano Gallo  
**Date:** March 2026  
**Version:** 1.0  
**Status:** Draft

---

## 1. 📌 Executive Summary

Analysis of October 2019 behavioural event data revealed a cart abandonment rate of **49.07%** across 573,098 sessions — representing hundreds of thousands of lost transactions in a single month. The top 10 most abandoned products alone account for over **$5.4M in potential lost revenue**.

Data analysis confirmed that abandonment is **not driven by price or product category** — it is driven by checkout friction and browsing behaviour. This means the fix lies in the process, not the product.

This document defines the business requirements for three initiatives designed to reduce cart abandonment and recover lost revenue.

---

## 2. 🎯 Business Objectives

| ID | Objective |
|---|---|
| BO-01 | Reduce overall cart abandonment rate from 49.07% by a minimum of 10% |
| BO-02 | Implement an automated cart recovery mechanism targeting the 64.9% of abandoners who never return |
| BO-03 | Improve checkout conversion during peak trading hours (5–9am UTC) |
| BO-04 | Prioritise recovery efforts on high-value abandoned products (Apple, Samsung) |
| BO-05 | Establish KPI monitoring to track abandonment trends on an ongoing basis |

---

## 3. 🔎 Scope

### 3.1 ✅ In Scope
- Guest checkout implementation
- Automated cart recovery email sequence (30 min, 24hr, 48hr)
- Checkout UX simplification (progress indicator, reduced steps)
- Power BI dashboard for ongoing KPI monitoring
- Timezone-aware email scheduling

### 3.2 ❌ Out of Scope
- Pricing strategy changes
- Full website redesign
- Mobile app development
- A/B testing execution
- Third-party logistics

---

## 4. 👥 Stakeholder Summary

| Stakeholder | Role | Key Interest |
|---|---|---|
| 👔 E-Commerce Director | Sponsor | Revenue recovery & ROI |
| 📣 Marketing Manager | Key stakeholder | Recovery email campaigns |
| 🎨 UX Designer | Key stakeholder | Checkout flow improvements |
| 💻 Development Lead | Key stakeholder | Technical implementation |
| 💰 Finance Analyst | Stakeholder | Budget & ROI validation |

---

## 5. 🗺️ Current State Summary (AS-IS)

Based on data analysis and process mapping, the following pain points were identified:

| ID | Pain Point | Evidence |
|---|---|---|
| PP-01 | Forced account creation before checkout | Process map — identified as primary drop-off point |
| PP-02 | No cart recovery mechanism exists | 64.9% of abandoners never return without a nudge |
| PP-03 | Cart sessions expire with no follow-up | Session expiry identified in AS-IS process map |
| PP-04 | No progress indicator during checkout | UX gap identified in process mapping |
| PP-05 | Recovery emails not timed to user timezone | Peak conversion at 5–9am UTC (Asia afternoon hours) |
| PP-06 | High abandonment on premium products | Apple $975 smartphone = $1.95M lost revenue in Oct |

---

## 6. ⚙️ Functional Requirements

### 6.1 🛒 Guest Checkout (Initiative 1)

| ID | Requirement | Priority |
|---|---|---|
| FR-01 | The system shall allow users to complete a purchase without creating an account | Must Have |
| FR-02 | The system shall present a clear choice between guest checkout and account login at the start of checkout | Must Have |
| FR-03 | The system shall not require account creation at any point during the guest checkout flow | Must Have |
| FR-04 | The system shall offer optional account creation after a guest purchase is completed | Should Have |
| FR-05 | The system shall save guest order details for 30 days to allow order tracking without an account | Should Have |

### 6.2 📧 Cart Recovery Email Sequence (Initiative 2)

| ID | Requirement | Priority |
|---|---|---|
| FR-06 | The system shall trigger an automated email 30 minutes after cart abandonment | Must Have |
| FR-07 | The system shall trigger a second email 24 hours after abandonment if no purchase has been made | Must Have |
| FR-08 | The system shall trigger a third and final email 48 hours after abandonment with a discount offer | Should Have |
| FR-09 | The system shall suppress recovery emails if the user completes a purchase before the email is sent | Must Have |
| FR-10 | Recovery emails shall be scheduled based on the user's local timezone, not UTC | Should Have |
| FR-11 | The system shall personalise recovery emails with the abandoned product name, image and price | Should Have |
| FR-12 | The system shall track email open rates, click rates and recovery rates per campaign | Must Have |

### 6.3 ✨ Checkout UX Improvements (Initiative 3)

| ID | Requirement | Priority |
|---|---|---|
| FR-13 | The checkout flow shall display a progress indicator showing the current step (e.g. 1 of 3) | Must Have |
| FR-14 | The checkout flow shall be completable in no more than 3 steps | Should Have |
| FR-15 | The system shall pre-fill returning user details where available | Should Have |
| FR-16 | The system shall display an exit-intent popup offering assistance when a user attempts to leave the checkout | Could Have |
| FR-17 | The checkout page shall load within 2 seconds on a standard mobile connection | Must Have |

---

## 7. 🔒 Non-Functional Requirements

| ID | Requirement | Category |
|---|---|---|
| NFR-01 | Recovery emails shall be delivered within 5 minutes of the trigger time | ⚡ Performance |
| NFR-02 | Guest checkout shall not increase page load time by more than 200ms | ⚡ Performance |
| NFR-03 | All user data collected during guest checkout shall comply with GDPR | ✅ Compliance |
| NFR-04 | Recovery email unsubscribe mechanism shall be present in every email | ✅ Compliance |
| NFR-05 | The system shall handle a minimum of 100,000 concurrent sessions without degradation | 📈 Scalability |
| NFR-06 | Cart data shall be persisted for a minimum of 7 days after abandonment | 💾 Data Retention |

---

## 8. ⚠️ Assumptions & Constraints

**Assumptions:**
- The platform has access to user email addresses for registered users
- An email service provider (ESP) is already in place or can be procured
- Development capacity is available to implement guest checkout within one sprint cycle
- The October 2019 dataset is representative of ongoing trading patterns

**Constraints:**
- Implementation budget is subject to Finance approval
- Guest checkout must not compromise existing account-based loyalty programme
- All initiatives must be implemented without disrupting live platform traffic

---

## 9. 🔗 Dependencies

| Dependency | Description | Owner |
|---|---|---|
| Email Service Provider | Required for recovery email sequence | 📣 Marketing Manager |
| User session tracking | Required to detect abandonment trigger | 💻 Development Lead |
| Timezone detection | Required for timezone-aware email scheduling | 💻 Development Lead |
| GDPR compliance review | Required before collecting guest user emails | ⚖️ Legal / Compliance |

---

## 10. 📈 Success Metrics

| KPI | Baseline (Oct 2019) | Target |
|---|---|---|
| Cart abandonment rate | 49.07% | < 44% (10% reduction) |
| Cart recovery rate | 0% | 5–15% |
| Guest checkout adoption | 0% | > 30% of new checkouts |
| Checkout completion rate | 50.93% | > 56% |
| Revenue per session | TBD | Measurable uplift |

---

*➡️ Next: [User Stories →](user_stories.md)*
