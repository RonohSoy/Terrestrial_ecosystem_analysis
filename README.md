<h1 align="center">Terrestrial Ecosystem Conservation and Restoration Analysis Forecasting</h1>
Terrestrial ecosystem analysis involves studying the structure, function, and dynamics of these land-based ecosystems.

<p align="center">
  <img src="https://pub.mdpi-res.com/land/land-12-02052/article_deploy/html/images/land-12-02052-g001.png?1699698383" alt="Description" width="600">
</p>

## Overview
Ecosystem Diversity Analysis project aims to analyze the biodiversity and ecological health of ecosystems using data and machine learning techniques. In today's world, maintaining ecosystem diversity is crucial for the planet's health and for sustaining life. Ecosystem diversity includes all the variety of ecosystems such as forests, oceans, wetlands, and grasslands, and the living organisms within them. By understanding the diversity of ecosystems, conservation efforts can be improved, policy decisions can be informed, and sustainable management practices can be adopted.
## Problem statement
Human activities like deforestation and climate change are driving unprecedented biodiversity loss, making effective conservation more urgent. Traditional, manual methods of monitoring ecosystems and biodiversity are slow and inefficient, hindering timely decision-making. The vast amount of environmental data—from research papers to reports—remains underutilized due to the difficulty of manual analysis. Automating this process using NLP, machine learning, and deep learning can enable faster, more accurate insights, empowering better decision-making for conservation, ecosystem restoration, and protected area monitoring.
## Business Value
Automating terrestrial ecology data extraction and analysis using NLP and machine learning accelerates insights from research papers, reports, and satellite imagery, enhancing conservation prioritization by identifying at-risk ecosystems for targeted protection. Predictive analytics optimizes ecosystem restoration by pinpointing degraded areas needing intervention and forecasting restoration outcomes. This automation improves decision-making, reduces manual effort, and enhances conservation efficiency, benefiting policymakers, researchers, and organizations working to mitigate biodiversity loss and climate change impacts.
## General objective
To assess land cover changes and ecosystem health in protected areas by integrating remote sensing techniques and Natural Language Processing (NLP), providing data-driven insights to support conservation efforts and sustainable land-use planning.
### Specific Objectives
1. To develop an integrated analytical framework that combines Natural Language Processing (NLP) techniques and remote sensing indices (NDVI, NDWI, and BSI) for monitoring land cover changes, assessing ecosystem health, and providing actionable insights for conservation and sustainable land-use planning in protected areas.
2. To analyze land cover changes using remote sensing indices such as NDVI, NDWI, and BSI to assess vegetation health, water availability, and soil exposure in protected areas.
3. To apply Natural Language Processing (NLP) techniques to extract, categorize, and analyze conservation-related information from textual data, including research articles, policy documents, and environmental reports.
4. To integrate geospatial analysis and NLP insights to develop a comprehensive framework for monitoring ecosystem health and supporting data-driven decision-making for conservation and sustainable land-use planning.
## Data Understanding
Data sources;

