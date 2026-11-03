# STA email research archive

Captured 2026-11-02 from a saved read of **STA Email Research**.
Original chat: https://chatgpt.com/c/6ac84a53-c528-83e8-afd0-aff8e52e9684

## Coverage and evidence

This archive contains eight assistant research entries dated October 29 through November 2, 2026. It is a partial recovery, not the complete conversation. The current chat reader could not load the original thread. The saved reader reported no next cursor, but its recent-entry view does not establish complete historical coverage.

Entries are preserved as historical research. Statements labeled “STA decision” were written by an assistant and remain proposed operating policies unless separately approved and deployed. Platform claims and defaults need current official-document verification before implementation. The original numeric citation markers could not be resolved to source URLs; they are replaced below with a missing-source marker. No live configuration or performance is established by these notes.

No customer records or internal financial reports are included.

## Recovered entries

### STA Email Research — October 29

**The review request should improve STA’s fit and condition data, not merely collect stars.**

1. **Reviews can confirm both the shirt and the buyer profile.**  
   Klaviyo separates product questions from profile questions. Product questions can capture fit; profile answers such as normal size become customer properties for segmentation. Profile answers overwrite the previous property value. [original citation URL unavailable]

   **STA Post-Purchase decision:** ask only three questions:

   - Did the condition match the listing?
   - How did the measured fit land: smaller, accurate or roomier?
   - What size do you normally buy for yourself?

   Store the last answer as `review_confirmed_size`, preserving `declared_shirt_size` and purchase history separately. Suppress this size question for identified gifts so the buyer’s profile does not inherit the recipient’s size.

2. **Online and in-store buyers need different timing.**  
   Klaviyo can time Shopify review requests from delivery and maintain a separate POS delay. Delivery-based timing avoids asking for feedback before an online order arrives; POS orders use fulfillment timing. [original citation URL unavailable]

   **STA decision:** keep one Post-Purchase flow with branches:

   - **Shipped:** request feedback after confirmed delivery and enough wear time.
   - **Rancho store/event purchase:** use the POS branch.
   - **Exchange or support case open:** pause the review request.
   - **Gift purchase:** ask whether the gift landed, without assigning fit preferences to the purchaser.

   **Subject:** *how did the shirt actually land?*

3. **Condition trust depends on accuracy, not a perfect score.**  
   Classic Football Shirts publicly acknowledges that condition grades are subjective and pairs them with detailed defect disclosure. That is observable public policy, not evidence about its private review automation or conversion rate. [original citation URL unavailable]

   **STA copy decision:** ask, *“Did the shirt arrive the way we described it?”* Use verified answers to improve grading and reassurance blocks across Browse, Cart and BFCM emails. Because many STA shirts are one-offs, extract reusable proof about measurement accuracy, condition transparency and service instead of relying only on reviews attached to a sold SKU.

   If STA later offers Kit Cash or a discount for reviews, Klaviyo requires the review to be marked as incentivized and the reward delivered regardless of whether the feedback is positive or negative. [original citation URL unavailable] Start without an incentive until the response rate and margin effect are known.

**Measure:** delivered/POS order → review request, submission rate, condition or fit mismatch rate, corrected size profiles, support cases, next eligible recommendation click, purchase and time-to-sale. This strengthens **Post-Purchase, Browse and Shirt Profile** inside the existing 10-flow foundation; it does not require another overlapping reminder flow. No live configuration was inspected or changed, and nothing was sent.

---

### STA Email Research — October 29 evening

**A Klaviyo product block cannot safely promise “your team, your size” by itself.**

1. **Standard personalization is behavioral, with a generic fallback.**  
   Klaviyo recommendations can use browsing, cart and purchase behavior while excluding previously purchased and unavailable items. When customer data is insufficient, the block falls back to the same bestseller or most-viewed logic for everyone. Feed filters cover categories, price and stock; they are not documented as automatically joining each profile’s declared team and size to matching inventory. [original citation URL unavailable]

   **STA decision:** label ordinary feeds **“you may like”**, not **“picked in your size.”** If no trustworthy personalized result exists, show Shirt Matching rather than generic bestsellers.

