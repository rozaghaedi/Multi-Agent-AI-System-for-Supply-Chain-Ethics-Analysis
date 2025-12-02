# Multi-Agent-AI-System-for-Supply-Chain-Ethics-Analysis
A 7-agent AI system for analyzing forced labour risks in ICT supply chains using the 2025 KnowTheChain benchmark. This system reduces analysis time from 80-120 hours to under 60 seconds.

### 🎯 Project Overview
This project analyzes data from 45 companies across 7 themes and 42 indicators to identify forced labour risks and predict improvements in corporate ethical practices.
27.6 million people are trapped in forced labour globally (ILO 2021). In the ICT sector, 80% of major companies are linked to unresolved forced labour allegations, with an industry average score of only 20/100 on ethical practices.


## Results

**Multi-Agent System Performance and Key Findings**

| Metric | Value | Interpretation |
|--------|-------|----------------|
| **System Performance** |
| Processing Time | <60 seconds | Reduces 80-120 hours of manual analysis |
| Model Accuracy (R²) | 1.00 | Near-perfect prediction of benchmark scores |
| **Benchmark Statistics** |
| Industry Average Score | 20.3/100 | Poor ethical performance overall |
| Top Performing Company | 61/100 | Best score achieved |
| Companies with Allegations | 80% | Linked to unresolved forced labour cases |
| **Regional Disparities** |
| US Companies Average | 23.7/100 | Highest regional performance |
| China Companies Average | 3.0/100 | 20+ point gap from US |
| **Key Correlation** |
| Traceability ↔ Recruitment | r = 0.84 (p<0.001) | Strongest relationship found |
| **Predictive Drivers** |
| Top Driver: Traceability | β = 0.24 | Largest impact on total score |
| Second Driver: Recruitment | β = 0.17 | Second largest impact |

**Key Insight:** Companies with better traceability systems (β = 0.24) tend to have stronger recruitment practices (r = 0.84), indicating these are the most critical areas for improvement in ICT supply chain ethics.



### System Architecture

The system implements a hierarchical multi-agent workflow with three operational stages:


![Multi-Agent System Architecture](flowchart_cover_16x9%20(1).png)

**Stage 1** - Data Acquisition: DataAgent, ResearchAgent, and TextMiningAgent operate in parallel on independent data sources.

**Stage 2** - Statistical & Predictive Analysis: AnalysisAgent processes cleaned data, followed by PredictionAgent for forecasting.

**Stage 3** - Integration & Validation: SynthesisAgent aggregates outputs and generates reports. EthicsAgent validates fairness and bias metrics.

### The Seven Agents


| Agent | Tools | Primary Function |
|-------|-------|------------------|
| DataAgent | 6 | Data loading, cleaning, standardization, company profiling |
| AnalysisAgent | 8 | Statistics, correlations, k-means clustering, regional comparison |
| ResearchAgent | 2 | External validation (ILO, BHRRC), allegation cross-reference |
| PredictionAgent | 6 | Linear regression, scenario forecasting, impact estimation |
| TextMiningAgent | 4 | NLP sentiment analysis, keyword tracking, section extraction |
| EthicsAgent | 3 | Regional bias detection, data quality checks, fairness monitoring |
| SynthesisAgent | 2 | Executive summaries, visualization data preparation |

### Technology Stack

- Google Agent Development Kit (ADK) for orchestration
- pandas and numpy for data processing
- scipy and scikit-learn for statistical analysis
- NLTK for natural language processing (VADER sentiment analysis)
- PyMuPDF for document processing

### Installation

Clone the repository:

```bash

git clone https://github.com/yourusername/Multi-Agent-System-for-Supply-Chain-Ethics.git
cd Multi-Agent-System-for-Supply-Chain-Ethics

```

Create virtual environment and install dependencie

```bash

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

```

Install NLTK data:

```bash

python -c "import nltk; nltk.download('vader_lexicon')"

```

**Usage**

```bash

from multi_agent_system import smart_answer

# Get company profile
result = smart_answer("What is Apple's profile?")
print(result['answer'])

# Compare regional performance
result = smart_answer("Compare regional performance")
print(result['answer'])

# Predict improvement scenarios
result = smart_answer("What if remedy scores improve by 20%?")
print(result['answer'])

# Analyze correlations
result = smart_answer("Show theme correlations")
print(result['answer'])

```

### Dataset
The project uses the 2025 KnowTheChain ICT Benchmark dataset covering 45 companies with 7 themes and 42 indicators. Major firms analyzed include Samsung, Apple, Dell, and Microsoft.
Seven evaluation themes:

1. Commitment & Governance (52 points)
2. Traceability & Risk Assessment (21 points)
3. Purchasing Practices (5 points)
4. Recruitment (20 points)
5. Worker Voice (5 points)
6. Monitoring (15 points)
7. Remedy (7 points)

## Performance

- Processing speed: Under 60 seconds (vs 80-120 hours manually)
- Model accuracy: R² ≈ 1.00 for benchmark score prediction
- Data coverage: 45 companies, 7 themes, 42 indicators
- Parallel processing in Stage 1 enables horizontal scaling

## Research Applications

This system enables:
- Policy impact assessment (e.g., UFLPA, UK Modern Slavery Act)
- Corporate benchmarking across regions and themes
- Risk prediction for high-risk suppliers
- Trend analysis over time
- Bias detection in supply chain practices























