## Executive Summary

Vietnam's garment exports reach 150+ countries but remain heavily concentrated. The US, Japan, and South Korea account for more than 70% of total demand, and this has not meaningfully changed over the decade.

**Concentration peaked in 2021 but not for strategic reasons.** A US stimulus-driven demand surge inflated the top-3 share temporarily. The subsequent decline reflects post-COVID recovery in smaller markets, not active diversification by Vietnam.

**Most major markets are stable, not exciting.** Western Europe, North America, East Asia, and Australia form a reliable but slow-growing core. Spain is the only major market in clear decline.

**Growth is happening at the edges.** Southeast Asia, parts of Africa, the Middle East, and Eastern Europe show strong CAGR but remain small and volatile. The clustering analysis confirms that emerging markets carry significantly higher demand uncertainty than established ones.

**Three markets need careful interpretation.** China's positive full-period CAGR masks consistent post-2019 decline. Hong Kong's falling exports reflect supply chain restructuring rather than demand weakness. Russia's classification is distorted by post-2022 sanctions.

**The central finding is a concentration risk that remains unresolved.** Vietnam's export base is structurally dependent on a small number of buyers, and the data does not show diversification happening at scale.


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
- 92 countries with both 2014 and 2023 data. (Only these countries will be used to calculate CAGR later)

<img width="1182" height="603" alt="download" src="https://github.com/user-attachments/assets/3dfefd10-28d5-411a-9252-3950b70dc043" />

## 1. Who buys Vietnamese garments?

### Geographic Overview

<img width="1942" height="959" alt="download" src="https://github.com/user-attachments/assets/c71e92d3-f64e-4d60-acc6-e23e8527f1d8" />


### Key observations

Vietnamese garment exports are geographically concentrated in three regions: North America, East Asia, and Western Europe. Medium-sized markets exist in Southeast Asia, Latin America, and parts of Eastern Europe, but their combined share remains small relative to the core regions. Most of Africa, Central Asia, and the Middle East show minimal export activity.

<img width="1389" height="592" alt="download" src="https://github.com/user-attachments/assets/5b5ec3ad-0f36-4b7f-9b26-8cdccd9199a9" />

The bar plot confirms the spatial pattern: demand is dominated by developed economies, with the US leading far ahead. Japan and South Korea form a distant second tier but still dominate the scale, followed are China, Canada, and the major Western European markets. Given how outsized the top 3 are relative to the rest, a natural question follows: how dependent is Vietnam on these few buyers, and has that dependence changed over time?

## 2. Is Vietnam dependent on a small set of buyers?
To investigate this, I plot the change over time of two metrics: 
1. The market share of the top 3 market: USA, Korea, Japan
2. Herfindahl-Hirschman Index (HHI): a formal index that measure market concentration. On a scale of 0 to 1.0, a larger number means a more concentrated market. An HHI above 0.25 indicates high concentration. 
### Top-3 Market Share and HHI plot:

<img width="1189" height="495" alt="download" src="https://github.com/user-attachments/assets/3d4d4fab-c2a0-4f3e-a6f9-680e3210be09" />


### Key observations

Market concentration peaked in 2021 before declining modestly in subsequent years. This pattern is consistent with external demand shocks rather than structural shifts in Vietnam's export base:
- In 2021, US export values rose sharply while Japan, South Korea, and smaller markets remained largely stagnant, consistent with the US stimulus-driven consumption surge of that period.
- In 2022, concentration declined despite all three major markets growing in absolute terms. This reflects a faster recovery in smaller markets, which grew the total export base more rapidly than the top 3, mechanically diluting their combined share.

=> The post-2021 decline in concentration therefore should not be interpreted as active market diversification on Vietnam's part, but rather as a demand normalization effect following an unusual period of concentrated US growth.

## 3. Which Markets Are Growing and Which Are Declining?

### Trends Among Major Markets

<img width="841" height="547" alt="download" src="https://github.com/user-attachments/assets/71283096-bc08-404f-b24b-a5255aa82bf5" />
<img width="855" height="547" alt="download" src="https://github.com/user-attachments/assets/e5264738-e10c-4ab8-8aa3-7c2e641bcf37" />
<img width="846" height="547" alt="download" src="https://github.com/user-attachments/assets/a16e13f6-40e3-4b6b-821f-371c77f26629" />

### Key observations
The first plot shows the overall trend of Vietnamese garment exports: a steady rise through the decade interrupted by a sharp 2020 dip and a strong 2021 recovery, consistent with the COVID demand shock. A dip was also observed in 2023.

The top 3 markets remain dominant and stable throughout the second plot, with consistently growing trends and unchanged rankings. One notable feature is that all countries experience decreases during the COVID shock (2020-2021) then recover after, asides from China, which continue to decline even after the pandemic. 

