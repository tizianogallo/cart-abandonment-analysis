# 📝 User Stories

**Project:** Reducing Cart Abandonment at an Undisclosed E-Commerce Platform  
**Author:** Tiziano Gallo  
**Date:** March 2026  
**Version:** 1.0

---

## 🏷️ Priority Key (MoSCoW)
- **M** — Must Have
- **S** — Should Have
- **C** — Could Have
- **W** — Won't Have (this iteration)

---

## 🛒 Initiative 1 — Guest Checkout

### US-01 — Guest Checkout Option
**As a** new visitor,  
**I want to** complete my purchase without creating an account,  
**So that** I can buy quickly without sharing unnecessary personal information.

**Priority:** M

**Acceptance Criteria:**
- ✅ **Given** I am on the checkout page
- ✅ **When** I begin checkout
- ✅ **Then** I am presented with a clear choice between "Guest Checkout" and "Sign In / Create Account"
- ✅ **And** I can complete my full purchase as a guest without being forced to register

---

### US-02 — Post-Purchase Account Creation
**As a** guest who has just completed a purchase,  
**I want to** be offered the option to create an account,  
**So that** I can track my order and save my details for future purchases.

**Priority:** S

**Acceptance Criteria:**
- ✅ **Given** I have completed a purchase as a guest
- ✅ **When** I reach the order confirmation page
- ✅ **Then** I am shown an optional prompt to create an account using the email I provided
- ✅ **And** declining the prompt does not affect my order confirmation

---

### US-03 — Guest Order Tracking
**As a** guest buyer,  
**I want to** track my order without an account,  
**So that** I don't need to register just to see my delivery status.

**Priority:** S

**Acceptance Criteria:**
- ✅ **Given** I completed a purchase as a guest
- ✅ **When** I enter my order number and email address on the tracking page
- ✅ **Then** I can see the full status and delivery details of my order

---

## 📧 Initiative 2 — Cart Recovery Emails

### US-04 — 30-Minute Recovery Email
**As a** marketing manager,  
**I want** an automated email sent to abandoners within 30 minutes of cart abandonment,  
**So that** we can re-engage users while purchase intent is still high.

**Priority:** M

**Acceptance Criteria:**
- ✅ **Given** a registered user has added items to cart and left without purchasing
- ✅ **When** 30 minutes have elapsed since the last cart activity
- ✅ **Then** an automated recovery email is sent containing the abandoned product name, image and price
- ✅ **And** the email contains a direct link back to the user's cart
- ✅ **And** the email is not sent if the user has already purchased

---

### US-05 — 24-Hour Follow-Up Email
**As a** marketing manager,  
**I want** a second recovery email sent 24 hours after abandonment,  
**So that** we can re-engage users who did not respond to the first email.

**Priority:** M

**Acceptance Criteria:**
- ✅ **Given** a recovery email was sent 30 minutes after abandonment
- ✅ **When** 24 hours have passed and no purchase has been made
- ✅ **Then** a second recovery email is sent with a slightly more urgent message
- ✅ **And** the email is suppressed if the user purchased after the first email

---

### US-06 — 48-Hour Discount Email
**As a** marketing manager,  
**I want** a final recovery email sent 48 hours after abandonment with a discount offer,  
**So that** we can convert price-sensitive abandoners with a targeted incentive.

**Priority:** S

**Acceptance Criteria:**
- ✅ **Given** two recovery emails have been sent with no purchase made
- ✅ **When** 48 hours have elapsed since abandonment
- ✅ **Then** a final email is sent offering a time-limited discount (e.g. 10% off)
- ✅ **And** the discount code expires within 24 hours of the email being sent
- ✅ **And** the email is suppressed if the user has since purchased

---

### US-07 — Timezone-Aware Email Scheduling
**As a** marketing manager,  
**I want** recovery emails to be sent based on the user's local timezone,  
**So that** emails arrive during peak engagement hours rather than in the middle of the night.

**Priority:** S

**Acceptance Criteria:**
- ✅ **Given** a user has abandoned their cart
- ✅ **When** the recovery email sequence is triggered
- ✅ **Then** the system detects the user's timezone based on their IP or account settings
- ✅ **And** emails are scheduled to arrive between 9am–6pm local time
- ✅ **And** if timezone cannot be detected, emails default to 9am UTC+8 (peak conversion window)

---

### US-08 — Email Unsubscribe
**As a** user,  
**I want to** easily unsubscribe from cart recovery emails,  
**So that** I don't receive unwanted communications.

**Priority:** M

**Acceptance Criteria:**
- ✅ **Given** I have received a cart recovery email
- ✅ **When** I click the unsubscribe link at the bottom of the email
- ✅ **Then** I am removed from the recovery email sequence within 24 hours
- ✅ **And** I receive a confirmation that I have been unsubscribed

---

## ✨ Initiative 3 — Checkout UX Improvements

### US-09 — Checkout Progress Indicator
**As a** shopper,  
**I want to** see a progress indicator during checkout,  
**So that** I know how many steps remain and don't feel lost in the process.

**Priority:** M

**Acceptance Criteria:**
- ✅ **Given** I have begun the checkout process
- ✅ **When** I am on any step of the checkout
- ✅ **Then** a progress bar or step indicator is visible showing my current step (e.g. Step 1 of 3)
- ✅ **And** completed steps are visually marked as done

---

### US-10 — Streamlined 3-Step Checkout
**As a** shopper,  
**I want to** complete my purchase in no more than 3 steps,  
**So that** the process is quick and I am less likely to give up.

**Priority:** S

**Acceptance Criteria:**
- ✅ **Given** I have chosen to checkout
- ✅ **When** I proceed through the checkout
- ✅ **Then** the process consists of no more than 3 distinct steps: (1) Delivery, (2) Payment, (3) Confirmation
- ✅ **And** each step is completable on a single page without scrolling excessively on mobile

---

### US-11 — Exit Intent Popup
**As a** shopper who is about to leave the checkout,  
**I want to** be shown a helpful prompt before I go,  
**So that** I have a chance to reconsider or get assistance.

**Priority:** C

**Acceptance Criteria:**
- ✅ **Given** I am on the checkout page
- ✅ **When** my cursor moves towards the browser close button or back button
- ✅ **Then** a popup appears offering assistance or a reminder of what is in my cart
- ✅ **And** I can easily dismiss the popup and continue or leave

---

*⬅️ Previous: [BRD ←](BRD.md)*  
*➡️ Next: [Traceability Matrix →](traceability_matrix.xlsx)*
