
## Executive Summary

- Analyze Vietnam's garment export destinations using UN Comtrade data from 2014–2023.
- Key findings:
    - Vietnam exports garments to more than 150 countries, but demand is highly concentrated.
    - The United States, Japan, and South Korea consistently account for more than 70% of export demand.
    - Market concentration peaked around 2021 before declining modestly.
    - Several established markets show signs of stagnation or decline.
    - Emerging growth markets are concentrated in Southeast Asia, Eastern Europe, and parts of Africa.
    - Clustering analysis identifies four distinct groups of export markets.
## Motivation:

- Vietnam is one of the world's largest garment exporters.
- Export-oriented industries are highly dependent on foreign demand.
- Understanding who buys Vietnamese garments and how that demand is changing can help identify:
    - concentration risk,
    - declining markets,
    - emerging opportunities.
- This analysis aims to answer three questions:
    1. Who buys Vietnamese garments?
    2. How dependent is Vietnam on a small number of buyers?
    3. Which markets are growing, declining, or emerging?
## Data

### Source
- UN Comtrade
### Scope
- Years: 2014–2023
- Products:
    - HS61: Articles of apparel and clothing accessories, knitted or crocheted
    - HS62: Articles of apparel and clothing accessories, not knitted or crocheted
- Unit: Export Value (USD)
### Data Coverage
- 150 destination countries
- 85 countries with complete coverage (2014–2023)
- 95 countries with at least 5 years of observations

<img width="1182" height="603" alt="download" src="https://github.com/user-attachments/assets/3dfefd10-28d5-411a-9252-3950b70dc043" />

## 1. Who buys Vietnamese garments?

### Geographic Overview

<img width="1942" height="959" alt="download" src="https://github.com/user-attachments/assets/a10f8f5b-a1ea-4dc9-8de0-7a22a72ea8eb" />

### Key observations
- Vietnamese garment exports are concentrated in:
    - North America
    - East Asia
    - Western Europe
- The United States is by far the largest destination market.
### Largest buyers:

<img width="1389" height="592" alt="download" src="https://github.com/user-attachments/assets/5b5ec3ad-0f36-4b7f-9b26-8cdccd9199a9" />


### Key observations
- The United States dominates all other destination markets.
- Japan and South Korea form a second tier of major buyers.
- China, Canada, the United Kingdom, Germany, France, and the Netherlands form the next group of important destinations.
- Vietnam's export demand is concentrated among developed economies.
### Takeaway
- Export demand is not evenly distributed across countries.
- A small number of markets account for the majority of garment exports.

## 2. Is Vietnam dependent on a small set of buyers?
To investigate this, I plot the change over time of two metrics: 
1. The market share of the top 3 market: USA, Korea, Japan
2. Herfindahl-Hirschman Index (HHI): a formal index that measure market concentration. On a scale of 0 to 1.0, a larger number means a more concentrated market. An HHI above 0.25 indicates high concentration. 
### Top-3 Market Share and HHI plot:

<img width="1189" height="495" alt="download" src="https://github.com/user-attachments/assets/3d4d4fab-c2a0-4f3e-a6f9-680e3210be09" />


### Key observations

Market concentration peaked in 2021 before declining modestly in subsequent years. This pattern is consistent with external demand shocks rather than structural shifts in Vietnam's export base. 
- In 2021, US export values rose sharply while Japan, South Korea, and smaller markets remained largely stagnant, consistent with the US stimulus-driven consumption surge of that period.
- In 2022, concentration declined despite all three major markets growing in absolute terms. This reflects a faster recovery in smaller markets, which grew the total export base more rapidly than the top 3, mechanically diluting their combined share.

=> The post-2021 decline in concentration therefore should not be interpreted as active market diversification on Vietnam's part, but rather as a demand normalization effect following an unusual period of concentrated US growth.

## 3. Which Markets Are Growing and Which Are Declining?

### Trends Among Major Markets