2. **Product-level blocks can hide a size mismatch.**  
   Klaviyo product blocks select products, not individual variants. Its inventory filter may qualify a product from total variant inventory, then display a default image or price belonging to a different variant. [original citation URL unavailable]

   **STA decision:** before adding automated recommendations to Welcome, Arcade, Browse or BFCM emails, test whether each STA vintage listing is represented as one purchasable size. For multi-size products, do not claim the recipient’s size is available unless variant-level eligibility has been verified.

   During BFCM, use a globally safe feed containing only eligible, in-stock merchandise above the approved margin floor, with Rare/Grail and one-of-one exclusions. Team-and-size matching remains a separate validation step.

3. **Exact matches need explicit product IDs.**  
   Klaviyo documents a custom route where an external matching process writes recommended catalog-item IDs to the customer profile and the email retrieves those exact items. Missing catalog items can cause the message to skip. [original citation URL unavailable]

   **STA Shirt Matching build:** after comparing team, player, era, size/fit, budget and condition against live inventory, write only verified matches to `shirt_match_product_ids`. If the list is empty, send no product reminder; keep the request open for sourcing.

   **Copy:** *“We found one that fits your hunt: the right club, your stated fit range, and within budget. Check the measurements and condition before it goes.”*

Classic Football Shirts publicly displays **“Recommended for you”** alongside **Shop by Size** on its clearance experience. That is observed storefront language, not proof that its private emails perform customer-specific team-and-size matching. [original citation URL unavailable]

Measure eligible products generated, verified size matches, fallback frequency, match-to-contact, click, purchase, time-to-sale and unavailable-item skips. No live STA catalog or Klaviyo configuration was inspected or changed, and nothing was sent.

---

### STA Email Research — October 30 evening

**A one-off Shirt Match needs a controlled handoff, so several supporters do not chase the same shirt.**

1. **Shopify can reserve the exact item for one customer.** A draft-order reservation moves tracked inventory into the Committed state, preventing other customers from purchasing it until a chosen expiration time. [original citation URL unavailable]

   **STA decision:** when one shirt satisfies several requests, offer it to the oldest qualified requester first. Reserve it only after confirming team, size/fit, budget, condition and location. Choose the hold period from STA’s operating capacity and eventual conversion data.

2. **The reservation can lead directly to secure checkout.** Shopify draft orders support an invoice or direct checkout link. Product prices are locked by default, while customer-entered discount codes require a separate setting. [original citation URL unavailable]

   **STA copy:**

   **Subject:** *found it — and held it for you*

   *The [season/player] shirt matches your hunt and sits inside your fit and budget. We’ve held this exact piece until [time]. Check the measurements and condition, then claim it below.*

   If no reservation was actually created, say **“available now; not reserved.”** A checkout link may be shared through Instagram only within a permitted conversation; it does not make a saved handle eligible for an automated outbound DM.

3. **Expiration should advance the queue, not start overlapping reminders.** Shopify exposes the reservation deadline in draft-order notifications. Klaviyo can recheck profile filters before every flow action, including whether someone has since purchased. [original citation URL unavailable]

   **STA workflow decision:**

   - Set the request to `reserved` and suppress Browse, Cart, low-stock and general Shirt Match reminders for that item.
   - On purchase, close the request as `purchased`.
   - On expiration without purchase, return the inventory to availability and contact the next qualified requester.
   - Keep other matching requests open for sourcing.
   - Do not release everyone simultaneously unless enough inventory exists.

Measure match → reservation, reservation → contact, checkout click, purchase, expiration rate, next-requester conversion, time-to-sale, contribution margin and duplicate contacts prevented.

