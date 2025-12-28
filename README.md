# Airline-Sentiment-Revenue-Decline-Analysis
## Executive Summary:
SkyWings Airlines faced a sharp revenue decline (Business −26%, Economy −18% YoY) alongside rising negative reviews. Using KNIME text mining and Tableau KPI dashboards, my team and identified the biggest pain points: cancellations at 15% vs 2% industry benchmark, and complaints concentrated in poor customer service (35.08%) and low quality perception (34.6%). Hence, we recommended the airline to:

1. Reduce cancellations and strengthen service recovery with a 3-stage “Service Netting” plan (prevent, respond, recover).
2. Win back returning Economy customers (core revenue segment) via loyalty perks + targeted recovery offers.
3. Redesign promotions (only 16.91% promo usage) to be more visible and targeted.

## Business Problem:
For an airline, bookings and reputation are closely tied to revenue. Despite having gained initial popularity for its competitive pricing, SkyWings is seeing booking decline and rising negative reviews. Given that the company has relevant data, it needs an analytical workflow to guide operational improvements for revenue growth. What is causing the decline in business performance and what changes should be prioritised to reverse it?

## Methodology:

1. KNIME text cleaning & document prep to convert Cust_Reviews into analysable text (Excel/CSV import → Strings to Document → de-dup → remove punctuation/numbers/stop words → lowercase + stemming).
2. KNIME sentiment + keyword extraction using MPQA lexicons (Dictionary Tagger → Bag of Words + Term Frequency → convert tags/terms to strings → filter missing → group/sum term frequencies → split positive vs negative → Tag Cloud) and export the cleaned sentiment-keyword output to Excel.
3. Tableau dashboard + story combining Fact_Trans, Cust_Reviews, and the KNIME export to visualise (a) positive/negative word clouds + (b) transaction KPI charts, add interactivity, and translate insights into retention + service-recovery recommendations.

## Skills:
**KNIME**: Lexicon-based sentiment text mining (pre-processing, MPQA enrichment, bag-of-words + term frequency keyword extraction)

**Tableau**: Multi-source data setup, calculated fields, interactive dashboards + story (KPI trends, segmentation, filters/tooltips)

**Analytics**: Customer sentiment analysis, KPI diagnostics + benchmarking, insight-to-recommendation storytelling

## Results & Business Recommendation:
Building a single view (2 dashboards) that connects transaction KPIs (bookings, revenue, disruptions) with voice-of-customer (reviews, complaint themes) clarifies why SkyWings is underperforming and where to intervene first.

### Key results & implications:
- Revenue fell >19% YoY (2024 vs 2023) because bookings fell, especially among repeat flyers.
  - **Implication**: The priority is retention/ win-back, not just acquisition.
- While Business class revenue fell more than Economy (25% vs 18% YoY), the biggest volume decline is in returning Economy bookings, and returning Economy customers generate more total revenue than new Economy through frequent repeat trips.
  - **Implication**: Returning Economy customers is the highest-ROI segment to fix.
- Cancelled flight rates are significantly higher than industry norms (15% vs 2% in 2024). 
  - **Implication**: Cancellations are the main operational "trust breaker" driving lost bookings and negative sentiment.
- Sentiment is net-negative (37% negative vs 30% positive). Top complaint themese are poor customer service (35.08%) and low qualty perception (34.6%).
  - **Implication**: Given that customers are more upset about "intangibles", not product features, improving service quality + perceived value is critical to rebuild loyatly.
- Only 16.91% of bookings used promo codes.
  - **Implication**: Promos likely lack visibility/ targeting and aren't currently helping retention.

### Business recommendations (prioritised)
Because the biggest risks sit in reliability + service recovery + returning Economy retention, I recommend:
1. **Reduce cancellations and strengthen disruption handling (“service netting”)**
   - Prevent avoidable disruptions, communicate early, and offer immediate rebooking/compensation to stop trust erosion.
2. **Win back returning Economy customers (highest-value repeat segment)**
   - Launch loyalty perks (e.g., priority boarding/seat selection) and proactively target lapsed returning customers with recovery offers/service guarantees.
3. **Redesign promotions to be targeted “win-back” campaigns (not generic discounts)**
   - Shift to personalised, time-triggered offers (birthday/anniversary/welcome-back) and test referral-style incentives to drive repeat bookings.
  
## Next Steps (to address limitations of this project):
1. **Strengthen the data so insights can be tied to action.**
   - Augment the provided 2023–2024 extracts with operational CX metrics (support response time/FCR, refund turnaround, rebooking success) and additional VoC sources (tickets/chats/surveys), and where possible link feedback to flight outcomes + segments to quantify impact on repeat bookings and revenue.
2. **Move from theme counts to theme severity + drivers.**
   - Weight themes by rating/strong negative language to identify “high-severity” issues, and split themes by disruption type (cancellation vs delay) to pinpoint the most damaging journey moments.
3. **Quantify ROI and run controlled tests on the fixes.**
   - Pilot the service netting recovery plan and targeted win-back promos (with A/B-tested urgency formats), tracking lift in repeat bookings, cancellation-related complaints, and promo redemption.
4. **Operationalize a “VoC → KPI” monitoring loop.**
   - Turn this into a recurring dashboard that flags spikes in cancellations/negative themes early, so leaders can intervene before booking decline worsens.
