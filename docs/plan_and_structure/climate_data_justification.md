# Climate Data Selection: Configuration Rationale  
**Flagship Project 2 – Climate–Housing Risk**

This document outlines the climate-data configuration used for the Climate–Housing Risk Project.  
The goal is to maintain a setup that is **scientifically robust, computationally efficient, and aligned with Australian climate-risk practice**.

The configuration below reflects an optimal balance between uncertainty coverage, interpretability, and workload.

---

## 1. Dataset Choice: CSIRO AGCD/QDC  
We use the **CSIRO AGCD/QDC application-ready dataset**, which is widely used in Australian climate-impact modelling. Key advantages include:

- Daily fields with consistent preprocessing  
- High spatial quality across Australia  
- Harmonised formatting across models and scenarios  
- Alignment with datasets commonly used in impact, insurance, and infrastructure studies

This makes it well suited for housing-risk applications that depend on high-quality local climate information.

---

## 2. Climate Model Selection  
The project uses a **three-model CMIP6 mini-ensemble** chosen to span a broad yet efficient range of uncertainty:

### ACCESS-CM2  
- Developed by CSIRO/Bureau of Meteorology  
- Strong land–atmosphere coupling over Australia  
- Good representation of temperature extremes  
- Acts as a regionally relevant anchor model

### EC-Earth3  
- Independent model lineage with realistic hydrology  
- Represents a mid-range warming trajectory  
- Helps capture central estimates of future climate change

### UKESM1-0-LL  
- Characterised by higher climate sensitivity  
- Produces stronger warming and hydrological responses  
- Useful for exploring upper-bound risk and stress-testing exposure

**Together**, these models provide a balanced envelope:  
an Australian-calibrated anchor (ACCESS-CM2), a central projection (EC-Earth3), and a high-sensitivity model (UKESM1-0-LL).  
This combination captures most of the structural uncertainty relevant to climate-risk analysis while keeping computational and storage demands manageable.

---

## 3. Emissions Scenarios: SSP245 and SSP585  
Two scenarios are included to cover the most relevant future trajectories for risk assessment:

### SSP245  
- Represents moderate climate mitigation  
- Often used for planning mid-century societal and economic conditions

### SSP585  
- High-forcing pathway  
- Important for examining upper-bound hazards and long-tail risks

Using these two scenarios provides a practical and meaningful range for decision-making without introducing unnecessary complexity from additional pathways.

---

## 4. Climate Variables: `tasmax` and `pr`  
The project focuses on the two variables most directly linked to housing-related climate risk in Australia:

### `tasmax` – Daily Maximum Temperature  
- Heat extremes and thermal stress  
- Building material performance  
- Energy demand and habitability

### `pr` – Daily Precipitation  
- Flooding and stormwater pressure  
- Soil movement and structural impacts  
- Drought and moisture-related building stress

Other variables (e.g., humidity, wind) are valuable in specialised contexts, but `tasmax` and `pr` capture the dominant climatic drivers affecting residential exposure for this project’s scope.

---

## 5. Summary of Advantages  
This configuration is designed to maximise scientific insight while maintaining efficiency:

- Captures central and upper-end climate uncertainty  
- Uses models with strong relevance to Australian conditions  
- Provides scenario breadth suited to housing-risk assessments  
- Focuses on variables with the highest explanatory power  
- Keeps data volume manageable for a production-grade workflow  
- Improves model interpretability for downstream financial, policy, and climate-risk applications

Overall, this setup provides a clear, balanced, and defensible foundation for analysing climate impacts on the Australian housing sector.