<img width="841" height="547" alt="download" src="https://github.com/user-attachments/assets/71283096-bc08-404f-b24b-a5255aa82bf5" />
<img width="855" height="547" alt="download" src="https://github.com/user-attachments/assets/e5264738-e10c-4ab8-8aa3-7c2e641bcf37" />
<img width="846" height="547" alt="download" src="https://github.com/user-attachments/assets/a16e13f6-40e3-4b6b-821f-371c77f26629" />

#### Key observations
- The United States, Japan, and South Korea remain the dominant destinations throughout the period.
- Several mid-sized markets exhibit substantially more volatility.
- Relative rankings among secondary markets change considerably over time.

---
### Growth vs Market Importance

#### Method
- Estimate annual growth using CAGR between 2014 and 2023.
    - 2014 and 2023 were selected as endpoints as both are relatively neutral years, unaffected by the demand distortions of the 2020–2021 COVID period.
    - 92 countries with valid export values in both endpoint years are included in this analysis.
    - Note that for smal and volatile markets, CAGR should be interpreted cautiously, single-year fluctuations at either endpoint directly affect the estimated rate.
- Classify countries according to:
    - Market share
    - Annual growth rate (CAGR)
- Define major markets as countries with an average market share above 0.5%.
#### Market Segments

| Market Segment            | Market Share | Growth Rate |
|---------------------------|-------------|-------------|
| Strategic Growth Markets  | Large       | Positive    |
| Emerging Markets          | Small       | Positive    |
| Mature/Declining Markets  | Large       | Negative    |
| Peripheral Markets        | Small       | Negative    |

<img width="1008" height="860" alt="download" src="https://github.com/user-attachments/assets/95865883-d59b-410f-a701-c74d477d4cca" />
<img width="1182" height="603" alt="download" src="https://github.com/user-attachments/assets/1764dfbf-9296-4cc2-8f28-5275b9a44032" />


|Segment|Examples|Interpretation|
|---|---|---|
|**Strategic Growth Markets**|USA, Japan, South Korea, China, most of Western Europe, Australia, Canada|Core export markets that continue to expand and remain the foundation of Vietnam's garment exports.|
|**Emerging Markets**|India, Southeast Asia, Poland, Croatia, Turkey, South and Southeast Africa, Mexico, Argentina, Peru, UAE, Egypt, Morocco, Algeria|Fast-growing destinations with currently limited share that could become increasingly important.|
|**Mature/Declining Markets**|Spain|The only major market with a clearly negative CAGR. Stands out against the broader pattern of stable or growing Western European markets. The cause is not clear from the data alone and warrants further investigation.|
|**Peripheral Markets**|Brazil, Chile, Norway, Denmark, Austria, Switzerland, Cambodia|Small markets with negative growth and limited strategic importance.|

#### Notable Observations

**United Kingdom** sits just above zero CAGR and is technically classified as a growth market, but its near-flat trajectory warrants caution. It should not be treated with the same confidence as other Strategic Growth Markets.

**Chile** is the largest Peripheral Market by export volume, approaching the 0.5% share threshold, and has a negative CAGR. It represents the most significant market currently classified as peripheral and merits monitoring.

**Cambodia** appears in the Peripheral segment but should be interpreted differently from pure consumer markets. Vietnam and Cambodia share deep garment supply chain linkages, and exports likely reflect intermediate trade activity rather than Cambodian domestic consumption.

#### Special Cases: Markets Requiring Cautious Interpretation

Three major markets are correctly classified by the quadrant but cannot be fully captured by CAGR alone:

**China** — classified as a Strategic Growth Market due to strong 2014–2019 growth that outweighs a consistent post-2019 decline. Its positive full-period CAGR masks a market that has been contracting for four consecutive years. China's trajectory should be monitored closely rather than treated as an expanding opportunity.

**Hong Kong** — classified as a Peripheral Market with negative CAGR. However, Hong Kong functions primarily as a re-export hub rather than a final consumer market. Its decline likely reflects supply chain restructuring and reduced triangular trade routing rather than weakening end consumer demand.

