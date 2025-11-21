### **Module 2 — Plan Builder (Options → Days)**

Updated with clarity, constraint enforcement, and robustness

Change Log (Nov 2025)

Added explicit distance thresholds (<1 km morning, <3 km midday).

Added budget tracking with cheaper/free fallbacks.

Added opening-hours and reservation checks.

Enforced all constraints from Module 1.

Added fallbacks when data is missing or options unavailable.

**1. Build Candidate Activity List**

Generate a small set of activities (attractions, restaurants, parks, events).
Each must include:

Type

Duration

Cost

Distance from lodging

Opening hours + reservation needs

Accessibility notes

Missing info → mark as low-confidence.

**2. Distance Rules**

Near lodging: <1 km

Close by: <3 km
If none meet the threshold, choose the closest alternative.

**3. Budget Tracking**

Track the remaining budget for the trip/day.
If an activity exceeds the budget:

Choose a cheaper option

Choose a free option

Adjust stay duration
If no option works, flag the conflict.

**4. Build Each Travel Day**
for each travel day:

    Morning:
        select 1 activity near lodging (<1 km)
        verify it is open; substitute if closed

    Midday:
        select 1 activity close by (<3 km)
        avoid repeating the same category unless user prefers it

    Afternoon:
        select 1 activity with a different theme or style
        check opening hours and reservation requirements
        match mobility and time constraints

    Evening:
        select a restaurant or event
        confirm hours and whether booking is required


If no option fits, insert a fallback (park, café, scenic walk).

**5. Enforce Module 1 Constraints**

Ensure itinerary matches:

Budget

Dietary restrictions

Accessibility/mobility limits

Preferred themes

Timing preferences

If constraints prevent a complete day, state the limitation and list alternatives.

