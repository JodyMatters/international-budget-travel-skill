---
name: international-budget-travel
description: Nationality-agnostic overseas budget travel skill for anyone traveling outside their home country. Covers both pre-trip full planning and on-the-ground instant rescue, using live web search to build structured tables, multi-hub flight & positioning cost comparisons, hostel/hospitality/home-exchange listings, LCC baggage & one-bag laundry rules, pre-trip app setup, cheapest airport transit & red-eye overnight options, FX/dynamic cash strategy, price-ascending attractions & seasonal events/markets, activity comparison & forum group-joining, budget food & convenience store hours, mall/outlet sales & customs/local penalty rules, and an editable Markdown plan.
---

# International Budget Travel (`international-budget-travel`)

A nationality-agnostic overseas budget travel skill designed for **anyone traveling outside their home country**. It supports both **pre-trip full planning** and **on-the-ground instant rescue**, always matching the user's input language while keeping internal instructions clear and consistent.

## Core Execution Rules (Mandatory)

1. **Language Matching:** Always respond in the **same language** the user uses (e.g., Simplified Chinese, Traditional Chinese, English, Japanese, Korean, etc.). Keep official URLs, exact place/station names, and official brand/platform names accurate.
2. **Live Web Search on Trigger:** Whenever invoked for a trip or on-the-ground query, perform live web searches for current exchange rates, flight/transit options, hostels and official websites, hospitality/home-exchange/house-sitting opportunities, attraction ticket prices and opening hours, local food spots and operating hours (including whether convenience stores are 24/7 or have limited hours), mall/outlet sales/promotions, and airport overnight/late-night transit options.
3. **Tables for Multi-Row Data:** Present multi-row comparisons and lists (flights/hubs, hostels, hospitality/home-exchange/house-sitting options, red-eye airport options, high-cost items, daily itinerary, attractions/events/markets, activities/platforms, budget food/convenience stores, mall/outlet sales, and local/customs rules) in clean Markdown tables.
4. **Budget Ranges First:** Always state a **daily budget range** and an **overall trip budget range** (distinguishing ground costs from international flights/positioning costs, with `[TBD]` / `[Your Budget]` placeholders where user inputs are missing).
5. **High-Cost Items Before Daily Itinerary:** List expensive items (international flights & positioning transport, accommodation, major paid tickets/passes/tours) **above** the day-by-day itinerary.
6. **Complete, Actionable Daily Itinerary:** Provide a concrete day-by-day schedule (morning/afternoon/evening blocks, transit lines/walking flow, meals with operating hours, and daily budget guidance) that calculates **intercity/multi-leg transit time first** before locking stops.
7. **Editable Markdown Output:** Include a structured, modular Markdown template with placeholders (e.g., `[TBD]`, `[Your Budget]`) and checkboxes (`- [ ]`) so the user can easily copy, edit, and maintain their own plan.

---

## The 11 Overseas Budget Travel Modules

### Module 1: Multi-Hub International Flights & Pre-Departure Positioning Cost
- Compare the cheapest international flight options (direct or connecting) not only from the user's home city, but also across major domestic international hubs (for example, comparing Kunming vs. Beijing, Shanghai, and Chengdu when flying to Austria).
- Calculate positioning transit costs (high-speed rail, domestic flights, buses, extra overnight stays, or airport transfers) from the user's home location to each alternative hub:
  $$\text{Total Departure Cost} = \text{Positioning Transit} + \text{International Airfare} + \text{Buffer Costs}$$
- Show both raw fare differences and net savings after positioning costs.

### Module 2: Local LCC Baggage Rules & One-Bag / Laundry Linkage
- Match luggage dimensions and weight limits to the **strictest low-cost carrier (LCC) segment** in the itinerary (including regional/domestic budget airlines) to avoid costly gate fees.
- When traveling light (such as solo travel with a single hiking backpack), prioritize accommodations with **laundry facilities (`Laundry` / washer & dryer)** and check whether they are free self-service, coin-operated, or paid per load/item.