**Russia** — classified as an Emerging Market based on its full-period CAGR. However, this classification does not account for the severe trade disruptions following the 2022 invasion of Ukraine and subsequent sanctions. Its current trajectory is not comparable to structurally emerging markets and should be treated separately.


## 4. Market Segmentation Using P Clustering

### Objective

Validate the quadrant classification using an unsupervised clustering approach that incorporates a third dimension — market volatility — not captured by the quadrant analysis alone.

### Variables Used

- Log average export value
- CAGR
- Coefficient of variation (volatility)

### Method

- Perform K-Means clustering on standardized features.
- Select three clusters using the elbow method.
- A four-cluster solution was tested but produced a singleton cluster driven by Malta, a micro-state with an unusually high CAGR on a negligible export base. Three clusters were retained as more meaningful.

### Cluster Profiles

|Cluster|Avg Exports|CAGR|Volatility (CV)|Label|
|---|---|---|---|---|
|0|$500M|3%|0.37|Established Markets|
|1|$30M|23%|0.72|Emerging Markets|
|2|$2M|-21%|1.17|Peripheral Markets|

### Cluster Visualization

<img width="1085" height="855" alt="download" src="https://github.com/user-attachments/assets/e3b91121-1f73-4d37-b828-18d7d466fec3" />


### Validation Against Quadrant Classification

The clustering broadly confirms the quadrant structure. Strategic Growth Markets from the quadrant analysis predominantly fall into Cluster 0, Emerging Markets into Cluster 1, and Peripheral Markets into Cluster 2.

Importantly, volatility largely correlates with the quadrant segments rather than cutting across them — Established Markets show the lowest volatility, Peripheral Markets the highest. This suggests that market reliability and market trajectory move together: fast-growing markets tend to be more volatile, while stable large markets are more predictable.

Where the two classifications diverge, clustering tends to absorb mildly negative-CAGR markets with low volatility into Cluster 0 rather than Peripheral. This reflects a meaningful distinction: a slightly declining but highly stable market is structurally different from a volatile declining one, and may still represent a reliable export destination despite negative growth.


### Spatial Distribution

<img width="1182" height="603" alt="download" src="https://github.com/user-attachments/assets/2b07df45-6bc4-43d1-9e3c-9e262a046e01" />


## Take away insights (conclusion):

Vietnam exports garments to 150+ countries, but the demand is highly concentrated.
The US, Japan, and South Korea alone account for more than 70% of total export value. The HHI confirms this is not just a top-3 problem — the entire export structure is concentrated, and despite recent improvements, it has not meaningfully diversified.
The 2021 concentration peak was a demand shock, not a structural shift.
The US stimulus-driven consumption surge pushed the top-3 share to its highest point. The subsequent decline reflects smaller markets recovering faster post-COVID, not Vietnam actively expanding into new destinations. The diversification story is weaker than the numbers suggest at first glance.
Most major markets are stable, but the growth frontier is small and volatile.
Western Europe, North America, East Asia, and Australia form a reliable core with moderate growth. Southeast Asia, parts of Africa, the Middle East, and Eastern Europe are growing fast but remain small. Spain is the only major market in clear long-term decline, and its cause is unexplained by the data.
Three major markets need more careful interpretation than the quadrant suggests.

China looks like a growth market on paper, but exports have been falling since 2019. The positive CAGR is a legacy of pre-2019 growth.
Hong Kong's declining exports reflect supply chain restructuring, not weakening consumer demand.
Russia's classification is distorted by post-2022 sanctions and is not comparable to other markets in its cluster.

Volatility is the hidden cost of emerging markets.
The clustering analysis shows that fast-growing markets are also significantly more volatile. For logistics planning, this matters: emerging market growth comes with less predictable demand, longer ramp-up uncertainty, and higher operational risk.
The core strategic tension is concentration vs growth.
Established markets are stable but growing slowly. Emerging markets are growing fast but remain small and unreliable. Vietnam's export base is still heavily dependent on a handful of buyers, and the data does not yet show diversification happening at scale. Reducing that concentration risk remains an open challenge.
