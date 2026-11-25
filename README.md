# ｜International Budget Travel Guide

An AI agent skill for planning affordable international trips and making practical decisions on the road. Compare the full cost of flying from different hubs, build a day-by-day itinerary, or check which airport transfers are still running after a late arrival. The skill replies in the language you use and works with a web-enabled agent to look up current travel information.

## What it covers

| Area | What the skill checks |
| --- | --- |
| Flights | Fares across departure hubs, including the trains, buses, transfers, or overnight stays needed to reach them |
| Bags | The strictest baggage allowance on your route and laundry options for one-bag travel |
| Stays | Hostels, hospitality exchanges, home swaps, and house- or pet-sitting options |
| Airport arrivals | Apps to set up before departure, low-cost airport transfers, last departures, and overnight options |
| Payments | Currency conversion, ATM and card fees, and how much local cash to carry |
| Multi-city routes | Travel times, transfer buffers, and the cost of each leg before stops go into the itinerary |
| Attractions | Free and paid sights in price order, plus seasonal events and markets |
| Activities | Operator and reseller prices, cancellation terms, and group-rate options |
| Food | Low-cost meals and convenience stores with opening hours |
| Shopping | Seasonal gear needs, outlet and mall sales, and tax-refund considerations |
| Local rules | Public facilities, common fines, and customs declaration requirements |

For a full trip, the plan opens with daily and total budget ranges, showing ground costs separately from international flights and transport to the departure hub. Major expenses appear before the itinerary. Comparison tables and an editable Markdown checklist make it easy to adjust the plan as prices or schedules change.

## Use the skill

Place [SKILL.md](SKILL.md) in a folder named `international-budget-travel` in your agent’s skills directory and invoke it by name. Use an agent with web access for current prices, opening hours, and schedules. For more relevant comparisons, include your departure city, destination, dates, budget and currency, and baggage constraints. For help on arrival, include the airport, arrival time, and where you need to go.

## Example prompts

- “I’m planning a five-day budget trip to Osaka and Kyoto with one backpack. Compare hostels with laundry and give me a budget breakdown and a day-by-day route.”
- “My flight lands at 12:30 a.m. What’s the cheapest way from the airport to my hostel tonight, and how much local cash should I withdraw?”