No meaningful new public football-shirt seller evidence appeared for this private handoff mechanic. These are documented Shopify/Klaviyo capabilities and a proposed STA process, not a live audit or performance claim. Nothing was changed or sent.

---

### STA Email Research — October 31

**BFCM needs a message-priority system. Smart Sending alone will not prevent every collision.**

1. **Email and SMS frequency limits operate separately.** Klaviyo’s defaults are 16 hours for email and 24 hours for SMS. An email does not stop a same-day SMS, and messages skipped by Smart Sending are not automatically rescheduled. [original citation URL unavailable]

   **STA decision:** use this priority order:

   1. Order, fulfillment and exchange information  
   2. Reserved Shirt Match  
   3. Checkout recovery  
   4. Cart or browse recovery  
   5. BFCM campaign  
   6. General discovery/community

   Pause lower-priority reminders through explicit filters when someone enters a higher-priority journey. Keep Smart Sending enabled as a second safeguard.

2. **Multi-message campaigns can stop after purchase.** Klaviyo’s omnichannel exit criteria can remove someone from all later campaign messages after a qualifying conversion, even when that purchase resulted from another flow or campaign. The exit condition must be configured before the first message sends. [original citation URL unavailable]

   **STA BFCM decision:** use `Placed Order` as the sequence exit condition. Once someone buys, replace sale reminders with the appropriate confirmation or post-purchase experience.

   **Copy before purchase:** *“Your size is still in the eligible lineup.”*  
   **After purchase:** no further countdown email or SMS.

3. **Holiday reach should expand through engagement tiers, not one full-list blast.** Klaviyo recommends starting major promotions with the most engaged subscribers, expanding cautiously and keeping the final inactive group outside promotional sends. Apple privacy opens should not be treated as reliable engagement by themselves. [original citation URL unavailable]

   **STA audience order:**

   - Recent purchasers and clickers with eligible favorite-team or size inventory
   - Recently engaged subscribers with available eligible inventory
   - Broader engaged audience using honest discovery copy
   - Inactive profiles remain in re-engagement or sunset treatment

   Rare/Grail and one-of-one pieces remain excluded unless their economics are separately approved. Never say *“in your size”* unless variant availability has been verified.

Measure unique people contacted across channels, Smart Sending skips, purchase-exit removals, messages received per customer, clicks, purchases, margin and post-purchase sale reminders prevented.

No meaningful new public football-shirt seller evidence appeared for this private orchestration issue. These are documented Klaviyo controls and proposed STA decisions, not evidence of another seller’s private automation or STA’s live setup. Nothing was changed or sent.

---

### STA Email Research — October 31 evening

**The Rancho store and community events should create useful shirt profiles, without turning every receipt or RSVP into a marketing subscriber.**

1. **Shopify POS can request customer information without blocking checkout.** POS Pro supports “Recommended” customer capture, letting staff skip it when someone declines. “Required” capture can prevent checkout and reduce sales. [original citation URL unavailable]

   **STA decision:** use voluntary capture at the store, Weekly FC, Cascarritas and pop-ups:

   *“Want us to remember your club and fit for the next drop?”*

   Collect only email or phone for verified linkage, favorite team, usual size/fit and capture source. Use Shirt Matching for specific player, era, budget and condition requests.

2. **A digital receipt and marketing permission are separate choices.** Shopify can create a customer profile from an emailed or texted receipt, but it presents email and SMS marketing choices separately. POS profiles also maintain distinct email and SMS marketing settings. [original citation URL unavailable]

   **STA decision:** staff should never describe receipt delivery as joining STA’s marketing list.

   - **Receipt:** *“Where should we send your receipt?”*
   - **Marketing:** *“Want first look at shirts from your clubs and events at the shop?”*
   - **Shirt Matching:** *“Should we contact you when we find this specific hunt?”*

   Record each permission independently. An FC RSVP, Instagram follow or saved phone number does not answer the other questions.

