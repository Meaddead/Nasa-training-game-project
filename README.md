# Sol Keepers

A browser game for kids ages 7–12 about running a Mars outpost for 30 sols. Built for the NASA hackathon challenge on teaching deep-space survival trade-offs through play.

## Play

Open `index.html` in any modern browser. There is nothing to install and no account. The whole game is that one file.

## How it works

You place solar panels, batteries, an oxygen maker, a greenhouse, a storm shelter, a science lab and a comms dish, then decide how to share limited power between air, food, safety and science. No choice is free:

- The storm shelter blocks radiation but drains power and stops science.
- Bonus science costs oxygen, power or food.
- A comms dish uses power but brings storm warnings from Earth earlier.

Running out of oxygen or food, or passing the radiation limit, ends the mission with a safe evacuation and a hint for next time.

## Real NASA data

| In the game | Source |
|---|---|
| Solar particle storms on sols 9, 10, 11 and 13 | NASA DONKI: 14 SEP detections on May 9, 10, 11 and 13, 2024. Each sol replays one real day. |
| Radio blackout on sol 14 | DONKI flare `2024-05-14T16:46:00-FLR-001`, class X8.7 |
| Storm on sol 20 | NASA JPL: on May 20, 2024 Curiosity measured 8,100 micrograys at Mars, equal to 30 chest X-rays |
| Background radiation, 0.67 mSv per day | Curiosity RAD instrument, published by the Southwest Research Institute (the instrument's lead institution) |
| Comms delay, 4 to 24 minutes | NASA Goddard, space communications |
| Oxygen maker | MOXIE on Perseverance, up to 12 grams of oxygen an hour (NASA JPL) |
| Dust storms cutting solar power | The 2018 storm that ended Opportunity's mission (NASA JPL) |
| Radiation and living things | NASA Open Science Data Repository studies OSD-73, OSD-97 and OSD-115 |
| Bone loss in space | NASA human research: spaceflight bone changes |

The storm data is an archived copy inside the game and is labelled as archived, not live. The game also has a "last 30 days" option that requests live DONKI data and falls back to the archive if the request fails; this live path has not been confirmed working.

`data/nasa_data.json` holds the collected dataset with a source URL for each value and notes on anything that could not be verified.

### Game rules that are not NASA numbers

- Storm size (small, medium, huge) is set by how many DONKI detections were logged that day; doses of 2, 4 and 8 mSv are simplified.
- The 40 mSv mission limit is a game limit.
- Power, oxygen, food and parts numbers are simplified, and a game sol has 24 hours.
- A dish gives 8 hours of storm warning instead of 1; the real delay is minutes.
- Dust storm and bonus science timing is random each game.

Sol Keepers is a student project and is not made or endorsed by NASA.