1. [IUCN Biodiversity data](https://www.iucnredlist.org/resources)
2. [PROTECTED PLANET Protected area data WDPA_WDOECM_Feb2025_Public_KEN_csv](https://www.protectedplanet.net/en/searchareassearch_term=KENYA&geo_type=sit)
3. [RCOE-ESA PROJECT](https://rcoe-geoportal.rcmrd.org/)
## Data Collection and Preprocessing
The analysis utilizes multiple data sources, including satellite imagery and textual datasets. Remote sensing data were derived from Sentinel-2 imagery, focusing on generating key environmental indices—Normalized Difference Vegetation Index (NDVI), Normalized Difference Water Index (NDWI), and Bare Soil Index (BSI). These indices were computed using Google Earth Engine (GEE) and Python-based geospatial libraries. Preprocessing steps involved atmospheric correction, cloud masking, and resampling to ensure consistency in spatial resolution.
In parallel, textual data were collected from research articles, policy documents, and conservation reports. This dataset was prepared for NLP tasks through standard text preprocessing techniques, including tokenization, stop-word removal, and lemmatization. These steps were implemented using Python libraries such as NLTK and spaCy. The textual data were then structured for analysis using term frequency-inverse document frequency (TF-IDF) and topic modeling methods.

## Data Analysis
The following libraries have been imported for the purpose of data manipulation, geospatial analysis, and machine learning. Each library is specialized in performing specific tasks, as outlined below:

**Fiona :** A library for reading and writing geographic data formats like shapefiles, GeoJSON, etc. It integrates with other geospatial libraries like geopandas.
**Shapefile (pyshp):** A library for reading and writing shapefiles, a common format for geospatial data.
**Geopandas:** Extends pandas to allow spatial operations on geospatial data, including shapefiles, GeoJSON, and other formats.
**Descartes:** Used for plotting geometries with matplotlib (necessary for visualizing geospatial data).
**Warnings:** To handle and suppress warnings during execution.
### 1. Remote Sensing Analysis
The remote sensing component focused on detecting land cover changes and assessing environmental health over time. The NDVI, NDWI, and BSI indices were calculated from the processed Sentinel-2 imagery. These indices provided critical insights into vegetation health, water body changes, and soil exposure, respectively.
To analyze temporal changes, multi-temporal satellite imagery from different years (e.g., 2008 and 2018) was compared to detect land cover dynamics. A machine learning classification approach was employed using a Random Forest (RF) classifier. This model was trained on extracted features and sample points to categorize land cover into relevant classes (e.g., forest, water bodies, bare soil). The classification model's accuracy was validated using a confusion matrix and performance metrics such as overall accuracy and the Kappa coefficient.
### 2. Natural Language Processing (NLP) Analysis
The NLP component aimed to extract thematic insights from conservation-related texts. Using Python-based NLP libraries, key features were extracted from the textual data using TF-IDF for term weighting and Latent Dirichlet Allocation (LDA) for topic modeling. Sentiment analysis was conducted to assess public opinion and policy sentiment regarding environmental conservation using pre-trained sentiment analysis models.
Named Entity Recognition (NER) was applied to identify significant entities such as organizations, locations, and species from the text corpus. These insights were visualized using word clouds and frequency distributions to highlight dominant themes and stakeholder involvement in conservation initiatives.
### 3. Integration of Remote Sensing and NLP Insights
A critical aspect of this study involved integrating spatial and textual analysis results. The output from the land cover classification and environmental indices was compared with thematic patterns derived from the NLP analysis. This integration helped identify correlations between ecosystem changes and conservation discourse, highlighting areas of concern or success.

The final output consisted of spatial visualizations and thematic maps created using GIS software, combined with textual summaries to provide actionable insights for ecosystem management. The integration of remote sensing and NLP results supported data-driven recommendations for sustainable land use, conservation prioritization, and environmental policy development.

<p align="center">
  <img src="https://github.com/user-attachments/assets/602c0396-00f0-4f50-ae66-a4265396e3ee" width="600"/>
  
  <img src="https://github.com/user-attachments/assets/5be6ab10-75b8-4a93-94b1-2da72da1a4e5" width="600"/>
  
  <img src="https://github.com/user-attachments/assets/f8586c0a-ce0a-44fe-8e15-31e7d5d35ebd" width="600"/>
  <br>
  <img src="https://github.com/user-attachments/assets/b2c1a5e3-8b36-45a0-a9cd-48885877ddaf" width="600"/>
  
  <img src="https://github.com/user-attachments/assets/2f883ab3-bbbb-47af-a298-bf6be5b4fa8e" width="600"/>
  
  <img src="https://github.com/user-attachments/assets/8744cb05-a6b9-4f08-b179-b8d071800df4" width="600"/>
  <br>
  <img src="https://github.com/user-attachments/assets/6bdbfa86-3e01-486f-9ed9-a03661ee0dfa" width="600"/>
  <img src="https://github.com/user-attachments/assets/92060332-64fb-4da7-a4a2-3fdc358702fb" width="600"/>
  <img src="https://github.com/user-attachments/assets/4a2ef3ff-979f-40d5-b778-9b3fef9d99d0" width="600"/>
</p>

## Modeling and Model Evaluation
The effectiveness of the analytical framework was assessed using both quantitative and qualitative methods. The Random Forest model's classification accuracy was evaluated using validation datasets, while NLP outputs were manually reviewed for relevance and coherence. The results were presented through charts, maps, and dashboards to ensure accessibility for decision-makers and conservation stakeholders.
**Baseline Model -** Xgboost Model
XGBoost Classification Report:
              precision    recall  f1-score   support

           0       0.74      0.61      0.67        23
           1       0.75      0.38      0.50         8
           2       1.00      0.50      0.67         4
           3       0.79      0.85      0.82        27
           4       0.60      0.71      0.65        42

    accuracy                           0.69       104
    macro avg       0.78      0.61      0.66       104
    weighted avg       0.71      0.69      0.69       104

**Deep learning Model -** MultiLayer Perceptron Model
<div align="center">
    <img src="https://github.com/user-attachments/assets/b8869099-1227-4457-870e-ac80a0850101" width="600">
</div>

## Conclusions
The analysis conducted in this project produced significant insights into land cover changes, environmental degradation, and ecosystem health by integrating remote sensing indices with natural language processing (NLP) techniques.
### 1. Remote Sensing Analysis
The application of remote sensing techniques using Sentinel-2 imagery provided a comprehensive assessment of land cover changes over time. The Normalized Difference Vegetation Index (NDVI) results indicated areas of declining vegetation cover, highlighting regions experiencing significant land degradation, potentially due to deforestation or unsustainable land-use practices. The NDVI trends revealed hotspots of ecosystem vulnerability, necessitating immediate conservation efforts.
The Normalized Difference Water Index (NDWI) analysis identified changes in water body coverage, detecting seasonal fluctuations and potential water scarcity zones. This finding is critical for monitoring drought-prone regions and informing water resource management. Additionally, the Bare Soil Index (BSI) analysis revealed areas with increasing soil exposure, often correlated with land degradation or urban expansion. High BSI values were predominantly observed in regions where vegetation cover had diminished, suggesting soil erosion risks and declining land productivity.
### 2. Natural Language Processing (NLP) Analysis
The NLP component of the project analyzed textual data from environmental reports, news articles, and scientific publications to extract relevant topics, sentiments, and trends. Sentiment analysis highlighted growing public concern over climate change impacts, deforestation, and water scarcity. Topic modeling revealed dominant themes related to land degradation, conservation policies, and sustainable land-use practices, aligning with the spatial data findings.
### 3. Integrated Insights
By combining spatial and textual data, the project provided a holistic understanding of environmental issues. Areas identified as having high land degradation through NDVI and BSI analysis also frequently appeared in textual data as regions of concern in public discourse and research studies. This alignment between spatial and textual insights strengthens the validity of the findings and underscores the need for targeted interventions in these critical regions.
### 4. Predictive Analysis Outcomes
Preliminary machine learning models applied for land cover classification demonstrated promising accuracy in distinguishing between vegetation, water bodies, and bare soil. The models can be further refined to support automated monitoring systems, enabling faster and more efficient detection of environmental changes.

## Recommendations
**Enhance Monitoring Systems with Automated Tools:** To improve the efficiency and accuracy of environmental monitoring, it is recommended to develop automated systems that integrate remote sensing and machine learning models. Utilizing real-time satellite imagery, these systems can enable faster detection of land cover changes, deforestation, and water body fluctuations. This approach would support timely interventions and resource allocation for conservation efforts.
Strengthen Conservation Policies for Degraded Areas: Regions identified with high NDVI decline and elevated Bare Soil Index (BSI) should be prioritized for conservation initiatives. Policymakers should implement stricter land-use regulations in these vulnerable ecosystems, encourage afforestation projects, and promote sustainable land management practices to restore degraded areas and mitigate the effects of climate change.

**Incorporate NLP-Driven Insights into Environmental Planning:** The application of natural language processing (NLP) revealed significant public and scientific concern regarding climate change, deforestation, and water scarcity. Incorporating these insights into environmental policy-making and awareness campaigns can help ensure that conservation efforts are aligned with societal priorities and ongoing discourse.

**Promote Sustainable Land-Use Practices:** To address soil degradation and erosion risks highlighted by BSI analysis, it is essential to promote sustainable agricultural and urban planning practices. Encouraging crop rotation, controlled grazing, and the use of cover crops can help maintain soil health, while urban planning should focus on minimizing environmental disruption.

**Support Further Research on Predictive Modeling:** Given the promising results from machine learning-based land cover classification, further research should focus on refining these models using larger datasets and incorporating additional environmental variables. Future studies could also explore time-series models for forecasting land cover changes, which would aid in long-term environmental planning.

**Increase Stakeholder Collaboration for Data Sharing:** Encouraging collaboration between governmental bodies, research institutions, and non-governmental organizations can improve data sharing and resource allocation. A centralized ecological data-sharing platform could facilitate real-time monitoring and support coordinated conservation efforts

## Model Deployment
Deploy a scalable ecosystem classification and NLP analysis system, integrating APIs, dashboards, and automated model updates for real-time monitoring and insights.

Deployment link [Streamlit App](https://gmoxmkyrmd5g89gzegdffp.streamlit.app)
## Next Steps
Model monitoring

Collecting more data