3. **Anonymous POS orders cannot support Klaviyo personalization.** Klaviyo requires a POS order to contain a customer record plus a valid email or phone number before it can sync. Synced orders include `Source Name = pos`, allowing POS and web purchases to be distinguished. [original citation URL unavailable]

   **STA flow decision:** branch Post-Purchase and Retention by verified order source:

   - **POS purchase:** skip shipping copy; ask whether the condition and measured fit landed correctly.
   - **Event purchase:** retain the event source for local follow-up and attribution.
   - **POS customer later buying online:** treat this as one customer journey when linked by verified email or phone.
   - **Name-only profile:** do not guess the Klaviyo or Instagram identity.

Measure POS orders with a verified customer, voluntary marketing opt-in, team-and-size completion, POS-to-online repeat purchase, Shirt Match requests, match-to-contact, click, purchase and time-to-sale.

No meaningful new public football-shirt seller evidence appeared for this private identity-capture process. These are documented Shopify/Klaviyo capabilities and proposed STA decisions, not a live configuration audit. Nothing was changed or sent.

---

### STA Email Research — November 1

**STA should have one recovery ladder. Shopify, Klaviyo, Browse, Cart and Checkout must not chase the same customer.**

1. **Shopify and Klaviyo can both send abandoned-checkout emails.** Klaviyo explicitly recommends disabling Shopify’s recovery automation immediately before enabling its replacement flow to avoid either duplicate messages or a coverage gap. [original citation URL unavailable]

   **STA decision:** assign one system as the owner of checkout recovery. Do not activate a Klaviyo replacement until its trigger, purchase suppression, links and inventory behavior have been tested. This is a proposed control; STA’s live Shopify and Klaviyo settings were not audited.

2. **Purchase intent should determine which recovery flow survives.** Klaviyo distinguishes Viewed Product, Added to Cart and Checkout Started. Its recommended filter removes someone from Cart recovery once they start checkout, while `Placed Order zero times since starting this flow` stops Checkout messages after purchase. [original citation URL unavailable]

   **STA hierarchy:**

   - Checkout recovery replaces Cart and Browse.
   - Cart recovery replaces Browse.
   - Reserved Shirt Matching outranks all three.
   - Purchase, exchange assistance or an unavailable shirt stops recovery.

   **Checkout copy:** *“Your checkout is still there. The shirt isn’t reserved, so check the measurements and condition before it changes hands.”*

   Do not introduce a fresh discount automatically; preserve margin and the original BFCM eligibility.

3. **Checkout recovery only begins after identifiable contact information exists.** Klaviyo records Checkout Started after Shopify supplies a valid email or phone number, and the event can contain variant details, cart value, discounts and a recovery URL. Shopify cannot email a phone-only checkout and suppresses recovery in cases including unavailable inventory or unsupported shipping. [original citation URL unavailable]

   **STA decision:** use email only when email recovery is eligible; use SMS only with valid SMS consent. A phone number, Instagram handle or prior event RSVP does not authorize marketing outreach. If contact is unavailable, improve onsite checkout recovery rather than guessing another identity or channel.

Measure Browse → Cart → Checkout → Purchase, cross-flow skips, duplicate messages, unavailable-item suppression, checkout recovery rate, contribution margin and time-to-sale.

No meaningful new public football-shirt seller evidence appeared for this private recovery architecture. These are official Shopify/Klaviyo capabilities and proposed STA decisions, not verified private automations or performance claims. Nothing was changed or sent.

---

### STA Email Research — November 1 evening

**A zero-result search should become a Shirt Match request, not a dead session or generic email signup.**

1. **Shopify reports searches with no results and searches with results that receive no clicks.** It also reports search click, add-to-cart and purchase rates. Predictive-search interactions are excluded from some Search & Discovery reports, and reporting can lag. [original citation URL unavailable]

   **STA decision:** review unmet searches by team, player, season, shirt type and size. Keep aggregate search demand separate from identifiable customer data unless the shopper voluntarily submits a request.

