# Friendship Formation Across Life Stages: A Comparative Study

A comprehensive social network analysis examining how friendships form across different educational stages, from primary school through university.

## Project Overview

This research project investigates the dynamics of friendship formation across four distinct educational stages:
- **Primary School** (ages 6-12)
- **Middle School** (ages 11-13)  
- **High School** (ages 15-18)
- **University** (ages 18-22)

### Research Questions
- How do different factors (age, gender, behavior) influence friendship formation at various life stages?
- What are the differences between wireless sensor data and survey-based data collection methods?
- Do consistent patterns emerge across different educational contexts?

## Team
University of Bologna, Alma MAter Studiorum - Artificial Intelligence MSc

- Guglielmo Biagini 
- Elisa Castagnari
- Matteo Fusconi
- Luca Trambaiollo

## Datasets

We analyzed four publicly available datasets, each representing a different educational stage:

| Stage | Source | Method | Nodes | Edges | Metadata |
|-------|--------|--------|-------|-------|----------|
| Primary School | French school (2009) | RFID sensors | 21 | 45 | Sex |
| Middle School | Dutch class (2003-2004) | Survey | 26 | 33-117* | Sex, Age, Religion, Alcohol, Delinquency |
| High School | French classes préparatoires | RFID sensors | 28 | 73 | Sex |
| University | Groningen Sociology (1996-1997) | Survey | 23 | 36-147* | Sex, Age, Smoking, Drugs, Religion, Associations |

*Undirected-Directed graph variations

### Data Collection Methods Compared

**RFID/Wireless Sensors:**
- Objective, unsupervised proximity detection
- Large-scale data collection
- Limited contextual information
- Requires threshold selection (we used 5-minute minimum contact duration)

**Questionnaire Surveys:**
- Rich metadata (behaviors, preferences, characteristics)
- Captures meaningful relationships
- Potential recall bias
- Smaller sample sizes


## Methodology & Measures

### Network Analysis Techniques

We implemented comprehensive social network analysis using **NetworkX** (Python), examining:

#### 1. Homophily Analysis
Measured tendency for individuals to befriend similar others using assortativity coefficient:
- Sexual homophily: **0.62-0.63** (Middle School & University) - strong same-gender clustering
- Age homophily: **0.83** (University) - students befriend same-age peers
- Behavioral factors (smoking, drugs): **~0** - minimal influence

#### 2. Centrality Measures
- **Degree Centrality**: Identified most popular individuals
- **In-Degree/Out-Degree**: Analyzed friendship reciprocity (directed graphs)

#### 3. Transitivity (Clustering Coefficient)
- Primary: 0.39
- Middle School: 0.38
- High School: 0.40
- **University: 0.46** (higher clustering, more cohesive groups)

#### 4. K-Cores Analysis
Identified tightly-knit subgroups within each network.

#### 5. Reciprocity (Directed Graphs)
- Middle School: **0.76**
- University: **0.49** - approximately 50% of friendships are non-reciprocal


## Key Findings

1. **Gender is the strongest predictor** of friendship formation across all life stages
   - Consistent same-gender clustering (homophily 0.62-0.63)
   - Less pronounced in wireless datasets due to higher connectivity

2. **Age matters more in university** than earlier stages
   - University students cluster by age groups (homophily 0.83)
   - Life experiences and shared schedules drive connections

3. **Behavioral factors (smoking, drugs) have minimal influence**
   - Low assortativity (~0) for substance use
   - School association involvement helps create connections but with lower reciprocity

4. **Transitivity increases with age**
   - University shows highest clustering (0.46)
   - More dynamic, resourceful social behavior in older students

5. **Friendship reciprocity varies significantly**
   - Only ~50% of university friendships are mutual
   - Could reflect survey bias OR genuine asymmetric relationships

6. **Data collection method matters**
   - Wireless: More connections, less structure, fewer metadata
   - Surveys: Richer context, potential recall bias

## Technologies Used

- **Python 3.x** - Primary programming language
- **NetworkX** - Social network analysis and graph algorithms
- **NumPy/Pandas** - Data manipulation
- **Matplotlib** - Visualization
- **LaTeX** - Academic paper formatting

## Implications & Future Work

- **Educational Policy**: Understanding social dynamics can inform classroom organization and intervention strategies
- **Disease Modeling**: RFID contact networks applicable to epidemic spread analysis
- **Social Psychology**: Insights into developmental changes in friendship formation

### Limitations & Future Directions
- **Longitudinal analysis**: Track how friendships evolve over academic years
- **Cross-cultural comparison**: Datasets from diverse geographical/cultural contexts
- **Personality traits**: Incorporate psychological assessments (cheerfulness, resourcefulness)
- **Standardized metadata**: Develop consistent feature collection across all life stages
- **Generational shifts**: Compare historical data with contemporary patterns (e.g., earlier smoking initiation)

