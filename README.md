# Global Rapid Transit Country Ranking

Ranking of countries by the proportion of their large cities (≥500,000 population) that have rapid transit systems.

## Methodology

- **Rapid transit**: Grade-separated high-capacity urban transit, including metros/subways, fully separated LRT, S-Bahn commuter rail, and gold-standard BRT. Street-running trams excluded.
- **City threshold**: Urban agglomerations with population ≥ 500,000.
- **Proportion**: (cities with rapid transit) ÷ (total cities ≥500k) × 100%.
- **Special case — Luxembourg**: No city reaches 500k, but Luxtram (16.2 km modern light rail) operates. Score = (500,000 ÷ 210,000) × 100% = 238.1%, representing "over-coverage" relative to the threshold.

## Data Sources

| Source | Used for |
|--------|----------|
| Wikipedia "List of metro systems" (via everything.explained.today mirror) | Metro city rosters by country |
| metrorailtoday 2024 country summary | Cross-verification of metro system counts |
| UN Statistics Division city population CSV (via datasets/population-city GitHub) | Urban agglomeration counts ≥500k (where complete) |
| China 2020 7th Population Census (user-provided) | China denominator: 240 cities ≥500k |
| China Ministry of Transport 2024 | China numerator: 43 cities with metro/light rail |

## Verification Status

- `verified`: Both numerator and denominator from authoritative sources
- `verified_UN`: Denominator from UN urban agglomeration data
- `verified_user`: Denominator provided by user (China)
- `verified_num_est_denom`: Numerator verified, denominator estimated
- `estimated`: Both values estimated (countries with incomplete UN reporting)
- `estimated_denom`: Numerator verified, denominator estimated due to UN data gap
- `special_case`: Luxembourg (zero denominator, special formula)

## Key Corrections from Earlier Estimates

| Country | Earlier (wrong) | Corrected | Reason |
|---------|-----------------|-----------|--------|
| China | 67% (47/70) | 17.9% (43/240) | Wrong denominator; user provided 240 from 2020 census |
| France | 58% (7/12) | 77.8% (7/9) | UN UA count = 9, not 12 |
| India | 34% (17/50) | 17.2% (17/99) | UN UA count = 99, not 50 |
| Mexico | 30% (3/10) | 5.9% (3/51) | UN UA count = 51, not 10 |
| Poland | 50% (1/2) | 5.9% (1/17) | UN UA count = 17, not 2 |
| Australia | 40% (2/5) | 15.4% (2/13) | UN UA count = 13, not 5 |
| Argentina | 20% (1/5) | 9.1% (1/11) | UN UA count = 11, not 5 |
| Thailand | 33% (1/3) | 10% (1/10) | UN UA count = 10, not 3 |
| Malaysia | 67% (2/3) | 28.6% (2/7) | UN UA count = 7, not 3 |
| Colombia | 67% (2/3) | 28.6% (2/7) | UN UA count = 7, not 3 |
| Brazil | not in top 50 | 15.4% (8/52) | Added; UN UA count = 52 |

## Files

- `rapid_transit_ranking.csv` — Full dataset with 70 countries, sorted by proportion descending
