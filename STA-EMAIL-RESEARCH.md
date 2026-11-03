# STA Email Research: conversation transcript

Original chat: [STA Email Research](https://chatgpt.com/c/6ac84a53-c528-83e8-afd0-aff8e52e9684)

Captured November 2, 2026. **43 messages: 42 assistant research entries and 1 user message.** This replaces the initial eight-entry recovery with all messages displayed by the original conversation, from October 8 through the latest November 2 user message.

## Capture method and limits

The long conversation virtualizes messages. Fourteen rendered snapshots were captured with overlap between every adjacent section. Messages were deduplicated by their original message keys; repeated bodies were checked for identical extracted content. The first snapshot begins with the October 8 research entry; the last ends with the November 2 user request. Source links exposed in each rendered message are preserved with tracking parameters removed. Additional sources behind an unopened citation may not be represented.

This is a transcript of the displayed conversation, not an account-wide ChatGPT data export. Hidden reasoning, alternate branches, attachments not displayed, and future updates are outside this capture. Display formatting was converted to Markdown; the message wording was not summarized. Browser session data and unrelated sidebar chats are excluded.

Assistant-authored “decisions” remain historical proposals unless independently approved and implemented. Historical platform claims require current verification before use. Later entries may revise earlier flow designs; preserve that sequence rather than treating all versions as simultaneous instructions.

The same message content and identifiers are available in [JSON](transcripts/sta-email-research.json). The [capture manifest](transcripts/capture-manifest.json) records overlapping message keys and snapshot hashes. Original browser snapshots remain local, outside this public repository.

## Messages

## Message 01: Assistant

Turn: `07ec6e7c-9021-4bd7-b825-e9439910977e`

STA Email Research — October 8

Three useful findings:

1. Personalization must be constrained by stock and fit

Klaviyo product feeds can prioritize behavior and categories, but recommendations are not automatically “favorite team + exact shirt size.” Inventory rules also need verification; certain catalog configurations can allow unavailable items into recommendation blocks. [help.klaviyo.com: How to use product feeds and recommendations](https://help.klaviyo.com/hc/en-us/articles/115005082787)

STA decision:

- Build feeds around team tags, then filter by available size and active inventory.
- Recommended hierarchy: exact team + size → related team/national side + size → same era/style + size → shirt-matching CTA.
- Never show a random bestseller merely to fill the block.
- Audit catalog inventory behavior before using recommendations in the Arcade follow-up, browse or win-back flows.

2. Vintage reassurance should replace early discounting

Classic Football Shirts publicly emphasizes individual inspection, labels, stitching, badge construction, condition grading, sizing notes and detailed photography. That is observable public merchandising—not evidence of their private email automations or results. [classicfootballshirts.co.uk: USA Classic Vintage Kits & Official World Cup 2026 Shirts](https://www.classicfootballshirts.co.uk/international-teams/north-america/usa.html)

STA decision:

Browse and checkout emails should show:

- Exact pit-to-pit and length
- STA condition score plus the specific flaw
- “Authenticity checked” with two or three inspection points
- Front, back, tag and defect images
- Exchange reassurance

Copy direction: “This is the exact shirt you viewed—not a stock photo.” Save discounts for controlled branches rather than leading with them.

3. Instagram can accelerate matching, but a saved handle is not DM permission

Manychat can initiate a DM when someone comments with a chosen keyword, replies to a Story or mentions STA. Its comment trigger generally activates on the person’s first qualifying comment, while Meta’s standard automated messaging window is normally 24 hours. Manychat describes the following seven-day period as manual human-agent messaging—not unrestricted automation. [Manychat Help: Instagram Post and Reel Comments trigger](https://help.manychat.com/hc/en-us/articles/14281316989724-Instagram-Post-and-Reel-Comments-trigger)

STA decision:

Use Instagram as a customer-initiated entry point:

- Reel/Story CTA: “Comment MATCH and we’ll help hunt your shirt.”
- Capture email, voluntary IG handle, team, player, era, size/fit, budget and acceptable condition.
- Link the Instagram contact to the customer profile only through customer-provided email or another verified match.
- Store email/SMS/Instagram preferences separately, plus the platform-scoped contact ID where available.
- Do not treat a saved handle as permission for automated outbound DMs.

Shirt Matching should now be a top-three build priority. Track:

request → viable match → customer contacted → clicked → purchased

Also measure match-to-contact rate, purchase rate and median time-to-sale. Unmatched requests become a sourcing-demand report by team, player, era, size and budget.

Current 10-flow foundation:

1. Welcome + team/size preference capture
2. Browse discovery
3. Added-to-cart recovery
4. Checkout recovery
5. Back-in-stock/rare-shirt alert
6. Shirt Matching service
7. Post-purchase authenticity, care and community
8. Second-purchase/team expansion
9. Lapsed-customer win-back
10. Gift shopper, recipient handoff and event/in-store follow-up

Overlap rule: browse recipients exit when they add to cart, start checkout or purchase; cart recipients exit when they start checkout or purchase; checkout recipients exit immediately after purchase. Klaviyo explicitly recommends Placed Order zero times since starting this flow, and lighter browse messaging with exclusions for higher-intent actions. [Klaviyo Help Center: How to create a browse abandonment flow](https://help.klaviyo.com/hc/en-us/articles/115002775252)

Seasonal direction:

- BFCM: team-and-size drops, controlled bundles/store credit, no blanket margin-eroding discount.
- December: gift finder, delivery deadlines, gift-card fallback and recipient preference handoff.
- January: jersey care, trade-in/store-credit education, new arrivals and FC community participation—not another generic sale.

---

## Message 02: Assistant

Turn: `3668b368-df01-4d6e-9074-8dd2916d1905`

STA Email Research — October 9

Today’s strongest new finding: the Shirt Matching service needs its own request record—not just more customer-profile fields.

1. Don’t overwrite a customer’s previous shirt hunt

Klaviyo confirms that profile properties can collect questionnaire answers, but repeat submissions overwrite the previous value. Klaviyo recommends a survey tool when every submission must be retained separately. [Klaviyo Help Center: Understanding custom profile properties](https://help.klaviyo.com/hc/en-us/articles/115000250912)

For STA:

- Store stable preferences on the profile: favorite teams, usual size, preferred fit and Instagram handle.
- Store every shirt request as a separate event/record: team, player, season, home/away/third, size, measurements, budget, acceptable condition and request date.
- Add statuses: Requested → Sourcing → Match Found → Contacted → Clicked → Purchased/Passed.
- If they pass, record why: price, condition, wrong size or wrong variation.

This turns unmatched demand into an actual buying list instead of repeatedly replacing the customer’s last request.

2. In-store/event identification and marketing permission are separate

Shopify POS can create profiles containing purchase history, email, phone, notes and marketing preference. Staff must still record whether the customer actually wants marketing; merely providing details or receiving a digital receipt is not blanket promotional consent. Shopify recommends making customer collection optional/recommended when refusal might otherwise block checkout. [Collecting customer contact information: Shopify Help Center](https://help.shopify.com/en/manual/promoting-marketing/create-marketing/customer-contact-information)

STA implementation:

- Use one QR destination with event-specific source codes: FC\_WEDNESDAY, SUNDAY\_CUP, CASCARRITAS, STA\_STORE, RED\_BULL.
- Klaviyo forms support hidden $source fields, so acquisition origin can be recorded without asking the customer another question. [Klaviyo Help Center: Understanding form blocks and fields](https://help.klaviyo.com/hc/en-us/articles/4413550187035)
- First screen: email and explicit marketing choice.
- Second screen: team and shirt size.
- Optional third screen: Instagram handle and “Can we contact you on Instagram about your shirt requests?” preference.
- At POS, staff language should be: “Want your receipt only, or do you also want first look at shirts in your team and size?”

Flow decision: these contacts enter the regular Welcome flow only with marketing consent; otherwise they retain the transaction/event profile without promotional sends.

3. December gifting needs an uncertainty-reduction lane

Classic Football Shirts publicly positions mystery products around selectable size, authenticity, minimum condition/value and duplicate prevention; its gift-card copy is simply “Let them decide.” These are observable merchandising choices—not evidence of its private flows or performance. [classicfootballshirts.co.uk: Mystery Football Shirt Boxes: Adults & Kids](https://www.classicfootballshirts.co.uk/mystery)

STA’s December Gift flow should split into:

- **“I know their club”** — team-and-size gift recommendations.
- **“I know football, not their exact shirt”** — curated mystery box with declared condition floor and exclusions.
- **“I have no idea”** — digital gift card.
- **“They collect seriously”** — Shirt Matching gift request.

Include a recipient card/QR inside the package: “Tell STA your clubs, size and grail shirt.” The recipient opts themselves into future marketing; the purchaser should not supply the recipient’s email for promotional enrollment.

Copy direction: **“You don’t need to know the exact shirt. Just tell us who they support and how they wear it.”**

---

## Message 03: Assistant

Turn: `6239e3be-3c70-41e3-9977-d04ed16e4fd0`

STA Email Research — October 10

Today’s finding: STA can create real urgency from one-of-one inventory without immediately discounting.

1. Build a one-message “Exact Shirt Almost Gone” flow

Klaviyo’s low-inventory trigger can target people who viewed, added or started checkout with a low-stock product. It recommends sending immediately, limiting repeat entry and being cautious with additional messages because the item may sell out quickly. [Klaviyo Help Center: How to create a low inventory flow](https://help.klaviyo.com/hc/en-us/articles/21374913673243)

For STA, nearly every vintage shirt has inventory of one, so targeting every browser would be excessive. Use this only for:

- Added to Cart or Started Checkout
- Active, in-stock vintage jerseys
- No purchase since engagement
- No more than one low-stock email within 14 days

Copy:

> **There isn’t another one in the back.**\
> The exact [Team / Year / Player] shirt you saved is still available—but there’s only one.

Include the exact condition, pit-to-pit, shoulder-to-hem and exchange reassurance. No discount.

2. BFCM price drops should be behavior-triggered, not blasted blindly

Klaviyo’s price-drop flow reaches people who previously viewed or began checkout with the specific item. It automatically excludes purchasers and will not trigger for unpublished or out-of-stock products. Its documentation was updated October 8, 2026. [Klaviyo Help Center: How to create a price drop flow](https://help.klaviyo.com/hc/en-us/articles/4404249033755)

STA decision:

- Use price-drop alerts only for inventory deliberately included in BFCM.
- Set a meaningful threshold, such as 15% or $20, so ordinary edits do not create messages.
- Prioritize checkout abandoners before browsers.
- Suppression priority: **Checkout flow → Price Drop → Low Inventory → Browse**.
- If someone qualifies for a higher-intent flow, pause the lower-intent reminder.

This protects margin because STA discounts the selected shirt once and informs proven interest, instead of giving every subscriber a storewide code.

3. “Fit proof” should become a standard email block

Public vintage-shirt listings increasingly prioritize exact garment measurements over the tag. Classic Football Shirts publishes pit-to-pit and shoulder-to-hem measurements on individual products; specialist size guides advise comparing those measurements with a shirt the buyer already owns and distinguishing fan versus player-issue cuts. These are observable public merchandising practices—not proof of private email performance. [(L): 1984-87 England Home Shirt - 6/10](https://www.classicfootballshirts.co.uk/1984-87-england-home-shirt-610-l-engh84584670.html)

Add this block to Browse, Cart, Checkout and Shirt Match emails:

- Tagged size
- Pit-to-pit
- Shoulder-to-hem
- Fan/replica or player/authentic version
- Fit note: fitted, regular, boxy or oversized
- CTA: **Compare it with your best-fitting shirt**

Best copy direction:

> **Don’t trust the letter on a 20-year-old tag. Trust the tape.**

This directly supports STA’s current sizing work and attacks a major trust barrier without sacrificing price.

---

## Message 04: Assistant

Turn: `9c5e267b-c997-48d7-a36c-4de6e388e228`

STA Email Research — October 10 evening

The January retention opportunity is bigger than a win-back coupon: turn every completed order into better fit data, trust proof and future inventory.

1. First purchase and repeat purchase need different post-purchase paths

Klaviyo’s post-purchase guidance recommends splitting new versus returning customers and coordinating timing with fulfillment messages. Its post-purchase documentation was updated October 8, 2026. [Klaviyo Help Center: How to create a post-purchase flow](https://help.klaviyo.com/hc/en-us/articles/360028872611)

STA sequence:

- **First purchase:** welcome to STA → explain condition grading/authenticity → fit check after delivery → introduce trade-ins and local community.
- **Repeat purchase:** thank them as a returning collector → recommend available shirts from their teams and confirmed fit → invite them to Shirt Matching.
- Delay sales recommendations until after expected delivery.
- Exclude anyone currently receiving an order-problem or exchange message.

Copy direction:

> **You didn’t just buy another jersey. You found one that survived long enough to reach you.**

2. The review request should collect fit and condition evidence

Klaviyo Reviews supports product questions such as “runs small/large” and profile questions such as normal size or height. Profile answers can become properties for segmentation, while product answers can help future shoppers filter reviews. [Klaviyo Help Center: How to create custom review questions](https://help.klaviyo.com/hc/en-us/articles/16319181846171)

STA’s delivery follow-up should ask:

- Did the measurements match what arrived?
- How did it fit: fitted, regular, boxy or oversized?
- Did the condition match the photos and rating?
- What size do you normally wear?
- Optional customer photo

Because each vintage SKU may never return, the bigger value is not accumulating dozens of reviews on that exact product. It is proving that **STA’s measurements and condition grading are trustworthy across the store**.

Track:

- Fit-confirmation rate
- “Condition matched” percentage
- Photo-review rate
- Exchange rate by era, brand and player/replica version

3. January should introduce a “Rotate Your Collection” lane

Classic Football Shirts publicly operates a sell-shirt intake that requests the front, back, size details and labels. That demonstrates a visible circular-retail model, but it does not reveal its private automation or performance. [www.classicfootballshirts.co.uk: Submit a request](https://www.classicfootballshirts.co.uk/sellshirts)

STA decision:

Create a January retention campaign for previous buyers:

> **Your collection doesn’t have to stay frozen.**\
> Send us what you stopped wearing. Turn it into your next shirt.

The intake should capture:

- Team, season, player and size
- Front, back, tag and flaw photos
- Desired cash or store-credit outcome
- What they want next

Then connect the final answer to Shirt Matching. A customer selling an old piece and naming their next grail becomes both a sourcing lead and a high-intent buyer—without another blanket January discount.

---

## Message 05: Assistant

Turn: `82e3d716-9121-45f9-94ef-0f59e183ed52`

STA Email Research — October 11

Today’s conclusion: **40 segments do not need 40 separate versions of every flow.** The team segments should power one personalization system.

1. Use team segments as intelligence, not duplicated automation

Klaviyo can show or hide email sections using profile properties, including text and list values. The same email can therefore display América content to one customer, Barcelona content to another and a generic discovery block when team data is missing. [Klaviyo Help Center: How to show or hide template blocks and sections based on dynamic variables](https://help.klaviyo.com/hc/en-us/articles/7655965301531)

Recommended architecture:

- Keep the 39 purchase-team segments for analysis and campaign targeting.
- Build one master version of each core flow.
- Use conditional team blocks and inventory-aware product feeds inside it.
- If several teams qualify, prioritize:

  1. Customer-declared favorite
  2. Most frequently purchased team
  3. Most recent team purchased
  4. Recently viewed team
  5. Shirt Matching CTA

This is easier to maintain and prevents 39 slightly different flows from drifting out of date.

2. Separate declared identity from inferred purchase behavior

Klaviyo supports custom properties for size, interests and communication preferences. [Klaviyo Help Center: Profile properties reference](https://help.klaviyo.com/hc/en-us/articles/115005074627)

STA should maintain distinct fields:

- Favorite\_Teams\_Declared
- Teams\_Purchased
- Primary\_Team\_Affinity
- Usual\_Shirt\_Size
- Preferred\_Pit\_to\_Pit
- Fit\_Preference
- Player\_or\_Replica\_Preference

A purchase does not always equal fandom—it could be a gift, resale buy or style purchase. Customer-declared preferences should beat inferred purchase history.

The useful KPI is no longer “How many segments exist?” Track:

- Percentage with a known team
- Percentage with a known size
- Percentage with both team and size
- Percentage currently matchable to in-stock inventory
- Personalized versus generic click and purchase rate

3. Add one global send-traffic policy before building more flows

Klaviyo Smart Sending limits marketing messages across flows and campaigns; its default email window is 16 hours. [Klaviyo Help Center: Understanding Smart Sending in Klaviyo](https://help.klaviyo.com/hc/en-us/articles/115002779311)

Recommended STA priority:

Checkout recovery → Cart recovery → Price drop → Low inventory → Browse → Welcome/Win-back → Campaign

- Keep Smart Sending on for browse, low-inventory, price-drop and win-back messages.
- Suppress BFCM campaigns for customers actively inside checkout recovery.
- A purchase immediately removes the customer from every purchase-reminder path.
- Transactional order and shipping information remains separate from promotional traffic.

This matters more than rapidly reaching “50 flows.” Ten coordinated flows will outperform 50 flows that collide, repeat offers or recommend the wrong club and size.

---

## Message 06: Assistant

Turn: `01f199f8-306d-43c5-a026-c0f18cd747ac`

### STA retention brief — October 11, 2026

#### 1. Give loyal customers access, not an automatic discount

Klaviyo’s current guidance recommends reserving stronger discounts for “At Risk” or “Needs Attention” customers; Champions and Loyal customers can instead receive limited drops, events, or early access. Its native RFM functionality requires Advanced KDP/Marketing Analytics. [Klaviyo Help Center: How to avoid over-discounting using RFM groups](https://help.klaviyo.com/hc/en-us/articles/26978522793627)

Classic Football Shirts publicly uses this positioning: “Join the Club” for early access to new drops and offers. That copy is observable; its private automation and performance are not. [classicfootballshirts.co.uk: 2018-19 Italy Home Shirt](https://www.classicfootballshirts.co.uk/2018-19-italy-home-shirt-itah18blkv.html)

**STA decision:** split BFCM treatment by relationship:

- **Best/repeat customers:** 12–24-hour first look, led by scarcity and relevance rather than a code.\
  *“First look: shirts from your clubs, in your size.”*
- **Recent first-time buyers:** complementary teams, eras or styles; no immediate second discount.
- **At-risk customers:** receive the stronger incentive only after identity, fit and condition proof.

If paid RFM is unavailable, approximate these groups using last-order date, order count and total spend. This changes the VIP, browse/cart and win-back flows without creating more overlapping flows.

#### 2. Use BFCM credit to create a January return fixture

Shopify explicitly supports store credit for retention and marketing campaigns. Online redemption requires the customer to be signed into customer accounts or using Shop Pay, and Shopify applies the maximum available credit rather than letting the customer choose a smaller amount. POS redemption is also supported when enabled. [Store credit: Shopify Help Center](https://help.shopify.com/en/manual/customers/store-credit)

**STA test concept:**\
*“Spend $150 during BFCM and earn $25 STA credit for your January shirt hunt.”*

Using STA’s planning assumption of roughly $0.24 inventory cost per $1 of credit, $25 face value represents about $6 of modeled product cost if redeemed. That is an internal planning estimate—not the full accounting cost, because it excludes displaced revenue, fees and operational expense.

Flow decisions:

- Issue the credit after the qualifying order, not as another same-cart discount.
- January email must say **“Sign in to use your STA credit.”**
- Exclude credit holders from broad January coupon sends.
- Exclude gift-card carts until Shopify’s redemption restrictions are verified.
- Confirm account type, store-creation date and transaction-fee treatment before advertising the program; no live configuration was audited.

#### 3. Make offer sequencing purchase-aware

The practical BFCM order should be:

1. Loyal/repeat early access
2. Public, team-and-size-relevant campaign
3. Selective at-risk incentive
4. Immediate exit from browse, cart and promotional reminders after purchase
5. Post-purchase reassurance, then January credit reminder

Measure **gross margin per recipient, full-price purchase rate, credit redemption, second-order contribution margin and days to second purchase**. Open rate and issued credit alone would make the offer look healthier than it is.

---

## Message 07: Assistant

Turn: `fd4c6d59-9dfa-4394-9889-7c4cbc1269c2`

### STA Email Research — October 12

Today’s conclusion: **a sold vintage shirt should become a sourcing signal, not a dead-end restock signup.**

#### 1. Split “Back in Stock” from “Find Me Another”

Klaviyo’s Back in Stock flow waits for the specific subscribed product or variant to regain inventory. That works for replenishable products, but most one-of-one STA jerseys will never receive that exact variant again. [Klaviyo Help Center: How to build a back in stock flow](https://help.klaviyo.com/hc/en-us/articles/115003872251)

**STA decision:**

- **Replenishable/current shirts:** “Notify me when it returns.”
- **One-of-one vintage shirts:** “Find me another like this.”

The second CTA should create a Shirt Matching request prefilled with the sold shirt’s:

- Team, player and season
- Home/away/third
- Tagged size and measurements
- Condition and price
- Product/variant ID

Then ask only what remains unknown: acceptable alternatives, budget and fit flexibility.

Copy direction:

> **That one’s gone. Your shirt hunt isn’t.**\
> Tell us what you’ll compromise on—and what you won’t.

#### 2. Every sold-out page needs live substitutes

Shopify’s Search & Discovery recommendations can place manually selected or automatically generated related products on a product page, while filtering unavailable complementary products. Shopify describes related products as substitutes for the original item. [help.shopify.com: Shopify Help Center | Customize product recommendations with Shopify Search & Discovery](https://help.shopify.com/en/manual/online-store/storefront-search/search-and-discovery-recommendations)

STA’s sold-out-page hierarchy should be:

1. Same team + same size
2. Same team + adjacent fit/measurements
3. Same player or era
4. Similar color/style in the correct size
5. Shirt Matching CTA

Never let a random bestseller fill the space merely because it is available.

Flow decision: when a match request is submitted, suppress the generic browse reminder for that sold product. Send available alternatives from the request instead.

#### 3. Treat unavailable demand as a buying report

Classic Football Shirts publicly emphasizes continual discovery—its New In page currently claims more than 500 products are added daily and lets shoppers browse by team, era and condition. That is observable merchandising, not evidence about its private retention flows or results. [Latest Arrivals: New In](https://www.classicfootballshirts.co.uk/new-products1.html)

Shopify also provides reports for searches with no results, recommendation clicks and recommendation-attributed purchases. [help.shopify.com: Shopify Help Center | Shopify Search & Discovery reports and analytics](https://help.shopify.com/en/manual/online-store/storefront-search/search-and-discovery-analytics)

Combine those signals into a weekly STA sourcing report:

- Most-requested teams, players and eras
- Requested size versus available size
- Budget and acceptable condition
- Sold-out page or search term that created the request
- Viable matches found
- Customer contacted
- Clicked and purchased
- Median request-to-contact and request-to-sale time

This upgrades Shirt Matching from a customer-service idea into an inventory engine: **the shirts STA cannot currently sell reveal what STA should source next.**

---

## Message 08: Assistant

Turn: `f1214505-4154-42d7-96b6-8c94175abd68`

### STA Email Research — October 12 evening

No meaningful new public seller-copy evidence appeared today. The useful additions concern Instagram entry points and Shirt Matching capture.

#### 1. Give every physical touchpoint an Instagram “fast lane”

Manychat’s Instagram Ref URL opens a customer-initiated DM and can pass source data into custom fields. It works only in Instagram’s mobile app; new contacts may need Conversation Starters enabled or must send the first message themselves. [Manychat Help: Instagram Ref URL Trigger](https://help.manychat.com/hc/en-us/articles/14281276006684-Instagram-Ref-URL-Trigger)

**STA decision:** create distinct ref URLs and QR codes for:

- Store counter
- Local football events
- Sold-out product pages
- Order inserts
- December gift-recipient cards

Pass a source such as STA\_STORE, FC\_EVENT, SOLD\_OUT, or GIFT\_INSERT. Open with:

> **Who are we hunting for?**\
> Send the club, player or era—and we’ll narrow it down by size, condition and budget.

Track QR/ref click → DM started → match request completed → viable match → product click → purchase, plus time-to-contact and time-to-sale.

#### 2. Don’t build Shirt Matching around automatic new-follower DMs

Manychat now documents an Instagram Follow-to-DM beta, but Meta controls eligibility. It runs only once per follower, and the recipient must reply or press a non-URL button before the normal 24-hour messaging window opens. [Manychat Help: Follow to DM on Instagram: Say Hi to New Followers [BETA]](https://help.manychat.com/hc/en-us/articles/23096654243740-Follow-to-DM-on-Instagram-Say-Hi-to-New-Followers-BETA)

A delay also does not reopen that window; after 24 hours, an ordinary automated follow-up may not be delivered unless the customer interacts again. [Manychat Help: Smart Delay](https://help.manychat.com/hc/en-us/articles/14281197046812-Smart-Delay)

**STA decision:**

- Treat Follow-to-DM as an optional welcome layer, not critical infrastructure.
- Use comment keywords, Story replies and Ref URLs for explicit Shirt Matching entry.
- First button: **“Start my shirt hunt.”**
- Collect email or another verified identifier inside the conversation before linking the Instagram contact to an existing customer.
- A stored handle still does not authorize arbitrary automated outbound DMs.

#### 3. Use Klaviyo forms for stable preferences—not the request ledger

Klaviyo supports multi-step forms and recommends separating email and phone collection across steps. Form answers live on the customer profile, but repeat answers overwrite earlier values; integration-synced properties can also be overwritten by the next platform sync. [Klaviyo Help Center: Understanding form blocks and fields](https://help.klaviyo.com/hc/en-us/articles/4413550187035)

**STA capture design:**

1. Email and separate marketing choice
2. Favorite teams and usual size
3. Preferred fit and optional Instagram handle
4. Button to create the detailed Shirt Matching request elsewhere

Keep stable fields such as Favorite\_Teams\_Declared, Usual\_Shirt\_Size and Fit\_Preference on the profile. Store every specific player/season/budget/condition hunt as its own dated request record.

For December gifts, the purchaser receives order communication; the recipient’s insert links to this self-directed preference path. That prevents the purchaser’s club or size from contaminating the recipient’s future recommendations.

---

## Message 09: Assistant

Turn: `005c2d4f-b2f6-4820-addc-1aba24ea0ab2`

### STA Email Research — October 13

No meaningful new vintage-seller copy appeared. Today’s useful evidence is BFCM inbox protection.

#### 1. Don’t treat every open as engagement

Apple Mail Privacy Protection can record an open without the customer viewing the email. Klaviyo recommends excluding these machine opens and using clicks, verified opens, recent subscriptions, purchases and site activity to determine engagement. [Klaviyo Help Center: How to create an engaged segment of email subscribers](https://help.klaviyo.com/hc/en-us/articles/115000200072)

**STA decision:** build BFCM audiences in layers:

1. Recent click, purchase, checkout or verified open
2. Recently subscribed but not yet given time to engage
3. Older purchasers with relevant team-and-size inventory
4. Unengaged subscribers tested separately

The 39 team segments answer **what to show**; engagement determines **who should receive the send**.

#### 2. Expand volume gradually before BFCM

Klaviyo recommends introducing small samples of unengaged profiles between normal sends and avoiding audience increases greater than 50% over the previous day’s volume. That is platform guidance, not a promised performance result. [Klaviyo Academy: Land in the inbox on BFCM: test your audiences - Land in the inbox on Black Friday Cyber Monday](https://academy.klaviyo.com/en-us/courses/land-in-the-inbox-on-black-friday-cyber-monday/lessons/land-in-the-inbox-on-bfcm-test-your-audiences)

**STA decision:** do not wake the entire inactive database on Black Friday.

- Test older subscribers now with discovery or preference content.
- Lead with available shirts from previously purchased teams—not a blanket discount.
- Return to the core engaged audience between expansion tests.
- Remove purchasers immediately from remaining offer and recovery reminders.

Copy direction:

> **Still collecting—or should we leave you on the bench?**\
> Pick your clubs and size, and we’ll only show you shirts worth seeing.

#### 3. Let subscribers skip BFCM without leaving STA entirely

Klaviyo supports a specific BFCM\_opt\_out profile property and an exclusion segment, allowing customers to avoid promotional BFCM messages without unsubscribing from every STA email. [Klaviyo Help Center: How to allow subscribers to opt out of Mother's Day, Father's Day, and other holiday messages](https://help.klaviyo.com/hc/en-us/articles/5495696206363)

**STA decision:** include a low-key footer link:

> **Not shopping BFCM? Sit this fixture out. You’ll still hear about new shirts and community events.**

Exclude that segment from BFCM campaigns and promotional SMS, while retaining permitted service, community and post-purchase communication. This protects long-term collector relationships from one overly aggressive weekend.

No live Klaviyo configuration was audited or changed.

---

## Message 10: Assistant

Turn: `ff0cfd27-4292-4ef4-8299-4578d9632692`

### STA Email Research — October 13 evening

Three new measurement findings worth adding to the build plan:

1. **Test whether the extra reminder earns its place.**\
   Klaviyo’s branch-testing guide, updated October 8, 2026, supports randomly splitting customers between an additional email and ending the flow. [Klaviyo Help Center: How to A/B test flow branches](https://help.klaviyo.com/hc/en-us/articles/360049849432)

**STA decision:** test the final Arcade or checkout reminder against no extra reminder. Compare purchases and contribution margin per eligible customer across both branches—not just revenue attributed to the email. Keep purchase exclusions identical. This tests whether another message adds sales or merely adds noise.

2. **A “winning” variation may still be inconclusive.**\
   Klaviyo’s October 7, 2026 guidance requires more than 500 delivered messages per variation, at least 10 measured actions overall, and additional probability/range criteria for statistical significance. A date-limit winner does not necessarily meet those criteria. [Klaviyo Help Center: Understanding statistical significance in flows](https://help.klaviyo.com/hc/en-us/articles/11233978755611)

**STA decision:** avoid splitting tests across 39 team segments. Test one change within a shared flow: **identity-led copy versus fit/condition-led copy**, holding the available inventory and offer constant. Label small-sample results “directional,” not proven.

3. **Security scanners can look like interested buyers.**\
   Klaviyo identifies automated email/SMS link checks with Bot Click; custom reports include them unless explicitly filtered. Its bot-click guidance was updated January 27, 2026. [Klaviyo Help Center: Understanding bot clicks](https://help.klaviyo.com/hc/en-us/articles/22981852783899)

**STA decision:** Shirt Matching’s “Clicked” stage should require a human click where identifiable, with actual site activity and purchase tracked separately. Evaluate Instagram’s faster-reach hypothesis using **match-to-contact, human click, purchase and time-to-sale**—not raw link clicks or collected handles.

These are documented platform capabilities and proposed STA tests—not verified STA results or evidence of sellers’ private automations. Nothing was changed or sent.

---

## Message 11: Assistant

Turn: `66f871cd-161a-4541-8507-e9e22c70738c`

### STA Email Research — October 14 evening

**Paid sourcing needs a service branch inside Shirt Matching—not a normal jersey-purchase sequence.**

1. **Get approval before committing to the shirt.**\
   [First11’s public request page](https://first11shirts.com/pages/request-a-shirt) collects season, version, size, nameset, minimum condition and budget, then asks customers to approve the shirt and price before payment. Observed October 14, 2026; this reveals its public process, not private automations or results. [First11: Request a Shirt | Find Your Vintage Football Shirt](https://first11shirts.com/pages/request-a-shirt)

**STA decision:** add explicit deal-breakers. For the 1996-era Chivas request: **no nameset, suitable for regular wear**, plus confirmed measurements and total budget. A deposit is not approval of any shirt STA finds.

2. **Separate “not found” from “customer declined.”**\
   [PURE’s public concierge listing](https://purefootballshirts.com/products/service-conciergerie-pure-recherche-sur-mesure) distinguishes failure to source within 30 days from declining a found shirt, with different deposit outcomes. Those are its advertised terms—not verified fulfillment performance. [Recherche Sur-Mesure – Pure Football Shirts: Service Conciergerie PURE](https://purefootballshirts.com/products/service-conciergerie-pure-recherche-sur-mesure)

**STA decision:** the planned $100 deposit/$150 store-credit outcome needs separate request statuses: Sourcing → Match offered → Accepted/Declined → Deadline reached → Credit issued. Confirmation should state the exact deadline and clearly distinguish **store credit from a cash refund**. Don’t mark credit issued until issuance is verified.

3. **A deposit order should not trigger “How does your jersey fit?”**\
   Klaviyo’s product-specific flow guidance, updated October 7, 2026, supports filtering or branching order journeys by purchased items when those properties exist in the event. [Klaviyo Help Center: How to create a product-specific flow](https://help.klaviyo.com/hc/en-us/articles/115002779431)

**STA decision:** deposit-only orders enter sourcing confirmation and progress updates; physical jersey purchases enter delivery, care and fit follow-up. Mixed orders need both branches. Keep the sourcing service out of jersey recommendations and BFCM bundle eligibility.

Nothing was created, changed or sent.

---

## Message 12: Assistant

Turn: `7f551a53-2947-41fc-843c-51266b5d1e1c`

### STA Email Research — October 15 evening

**The BOGO + gift + Kit Cash concept needs checkout instructions as clear as the headline.** Two new findings, checked October 15:

1. **“Automatic discount” does not mean “automatically added gift.”**\
   Shopify’s native Buy X Get Y requires shoppers to add both qualifying and free items themselves. When both sides use the same collection, the lower-priced eligible item receives the discount. [Shopify documentation](https://help.shopify.com/en/manual/discounts/discount-types/buy-x-get-y). [Buy X get Y discounts: Shopify Help Center](https://help.shopify.com/en/manual/discounts/discount-types/buy-x-get-y)

**STA decision:** BFCM campaign and cart-recovery emails should explain the actual steps: choose eligible shirts, add the qualifying second piece, then select the gift if required. Don’t promise automatic gift inclusion until that behavior is tested. Recommend only available, size-relevant eligible pieces; keep Rare/Grail excluded unless explicitly approved.

2. **An old welcome or Arcade code can compete with BOGO.**\
   Shopify documents restrictions on additional product discounts for Buy X Get Y items; combination settings and store plan affect which savings apply. A unique Klaviyo code does not bypass those rules. [Shopify combination rules](https://help.shopify.com/en/manual/discounts/discount-combinations). [Combining discounts: Shopify Help Center](https://help.shopify.com/en/manual/discounts/discount-combinations)

**STA decision:** give Welcome, Arcade and checkout recovery a BFCM-specific branch that explains the approved offer without introducing another coupon. Before launch, test BOGO alone, BOGO plus gift, and each with an existing customer code. Explain Kit Cash separately as a future-use reward only once earning and redemption terms are finalized.

These are documented platform mechanics—not a live STA checkout audit or evidence of private seller performance. Nothing was changed or sent.

---

## Message 13: Assistant

Turn: `0e0368c2-ee1a-44e1-b00a-34d18cc4fe94`

### STA Email Research — October 16

**Keep Welcome. Remove its competing signup offer. Arcade should own the reward; Welcome should build confidence in STA.**

1. **A welcome series has jobs beyond discounting.**\
   Klaviyo’s September 28, 2026 practitioner guide identifies brand credibility, product education and preference collection as welcome-series functions—not just coupons. These are published recommendations, not verified STA results. [Source](https://www.klaviyo.com/blog/welcome-email-examples). [Klaviyo: 7 welcome email examples, + best practices to boost sales](https://www.klaviyo.com/blog/welcome-email-examples)

**STA decision:** make Welcome a short introduction:

- Who STA is: football, vintage and the local community.
- Why buy confidently: exact-shirt photos, condition details and measurements.
- What to discover: available shirts from their clubs, in their fit—or Shirt Matching when nothing fits.

Copy direction: *“You’ve got your reward. Now find a shirt that means something.”*

2. **Deliver the promised incentive—not another incentive.**\
   Klaviyo recommends including the signup offer in the first welcome email and using conditional branches to tailor treatment. Its guidance also recommends matching email design to the website. [Source](https://help.klaviyo.com/hc/en-us/articles/115002775172). [Klaviyo Help Center: How to create an email welcome series](https://help.klaviyo.com/hc/en-us/articles/115002775172)

**STA decision:** use one coordinated signup journey:

- **Arcade reward earned:** deliver that reward once; no separate welcome coupon.
- **No reward promised:** brand-and-discovery welcome, without inventing a discount.
- **Purchased:** stop reward reminders and move to post-purchase reassurance.

Judge the change by first-purchase rate, discount cost per order, margin per subscriber and unsubscribes—not how many welcome emails exist.

No live flows were inspected, edited or activated.

---

## Message 14: Assistant

Turn: `681e64c7-09d8-4147-b6f6-bf46b60d7cef`

### STA Email Research — October 17

No meaningful new vintage-seller copy surfaced. Today’s useful evidence is about preventing Kit Cash from compounding and protecting January margin.

1. **A discounted order can earn more credit than expected.**\
   Rise documents that some reward calculations use item prices before discounts. Its workflow conditions include order value, product, tag, and customer-segment criteria—but the public documentation reviewed does not confirm an automatic “paid with store credit” exclusion. [Rise workflow actions](https://help.rise.ai/en/articles/4020866-workflow-actions) and [conditions](https://help.rise.ai/en/articles/4020835-workflow-conditions), checked October 17, 2026. [Rise.ai Help Center: Workflow Actions](https://help.rise.ai/en/articles/4020866-workflow-actions)

**STA decision:** make this an explicit Kit Cash rule:

> **Orders using any Kit Cash earn zero new Kit Cash.**

Do not assume the current workflow enforces it. Before promoting the program, test full-credit, partial-credit, discount-plus-credit, BOGO, gift, and mixed-tender orders. Calculate earning from the customer’s eligible cash-paid merchandise amount after discounts—not headline subtotal.

2. **Delay earning until the return risk has passed.**\
   Rise says rewards linked to refunded or cancelled orders are normally removed or recalculated. It also recommends delayed issuance to prevent customers from spending rewards before returning the qualifying purchase. [Source](https://help.rise.ai/en/articles/4383790-canceling-and-management-of-rewards-for-refunded-orders). [Rise.ai Help Center: Canceling and Management of Rewards for Refunded Orders](https://help.rise.ai/en/articles/4383790-canceling-and-management-of-rewards-for-refunded-orders)

**STA flow decision:** in Post-Purchase, show “Kit Cash pending” first. Issue it only after the approved return window, then begin January-retention messaging. Cancelled, fully refunded, deposit-only and sourcing-service orders should earn nothing; partial refunds require a recalculated eligible amount.

3. **One balance reminder system should own the message.**\
   Rise’s April 30, 2026 documentation supports reminders after wallet activity or before expiration, with minimum-balance thresholds. Redeeming even part of a balance resets its activity clock. [Source](https://intercom.help/internal-303707/en/articles/12059432-store-credit-reminders). [Rise.ai Knowledge Base: Store Credit Reminders](https://intercom.help/internal-303707/en/articles/12059432-store-credit-reminders)

**STA decision:** choose Rise or Klaviyo as the sole Kit Cash reminder owner. Suppress generic January coupons and duplicate credit reminders while someone has an active balance.

Copy direction:

*“You’ve already earned your next move. Use your Kit Cash on an available shirt from your clubs—or tell us the one you’re hunting.”*

Measure cash revenue and contribution margin per redemption order, incremental second purchases, days to redemption, and the percentage of redemption orders incorrectly earning fresh credit. No live workflow was inspected or changed.

---

## Message 15: Assistant

Turn: `81c151a9-6837-440a-9d93-8f54b97ec4de`

### STA Email Research — October 17 evening

**Link Instagram to the customer profile without making a destructive merge the default.** Three useful implementation findings, checked October 17:

1. **Manychat merging can erase conversation history.**\
   Its documentation warns that the secondary contact’s Inbox history is deleted and says two different Instagram contacts cannot be linked through its merge feature. [Manychat merge guidance](https://help.manychat.com/hc/en-us/articles/14281101369116-How-to-merge-duplicate-contacts). [Manychat Help: How to merge duplicate contacts](https://help.manychat.com/hc/en-us/articles/14281101369116-How-to-merge-duplicate-contacts)

**STA decision:** Shirt Matching should use a separate identity-link record: Manychat Contact ID, optional Instagram handle, Shopify/Klaviyo profile IDs, and linkage source/date. Treat a customer-provided email as a candidate match; confirm ownership before exposing purchase history or resolving conflicting records. Never match by display name alone.

2. **Email capture and email opt-in are separate controls.**\
   Manychat stores email in a System Field and documents a distinct Set Email Opt-In setting. It also recommends explaining the intended use and considering confirmation. [Email collection guidance](https://help.manychat.com/hc/en-us/articles/14281215436188-How-to-send-emails-with-Manychat). [Manychat Help: How to send emails with Manychat](https://help.manychat.com/hc/en-us/articles/14281215436188-How-to-send-emails-with-Manychat)

**STA decision:** separate these questions:

- “Which email should we attach to your shirt hunt?”
- “Want new-drop and offer emails too?”

The first must not silently trigger Welcome, Arcade rewards, or marketing subscription. Preserve existing opt-outs; keep gift-buyer and wearer preferences separate.

3. **“Last seen” is not the same as messaging eligibility.**\
   Manychat exposes distinct Instagram fields for last seen, last interaction, and messaging-window eligibility. It also says Instagram contact timezones default to UTC+0—not the shopper’s actual location. [System Fields](https://help.manychat.com/hc/en-us/articles/14281292522652-System-Fields). [Manychat Help: System Fields](https://help.manychat.com/hc/en-us/articles/14281292522652-System-Fields)

**STA decision:** when inventory matches a request, check current messaging eligibility—not whether the customer viewed a DM. Ordinary automation belongs within the permitted 24-hour window; the extended human-agent window is for manual support, not automated sales notifications. Otherwise use a separately permitted contact route. A saved handle is insufficient. [Messaging-window guidance](https://help.manychat.com/hc/en-us/articles/14281199732892-How-to-send-messages-outside-the-24-hour-and-7-day-windows-in-Messenger-and-Instagram). [Manychat Help: How to send messages outside the 24-hour and 7-day windows in Messenger and Instagram](https://help.manychat.com/hc/en-us/articles/14281199732892-How-to-send-messages-outside-the-24-hour-and-7-day-windows-in-Messenger-and-Instagram)

Test Instagram’s speed advantage through **viable match → eligible contact → human click → purchase**, plus time-to-contact and time-to-sale. These are proposed build decisions, not verified STA capabilities or results. Nothing was changed or sent.

---

## Message 16: Assistant

Turn: `21c69c44-5feb-4b7a-8ad8-57733155015f`

### STA Email Research — October 18

**December gifting needs three different handoffs: digital gift, shipped shirt, and local pickup.** Two findings worth adding to the existing Gift and Post-Purchase flows:

1. **A scheduled gift needs different buyer and recipient messages.**\
   Classic Football Shirts’ public gift-card page offers recipient details, a message, and “send now/send later.” That is observable merchandising—not evidence of its private automations or results. Shopify separately documents recipient delivery and buyer receipts; scheduled delivery occurs approximately 4–10 a.m. in the purchaser’s timezone, not at an exact promised hour. Checked October 18, 2026. [CFS gift card](https://www.classicfootballshirts.co.uk/gift-card.html) · [Shopify guidance](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/common-customizations/add-gift-card-recipient-fields). [classicfootballshirts.co.uk: Classic Football Shirts Gift Card](https://www.classicfootballshirts.co.uk/gift-card.html)

**STA decision:** give December gift-card buyers a delivery-confirmation branch, not jersey-care or fit-check emails. Don’t duplicate the platform’s code-delivery message. Verify STA’s actual gift-card provider and scheduling behavior before advertising either feature.

Copy direction: *“Know their club, but not their fit? Let them choose the shirt.”*

Recipient marketing and preference collection remain voluntary; receiving a gift must not enroll someone into Welcome.

2. **“Ready for pickup” is not “customer has the shirt.”**\
   Shopify distinguishes ready-for-pickup notification from marking an order collected; the latter marks it fulfilled and can send a separate confirmation. [Shopify pickup guidance](https://help.shopify.com/en/manual/sell-in-person/shopify-pos/order-management/pickup-in-store-for-online-orders), checked October 18. [help.shopify.com: Shopify Help Center | Managing pickup in store orders in Shopify POS](https://help.shopify.com/en/manual/sell-in-person/shopify-pos/order-management/pickup-in-store-for-online-orders)

**STA decision:** start local buyers’ care/fit follow-up after confirmed collection—not payment or readiness. Pickup messages should contain the verified location, collection hours, and order-identification instructions.

At collection, offer a separate QR invitation: *“What shirt are you hunting next?”* Link to Shirt Matching without treating pickup details as marketing consent.

Measure gift-delivery issues, ready-to-collected time, recipient opt-in, and subsequent shirt purchases—not gift-card sales alone. No live configuration was inspected, changed, or activated.

---

## Message 17: Assistant

Turn: `749f6e61-4095-4174-90f4-4ffc4682379e`

### STA Email Research — October 18 evening

**A Shopify inventory edit does not guarantee the next email reflects it.** Two useful findings for BFCM:

1. **Collection eligibility can lag behind product updates.**\
   Klaviyo documents real-time Shopify item syncing, but new categories and category membership sync every **six hours**. Refreshing category names alone does not refresh their products. [Catalog-sync documentation](https://help.klaviyo.com/hc/en-us/articles/4406529213083), checked October 18, 2026. [Klaviyo Help Center: How to resync your Shopify catalog feed](https://help.klaviyo.com/hc/en-us/articles/4406529213083)

**STA decision:** after changes to brown-hanger eligibility or Rare/Grail exclusions, verify the relevant collection membership in Klaviyo before BFCM sends. Preview both eligible recommendations and excluded examples. An old email preview is not proof that today’s selection is correct.

2. **Product-level stock protection can miss a sold-out size.**\
   Klaviyo’s documented Shopify safeguard considers a product unavailable only when **all variants** are out of stock—and only when selling past zero inventory is disabled. With its catalog-cancellation method, one unavailable item cancels the entire recovery email rather than removing only that item. [Out-of-stock flow guidance](https://help.klaviyo.com/hc/en-us/articles/115005253188), checked October 18. [Klaviyo Help Center: How to configure out-of-stock items for automated flows on Shopify](https://help.klaviyo.com/hc/en-us/articles/115005253188)

**STA decision:** Browse, Cart, Checkout and Shirt Matching need an exact-size/variant availability check, not just “this product exists.”

Before launch, test:

- A one-of-one shirt sells before its reminder.
- The requested size sells out while another size remains.
- One item in a multi-shirt cart becomes unavailable.

Suppress the obsolete reminder. A separately designed replacement message can offer verified alternatives or Shirt Matching—but should not assume Klaviyo automatically creates that fallback.

Copy direction: *“That shirt’s gone. Here’s what still fits your hunt.”* Use it only when genuine matches exist.

Track unavailable-item skips, wrong-size recommendations, and alternative-match purchases. These are documented platform constraints and proposed STA safeguards—not a live audit. Nothing was changed or sent.

---

## Message 18: Assistant

Turn: `9eecc712-edda-4118-b7be-6456eb3c4be0`

### STA Email Research — October 19

**A human conversation needs its own reminder hold—not just a purchase exclusion.** Two useful findings, checked October 19, 2026:

1. **Manychat’s automatic pause is temporary.**\
   Manychat documents a default 30-minute automation pause when an agent starts replying. An already-running automation can continue until its next breakpoint; manually launching another automation also removes the pause. [Inbox guidance](https://help.manychat.com/hc/en-us/articles/14281070478748-Manychat-Inbox). [Manychat Help: Manychat Inbox](https://help.manychat.com/hc/en-us/articles/14281070478748-Manychat-Inbox)

**STA decision:** when someone asks about measurements, authenticity, condition, or a specific shirt match, assign an owner and deliberately hold competing reminders until the question is resolved. Don’t rely on the default pause to cover a conversation that lasts several hours.

Manychat also offers an explicit pause action, including indefinite holds, while retaining manual chat. That does **not** extend Instagram’s messaging eligibility. [Pause documentation](https://help.manychat.com/hc/en-us/articles/19957883687708-How-to-pause-all-automations). [Manychat Help: How to pause all automations](https://help.manychat.com/hc/en-us/articles/19957883687708-How-to-pause-all-automations)

2. **Support status can inform email suppression—but requires a connected signal.**\
   Klaviyo’s Zendesk integration documents ticket events usable in flows and segments, specifically recommending exclusions for customers with unresolved issues. This is a documented integration example, **not evidence that STA uses Zendesk or already has this protection**. [Klaviyo guidance](https://help.klaviyo.com/hc/en-us/articles/115005253728). [Klaviyo Help Center: Getting started with Zendesk](https://help.klaviyo.com/hc/en-us/articles/115005253728)

**STA build decision:** add a shared, verified Human\_Assistance\_Open status with an owner, reason, and review date.

- **Pre-purchase question:** hold competing Browse/Cart/Checkout reminders while the assigned person helps.
- **Order problem or exchange:** hold promotional follow-ups; preserve necessary order/service communication.
- **Resolved:** recheck purchase, inventory, consent, and channel eligibility before resuming—don’t release a backlog of stale reminders.

Copy direction: *“Let’s get the fit right before you commit.”*

Measure response time, purchases after assistance, and automated reminders sent during an active hold. These are proposed safeguards within the existing flows; nothing was inspected live, changed, or sent.

---

## Message 19: Assistant

Turn: `6cd488de-0660-4286-b6f0-16323e8cdea3`

### STA Email Research — October 19 evening

**Shirt Matching needs a reliable conversation entry—not just an Instagram link.** Two useful findings checked today:

1. **A website-link click does not open Instagram’s messaging window.**\
   Manychat documents that a comment-triggered private reply needs a reply or qualifying button/Quick Reply interaction to open the 24-hour window. An **“Open website” button does not qualify**. The comment trigger also runs only for someone’s first comment on that post or Reel. [Documentation](https://help.manychat.com/hc/en-us/articles/14281316989724-Instagram-Post-and-Reel-Comments-trigger). [Manychat Help: Instagram Post and Reel Comments trigger](https://help.manychat.com/hc/en-us/articles/14281316989724-Instagram-Post-and-Reel-Comments-trigger)

   **STA decision:** test a shirt-hunt Reel with “Comment HUNT,” followed by an opening DM: *“Which shirt are you chasing?”* Use a **“Start my hunt” Quick Reply** before collecting team, player/era, size/fit, budget and acceptable condition. Give returning hunters a direct-DM route; don’t tell them to keep commenting.
2. **An in-store QR-to-DM journey needs a fallback.**\
   Manychat’s Instagram referral links work only in the mobile app. New contacts need Conversation Starters enabled or must send a message manually; existing conversations behave differently. Its August 27 documentation also supports referral data in custom fields. [Documentation](https://help.manychat.com/hc/en-us/articles/14281276006684-Instagram-Ref-URL-Trigger). [Manychat Help: Instagram Ref URL Trigger](https://help.manychat.com/hc/en-us/articles/14281276006684-Instagram-Ref-URL-Trigger)

   **STA decision:** use separately tracked entry links for the shop counter, community events, sold-out pages and December gift shoppers. Offer a web request form alongside Instagram. Start gift requests with *“For you—or someone else?”* Keep recipient preferences separate.

   Test with both a **brand-new Instagram contact and an existing conversation** before printing QR cards. Store a source code in the link—not customer email or personal details.

**Measure:** completed requests → available matches → eligible contacts reached → human clicks → purchases, plus time-to-contact and time-to-sale. Instagram being faster remains a hypothesis. Neither a saved handle nor a QR scan grants ongoing automated-DM permission.

These are documented platform mechanics and proposed STA decisions—not observed seller automations or verified STA results. Nothing was changed or sent.

---

## Message 20: Assistant

Turn: `be0b583d-4e24-4294-8bd5-a6892922a25e`

### STA retention brief: sold-out shirts

1. **Split “restock” from “find me another.”** Klaviyo’s back-in-stock flow waits for the same product or variant to be replenished. That fits repeatable stock, but many vintage shirts are effectively one-offs. [Klaviyo Help Center: Understanding how back in stock flows work](https://help.klaviyo.com/hc/en-us/articles/360051612551)\
   **STA decision:** On unique sold-out listings, replace “Notify me when available” with **“Find me another one.”** Carry the viewed shirt into a matching form, then capture team, season/player, size or measurements, preferred fit, budget, and acceptable condition. Keep literal back-in-stock alerts only for SKUs likely to return.
2. **One shirt should not trigger a terrace-sized rush.** Klaviyo can batch alerts according to available units and wait between batches; its default is to notify everyone at once. [Klaviyo Help Center: How to build a back in stock flow](https://help.klaviyo.com/hc/en-us/articles/115003872251)\
   **STA decision:** For single-unit arrivals, use a very small first batch and oldest-request-first priority. Copy should stay operationally honest: **“One just came in. It’s available now—first completed order gets it.”** Don’t imply a reserved window unless Shopify inventory is actually held. Suppress browse/cart reminders for the same shirt while this alert is active.
3. **Treat unmatched requests as sourcing intelligence.** Klaviyo’s queue export includes date added, SKU, variant, product title, variant title, and price, and explicitly positions the data as a way to identify demand. [Klaviyo Help Center: How to export a list of queued back in stock subscribers](https://help.klaviyo.com/hc/en-us/articles/1260805819449)\
   **STA decision:** Add a weekly demand view grouped by team × era/player × size × budget. Track **request-to-match, match-to-contact, click, purchase, and median time-to-sale**—plus unmet demand after 30/60/90 days.

Public seller evidence supports the broader discovery layer: Classic Football Shirts openly tells Manchester City shoppers that new stock arrives regularly and promotes its newsletter, while foregrounding individual authentication, size, and condition. [Vintage Kits & Jerseys: Manchester City Classic Football Shirts](https://www.classicfootballshirts.co.uk/premiership-clubs/manchester-city.html) That is observable site copy—not evidence of its private automations or results.

**Flow-foundation update:** Make **Flow 6: Sold-out → Shirt Matching** the build priority, separate from **Flow 7: True Back-in-Stock**. This prevents false promises while turning every missed shirt into useful sourcing demand.

---

## Message 21: Assistant

Turn: `539fe680-3569-440d-917a-1321dd2963fa`

### STA Email Research — October 21

**Flow 8 should be Exchange & Store-Credit Resolution—not a generic refund flow.**

1. **An exchange request is not an approved exchange.**\
   Shopify’s self-service system lets customers request returns or cancellations, but the request does not change the order automatically. Native self-service also cannot accept an exchange-specific request. [help.shopify.com: Setting up self-serve returns and cancellations](https://help.shopify.com/en/manual/fulfillment/managing-orders/returns/self-serve-returns/setup)

   **STA decision:** use explicit statuses: Requested → Eligibility checked → Approved → Shirt received/inspected → Credit issued or replacement selected → Closed. Pause review requests, care follow-ups, Kit Cash issuance and promotional reminders while unresolved. Necessary service updates continue.
2. **Klaviyo sees refunds and cancellations—but not necessarily STA’s full exchange journey.**\
   Its Shopify integration documents Refunded Order and Cancelled Order events. A return request, inspection or completed store-credit exchange may require another verified signal. [Klaviyo Help Center: Shopify data reference](https://help.klaviyo.com/hc/en-us/articles/115005080447)

   **STA decision:** suppress stale post-purchase messaging immediately on refund or cancellation. Don’t automate exchange-resolution copy until a dependable status source is confirmed. After resolution, recommend only available shirts matching the customer’s team and actual fit—not the returned item.
3. **State exactly which credit system the customer received.**\
   Shopify’s native credit requires customer-account or Shop Pay sign-in, cannot be used on draft or edited orders, and applies the available balance rather than letting shoppers choose a partial amount. [help.shopify.com: Store credit](https://help.shopify.com/en/manual/customers/store-credit) Since STA also uses Rise Kit Cash, “store credit” and “Kit Cash” should not be presented as interchangeable unless verified.

   **Copy decision:**\
   *“Your exchange is complete. You now have $\_\_\_ in [exact credit type]. Here’s where to see it and how to use it.”*

Classic Football Shirts publicly requires returns to remain unworn, unwashed and in the original condition, including attached tags. That is observable policy copy—not evidence of its private workflows or performance. [classicfootballshirtssupport.zendesk.com: Returns](https://classicfootballshirtssupport.zendesk.com/hc/en-us/articles/360024047491-Returns)

**STA implementation:** photograph and re-grade returned vintage shirts before restocking. Track request-to-resolution time, credit issued correctly, exchange-credit redemption, repeat purchase and messages incorrectly sent during an open case. Nothing was changed or sent.

---

## Message 22: Assistant

Turn: `de01bde3-76a0-4c21-bbdc-8885a6a37540`

### STA Email Research — October 21 evening

**BFCM needs a message-priority system. Smart Sending alone cannot decide which message deserves the shirt.**

1. **A skipped flow email is not sent later.**\
   Klaviyo’s Smart Sending skips marketing messages when someone was contacted recently, but does not automatically reschedule them. If a broad campaign lands first, the more relevant checkout or cart message can disappear entirely. [Klaviyo documentation](https://help.klaviyo.com/hc/en-us/articles/115002779311). [help.klaviyo.com: Understanding Smart Sending in Klaviyo](https://help.klaviyo.com/hc/en-us/articles/115002779311)

   **STA decision:** campaigns should yield to active buying journeys:

   Service/transactional → human assistance → available Shirt Match → checkout → cart → browse → Welcome/broad campaign

   Exclude active checkout, open assistance and viable-shirt-match customers from broad BFCM sends. Their dedicated message should contain the approved BFCM offer so they do not miss it.
2. **Email frequency protection does not control SMS.**\
   Klaviyo manages email and SMS Smart Sending separately. Someone can therefore receive both channels close together even when both settings are enabled. [help.klaviyo.com: Understanding Smart Sending in Klaviyo](https://help.klaviyo.com/hc/en-us/articles/115002779311)

   **STA decision:** add a cross-channel contact rule outside Smart Sending. Use SMS only when consent is verified and it adds urgency—such as an expiring customer-earned reward or genuinely available requested shirt. Don’t follow every BFCM email with a text.
3. **Use live eligibility checks, not entry-time assumptions.**\
   Klaviyo rechecks profile filters before each flow message, allowing purchasers or open-support cases to be skipped before the next send. Trigger filters are not rechecked the same way. [Flow guidance](https://help.klaviyo.com/hc/en-us/articles/115002774932). [help.klaviyo.com: Getting started with flows](https://help.klaviyo.com/hc/en-us/articles/115002774932)

   **STA decision:** before every purchase reminder, recheck purchase, exact-variant availability, open assistance/exchange, current offer eligibility and active Shirt Match. Don’t release accumulated reminders when a hold ends.

**Foundation update:** build **Flow 9: BFCM Offer Orchestration** around this hierarchy. Measure reminders suppressed correctly, purchase-message collisions, messages per customer, conversion and contribution margin—not total sends.

These are documented Klaviyo mechanics and proposed STA controls, not evidence of competitor automations or STA’s current configuration. Nothing was changed or sent.

---

## Message 23: Assistant

Turn: `f228a4c1-2692-459f-9794-99ee4b1cf857`

### STA Email Research — October 22

**Flow 10 should be Community → Customer, built around permission—not harvesting everyone who walks into Weekly FC, Cascarritas or the shop.**

1. **A digital receipt creates a profile, not automatic marketing permission.**\
   Shopify POS can create a customer profile from an email or phone used for a receipt, but marketing signup is presented as a separate choice. [Shopify POS documentation](https://help.shopify.com/en/manual/sell-in-person/shopify-pos/receipt-management/customer-receipt-selection). [Customer receipt selection: Shopify Help Center](https://help.shopify.com/en/manual/sell-in-person/shopify-pos/receipt-management/customer-receipt-selection)

   **STA decision:** keep three permissions distinct:

   - Contact details needed for an RSVP or receipt.
   - Email/SMS marketing opt-in.
   - Optional Instagram contact for Shirt Matching.

   Never place an FC attendee into Welcome merely because they RSVP’d, received a receipt or joined a group chat.
2. **In-store purchases can be separated from online behavior.**\
   Klaviyo’s Shopify integration syncs source\_name, including POS, plus location information when available. [Klaviyo documentation](https://help.klaviyo.com/hc/en-us/articles/115005253248). [Klaviyo Help Center: How to differentiate Shopify POS and Shopify web data](https://help.klaviyo.com/hc/en-us/articles/115005253248)

   **STA decision:** after a verified POS purchase, send an in-store-specific follow-up rather than the generic online sequence:

   *“Good seeing you at STA. How did the shirt fit once you got it into the rotation?”*

   Then offer available shirts from their club and size, the next community event, or Shirt Matching. Do not send shipping education to a walk-in buyer.
3. **Don’t make excessive data capture the price of entering the community.**\
   Shopify warns that requiring customer information at POS can prevent checkout when someone declines. Its recommended setting allows staff to skip collection. [help.shopify.com: Shopify Help Center | Managing required checkout information for your Shopify POS](https://help.shopify.com/en/manual/sell-in-person/getting-started/shopify-pos-from-admin/required-checkout-information)

   **STA decision:** keep event entry light. After attendance, invite people to voluntarily add favorite team, shirt size/measurements and the specific shirt they are hunting. If they choose Instagram, let them initiate the conversation; a saved handle still does not permit automated outbound DMs.

**Measure:** attendee → identified profile, voluntary opt-in, preference completion, first purchase, repeat attendance and time-to-sale. Separate community participation from revenue so STA can see whether FC and Cascarritas actually create customers rather than merely collecting contacts.

**Foundation complete:** Flow 10 is Community → Customer. No meaningful new public vintage-seller automation evidence appeared in this pass; these are documented Shopify/Klaviyo capabilities and proposed STA decisions. Nothing was changed or sent.

---

## Message 24: Assistant

Turn: `0cd3aea3-d657-40b7-a947-f8f8cdbe6aaa`

### STA Email Research — October 22 evening

**The highest-leverage email improvement may begin inside site search—not inside another email.**

1. **“No results” and “results nobody clicks” are different failures.**\
   Shopify reports them separately and warns that search-report data can lag by up to 72 hours. No-result searches expose inventory gaps; no-click searches suggest weak titles, images, relevance or filtering. [Shopify behavior reports](https://help.shopify.com/en/manual/reports-and-analytics/shopify-reports/report-types/default-reports/behaviour-reports). [help.shopify.com: Behavior reports](https://help.shopify.com/en/manual/reports-and-analytics/shopify-reports/report-types/default-reports/behaviour-reports)

   **STA decision:** review searches weekly by:

   - Team, player and era.
   - Requested size.
   - No results versus results with no clicks.
   - Available inventory and eventual purchase.

   Send repeated no-result demand into Shirt Matching and sourcing. Don’t interpret the report as real-time demand.
2. **Klaviyo can receive Submitted Search, but a search is not automatically permission to email.**\
   Klaviyo documents server-side Shopify pixel support for search events and flow triggering. [help.klaviyo.com: Understanding identity resolution in Klaviyo](https://help.klaviyo.com/hc/en-us/articles/12902308138011)

   **STA decision:** use search behavior only for already identified, properly consented profiles. Add purchase and reminder-priority exclusions. Then:

   - **Verified available match:** *“Still looking for Chivas? These are actually available in your size.”*
   - **No verified match:** offer Shirt Matching, capturing the exact season/player/version, fit, budget and acceptable condition.
   - **Anonymous or unsubscribed visitor:** improve the search experience; don’t manufacture a contact route.
3. **Fix discoverability before recovering the visitor.**\
   Shopify Search & Discovery supports synonyms, product boosts and availability/attribute filters. Boosts apply only to available products; sold-out products are pushed behind purchasable inventory. [help.shopify.com: Shopify Help Center | Modifying search with Shopify Search & Discovery](https://help.shopify.com/manual/online-store/search-and-discovery/product-boosts)

   **STA decision:** build synonyms for genuine equivalents—club names, abbreviations and common shirt terminology—while keeping loose associations separate. Make size, condition and availability prominent filters. A customer searching “Chivas 96” should reach the closest available Chivas pieces and a clear **“Find me the exact one”** route.

**Measure:** search → product click, search → matching request, match-to-contact, purchase and time-to-sale. This extends Browse and Shirt Matching; it should not become an overlapping eleventh reminder flow.

No meaningful public competitor-automation evidence appeared in this pass. These are documented platform capabilities and proposed STA decisions, not a live funnel audit. Nothing was changed or sent.

---

## Message 25: Assistant

Turn: `4f573bf7-b51e-4772-b96f-bb76db720f48`

### STA Email Research — October 23

**TikTok LIVE mystery auctions need their own acquisition-source branch inside Post-Purchase—not a separate retention universe.**

1. **A synced TikTok order is not documented marketing consent.**\
   Shopify and TikTok document syncing TikTok Shop catalog, inventory, fulfillment and orders into Shopify. Their public setup guidance does not say that a marketplace buyer becomes an email or SMS subscriber. That absence matters. [Shopify setup](https://help.shopify.com/en/manual/online-sales-channels/social-commerce/tiktok/setup) · [TikTok setup](https://ads.tiktok.com/business/en/guides/tiktok-shop-shopify-setup-guide). [help.shopify.com: Setting up TikTok Shop](https://help.shopify.com/en/manual/online-sales-channels/social-commerce/tiktok/setup)

   **STA decision:** identify TikTok orders by verified order source, but treat marketing permission as unknown until confirmed. Put a voluntary parcel QR behind the purchase:

   *“Tell us what you pulled—and what shirt you actually hunt.”*

   Capture favorite teams, teams to avoid, size/fit, player/era, budget, acceptable condition, email preference and optional Instagram contact separately.
2. **Mystery cannot mean unclear.**\
   TikTok requires accurate, non-misleading LIVE product claims, and its US auction terms say winning auction orders must be fulfilled; eligible LIVE Auction orders are generally treated as final sale subject to platform return/refund rules. [seller-us.tiktok.com: Content Policy](https://seller-us.tiktok.com/university/essay?knowledge_id=6837891779151617)

   **STA decision:** before bidding begins, state the verified size, authenticity standard, condition range, whether the shirt is revealed or genuinely unknown, and the channel-specific return treatment. Don’t let the normal STA exchange message contradict TikTok auction terms.
3. **Preference flexibility can differentiate STA’s next purchase.**\
   Classic Football Shirts publicly says its mystery boxes cannot currently accommodate specific team or league inclusion/exclusion requests, while emphasizing authenticity and selectable sizing. That is observable product copy—not evidence of its private retention automations or performance. [classicfootballshirts.co.uk: Mystery Shirt Box](https://www.classicfootballshirts.co.uk/mystery-shirt-box.html)

   **STA decision:** don’t promise customization for an already-won mystery auction. Instead, use the unboxing follow-up to learn what the buyer loved or would avoid next time, then route future demand to verified inventory or Shirt Matching.

**Measure:** LIVE viewer → bidder → buyer, delivered order → voluntary preference completion, match-to-contact, second purchase and time-to-sale. TikTok customer data alone should not trigger Welcome, Arcade or promotional SMS.

Nothing was inspected live, changed or sent.

---

## Message 26: Assistant

Turn: `fc5f37dd-5457-40f1-be8f-d109ab6b81d0`

### STA research brief — October 23, 2026

1. **“Pick any three for $100” needs a mix-and-match implementation.** Shopify’s first-party Bundles app supports predetermined bundles and multipacks. Shopify classifies customer-selected combinations as mix-and-match bundles and points merchants toward compatible third-party or custom solutions. Standard amount-off discounts can target a collection and require a minimum quantity, but they subtract a fixed amount or percentage; they do not inherently make three differently priced items total exactly $100. [help.shopify.com: Shopify Bundles](https://help.shopify.com/en/manual/products/bundles/shopify-bundles)

   **STA decision:** Before advertising the Hat Trick, test three different Brown Hanger products, duplicate quantities, and carts containing four or six eligible items. If the exact-total mechanic cannot be implemented cleanly, sell selected three-piece bundles instead. Copy should say **“Choose any 3 eligible Brown Hanger pieces for $100”** only after that test passes.
2. **Make the reassurance part of the offer, especially for vintage pieces.** Classic Football Shirts publicly describes its vintage mystery stock as pre-loved, specifies the promised condition range, states a minimum value, and offers explicit size choices. That is observed storefront copy; it provides no evidence about private email automation or conversion performance. [classicfootballshirts.com: Vintage Mystery Shirt Box](https://www.classicfootballshirts.com/awaydays-mens-mystery-vintage-football-shirt-box009.html)

   **STA decision:** Put this directly below the Hat Trick headline: **“Three real pieces, picked by you. Check each listing for tagged size, measured fit and condition before adding it to your three.”** Link to the eligible collection filtered by available size. Avoid a generic “vintage condition may vary” disclaimer that makes the deal feel like a clearance gamble.
3. **The deadline must govern both the discount and every reminder.** Klaviyo documents that campaign coupons cannot use the variable expiration available in flows, while coupon links still depend on Shopify’s product, expiration, combination and minimum-purchase rules. [help.klaviyo.com: How to create unique coupon codes for Shopify](https://help.klaviyo.com/hc/en-us/articles/115006155388)

   **STA decision:** Use one published Pacific Time cutoff across the landing page, campaign copy and Shopify discount. Suppress purchasers from later Hat Trick sends, stop all sale reminders at the cutoff, and replace any post-cutoff abandoned-cart message with ordinary Brown Hanger availability or shirt-matching copy. Do not let a stale reminder promise **3 for $100** after checkout can no longer honor it.

No public source verifies STA’s current Shopify configuration, inventory, margins or private Klaviyo logic, so those remain implementation checks rather than audit findings.

---

## Message 27: Assistant

Turn: `08d4f0c5-b4fb-4840-b9ce-b85ffaa69248`

### STA Email Research — October 24

**December gifting needs a clean handoff from purchaser to recipient.**

1. **Shopify supports scheduled digital gifting.** Buyers can enter a recipient, personal message and future delivery date when the theme supports Shopify’s gift-card recipient fields. [shopify.dev: Add a gift card recipient form](https://shopify.dev/docs/storefronts/themes/product-merchandising/gift-cards)

   **STA decision:** Make gift cards the low-friction fallback for shoppers unsure about team, era, condition or fit. Copy direction:

   *“They know the shirt when they see it. Send STA credit now—or schedule it for Christmas morning.”*

   Classic Football Shirts publicly uses the simple proposition “Let them decide.” That is observed storefront copy, with no public evidence about its automation or performance. [classicfootballshirts.com: Classic Football Shirts Gift Card (Digital)](https://www.classicfootballshirts.com/classic-football-shirts-gift-card-digital-1920952.html)
2. **A recipient email is not marketing permission.** Shopify records purchaser and recipient emails separately, while its marketing documentation requires a separate checkout, sign-in or form opt-in. Klaviyo likewise distinguishes transactional delivery from promotional consent. [Collecting customer contact information: Shopify Help Center](https://help.shopify.com/en/manual/promoting-marketing/create-marketing/customer-contact-information)

   **STA decision:** Send the gift and redemption instructions to the recipient, but do not trigger Welcome, Browse, Arcade or promotional SMS from the recipient address. After redemption, offer a voluntary preference step for favorite teams, size/fit, players/eras and Shirt Matching.
3. **Use gift receipts to prevent the wrong January follow-up.** Shopify POS gift receipts hide the amount and can support a return or exchange. They cover the full order, so gifts for different recipients should be processed separately when individual receipts are needed. [help.shopify.com: Managing Shopify POS receipts](https://help.shopify.com/en/manual/sell-in-person/shopify-pos/receipt-management/managing-receipts)

   **STA decision:** Mark verified gift purchases so the buyer does not receive *“How does your shirt fit?”* Instead, send:

   *“Did the gift land? If the fit or era missed, we’ll help them find the right shirt.”*

   Route exchanges through the existing resolution flow. Contact the recipient with recommendations only after verified opt-in.

**Measure:** gift purchase → successful delivery, redemption, voluntary recipient opt-in, preference completion, Shirt Match request, purchase and time-to-sale. These are proposed December-to-January controls, not a live audit. Nothing was changed or sent.

---

## Message 28: Assistant

Turn: `b998581d-9d50-4b3b-be6b-b5f4a6d95724`

### STA Email Research — October 24 evening

**January retention should restart the hunt, not immediately discount another shirt.**

1. **Time win-back from STA’s buying cycle.** Klaviyo recommends placing the first message slightly after the store’s normal repeat-purchase interval. It also recommends a live profile filter requiring zero orders since entering the flow, so a customer who buys again stops receiving win-back messages. [help.klaviyo.com: How to create a winback flow](https://help.klaviyo.com/hc/en-us/articles/115002775192)

   **STA decision:** Calculate STA’s median days between first and second purchases before choosing the delay. January campaign sends should suppress customers already in Checkout, Cart, Shirt Matching, exchange assistance or a recent-purchaser sequence.
2. **Use purchasing behavior to protect margin.** Klaviyo’s RFM analysis can separate recent, loyal and inactive buyers, but requires at least 500 purchasing customers, 180 days of order history, recent orders and some customers with three-plus orders. [help.klaviyo.com: Getting started with the recency, frequency, and monetary ...](https://help.klaviyo.com/hc/en-us/articles/17797889315355)

   **STA decision:** Verify eligibility before relying on RFM. If qualified:

   - **Recent first-time buyer:** discovery and preference capture; no automatic discount.
   - **Loyal collector:** first look at verified team-and-size inventory or a Shirt Match.
   - **Lapsed one-time buyer:** identity-led win-back, with an incentive tested only after a non-discount message.

   If RFM is unavailable, reproduce the logic with verified order count and last-purchase date.
3. **Collector language is stronger than generic “we miss you” copy.** Classic Football Shirts publicly frames retention around building a collection, wearing football history and discovering forgotten kits; Cult Kits similarly speaks to collectors and pieces that rarely surface twice. These are observable public messages, not evidence of private automations or sales performance. [Classic Retro Vintage Football Shirts: Classic Football Shirts : retro vintage soccer jerseys](https://www.classicfootballshirts.com/2024-25.html)

   **STA copy direction:**

   **Subject:** *what shirt are you hunting in 2027?*\
   **Body:** *New year, new hunt. Tell us the club, player or era—and the fit you actually wear. If it’s already at STA, we’ll show you. If it isn’t, we’ll track the demand and start looking.*

   Link into Shirt Matching with known team and size prefilled when verified. Track preference completion, match-to-contact, purchase, repeat-purchase interval and time-to-sale. Nothing was inspected live, changed or sent.

---

## Message 29: Assistant

Turn: `e42c77aa-d3f5-484c-8c66-b564c96100a7`

### STA Email Research — October 25

**Hat Trick can leak margin through Kit Cash even when discount stacking is disabled.**

1. **Store credit applies after Shopify discounts.** Shopify says gift cards and store credit used as payment do not reduce a promotion’s minimum-purchase calculation. A customer can therefore qualify for Hat Trick pricing and then use available credit against the discounted total. [help.shopify.com: Amount off discounts](https://help.shopify.com/en/manual/discounts/discount-types/percentage-fixed-amount)

   **STA decision:** Model cash collected after both the promotion and Kit Cash redemption. Turning off discount combinations does not necessarily block credit because credit is a payment method.
2. **Rise’s documented “Order Paid” trigger may create the double-dip STA wants to prevent.** Rise says the workflow activates when payment is captured. Its documented Order Subtotal Price condition does not account for discounts, so a heavily discounted order can still satisfy a reward threshold. The public documentation does not prove whether STA’s workflow excludes credit-funded purchases. [Rise.ai Help Center: Workflow Triggers](https://help.rise.ai/en/articles/4020864-workflow-triggers)

   **STA decision:** Before promoting Hat Trick, test these orders:

   - Promotion only.
   - Promotion plus partial Kit Cash.
   - Promotion fully covered by Kit Cash.
   - Promotion plus another discount code.
   - Refunded or exchanged promotion order.

   Confirm that credit-funded purchases earn **zero new Kit Cash**, matching STA’s stated policy. Until verified, do not let a Rise reward email promise newly earned credit for these orders.
3. **Delayed reward issuance can reduce reversals.** Rise recommends placing a delay before rewards when an order might be refunded, because rewards are otherwise issued and later adjusted or canceled. [Rise.ai Help Center: Canceling and Management of Rewards for Refunded Orders](https://help.rise.ai/en/articles/4383790-canceling-and-management-of-rewards-for-refunded-orders)

   **STA decision:** Coordinate any reward delay with STA’s exchange window and keep exchange-resolution messages ahead of reward notifications. Once enforcement is verified, state plainly:

   *“Kit Cash works on this order. Hat Trick purchases do not earn additional Kit Cash.”*

Track discounted revenue, cash collected after credit, credit redeemed, new credit issued incorrectly and contribution margin per Hat Trick order. No meaningful public football-shirt seller evidence appeared for this private checkout mechanic, and STA’s live Rise configuration was not audited. Nothing was changed or sent.

---

## Message 30: Assistant

Turn: `279d1edd-2235-4d44-ac00-0a8b2f512107`

### STA Email Research — October 26

**Instagram’s speed advantage needs a controlled test; platform-attributed revenue alone will not prove it.**

1. **Klaviyo can credit a purchase after an email open without a click.** Its default last-touch model considers eligible email opens, clicks and other channel interactions inside configured windows. New accounts default to five-day email windows, and Apple privacy opens can count unless excluded. [Klaviyo Help Center: Understanding message conversion tracking](https://help.klaviyo.com/hc/en-us/articles/115005248128)

   **STA decision:** Do not call email the winner from attributed revenue alone. For Shirt Matching, prioritize confirmed link clicks, purchases tied to the request and median time-to-sale.
2. **Manychat measures DM activity, but an external Shopify purchase needs reconciliation.** Manychat reports automation sends, CTR and contacts captured. Its automatic Purchase event applies to purchases completed through its own Buy Button; a click leading to STA’s Shopify store does not by itself prove the resulting order. [Manychat Help: Conversions API (CAPI) integration](https://help.manychat.com/hc/en-us/articles/14580897414300-Conversions-API-CAPI-integration)

   **STA decision:** Give every matching request a non-personal request\_id. Carry it through the email or Instagram link using a custom field and UTM parameter, then connect it to the Shopify order when available. Never put an email address or Instagram handle in the URL.
3. **Shopify can reconcile channels through several attribution views.** Shopify supports first-click, last-click, last non-direct, linear and any-click reporting. It warns that any-click can allocate more credit than the number of orders. Order conversion summaries can expose UTMs and session referrals, though tracking may be incomplete when cookies or apps block it. [help.shopify.com: Marketing reports](https://help.shopify.com/en/manual/reports-and-analytics/shopify-reports/report-types/default-reports/marketing-reports)

   **STA test:** Among customers eligible for both channels, randomly send the first verified match by email or Instagram DM and hold the other marketing channel temporarily.

   Measure:

   - Match ready → first contact
   - Contact → click
   - Click → purchase
   - Match ready → purchase
   - Contribution margin
   - Cross-channel reminders prevented

Instagram is faster only if it reduces contact or sale time without increasing collisions or lowering margin. No meaningful new public seller evidence appeared for this private measurement question. These are documented platform capabilities and a proposed test, not verified STA results. Nothing was changed or sent.

---

## Message 31: Assistant

Turn: `d4aaee7d-c002-4057-819d-6713dc949600`

### STA Email Research — October 26 evening

**Shirt Matching needs an Instagram permission ladder. Capturing a handle is only the first step.**

1. **A comment does not necessarily open unrestricted automated messaging.**\
   With Manychat’s Instagram comment trigger, the private reply must prompt a button or Quick Reply interaction to open the 24-hour messaging window. An external website button does not opt the person in or open that window. Follow-to-DM similarly requires a reply or non-URL button interaction before continuing the automation. [help.manychat.com: Instagram Post and Reel Comments trigger](https://help.manychat.com/hc/en-us/articles/14281316989724-Instagram-Post-and-Reel-Comments-trigger)

   **STA decision:** use a clear two-step entry:

   - Comment keyword: **“MATCH”**
   - Opening DM: *“Want us to help hunt the exact shirt? Tap below to start your request.”*
   - Quick Reply: **Start my shirt hunt**

   Only after that interaction should STA collect team, shirt, player, era, size/fit, budget and acceptable condition. A saved handle alone must not trigger future automated DMs.
2. **Manual response time and automated messaging time are different.**\
   Meta’s standard automated messaging window is 24 hours after the qualifying interaction. Its Human Agent feature can support a person manually responding within seven days of the customer’s message; this is for human follow-up, not scheduled promotional automation. [developers.facebook.com: Messenger Platform and IG Messaging API policy](https://developers.facebook.com/documentation/business-messaging/messenger-platform/policy)

   **STA decision:** when a shirt match becomes available:

   - Inside the active 24-hour window: the matching automation may send it.
   - Outside 24 hours but within an eligible support conversation: a staff member may respond manually where Meta permits.
   - Outside those conditions: use the customer’s separately authorized email channel or wait for them to re-engage.

   Copy should never promise *“We’ll DM whenever one arrives”* unless the future messaging route is actually permitted.
3. **Link the identity through customer-provided information, not a guessed handle match.**\
   Manychat assigns a Contact ID, while Meta uses a separate Instagram-scoped user ID. Manychat explicitly says these are different identifiers. Klaviyo can identify or merge profiles through email or a shared external ID, but profile merges carry history and cannot be casually reversed. [Manychat Help: System Fields](https://help.manychat.com/hc/en-us/articles/14281292522652-System-Fields)

   **STA data decision:** store:

   - shirt\_match\_request\_id
   - Manychat Contact ID
   - Instagram-scoped ID where available
   - Instagram username as a changeable display field
   - Customer-provided email
   - Verified Shopify/Klaviyo customer ID after deterministic linkage
   - Preferred match-notification channel and consent timestamp

   Use the customer-provided email or an identified email-to-Instagram referral link to establish the relationship. Do not merge profiles merely because names, handles or favorite teams look similar.

**Important consent guard:** Manychat can collect an email and push it into a Klaviyo list, and its integration guidance can cause those contacts to become subscribed depending on the list’s opt-in configuration. STA should ask separately:

*“Where should we contact you about this shirt request?”*\
*“Do you also want STA drops and community emails?”*

Those are two different permissions. [help.manychat.com: Klaviyo integration](https://help.manychat.com/hc/en-us/articles/14281297264924-Klaviyo-integration)

This strengthens the existing **Shirt Matching** and **Community → Customer** flows rather than creating an overlapping eleventh flow. Measure request → eligible contact, contact → click, purchase and time-to-sale. No meaningful new public vintage-seller automation evidence appeared in this pass; these are documented Meta/Manychat/Klaviyo capabilities and proposed STA controls. Nothing was changed or sent.

---

## Message 32: Assistant

Turn: `614f13dc-ceac-4528-ad5b-fe39c1d8d553`

### STA Email Research — October 27

**A sold-out vintage shirt needs two different exits: exact restock or keep hunting.**

1. **Back-in-stock and Shirt Matching represent different intent.**\
   Klaviyo’s updated Shopify form records the selected out-of-stock variant and can collect an email specifically for its restock alert. Promotional-email permission is a separate optional checkbox. [Klaviyo Help Center: How to set up a back in stock form](https://help.klaviyo.com/hc/en-us/articles/38767539287323)

   **STA decision:**

   - Repeatable merchandise: **“Tell me when this exact size returns.”**
   - Vintage, player-issued or one-of-one pieces: **“Find me another one like this.”**

   The second route should prefill the sold-out shirt, then collect acceptable alternatives: exact or similar season, player, home/away version, size/fit, budget and condition.
2. **Do not alert the whole waiting list for one available shirt.**\
   Klaviyo can impose a restock minimum and release notifications in batches based on available inventory. Its Shopify integration can also count inventory held in the physical store when determining availability. [Klaviyo Help Center: How to build a back in stock flow](https://help.klaviyo.com/hc/en-us/articles/115003872251)

   **STA decision:** reserve exact restock alerts for inventory that is genuinely purchasable online. For a single returned vintage shirt, notify the oldest qualified requester first and hold everyone else. Confirm the shirt’s new condition grade, measurements and fulfillment location before releasing the alert.

   **Copy:** *“The exact shirt you asked about is available again. Same listing, updated condition and measurements. One is available.”*
3. **One alert is safer than a reminder sequence.**\
   Klaviyo says it cannot recheck whether the product has sold out again before a second back-in-stock message. [help.klaviyo.com: Understanding how back in stock flows work](https://help.klaviyo.com/hc/en-us/articles/360051612551)

   **STA decision:** send one exact-item alert. If it sells, suppress further product reminders and return remaining demand to Shirt Matching:

   *“That one went quickly. Want us to keep hunting the same shirt—or widen the search to the same club and era?”*

Cult Kits publicly preserves sold-out shirt pages and uses collector-oriented signup language such as **“Count me IN!”** This is observable storefront copy; it does not verify that Cult Kits runs variant-specific alerts or any particular private automation. [Cult Kits: 2007/09 MANCHESTER UNITED RONALDO #7 HOME SHIRT (L) NIKE](https://www.cultkits.com/products/2007-09-manchester-united-ronaldo-7-home-shirt-l-nike35)

This strengthens the existing **Browse/Availability** and **Shirt Matching** journeys. Measure exact-alert subscription, match-request completion, match-to-contact, purchase, time-to-sale and repeated unmet demand by team, era and size. Nothing was changed or sent.

---

## Message 33: Assistant

Turn: `b8d7e8d5-5fda-4e14-aae8-425d0f2cc2d9`

### STA Email Research — October 27 evening

**STA needs a customer-editable “shirt profile,” not permanent assumptions from one click or purchase.**

1. **Klaviyo can store declared size, interests and contact frequency.**\
   Customers can update custom profile properties through signup forms, preference pages or email links. Klaviyo specifically supports fields for size, interests, questionnaires and preferred email frequency. [Klaviyo Help Center: Profile properties reference](https://help.klaviyo.com/hc/en-us/articles/115005074627)

   **STA build priority:** create a **Your Shirt Profile** page containing:

   - Favorite teams and teams to avoid
   - Normal tagged size and preferred fit
   - Optional pit-to-pit range
   - Players and eras they hunt
   - Budget and acceptable condition
   - Broad-drop email frequency
   - Preferred Shirt Match contact channel

   After completion, recommend only genuinely available inventory. When nothing qualifies, show Shirt Matching instead of weaker unrelated products.
2. **One-click email answers overwrite prior values.**\
   Klaviyo’s property-update links can record a choice directly from an email, but the newest selection replaces the previous value. For list properties, the entire list is replaced rather than adding another choice. [Klaviyo Help Center: How to update a profile property when someone clicks a link](https://help.klaviyo.com/hc/en-us/articles/115005255248)

   **STA decision:** a one-click question works for a single current size:

   *“What size are you actually looking for right now?”*

   Use the full preference page for multiple favorite teams, players or acceptable eras. Maintain separate fields for:

   - declared\_shirt\_size
   - purchase\_primary\_size
   - inferred\_size\_interest

   Customer-declared information should outrank inferred browsing and purchase history without erasing that history.
3. **Size-first discovery is visible across leading sellers.**\
   Classic Football Shirts publicly places **Shop by Size** prominently in its collections. Cult Kits publicly shows size, condition and authentication reassurance on listings, then offers alternatives and newsletter signup when the viewed shirt is unavailable. These are observable storefront decisions, not evidence of their private segmentation or email performance. [classicfootballshirts.co.uk: Classic Clearance - Save up to 35% off Vintage Kits](https://www.classicfootballshirts.co.uk/classic-sale.html?era=1970s)

   **STA copy direction:**

   **Subject:** *make sta look more like your locker*\
   *Tell us your teams, your fit and the shirts you’re hunting. We’ll show you fewer random pieces—and more shirts that actually belong in your rotation.*

This strengthens Welcome, Browse, Post-Purchase, January Retention and Shirt Matching without adding another flow. Track preference completion, eligible inventory shown, click, purchase, match-to-contact, time-to-sale and broad-message frequency respected. Nothing was changed or sent.

---

## Message 34: Assistant

Turn: `e2a0cf1d-ec49-41de-a1da-3d53e022cc4d`

### STA Email Research — October 28

**“Low stock” automation is a poor default for one-off vintage shirts.**

1. **A shirt listed with quantity one may never trigger a low-inventory flow.**\
   Klaviyo triggers only when inventory crosses from above the chosen threshold to that threshold or below. Further reductions below it do not retrigger. It also cautions against multiple messages because the item may sell quickly. [Klaviyo Help Center: How to create a low inventory flow](https://help.klaviyo.com/hc/en-us/articles/21374913673243)

   **STA decision:** exclude one-off vintage inventory from generic low-stock automation. Use it only for replenishable products that genuinely cross a stock threshold. For unique shirts, let Browse/Availability send one inventory-verified message:

   *“Still thinking about this one? It’s available in your size right now, and there’s one.”*

   Checkout, Shirt Matching, exchange assistance and recent purchase messages should outrank it.
2. **Price-drop alerts offer better intent and margin control.**\
   Klaviyo can qualify customers who viewed or started checkout, rechecks eligibility before sending, and excludes recent purchasers plus out-of-stock or unpublished items. Checkout intent produces the narrower, more purchase-ready audience. [Klaviyo Help Center: How to create a price drop flow](https://help.klaviyo.com/hc/en-us/articles/4404249033755)

   **STA decision:** use price-drop alerts only after an approved merchandising reduction clears STA’s margin floor. Prioritize started-checkout customers, then verified favorites where available; avoid alerting every casual viewer during BFCM.

   **Copy:** *“The shirt you looked at is still available—and the price just changed. Same authentic piece, same condition notes and measurements.”*
3. **Reduced vintage can feel like discovery rather than clearance.**\
   Cult Kits publicly presents its reduced one-offs as “Hidden Classics,” explaining that some were overlooked because of size, club or era while retaining authenticity and condition reassurance. This is observed storefront copy, with no public evidence about its private automation or performance. [Cult Kits: Vintage Price Drop - Hidden Classics and Reduced Vintage Football Shirts](https://www.cultkits.com/collections/vintage-price-drop)

   **STA decision:** frame January reductions around rediscovery:

   *“Some shirts need the right supporter. These authentic pieces are still here—filtered to your teams and fit.”*

   Show only available inventory. If the shirt sells, Klaviyo can skip browse or cart email containing the unpublished item; for a multi-item cart, that safeguard cancels the entire message rather than silently removing one product. [Klaviyo Help Center: How to configure out-of-stock items for automated flows on Shopify](https://help.klaviyo.com/hc/en-us/articles/115005253188) Route remaining interest to Shirt Matching instead of sending stale reminders.

This strengthens **Browse/Availability, Cart Recovery and January Retention** within the existing 10-flow foundation. Measure eligible alerts, unavailable-item skips, click, purchase, contribution margin, match requests and time-to-sale. No live STA configuration was inspected or changed, and nothing was sent.

---

## Message 35: Assistant

Turn: `2485ab59-55bb-4bf3-ac00-fec397e6db02`

### STA Email Research — October 29

**The review request should improve STA’s fit and condition data, not merely collect stars.**

1. **Reviews can confirm both the shirt and the buyer profile.**\
   Klaviyo separates product questions from profile questions. Product questions can capture fit; profile answers such as normal size become customer properties for segmentation. Profile answers overwrite the previous property value. [Klaviyo Help Center: How to create custom review questions](https://help.klaviyo.com/hc/en-us/articles/16319181846171)

   **STA Post-Purchase decision:** ask only three questions:

   - Did the condition match the listing?
   - How did the measured fit land: smaller, accurate or roomier?
   - What size do you normally buy for yourself?

   Store the last answer as review\_confirmed\_size, preserving declared\_shirt\_size and purchase history separately. Suppress this size question for identified gifts so the buyer’s profile does not inherit the recipient’s size.
2. **Online and in-store buyers need different timing.**\
   Klaviyo can time Shopify review requests from delivery and maintain a separate POS delay. Delivery-based timing avoids asking for feedback before an online order arrives; POS orders use fulfillment timing. [Klaviyo Help Center: How to adjust review request timing](https://help.klaviyo.com/hc/en-us/articles/16682549669403)

   **STA decision:** keep one Post-Purchase flow with branches:

   - **Shipped:** request feedback after confirmed delivery and enough wear time.
   - **Rancho store/event purchase:** use the POS branch.
   - **Exchange or support case open:** pause the review request.
   - **Gift purchase:** ask whether the gift landed, without assigning fit preferences to the purchaser.

   **Subject:** *how did the shirt actually land?*
3. **Condition trust depends on accuracy, not a perfect score.**\
   Classic Football Shirts publicly acknowledges that condition grades are subjective and pairs them with detailed defect disclosure. That is observable public policy, not evidence about its private review automation or conversion rate. [Help Centre: Condition Grading](https://classicfootballshirtssupport.zendesk.com/hc/en-gb/articles/360023921572-Condition-Grading)

   **STA copy decision:** ask, *“Did the shirt arrive the way we described it?”* Use verified answers to improve grading and reassurance blocks across Browse, Cart and BFCM emails. Because many STA shirts are one-offs, extract reusable proof about measurement accuracy, condition transparency and service instead of relying only on reviews attached to a sold SKU.

   If STA later offers Kit Cash or a discount for reviews, Klaviyo requires the review to be marked as incentivized and the reward delivered regardless of whether the feedback is positive or negative. [Klaviyo Help Center: How to request reviews from your customers with Klaviyo Reviews flows](https://help.klaviyo.com/hc/en-us/articles/16319809379611) Start without an incentive until the response rate and margin effect are known.

**Measure:** delivered/POS order → review request, submission rate, condition or fit mismatch rate, corrected size profiles, support cases, next eligible recommendation click, purchase and time-to-sale. This strengthens **Post-Purchase, Browse and Shirt Profile** inside the existing 10-flow foundation; it does not require another overlapping reminder flow. No live configuration was inspected or changed, and nothing was sent.

---

## Message 36: Assistant

Turn: `1915cef2-c8ad-4694-a81a-7a0833227964`

### STA Email Research — October 29 evening

**A Klaviyo product block cannot safely promise “your team, your size” by itself.**

1. **Standard personalization is behavioral, with a generic fallback.**\
   Klaviyo recommendations can use browsing, cart and purchase behavior while excluding previously purchased and unavailable items. When customer data is insufficient, the block falls back to the same bestseller or most-viewed logic for everyone. Feed filters cover categories, price and stock; they are not documented as automatically joining each profile’s declared team and size to matching inventory. [Klaviyo Help Center: How to use product feeds and recommendations](https://help.klaviyo.com/hc/en-us/articles/115005082787)

   **STA decision:** label ordinary feeds **“you may like”**, not **“picked in your size.”** If no trustworthy personalized result exists, show Shirt Matching rather than generic bestsellers.
2. **Product-level blocks can hide a size mismatch.**\
   Klaviyo product blocks select products, not individual variants. Its inventory filter may qualify a product from total variant inventory, then display a default image or price belonging to a different variant. [Klaviyo Help Center: How to add a product block to an email](https://help.klaviyo.com/hc/en-us/articles/115000219092)

   **STA decision:** before adding automated recommendations to Welcome, Arcade, Browse or BFCM emails, test whether each STA vintage listing is represented as one purchasable size. For multi-size products, do not claim the recipient’s size is available unless variant-level eligibility has been verified.

   During BFCM, use a globally safe feed containing only eligible, in-stock merchandise above the approved margin floor, with Rare/Grail and one-of-one exclusions. Team-and-size matching remains a separate validation step.
3. **Exact matches need explicit product IDs.**\
   Klaviyo documents a custom route where an external matching process writes recommended catalog-item IDs to the customer profile and the email retrieves those exact items. Missing catalog items can cause the message to skip. [Klaviyo Help Center: Catalog lookup tag reference](https://help.klaviyo.com/hc/en-us/articles/360004785571)

   **STA Shirt Matching build:** after comparing team, player, era, size/fit, budget and condition against live inventory, write only verified matches to shirt\_match\_product\_ids. If the list is empty, send no product reminder; keep the request open for sourcing.

   **Copy:** *“We found one that fits your hunt: the right club, your stated fit range, and within budget. Check the measurements and condition before it goes.”*

Classic Football Shirts publicly displays **“Recommended for you”** alongside **Shop by Size** on its clearance experience. That is observed storefront language, not proof that its private emails perform customer-specific team-and-size matching. [classicfootballshirts.co.uk: Warehouse Clearance](https://www.classicfootballshirts.co.uk/warehouse-clearance.html?printed=Yes)

Measure eligible products generated, verified size matches, fallback frequency, match-to-contact, click, purchase, time-to-sale and unavailable-item skips. No live STA catalog or Klaviyo configuration was inspected or changed, and nothing was sent.

---

## Message 37: Assistant

Turn: `8c5999ea-5a58-400e-9f63-ed24bb062005`

### STA Email Research — October 30 evening

**A one-off Shirt Match needs a controlled handoff, so several supporters do not chase the same shirt.**

1. **Shopify can reserve the exact item for one customer.** A draft-order reservation moves tracked inventory into the Committed state, preventing other customers from purchasing it until a chosen expiration time. [Creating draft orders: Shopify Help Center](https://help.shopify.com/en/manual/fulfillment/managing-orders/create-orders/create-draft)

   **STA decision:** when one shirt satisfies several requests, offer it to the oldest qualified requester first. Reserve it only after confirming team, size/fit, budget, condition and location. Choose the hold period from STA’s operating capacity and eventual conversion data.
2. **The reservation can lead directly to secure checkout.** Shopify draft orders support an invoice or direct checkout link. Product prices are locked by default, while customer-entered discount codes require a separate setting. [Sending invoices for draft orders: Shopify Help Center](https://help.shopify.com/en/manual/fulfillment/managing-orders/create-orders/send-draft)

   **STA copy:**

   **Subject:** *found it — and held it for you*

   *The [season/player] shirt matches your hunt and sits inside your fit and budget. We’ve held this exact piece until [time]. Check the measurements and condition, then claim it below.*

   If no reservation was actually created, say **“available now; not reserved.”** A checkout link may be shared through Instagram only within a permitted conversation; it does not make a saved handle eligible for an automated outbound DM.
3. **Expiration should advance the queue, not start overlapping reminders.** Shopify exposes the reservation deadline in draft-order notifications. Klaviyo can recheck profile filters before every flow action, including whether someone has since purchased. [Notifications variables reference: Shopify Help Center](https://help.shopify.com/en/manual/fulfillment/setup/notifications/email-variables)

   **STA workflow decision:**

   - Set the request to reserved and suppress Browse, Cart, low-stock and general Shirt Match reminders for that item.
   - On purchase, close the request as purchased.
   - On expiration without purchase, return the inventory to availability and contact the next qualified requester.
   - Keep other matching requests open for sourcing.
   - Do not release everyone simultaneously unless enough inventory exists.

Measure match → reservation, reservation → contact, checkout click, purchase, expiration rate, next-requester conversion, time-to-sale, contribution margin and duplicate contacts prevented.

No meaningful new public football-shirt seller evidence appeared for this private handoff mechanic. These are documented Shopify/Klaviyo capabilities and a proposed STA process, not a live audit or performance claim. Nothing was changed or sent.

---

## Message 38: Assistant

Turn: `260b25cf-bd1b-4a21-8c02-981aa5bdd894`

### STA Email Research — October 31

**BFCM needs a message-priority system. Smart Sending alone will not prevent every collision.**

1. **Email and SMS frequency limits operate separately.** Klaviyo’s defaults are 16 hours for email and 24 hours for SMS. An email does not stop a same-day SMS, and messages skipped by Smart Sending are not automatically rescheduled. [Klaviyo Help Center: Understanding Smart Sending in Klaviyo](https://help.klaviyo.com/hc/en-us/articles/115002779311)

   **STA decision:** use this priority order:

   1. Order, fulfillment and exchange information
   2. Reserved Shirt Match
   3. Checkout recovery
   4. Cart or browse recovery
   5. BFCM campaign
   6. General discovery/community

   Pause lower-priority reminders through explicit filters when someone enters a higher-priority journey. Keep Smart Sending enabled as a second safeguard.
2. **Multi-message campaigns can stop after purchase.** Klaviyo’s omnichannel exit criteria can remove someone from all later campaign messages after a qualifying conversion, even when that purchase resulted from another flow or campaign. The exit condition must be configured before the first message sends. [Klaviyo Help Center: Automatically prevent over-messaging with omnichannel campaigns exit criteria](https://help.klaviyo.com/hc/en-us/articles/43671905324187)

   **STA BFCM decision:** use Placed Order as the sequence exit condition. Once someone buys, replace sale reminders with the appropriate confirmation or post-purchase experience.

   **Copy before purchase:** *“Your size is still in the eligible lineup.”*\
   **After purchase:** no further countdown email or SMS.
3. **Holiday reach should expand through engagement tiers, not one full-list blast.** Klaviyo recommends starting major promotions with the most engaged subscribers, expanding cautiously and keeping the final inactive group outside promotional sends. Apple privacy opens should not be treated as reliable engagement by themselves. [Klaviyo Help Center: Creating a sending schedule based on email engagement reference](https://help.klaviyo.com/hc/en-us/articles/360037527052)

   **STA audience order:**

   - Recent purchasers and clickers with eligible favorite-team or size inventory
   - Recently engaged subscribers with available eligible inventory
   - Broader engaged audience using honest discovery copy
   - Inactive profiles remain in re-engagement or sunset treatment

   Rare/Grail and one-of-one pieces remain excluded unless their economics are separately approved. Never say *“in your size”* unless variant availability has been verified.

Measure unique people contacted across channels, Smart Sending skips, purchase-exit removals, messages received per customer, clicks, purchases, margin and post-purchase sale reminders prevented.

No meaningful new public football-shirt seller evidence appeared for this private orchestration issue. These are documented Klaviyo controls and proposed STA decisions, not evidence of another seller’s private automation or STA’s live setup. Nothing was changed or sent.

---

## Message 39: Assistant

Turn: `5664c511-f316-4a05-a274-ddd3e57bbecc`

### STA Email Research — October 31 evening

**The Rancho store and community events should create useful shirt profiles, without turning every receipt or RSVP into a marketing subscriber.**

1. **Shopify POS can request customer information without blocking checkout.** POS Pro supports “Recommended” customer capture, letting staff skip it when someone declines. “Required” capture can prevent checkout and reduce sales. [help.shopify.com: Shopify Help Center | Managing required checkout information for your Shopify POS](https://help.shopify.com/en/manual/sell-in-person/getting-started/shopify-pos-from-admin/required-checkout-information)

   **STA decision:** use voluntary capture at the store, Weekly FC, Cascarritas and pop-ups:

   *“Want us to remember your club and fit for the next drop?”*

   Collect only email or phone for verified linkage, favorite team, usual size/fit and capture source. Use Shirt Matching for specific player, era, budget and condition requests.
2. **A digital receipt and marketing permission are separate choices.** Shopify can create a customer profile from an emailed or texted receipt, but it presents email and SMS marketing choices separately. POS profiles also maintain distinct email and SMS marketing settings. [help.shopify.com: Shopify Help Center | Editing a customer profile on Shopify POS](https://help.shopify.com/en/manual/sell-in-person/shopify-pos/customer-management/edit-a-customer-profile?locale=en%23%2Flogin)

   **STA decision:** staff should never describe receipt delivery as joining STA’s marketing list.

   - **Receipt:** *“Where should we send your receipt?”*
   - **Marketing:** *“Want first look at shirts from your clubs and events at the shop?”*
   - **Shirt Matching:** *“Should we contact you when we find this specific hunt?”*

   Record each permission independently. An FC RSVP, Instagram follow or saved phone number does not answer the other questions.
3. **Anonymous POS orders cannot support Klaviyo personalization.** Klaviyo requires a POS order to contain a customer record plus a valid email or phone number before it can sync. Synced orders include Source Name = pos, allowing POS and web purchases to be distinguished. [Klaviyo Help Center: How to differentiate Shopify POS and Shopify web data](https://help.klaviyo.com/hc/en-us/articles/115005253248)

   **STA flow decision:** branch Post-Purchase and Retention by verified order source:

   - **POS purchase:** skip shipping copy; ask whether the condition and measured fit landed correctly.
   - **Event purchase:** retain the event source for local follow-up and attribution.
   - **POS customer later buying online:** treat this as one customer journey when linked by verified email or phone.
   - **Name-only profile:** do not guess the Klaviyo or Instagram identity.

Measure POS orders with a verified customer, voluntary marketing opt-in, team-and-size completion, POS-to-online repeat purchase, Shirt Match requests, match-to-contact, click, purchase and time-to-sale.

No meaningful new public football-shirt seller evidence appeared for this private identity-capture process. These are documented Shopify/Klaviyo capabilities and proposed STA decisions, not a live configuration audit. Nothing was changed or sent.

---

## Message 40: Assistant

Turn: `615fa44b-9439-4dd6-b1b5-01b976ca6bb8`

### STA Email Research — November 1

**STA should have one recovery ladder. Shopify, Klaviyo, Browse, Cart and Checkout must not chase the same customer.**

1. **Shopify and Klaviyo can both send abandoned-checkout emails.** Klaviyo explicitly recommends disabling Shopify’s recovery automation immediately before enabling its replacement flow to avoid either duplicate messages or a coverage gap. [Klaviyo Help Center: How to disable notification emails sent by Shopify](https://help.klaviyo.com/hc/en-us/articles/4403589811611)

   **STA decision:** assign one system as the owner of checkout recovery. Do not activate a Klaviyo replacement until its trigger, purchase suppression, links and inventory behavior have been tested. This is a proposed control; STA’s live Shopify and Klaviyo settings were not audited.
2. **Purchase intent should determine which recovery flow survives.** Klaviyo distinguishes Viewed Product, Added to Cart and Checkout Started. Its recommended filter removes someone from Cart recovery once they start checkout, while Placed Order zero times since starting this flow stops Checkout messages after purchase. [Klaviyo Help Center: How to create an abandoned cart flow](https://help.klaviyo.com/hc/en-us/articles/115002779411)

   **STA hierarchy:**

   - Checkout recovery replaces Cart and Browse.
   - Cart recovery replaces Browse.
   - Reserved Shirt Matching outranks all three.
   - Purchase, exchange assistance or an unavailable shirt stops recovery.

   **Checkout copy:** *“Your checkout is still there. The shirt isn’t reserved, so check the measurements and condition before it changes hands.”*

   Do not introduce a fresh discount automatically; preserve margin and the original BFCM eligibility.
3. **Checkout recovery only begins after identifiable contact information exists.** Klaviyo records Checkout Started after Shopify supplies a valid email or phone number, and the event can contain variant details, cart value, discounts and a recovery URL. Shopify cannot email a phone-only checkout and suppresses recovery in cases including unavailable inventory or unsupported shipping. [Klaviyo Help Center: Shopify data reference](https://help.klaviyo.com/hc/en-us/articles/115005080447)

   **STA decision:** use email only when email recovery is eligible; use SMS only with valid SMS consent. A phone number, Instagram handle or prior event RSVP does not authorize marketing outreach. If contact is unavailable, improve onsite checkout recovery rather than guessing another identity or channel.

Measure Browse → Cart → Checkout → Purchase, cross-flow skips, duplicate messages, unavailable-item suppression, checkout recovery rate, contribution margin and time-to-sale.

No meaningful new public football-shirt seller evidence appeared for this private recovery architecture. These are official Shopify/Klaviyo capabilities and proposed STA decisions, not verified private automations or performance claims. Nothing was changed or sent.

---

## Message 41: Assistant

Turn: `9f52ae53-eb3e-40ed-8481-7c8d39536819`

### STA Email Research — November 1 evening

**A zero-result search should become a Shirt Match request, not a dead session or generic email signup.**

1. **Shopify reports searches with no results and searches with results that receive no clicks.** It also reports search click, add-to-cart and purchase rates. Predictive-search interactions are excluded from some Search & Discovery reports, and reporting can lag. [help.shopify.com: Shopify Help Center | Shopify Search & Discovery reports and analytics](https://help.shopify.com/en/manual/online-store/storefront-search/search-and-discovery-analytics)

   **STA decision:** review unmet searches by team, player, season, shirt type and size. Keep aggregate search demand separate from identifiable customer data unless the shopper voluntarily submits a request.
2. **Search merchandising should only surface real, available inventory.** Shopify product boosts apply to available products; sold-out products move toward the end of results. Synonyms are intended for true substitutes and Shopify cautions against grouping loosely related terms. [help.shopify.com: Shopify Help Center | Modifying search with Shopify Search & Discovery](https://help.shopify.com/manual/online-store/search-and-discovery/product-boosts)

   **STA decision:** use synonyms for genuine language variants such as *Barça / Barcelona* or *keeper / goalkeeper*. Do not treat different clubs, eras or player versions as interchangeable. When no accurate item exists, route to Shirt Matching instead of boosting a weak substitute.
3. **The no-result page can capture structured sourcing demand.** Klaviyo can accept a custom event through its Events API, but a customer-facing Shirt Match form remains the useful action: prefill the search phrase, then ask for team, exact shirt, player, era, size/fit, budget and acceptable condition. [Klaviyo Help Center: Getting started with metrics](https://help.klaviyo.com/hc/en-us/articles/115005076787)

   **STA copy:**

   *“Nothing matched that hunt today. Tell us the size, era and condition you’ll accept. If one is already at STA, we’ll show you. If not, your request becomes sourcing demand.”*

   Ask where they want match updates. Email requires the appropriate permission; an optional Instagram handle should be linked through customer-provided email or another verified path. A handle alone still does not authorize future automated DMs.

Measure search → result, click, cart and purchase; no-result search → Shirt Match request; request → eligible contact, click, purchase and time-to-sale. Aggregate unmet requests by team, player, era and size so sourcing follows demonstrated demand.

No meaningful new public football-shirt seller evidence appeared for this private search-to-sourcing process. These are official Shopify/Klaviyo capabilities and proposed STA decisions, not live STA search or flow audit results. Nothing was changed or sent.

---

## Message 42: Assistant

Turn: `908e9b84-a413-4ca3-a010-b9c70ca27bcf`

### STA Email Research — November 2

**An open exchange should pause normal retention and become a fit-resolution journey.**

1. **An exchange item is not reserved when the return is first created.** Shopify reserves its inventory only when the return is processed. For a one-off vintage shirt, the proposed replacement could sell during that gap. [Creating and processing returns and exchanges: Shopify Help Center](https://help.shopify.com/en/manual/orders/refunds-returns/exchanges)

   **STA decision:** never email *“your replacement is secured”* until inventory is actually reserved or processed. If no exact replacement exists, move the customer into Shirt Matching with the original team, era, measurements and condition issue prefilled.
2. **Return reasons can improve future fit recommendations.** Shopify records apparel-specific reasons such as “Too big” and “Too small” and supports reporting by reason. A refund issued without creating a return does not preserve this structured reason. [Creating and processing returns and exchanges: Shopify Help Center](https://help.shopify.com/en/manual/orders/refunds-returns/exchanges)

   **STA decision:** capture:

   - Original tagged size and measurements
   - Too small, too large, condition mismatch or preference change
   - Desired tagged size and pit-to-pit range
   - Exact replacement versus broader team/era search

   Treat this as resolution data. Do not silently overwrite the customer’s declared size from one exchange.
3. **Do not assume a return request automatically stops Klaviyo marketing.** Klaviyo documents Shopify metrics for Refunded Order and Cancelled Order, while flow eligibility depends on the metrics and filters actually available in the account. [Klaviyo Help Center: How to create a metric-triggered flow](https://help.klaviyo.com/hc/en-us/articles/360003057151)

   **STA flow decision:** use a verified resolution\_open status or custom event to pause review requests, win-back, Browse, Cart and BFCM reminders. Resume retention only after the exchange, credit or Shirt Match path is resolved.

   **Copy:**\
   **Subject:** *let’s get the fit right*\
   *Your exchange is open. We’ll sort the measurements first. If the same shirt isn’t available, tell us how wide you want the search—same club, same era or a completely different piece.*

Track exchange reason, resolution time, replacement availability, store-credit issuance and redemption, Shirt Match completion, repeat purchase, time-to-sale and contribution margin. Shopify notes that Shopify Payments card fees are not returned after a refund, so additional discounting during resolution should be deliberate. [Refunding orders: Shopify Help Center](https://help.shopify.com/en/manual/fulfillment/managing-orders/refunding-orders)

No meaningful new public football-shirt seller evidence appeared for this private resolution workflow. These are official Shopify/Klaviyo capabilities and proposed STA controls, not a live account audit. Nothing was changed or sent.

---

## Message 43: User

Turn: `0e8efd13-882a-4fdd-8ac3-5c8dc396c772`

i want you to reread this whole chat, and thorougly make document everything you have found in the wiki. Everything that is reperateble and automated should be a skill. whatever you have found about the status of emailing in our niche for STA needs to be throogly deocument iin the llm wiki

---

