# Reflections — TD5 Dashboard design: three roles, three KPIs, one network

## 1. Which stakeholder will disagree most? (before building)
My prediction: the **operations/cost manager** will disagree most with the
other two. The sustainability manager wants shorter routes (less CO2) and the
strategy manager wants better coverage, so both should like opening a new
warehouse, while the cost manager will see a new warehouse as an extra fixed
cost and push to change nothing, or even close the idle one.

## 2. Which assumption I would least like to defend to a client
The **cost figures** (0.12 EUR/tonne-km, 40 EUR/tonne/year). The CO2 factor
(0.10 kg CO2e/tonne-km) sits inside a real, cited, government-published range
(0.047 to about 0.12 according to the French Ministry of Ecology and ADEME),
so I can show where it comes from. The cost figures have no source and no
range at all: if a client asks "where does 0.12 come from?", the only honest
answer is "it is a placeholder". The population-as-demand proxy is a close
second, because it feeds all three dashboards, but at least it is clearly
labelled as a proxy and is directionally reasonable.

## 3. Two KPIs pointing to different actions for the same warehouse
**Lille.** In the CO2 and cost views Lille looks useless: 0 kg CO2 and 0 EUR
of transport, because no other city is closer to Lille than to Paris or Lyon
(Lille only "delivers" to itself; it costs only 466,196 EUR of storage). A
cost-only reading says "close it". The network KPI says the opposite: closing
Lille raises the population-weighted average distance from **168.04 km to
174.43 km**, because Lille's own 233,098 residents would then be served from
Paris. Same warehouse, opposite recommendation, depending on which KPI you
look at.

## 4. Would I recommend the #1 CO2 route as-is?
No, not without checking. The #1 route is **Marseille <- Lyon** (277.6 km,
about 1.21 million kg CO2/year, far above the second one, Toulouse <- Lyon).
Three things make me double-check it:
- It is so large because Marseille is the biggest city served from outside
  (873,076 residents, so about 43,650 tonnes/year with the proxy): the
  problem is not a badly organised route but a big market with no local
  warehouse. Consolidation will not fix that; opening Marseille would.
- 277.6 km is a straight-line distance; the real road distance is longer,
  so the true CO2 is probably underestimated.
- The Lyon–Marseille corridor (Rhône valley) has good rail infrastructure, so
  a rail shift is a realistic option here, unlike for a route with no rail
  link.
So I would present it as "the top priority, but the right action is probably
rail or a new warehouse, not consolidation".

## 5. Which lever to pull first for the highest-cost warehouse
The highest-cost warehouse is **Lyon: 13,476,013 EUR/year** (transport
5,687,061 + storage 7,788,952, i.e. 69.21 EUR/tonne). Storage is the larger
part, but I would pull the **transport** lever first. In this model storage
costs 40 EUR/tonne everywhere, so it only grows with the tonnes handled and
cannot be "fixed" per warehouse. Transport is where Lyon is abnormal: about
29 EUR/tonne at Lyon (5,687,061 EUR / about 194,700 tonnes) versus about
11 EUR/tonne at Paris (1,796,513 EUR / about 164,700 tonnes). The number that
convinced me is the 5.69 M EUR of transport, driven by long routes like
Marseille (1,454,195 EUR) and Toulouse.

## 6. My recommendation for the network
I would **open Marseille and keep Lille**. Opening Marseille cuts the
population-weighted average distance from 168.04 km to **115.03 km (-31.5%)**,
much better than Bordeaux (139.89 km). Closing Lille makes things worse
(174.43 km). One weakness: with Marseille, the worst-served city is still at
435.8 km (Bordeaux, from Lyon), while the Bordeaux scenario lowers the worst
case to 382.3 km, so Bordeaux would be the better choice if the goal were
"no city too far" rather than "best on average".
The caveat (no capex, no lease-exit cost, no cross-border value for Lille)
does not change my choice: I would make the same call and list a capex study
for Marseille as the next step, because a 31.5% reduction is large enough to
probably survive the cost of a new site.
Back to Reflection 1: I was **partly wrong**. I expected the cost manager to
oppose a new warehouse, but in this model storage is charged per tonne, not
per site, so a new warehouse adds no storage cost and actually cuts transport
cost: all three views point towards Marseille. The real disagreement is
about **Lille**: cost and CO2 views make it look idle, while the network view
says keep it.

## 7. My fourth chart (Step 15)
I extended the **CO2 dashboard** with a bar chart of **kg CO2 per tonne
delivered, per warehouse**, with the network average (16.8 kg/tonne) as a
dashed line and bars above average in red. The page's own decision statement
asks "which warehouse is the least CO2-efficient per tonne delivered", but
neither existing chart answers it: the ranking shows routes, not warehouses,
and the map shows totals, which mix "far" with "big". The new chart shows
that Lyon (about 24.3 kg/tonne) is well above average while Paris (about
9.1) is well below. I chose a bar chart because these are rates to compare
side by side, not parts of a whole, so a pie chart would be meaningless; the
average line turns "is this good or bad?" into a one-glance answer.