### Module 3: Accommodation Channels, Top Hostels & Hospitality/Exchange Listings
- **Top 3–5 Hostels:** List 3–5 high-value/well-reviewed hostels for the destination with room types, price ranges, laundry/kitchen/location notes, and **official websites**.
- **Other Relevant Official Websites:** Include official websites for relevant transit operators, attractions, shopping malls/outlets, or tourism/booking platforms.
- **Hospitality, Home Exchange & House/Pet Sitting (3–5 Filtered Options):** Surface 3–5 relevant opportunities/listings or active destination searches across platforms such as Couchsurfing, Couchers.org, BeWelcome, Trustroots, TrustedHouseSitters, Nomador, HomeExchange, and People Like Us, noting cost/exchange rules and safety precautions.
- **Split Stays / Room-Sharing:** Note forum/community room-sharing (e.g., Reddit, travel forums) with reminders to verify account history, start with short trial stays, and clarify deposits and cancellation liability.

### Module 4: Pre-Trip App Setup, Cheapest Airport Transit & Red-Eye Overnight Strategy
- Advise downloading, registering, logging in, and binding payment methods for local ride-hailing, transit, map, and translation apps **before departure** in case of poor connectivity or login blocks after arrival.
- Match the arrival airport with the **cheapest ground transit** (regular metro/subway, public bus, or budget shuttle) rather than expensive express trains or taxis.
- **Red-Eye / Late-Night Arrivals & Departures:** Detail whether to stay at the airport (rest zones, sleep/capsule pods, 24-hour areas) or head into the city, including late-night buses/shuttles, last-train cutoffs, and safety/cost trade-offs.

### Module 5: Payment Apps, FX Optimization & Dynamic Cash Advice
- Recommend downloading and linking cards to local or cross-border payment apps ahead of time when they offer better exchange rates or lower fees than standard bank cards.
- Enforce paying in **Local Currency** on POS terminals and ATMs (avoid Dynamic Currency Conversion / DCC) and carrying backup cards from different networks.
- Calculate **whether cash is needed** and **how much cash to carry** based on the **current date/exchange rate at query time**, **destination region/cash habits or card surcharges**, and **trip length**, recommending a rolling cash buffer rather than carrying all cash at once.

### Module 6: Complex Multi-Leg Transit & Transit-Time-First Scheduling
- Break down complex intercity or multi-mode transfers (e.g., train + ferry + local bus/transit in a single day) with cost-saving alternatives and transfer buffers.
- Account for transfer and travel time **before** finalizing A → B → C stops so travelers are not rushed into expensive last-minute taxis or missed connections.

### Module 7: Attractions (Price Low-to-High), Seasonal Events & Local Markets
- Recommend top must-see attractions ranked **from lowest ticket price to highest (Free → Low-Cost → Paid)** with ticket prices, free-entry perks, and booking notes.
- Match the user's travel dates with high-value seasonal/cultural events (such as summer festivals or fireworks) and local markets offering authentic, budget-friendly food and goods.

### Module 8: Activity Price Comparison, Local Forums & Group-Joining Hacks
- Compare **official operator websites** vs. **experience/reseller platforms** (e.g., Airbnb Experiences, GetYourGuide, Viator, Klook) for the destination, checking inclusions and cancellation terms.
- Include local forums/review platforms (e.g., Reddit subreddits, Google Maps, Tripadvisor, Yelp) and note how to find group-rate partners on forums/communities for headcount-discounted activities while confirming cost-splitting and refund rules.

### Module 9: Budget Food, Operating Hours & Convenience Store Cuisine
- Filter food recommendations within a **budget-per-meal cap** using reviews, price range, and location/route convenience.
- Include high-value food tours/experiences (such as afternoon food walks that combine tasting, walking, and time filler) and **local convenience store food** (especially in convenience-store-heavy destinations).
- Always list **operating hours** for recommended eateries, markets, and convenience stores, explicitly noting **non-24-hour stores**, cutoffs, and closed/holiday days.

### Module 10: High-Spend Traps, Reverse-Season Gear & Mall/Outlet Sales
- Warn against emergency high-markup purchases on site (e.g., buying overpriced gear at piers/resorts) and flag **reverse-season/climate mismatches** (such as needing winter layers in the Southern Hemisphere during Northern Hemisphere summer).
- Search and list **local shopping malls, department stores, and outlets** with active/upcoming **sales, discounts, or seasonal clearance** around the travel dates, alongside tax/refund and customs allowance reminders.

### Module 11: Local Rules, Public Facilities, Fines & Customs Red Lines
- Automatically surface destination-specific rules and facility differences—such as public restroom availability, strict trash/littering rules and scarce street bins, smoking zones vs. fines—and **customs/quarantine declaration red lines** (especially meat, eggs, dairy, fresh produce, plants, and restricted goods) to prevent heavy fines or confiscation.
