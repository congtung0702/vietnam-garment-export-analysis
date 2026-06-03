
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

<img width="1389" height="592" alt="download" src="https://github.com/user-attachments/assets/8be225ef-27c5-4f3f-96ee-1bdbb5968d3f" />


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
### Top-3 Market Share

<img width="700" height="470" alt="download" src="https://github.com/user-attachments/assets/df770e84-cb0c-4eac-a585-1823eab3e882" />


### Key observations
- The United States, Japan, and South Korea consistently account for more than 70% of total exports.
- Dependence on these three markets peaked during 2021 and then moderately declined afterwards.

---
### Herfindahl-Hirschman Index (HHI)

<img width="700" height="470" alt="download" src="https://github.com/user-attachments/assets/f1af13db-4600-416d-8731-b4ae228d2162" />


### Key observations
- HHI confirms a highly concentrated export structure.
- Concentration peaked around 2021 before declining modestly.
- Despite recent diversification, export demand remains heavily concentrated.
### Takeaway
- Vietnam exports to many countries, but a small number of buyers continue to dominate demand.
- The industry remains vulnerable to shocks affecting a handful of major markets.
## 3. Which Markets Are Growing and Which Are Declining?

### Trends Among Major Markets

<img width="855" height="547" alt="download" src="https://github.com/user-attachments/assets/e5264738-e10c-4ab8-8aa3-7c2e641bcf37" />
<img width="846" height="547" alt="download" src="https://github.com/user-attachments/assets/a16e13f6-40e3-4b6b-821f-371c77f26629" />

#### Key observations
- The United States, Japan, and South Korea remain the dominant destinations throughout the period.
- Several mid-sized markets exhibit substantially more volatility.
- Relative rankings among secondary markets change considerably over time.

---
### Growth vs Market Importance

#### Method
- Estimate annual growth using a linear trend in log export values.
- Classify countries according to:
    - Market share
    - Growth rate
- Define major markets as countries with an average market share above 1%.
#### Market Segments

| Market Segment            | Market Share | Growth Rate |
|---------------------------|-------------|-------------|
| Strategic Growth Markets  | Large       | Positive    |
| Emerging Markets          | Small       | Positive    |
| Mature/Declining Markets  | Large       | Negative    |
| Peripheral Markets        | Small       | Negative    |

<img width="1008" height="860" alt="download" src="https://github.com/user-attachments/assets/3f852b27-e04b-453a-a85e-2dac70167982" />
<img width="1182" height="603" alt="download" src="https://github.com/user-attachments/assets/99f2527e-76d8-4af0-8ffd-3e6b9bf1bd27" />

| Segment | Characteristics | Examples | Interpretation |
|----------|----------|----------|----------|
| **Strategic Growth Markets** | Large market share, positive growth | USA, Japan, South Korea, China, Germany, France, Netherlands, Belgium | Core export markets that continue to expand and remain the foundation of Vietnam's garment exports. |
| **Emerging Markets** | Small market share, positive growth | India, Indonesia, Thailand, Malaysia, Poland, Philippines, Croatia, Slovenia | Fast-growing destinations that could become more important in the future. |
| **Mature / Declining Markets** | Large market share, negative growth | United Kingdom, Spain | Important markets showing long-term weakness and requiring monitoring. |
| **Peripheral Markets** | Small market share, negative growth | Brazil, Argentina, Norway, Austria, Switzerland, Pakistan, Sri Lanka | Markets with limited current importance and weak growth prospects. |

## 4. Market Segmentation Using PCA and Clustering

### Objective

- Identify groups of countries with similar export characteristics.

### Variables Used

- Log average export value
- Average market share
- Estimated growth rate
- Coefficient of variation (volatility)

### Method

- Apply Principal Component Analysis (PCA).
- Retain three principal components explaining approximately 94% of total variance.
- Perform K-Means clustering.
- Select four clusters using the elbow method.

### Cluster Visualization

<img width="1077" height="855" alt="download" src="https://github.com/user-attachments/assets/f7960f41-3b8a-4e3f-8384-d3404c075f53" />

### Cluster Profiles
| Cluster | Characteristics | Typical Markets | Interpretation |
|----------|----------|----------|----------|
| **Stable Core Markets** | Large export volumes, moderate growth, low volatility | Most of Western Europe, Canada, Australia, East Asia, Southeast Asia | Core destinations that provide stable and predictable demand for Vietnamese garments. |
| **Declining Peripheral Markets** | Small market share, negative growth, high volatility | Parts of Africa, Central Asia, Eastern Europe, South Asia | Markets with limited importance and weakening demand. |
| **United States** | Extremely large export volume and market share, positive growth, very low volatility | United States | A unique outlier that dominates Vietnam's garment exports and forms its own cluster. |
| **Emerging Growth Markets** | Small market share, rapid growth, moderate volatility | India, Cambodia, Egypt, Nigeria, East Africa, Portugal, Ecuador | Fast-growing markets that could become increasingly important export destinations. |### Spatial Distribution of Clusters
To clearly shows the spatial patterns of clustering, I plot the following world map showing each country's cluster:

<img width="1182" height="603" alt="download" src="https://github.com/user-attachments/assets/d50425a4-90c3-40f8-87ac-c715e89aa42a" />


### Key observations
- Stable core markets dominate Europe, North America, and East Asia.
- Emerging growth markets are concentrated in developing economies, spreaded throughout Africa, the Middle East, India, and some Europe countries.
- Declining peripheral markets are scattered across several regions.
- The United States remains a unique outlier.

## Take away insights (conclusion):

- Vietnam's garment exports are highly concentrated despite serving more than 150 destination countries.
- The United States, Japan, and South Korea account for more than 70% of export demand.
- Market concentration peaked around 2021 before declining modestly.
- Most future growth opportunities appear to come from emerging markets rather than traditional buyers.
- The United Kingdom and Spain are notable examples of large markets experiencing long-term decline.
- Clustering analysis reveals four distinct market types:
    - Stable Core Markets
    - Declining Peripheral Markets
    - United States (Unique Dominant Market)
    - Emerging Growth Markets
- Vietnam's export strategy faces a trade-off between maintaining relationships with core buyers and expanding into faster-growing emerging markets.