Another important observation is a decrease across all top 10 markets in 2023 except for Spain, pulling total export value down with it. This simultaneous dip across different destinations suggests a global demand contraction rather than market-specific factors, which is consistent with the broader softening in global apparel consumption following the post-COVID demand surge.

The picture looks considerably different further down the rankings (3rd plot). Mid-sized markets show much higher volatility, with rankings shifting multiple times over the decade. China was the largest secondary market until 2022, when it was overtaken by Canada, Germany, and the Netherlands, consistent with the described post-COVID decline of the Chinese market.

This instability among secondary markets suggests that growth trajectories vary significantly across destinations. To understand which markets are structurally expanding and which are stagnating or declining, the next section classifies countries by growth rate and market share.


## 4. Market classification using growth rate and market share
### Method
- Estimate annual growth using CAGR between 2014 and 2023.
    - 2014 and 2023 were selected as endpoints as both are relatively neutral years, unaffected by the demand distortions of the 2020–2021 COVID period.
    - 92 countries with valid export values in both endpoint years are included in this analysis.
    - Note that for smal and volatile markets, CAGR should be interpreted cautiously, single-year fluctuations at either endpoint directly affect the estimated rate.
- Classify countries according to:
    - Market share
    - Annual growth rate (CAGR)
- Define major markets as countries with an average market share above 0.5%.
### Market Segments

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
|**Mature/Declining Markets**|Spain|Classified as declining based on full-period CAGR, though the trajectory is more nuanced than the label suggests.|
|**Peripheral Markets**|Brazil, Chile, Norway, Denmark, Austria, Switzerland, Cambodia|Small markets with negative growth and limited strategic importance.|

### Notable Observations

**Spain** is the only major market with a negative full-period CAGR, but its trajectory deserves closer inspection. As can be seen from the plots in the previous Section 3, exports declined steadily from 2014 to 2020, but have been recovering since, and uniquely, Spain was the only top 10 market that continued growing through the broad 2023 dip. Its negative CAGR is therefore a legacy of pre-2020 decline rather than a reflection of current momentum. Whether this recovery is structural or temporary cannot be determined from the data alone, but Spain should not be treated as a straightforwardly declining market without further monitoring.

**United Kingdom** sits just above zero CAGR and is technically classified as a growth market, but its near-flat trajectory warrants caution. It should not be treated with the same confidence as other Strategic Growth Markets.

**Chile** is the largest Peripheral Market by export volume, approaching the 0.5% share threshold, and has a negative CAGR. It represents the most significant market currently classified as peripheral and merits monitoring.

**Cambodia** appears in the Peripheral segment but should be interpreted differently from pure consumer markets. Vietnam and Cambodia share deep garment supply chain linkages, and exports likely reflect intermediate trade activity rather than Cambodian domestic consumption.

#### Special Cases: Markets Requiring Cautious Interpretation

Three major markets are correctly classified by the quadrant but cannot be fully captured by CAGR alone:

**China** — classified as a Strategic Growth Market due to strong 2014–2019 growth that outweighs a consistent post-2019 decline. Its positive full-period CAGR masks a market that has been contracting for four consecutive years. China's trajectory should be monitored closely rather than treated as an expanding opportunity.

**Hong Kong** — classified as a Peripheral Market with negative CAGR. However, Hong Kong functions primarily as a re-export hub rather than a final consumer market. Its decline likely reflects supply chain restructuring and reduced triangular trade routing rather than weakening end consumer demand.

**Russia** — classified as an Emerging Market based on its full-period CAGR. However, this classification does not account for the severe trade disruptions following the 2022 invasion of Ukraine and subsequent sanctions. Its current trajectory is not comparable to structurally emerging markets and should be treated separately.


## 4. Market Segmentation Using K-Means Clustering

### Objective

Validate the quadrant classification using an unsupervised clustering approach that incorporates a third dimension — market volatility — not captured by the quadrant analysis alone.

### Variables Used

- Log average export value
- CAGR
- Coefficient of variation (volatility)

### Method

- Perform K-Means clustering on standardized features.
- Select three clusters using the elbow method.
- A four-cluster solution was tested but produced a cluster containing only Malta, a micro-country with an unusually high CAGR on a negligible export base. Malta was removed as an outlier, and three clusters were retained as more meaningful.

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

Importantly, volatility largely correlates with the quadrant segments rather than conflicting with them: Established Markets show the lowest volatility, Peripheral Markets the highest. This suggests that market reliability and market trajectory move together: fast-growing markets tend to be more volatile, while stable large markets are more predictable.

Where the two classifications differ, clustering tends to absorb mildly negative-CAGR markets with low volatility into Cluster 0 rather than Peripheral. This reflects a meaningful distinction: a slightly declining but highly stable market is structurally different from a volatile declining one, and may still represent a reliable export destination despite negative growth.


### Spatial Distribution of Clusters

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
