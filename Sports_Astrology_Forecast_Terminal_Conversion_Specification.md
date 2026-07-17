# Sports Astrology Forecast Terminal Conversion Specification

## Objective
Convert the existing Financial Astrology Terminal into a Sports Astrology Forecast Terminal for Cricket, Football, and Hockey while preserving the complete astrology and astronomy engine.

---

# 1. Remove Financial Components

Remove:
- All Index charts (Nifty, Bank Nifty, Sensex, etc.)
- Commodity charts (Gold, Silver, Crude, etc.)
- Currency charts
- TradingView/OHLC/Candlestick charts
- Market terminology (Buy, Sell, Bullish, Bearish, Futures, Options, IV, Greeks, OI, NSE/BSE/MCX)
- Trading sessions and exchange references

Do **not** remove any astronomy or astrology engine.

---

# 2. Preserve All Astrology

Retain:
- Astronomy Engine (VSOP87/ELP2000)
- Planetary calculations
- KP Astrology
- Vedic Astrology
- Western Astrology
- Nakshatra
- Dasha/Bhukti
- Panchang
- Hora
- Choghadiya
- Muhurat
- Sidereal/Tropical calculations
- Sunrise/Sunset/Moonrise/Moonset
- Planetary transits
- Ayanamsa
- Eclipse calculations
- Local Sidereal Time
- Coordinate transformations

---

# 3. Global Location Engine

Implement intelligent autocomplete.

Typing first 3 characters should search worldwide.

Examples:

Lon -> London

Mum -> Mumbai

Del -> Delhi, Delaware, Delray Beach...

Return:

- Country
- State
- City
- Latitude
- Longitude
- Elevation
- Timezone (IANA)
- UTC Offset
- DST
- Current local time
- Sunrise
- Sunset
- Moonrise
- Moonset
- Solar Noon
- Sidereal Time

Support:
- All countries
- All cities
- Villages (where available)
- Cricket stadiums
- Football stadiums
- Hockey stadiums
- Olympic venues
- Airports
- Universities
- Capitals

---

# 4. Replace Market Time Engine

Replace 09:15–15:30 with a full 24-hour engine.

Support:

00:00 through 23:59

No hardcoded exchange timings.

---

# 5. Sports Prediction Dashboard

Sports:
- Cricket
- Football
- Hockey

Inputs:
- Match Date
- Match Time
- Venue
- Timezone
- Team A
- Team B
- Captain
- Coach
- Tournament
- Match Type
- Weather
- Ground
- Referee/Umpire

Outputs:
- Winning Probability
- Favoured Team
- Momentum Score
- Confidence %
- Planetary Strength
- Upset Probability
- Tie Probability
- Critical Match Windows
- Lucky Numbers
- Lucky Colours
- Dominant Planet
- Weak Planet

---

# 6. Vedic Numerology Module

Include:
- Birth Number
- Destiny Number
- Name Number
- Psychic Number
- Kua Number
- Personal Year
- Personal Month
- Personal Day
- Universal Year
- Universal Month
- Universal Day
- Lo Shu Grid
- Lucky Numbers
- Unlucky Numbers
- Lucky Colours
- Lucky Dates
- Compatible Numbers
- Planet Mapping

---

# 7. Match Muhurat

Generate:
- Best Kickoff Time
- Best Toss Time
- Best Batting Period
- Best Bowling Period
- Best Substitution Window
- Hora
- Rahu Kalam
- Gulika
- Yamaganda
- Choghadiya
- Abhijit Muhurat

---

# 8. Team Horoscope

Support charts using:
- Club foundation date
- Captain DOB
- Coach DOB
- Owner DOB
- Tournament chart
- Event chart

---

# 9. Event Astrology

Display:
- Planetary Wheel
- KP Cusps
- Nakshatra Wheel
- Transit Wheel
- Dasha Timeline
- Retrograde Timeline
- Planetary Speed
- Moon Phase
- Aspects
- Element Balance

---

# 10. World Time Dashboard

Display simultaneously:
- UTC
- Venue Time
- User Time
- Local Sidereal Time
- Solar Time
- Planetary Hour
- Sunrise
- Sunset
- Moonrise
- Moonset

---

# 11. Weather Module

Display:
- Temperature
- Humidity
- Pressure
- Wind
- Rain %
- UV
- Cloud Cover
- Visibility
- Moon Phase

---

# 12. Stadium Database

Store:
- Stadium Name
- Sport
- Country
- Coordinates
- Elevation
- Capacity
- Surface
- Roof Type
- Indoor/Outdoor

---

# 13. AI Prediction Layer

Fuse:
- KP Astrology
- Vedic Astrology
- Western Astrology
- Numerology
- Weather
- Venue
- Historical Event Charts

Output:
- Final Prediction Score
- Confidence Score
- Supporting Factors
- Contradicting Factors

---

# 14. UI Terminology

Replace:

Market → Match

Index → Tournament

Trading Session → Match Session

Market Open → Kickoff

Market Close → Full Time

Bullish → Positive Momentum

Bearish → Negative Momentum

Buy → Favoured

Sell → Unfavoured

---

# 15. Additional Improvements (Recommended)

- Remove all hardcoded financial assumptions.
- Add tournament calendar.
- Add live score API integration hooks.
- Add historical match archive.
- Add player birth chart analysis.
- Add referee/umpire astrology.
- Add team compatibility matrix.
- Add stadium astro profile.
- Add multilingual support.
- Add dark/light themes.
- Add PDF export.
- Add CSV export.
- Add prediction history.
- Add API-ready architecture.
- Keep the astronomy engine completely intact and unchanged.