2. **Search merchandising should only surface real, available inventory.** Shopify product boosts apply to available products; sold-out products move toward the end of results. Synonyms are intended for true substitutes and Shopify cautions against grouping loosely related terms. [original citation URL unavailable]

   **STA decision:** use synonyms for genuine language variants such as *Barça / Barcelona* or *keeper / goalkeeper*. Do not treat different clubs, eras or player versions as interchangeable. When no accurate item exists, route to Shirt Matching instead of boosting a weak substitute.

3. **The no-result page can capture structured sourcing demand.** Klaviyo can accept a custom event through its Events API, but a customer-facing Shirt Match form remains the useful action: prefill the search phrase, then ask for team, exact shirt, player, era, size/fit, budget and acceptable condition. [original citation URL unavailable]

   **STA copy:**

   *“Nothing matched that hunt today. Tell us the size, era and condition you’ll accept. If one is already at STA, we’ll show you. If not, your request becomes sourcing demand.”*

   Ask where they want match updates. Email requires the appropriate permission; an optional Instagram handle should be linked through customer-provided email or another verified path. A handle alone still does not authorize future automated DMs.

Measure search → result, click, cart and purchase; no-result search → Shirt Match request; request → eligible contact, click, purchase and time-to-sale. Aggregate unmet requests by team, player, era and size so sourcing follows demonstrated demand.

No meaningful new public football-shirt seller evidence appeared for this private search-to-sourcing process. These are official Shopify/Klaviyo capabilities and proposed STA decisions, not live STA search or flow audit results. Nothing was changed or sent.

---

### STA Email Research — November 2

**An open exchange should pause normal retention and become a fit-resolution journey.**

1. **An exchange item is not reserved when the return is first created.** Shopify reserves its inventory only when the return is processed. For a one-off vintage shirt, the proposed replacement could sell during that gap. [original citation URL unavailable]

   **STA decision:** never email *“your replacement is secured”* until inventory is actually reserved or processed. If no exact replacement exists, move the customer into Shirt Matching with the original team, era, measurements and condition issue prefilled.

2. **Return reasons can improve future fit recommendations.** Shopify records apparel-specific reasons such as “Too big” and “Too small” and supports reporting by reason. A refund issued without creating a return does not preserve this structured reason. [original citation URL unavailable]

   **STA decision:** capture:

   - Original tagged size and measurements
   - Too small, too large, condition mismatch or preference change
   - Desired tagged size and pit-to-pit range
   - Exact replacement versus broader team/era search

   Treat this as resolution data. Do not silently overwrite the customer’s declared size from one exchange.

3. **Do not assume a return request automatically stops Klaviyo marketing.** Klaviyo documents Shopify metrics for Refunded Order and Cancelled Order, while flow eligibility depends on the metrics and filters actually available in the account. [original citation URL unavailable]

   **STA flow decision:** use a verified `resolution_open` status or custom event to pause review requests, win-back, Browse, Cart and BFCM reminders. Resume retention only after the exchange, credit or Shirt Match path is resolved.

   **Copy:**  
   **Subject:** *let’s get the fit right*  
   *Your exchange is open. We’ll sort the measurements first. If the same shirt isn’t available, tell us how wide you want the search—same club, same era or a completely different piece.*

Track exchange reason, resolution time, replacement availability, store-credit issuance and redemption, Shirt Match completion, repeat purchase, time-to-sale and contribution margin. Shopify notes that Shopify Payments card fees are not returned after a refund, so additional discounting during resolution should be deliberate. [original citation URL unavailable]

No meaningful new public football-shirt seller evidence appeared for this private resolution workflow. These are official Shopify/Klaviyo capabilities and proposed STA controls, not a live account audit. Nothing was changed or sent.

---

