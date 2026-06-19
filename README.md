**Air Quality & Market Opportunity Analysis: Demand Validation for AirPure Innovations**

1. **PROJECT BACKGROUND**
AirPure Innovations is a UK-based startup born out of India's air quality crisis, with 14 Indian cities ranking among the [world's top 20 most polluted urban centers](https://www.iqair.com/in-en/world-most-polluted-cities). The company is in the early stages of product development and is unsure whether there is a strong, sustained demand for its air purifier product. Before committing to production and R&D spend, leadership (Tony) reached out to Data Analyst Peter Pandey to validate demand and answer five critical questions: (1) What pollutants or particles should the purifier target? (2) What are the most essential features to incorporate? (3) Which cities carry the highest demand and what is the market size? (4) How can R&D be aligned with localized pollution patterns? (5) Where does sustained, defensible demand actually exist? The objective of this project was to design an interactive Power BI dashboard that interrogates three market dimensions — **Severity Mapping** (persistent/worsening AQI), **Health Impact Correlation** (pollution-linked disease burden), and **Demand Triggers** (emission load and addressable market) — to support a go/no-go and a geo-prioritized go-to-market decision.

2. **KEY INSIGHTS**
**Severity Baseline**: The national mean AQI sits at 118.9, anchoring India in the "Moderate" band, while 14.6% of all city-day readings fall in the Poor / Very Poor / Severe bands — a structurally unsafe baseline for a large urban cohort.

**Target Pollutant Signal**: PM2.5 / PM10 is the prominent pollutant in 83.5% of all readings, making particulate matter — not gaseous pollutants — the single highest-priority filtration target.

**Severity Hotspots**: The Delhi-NCR corridor dominates the worst-air rankings — Byrnihat (235), Gurgaon (223), Delhi (216), Ghaziabad (213), Greater Noida (206), Bhiwadi (206) — with Delhi posting 51.4% of readings in Poor+ bands.

**Improving-but-Concentrated Trend**: National mean AQI improved from 156.5 (2015) to 103.2 (2025), a −34.0% decade shift; however, severity remains geographically concentrated in the northern Indo-Gangetic belt rather than resolved.

**Health Burden**: Pollution-adjacent illness reporting totals 1,663,762 cases and 27,992 deaths (overall CFR 1.68%). The respiratory subset alone (Influenza/H1N1/pneumonia-class) carries 197,645 cases and 16,941 deaths — a CFR of ~8.6%, ~5× the all-cause rate — quantifying the well-being cost air purifiers address.

**Emission Load (Demand Trigger)**: Of 248.3M vehicle registrations, internal-combustion fuels make up 93.3% of the fleet (Petrol 81.6%, Diesel 11.7%), sustaining the particulate load; EV penetration is just 2.1% but surging (+359% from 2021 to 2023), signaling a population already shifting toward clean-air behaviors.

**Addressable Market**: Coverage spans 32 states, 296 cities, and 559 monitoring stations, with urban-population concentration in Maharashtra, Uttar Pradesh, Tamil Nadu, Gujarat, and West Bengal framing the serviceable market beyond the high-AQI launch belt.

3. **RECOMMENDATIONS**
**Pollutant-Led Product Spec**: Engineer the core unit around PM2.5/PM10 capture (true-HEPA + activated carbon), since particulates drive 83.5% of severity events.

**Geo-Phased Launch**: Prioritize the Delhi-NCR severity cluster (Delhi, Gurgaon, Ghaziabad, Greater Noida) as Tier-1 demand, then expand to high-population secondary states.

**Health-Anchored Positioning**: Lead messaging with the respiratory health burden (CFR ~8.6%) rather than generic "clean air" claims to justify premium pricing.

**Behavioral Tailwind Capture**: Time campaigns to seasonal AQI spikes and ride the documented EV/clean-tech adoption curve as a proxy for purchase intent.

**Localized R&D**: Tune filter ratings and sensor calibration to state-level pollution profiles instead of a one-size-fits-all SKU.

An interactive Power BI Dashboard (as shown in the screenshots) can be downloaded
[HERE](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/CODEBASICS_AIRPURE_PURIFIER.pbix).

The SQL Queries utilized for inspection and validation can be found
[HERE](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/AirPure%20Inspection.sql).

SQL Queries used for cleaning and transformation can be found HERE.

Targeted SQL Queries for deeper analysis can be found
[HERE](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/AirPure%20Targeted.sql).

**Data Structure & Initial Checks**
AirPure Innovations' analytical model, as illustrated in the model view, consists of 10 tables: CITY STATE AQI, DISEASE AND DEATTH REPORT CASES, VEHICLE & FUEL, URBAN POPU GENEDER AQI, and six conformed dimensions (DIM 1 STATE & CITY, DIM 2 STATE AND CITY, DIM 2 DISEASE, DIM 3 FUEL TYPE, DIM 3 STATES, DIM 3 VEHICLE), with a total row count of 656,794 records across a 2009–2025 reporting horizon.

![Dashboard](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/DATAMODEL.png)

Prior to the beginning of the analysis, a variety of checks were conducted for quality control & familiarization with the datasets. The SQL Queries utilized to inspect & perform quality checks can be found here.

**Executive Summary**

**Overview of Findings**

![Dashboard](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/OVERVIEW.png)

AirPure Innovations' market-opportunity analysis validates a strong, structurally durable demand case for entry into India. The national mean AQI of 118.9 (Moderate band) masks a sharply concentrated severity profile: 14.6% of city-day readings sit in Poor+ bands, and the Delhi-NCR corridor (Delhi mean AQI 216, with 51.4% of readings in Poor+) anchors a Tier-1 demand cluster. Particulate matter is unambiguously the product target — PM2.5/PM10 is the prominent pollutant in 83.5% of all readings — which directly answers the engineering question around filtration priority. The health dimension quantifies the consumer cost: 1,663,762 reported cases and 27,992 deaths (CFR 1.68%), with the respiratory subset far deadlier at a ~8.6% CFR, giving the brand a defensible, health-anchored value proposition. On the demand-trigger side, an internal-combustion-dominated fleet (93.3% Petrol+Diesel of 248.3M registrations) sustains the particulate load, while a +359% EV surge (2021→2023) signals a population already migrating toward clean-air behavior. Although national AQI has improved −34.0% over the decade, severity remains geographically locked into the northern belt rather than resolved — meaning demand is persistent, not transient. AirPure should therefore proceed to production with a PM-led HEPA+carbon spec, a geo-phased NCR-first launch, and health-led positioning.

Below is the overview page from the Power BI dashboard, and more examples are included throughout the report. The entire interactive dashboard can be downloaded HERE.

**SEVERITY MAPPING (AQI & CAPACITY)**
This section evaluates where air quality is persistently or worsening across states and cities, establishing the geographic spine of demand.

![Dashboard](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/SEVERITY%20MAPPING.png)

**Severity Baseline**: The national mean AQI of **118.9** places India in the Moderate band, but **14.6%** of all readings fall in Poor / Very Poor / Severe categories — a large, chronically exposed urban cohort.

**Hotspot Concentration**: The worst-AQI cities cluster tightly in the northern Indo-Gangetic belt — **Byrnihat (235), Gurgaon (223), Delhi (216), Ghaziabad (213), Greater Noida (206), Bhiwadi (206)** — indicating demand is regional, not uniform.

![Dashboard](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/POLLUTANT%20BREAKDOWN.png)

**Target Pollutant**: **PM2.5/PM10 drives 83.5%** of prominent-pollutant readings, confirming particulate filtration (true-HEPA) as the core engineering requirement over gaseous-pollutant handling.

**Trend Implication**: National AQI improved from 156.5 (2015) to 103.2 (2025), a **−34.0%** shift, yet severity stays locked into the NCR corridor — demand is persistent rather than fading, de-risking long-term investment.

**HEALTH IMPACT CORRELATION**
This section quantifies the health burden attributable to poor air quality and translates it into a consumer well-being argument.

![Dashboard](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/HEALTH%20IMPACT.png)

**Disease Burden**: Reported pollution-adjacent illness totals **1,663,762 cases** and **27,992 deaths**, an overall **CFR of 1.68%**, establishing a measurable population-level health cost.

**Respiratory Severity**: The respiratory subset (Influenza/H1N1/pneumonia-class) carries **197,645 cases and 16,941 deaths** — a **CFR of ~8.6%**, roughly **5×** the all-cause rate — directly tying air quality to the most lethal illness category the product mitigates.

**Geographic Overlap**: High-burden states (West Bengal, Maharashtra, Karnataka, Uttar Pradesh, Madhya Pradesh, Delhi) intersect with high-AQI zones, reinforcing a combined severity-plus-health demand signal.

**Positioning Insight**: The health-cost magnitude justifies a premium, outcome-led value proposition rather than commodity "air cleaner" messaging.

**DEMAND TRIGGERS (EMISSION LOAD & MARKET SIZE)**
This section examines the structural drivers of pollution and the addressable market that converts severity into purchasing demand.

![Dashboard](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/DEMAND%20TRIGGERS.png)

**Emission Source Load**: Of **248.3M vehicle registrations**, internal-combustion fuels constitute **93.3%** of the fleet (**Petrol 81.6%, Diesel 11.7%**), a sustained structural contributor to ambient particulates that keeps demand from self-correcting.

**Behavioral Tailwind**: EV penetration is only **2.1%** today but registrations surged **+359%** from 2021 to 2023 — a leading indicator of a consumer base already adopting clean-air, health-conscious behaviors.

![Dashboard](https://github.com/bhawna407/AirPure-Innovations-Analysis/blob/main/MARKET%20SIZE.png)

**Addressable Market**: Coverage across **32 states, 296 cities, and 559 monitoring stations**, with urban-population mass concentrated in **Maharashtra, Uttar Pradesh, Tamil Nadu, Gujarat, and West Bengal**, frames a serviceable market well beyond the high-AQI launch belt.

**Strategic Risk**: Demand is geographically lumpy; a national-uniform launch would dilute spend, whereas a severity-weighted, population-weighted rollout maximizes capital efficiency.

**RECOMMENDATIONS**
Based on the uncovered insights, the following priority actions are recommended:

**Pollutant-Led Product Spec**: Anchor the core SKU on **PM2.5/PM10 capture (true-HEPA + activated carbon)**, since particulates account for 83.5% of severity events; add PM-real-time sensing as the headline feature.

**Geo-Phased Go-To-Market**: Launch into the **Delhi-NCR severity cluster** (Delhi, Gurgaon, Ghaziabad, Greater Noida, Bhiwadi) as Tier-1 demand, then sequence into high-population secondary states to optimize CAC and inventory.

**Health-Anchored Positioning**: Lead with the **respiratory health burden (~8.6% CFR)** to justify premium pricing and differentiate from commodity purifiers competing on price.

**Behavioral & Seasonal Targeting**: Time campaigns to **seasonal AQI spikes** and ride the documented **+359% EV adoption** curve as a proxy for clean-air purchase intent.
