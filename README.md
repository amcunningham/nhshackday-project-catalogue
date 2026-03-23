UK Vaccination Eligibility Checker
A single-page web app that shows which routine NHS vaccines a person was (or is) eligible for, based on their date of birth and sex. Covers anyone born from 1980 to the present day.
Live site: https://amcunningham.github.io/myvaccs/
What it does
Enter a date of birth and sex, and the app generates a personalised vaccination timeline showing:

Infant vaccines — the correct combination vaccine for the era (DTP+OPV, 5-in-1, or 6-in-1), plus rotavirus, MenB, MenC, and PCV where applicable
Pre-school boosters — DTaP/IPV and MMR/MMRV second dose, childhood flu, and the 1994 MR catch-up campaign
Teenage vaccines — HPV (with correct product and dose count for the era), Td/IPV booster, MenACWY or MenC, and BCG for older cohorts
Adult vaccines — annual flu, pneumococcal (PPV23), shingles (Shingrix), and COVID-19 programme context

The schedule is historically accurate: it reflects what was actually in the routine programme at the time each vaccine would have been due, not just the current schedule. For example, a male born in 2003 correctly sees "HPV — not offered" (the programme only extended to boys from 2019), while a female born in 1985 sees the single measles vaccine rather than MMR (which wasn't introduced until 1988).
Key schedule changes covered
YearChange1988MMR replaced single measles vaccine1990Accelerated schedule (2, 3, 4 months instead of 3, 5, 9 months)1992Hib added (October 1992)1994One-off MR catch-up campaign for 5–16 year olds1996MMR second dose introduced at pre-school age (October 1996)1999MenC conjugate vaccine introduced (November 1999)20045-in-1 (DTaP/IPV/Hib) replaced DTP/Hib + OPV2005Universal schools BCG programme ended2006PCV7 introduced (September 2006)2008HPV for girls — Cervarix, 3 doses (September 2008)2010PCV13 replaced PCV72012HPV switched to Gardasil (still 3 doses)2013Rotavirus introduced (July 2013); childhood flu nasal spray phased rollout begins2014HPV reduced to 2 doses2015MenB introduced (September 2015); MenACWY replaced teenage MenC20176-in-1 replaced 5-in-1, adding hepatitis B (August 2017)2019HPV extended to boys (September 2019)2020PCV schedule reduced to 1+1 (January 2020)2023HPV reduced to single dose (September 2023)2025MenB timing changed; PCV moved to 16 weeks (July 2025)2026MMRV replaces MMR; new 18-month 6-in-1 booster dose (January 2026)
Data sources
Schedule data was verified against:

UKHSA Vaccination Timeline — official chronology of UK vaccine introductions from 1796 to present
The Green Book (Immunisation Against Infectious Disease) — Chapter 11: The UK immunisation schedule
Complete Routine Immunisation Schedule — current schedule from January 2026
Individual GOV.UK announcements for programme changes (HPV single dose, 6-in-1 introduction, MenB programme, childhood schedule changes 2025/26)

Limitations

Covers the routine programme only — does not include targeted vaccines (e.g. neonatal BCG for high-risk groups, hepatitis B for at-risk infants pre-2017, occupational or travel vaccines)
Birth date cutoffs for vaccine introductions are approximate where programmes were phased in over weeks
Based on the England schedule — Scotland, Wales, and Northern Ireland broadly follow the same programme but may have minor timing differences
The childhood flu rollout was phased year-by-year from 2013 to ~2020; exact eligibility by school year is approximated
This is not a medical device and should not be used as a substitute for checking individual health records

Technical details
Single self-contained HTML file with no external dependencies. Uses vanilla JavaScript — no build step, no frameworks. Works in any modern browser.
Features:

Shareable URLs with query parameters (?dob=2003-06-01&sex=male)
Print-friendly layout (hides input form, clean formatting)
Download schedule as plain text
Responsive design for mobile
