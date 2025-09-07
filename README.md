# Lesson Completion Anomaly Detection

Root cause analysis of suspicious lesson completions on platform. Includes SQL-based detection, storytelling for stakeholders, and dashboard-informed recommendations.

---

## Overview

This repository investigates unusual user behavior on the learning platform—specifically, lessons completed in unrealistically short timeframes. Prompted by a **suspected system issue following a platform update**, the goal was to identify false completions that could skew engagement metrics and mislead decision-making.

---

## Persona Card: Framing the Problem

- **Persona**: *Lena, Learning Product Manager*
- **Pain Point**: After a recent platform update, Lena notices a spike in completion rates. Some users appear to finish two lessons in the *same profession* within **under 5 seconds**.
- **Goal**: Understand if these completions are legitimate or system-generated anomalies.
- **Business Impact**: False completions can distort engagement metrics, affecting data-driven product decisions.

---

## Key Insight

> Out of 345 users in the April 2020 data-analyst cohort, 2 exhibited suspicious behavior; completing lessons less than 5 seconds apart. 

---

## Additional Observations

- Only **4 total completions under 5 seconds** were identified across all professions:  
  → *2 in data-analyst*  
  → *2 in software-engineer*

- Additional completions between **5 and 60 seconds** may not indicate bugs but still fall below expected engagement thresholds.
- All suspicious completions occurred in **early April 2020**, suggesting a **possible bug introduced by a system update**.
- No anomalies were observed in the *data-scientist* profession or outside April 2020.

---

## Conclusion

> The 5-second rule isolates **clear outliers,** while lessons finished in under a minute may still need a closer look based on how users typically learn.  
> **Average time between lessons dropped** significantly in April, indicating a dip in overall user engagement during the suspected bug period.
> Additionally, a notable **drop in new user onboarding** suggests the crash may have impacted user acquisition or initial engagement.

---

## Recommendations

- **Introduce real-time flags** that trigger alerts when multiple lesson completions occur within 5 seconds in the same profession track. This will enable early detection of recurring anomalies and support faster investigation.
- **Enhance event logging** capabilities to capture more granular user interactions and system events. This will improve traceability, making it easier to audit, diagnose, and monitor unusual behaviors through dashboards such as an issue tracker.
- **Investigate post-crash user retention trends** to assess the impact on onboarding and long-term engagement, and guide recovery strategies.

---

## Repository Navigation

- `/sql/` – All SQL queries used in this analysis (Task 1)
- `/dashboard/` – Event-logging dashboard mockups (Task 2)

---

