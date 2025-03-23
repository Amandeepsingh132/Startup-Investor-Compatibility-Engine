# InvestMatch AI: Startup-Investor Compatibility Engine 🚀

## Overview
InvestMatch AI is an artificial intelligence platform that analyzes compatibility between startups and potential investors. The system leverages advanced language models through **Google's Gemini API** to calculate a comprehensive **match score** based on multiple compatibility factors, helping founders connect with the most suitable investors for their ventures.

## Features ✨
- **AI-Powered Matching**: Utilizes LLM capabilities to provide nuanced compatibility analysis
- **Multi-Factor Compatibility Assessment**: Evaluates alignment across industry, funding stage, business model, and investment preferences
- **Quantitative Scoring System**: Generates percentage-based compatibility scores
- **Ranked Investor Recommendations**: Organizes potential investors by match quality
- **Customizable Matching Parameters**: Ability to adjust weighting of different matching factors
- **Synthetic Data Generation**: Includes tools for creating test datasets

## How It Works ⚙️
1. **Data Collection & Processing** 📊  
   - **Startup profiles** containing industry, stage, funding needs, traction metrics, and business models
   - **Investor preferences** including target industries, investment ranges, stage focus, and historical investments

2. **Compatibility Analysis** 🎯  
   - Structured prompts are processed by the Gemini API
   - AI evaluates alignment across multiple dimensions
   - Weighted scoring algorithm produces a compatibility percentage

3. **Results Presentation** 📈  
   - Ranked list of potential investors with compatibility scores
   - Detailed breakdown of compatibility factors
   - Visual representation of match quality

## Dataset Structure 🏗️
The system works with two primary data files:

- **`startups.csv`** 🏢  
  - Contains startup profiles with attributes including industry, development stage, funding requirements, traction metrics, and business model
  
- **`investors.csv`** 💰  
  - Includes investor profiles with preferences for industries, investment ranges, stage focus, and investment history

**Example Data:**
```
Startup 1 | Industry: FinTech | Stage: Seed | Funding: $500K | Model: B2B SaaS
Investor 1 | Prefers: FinTech | Range: $100K-$500K | Stage: Seed
```

## Installation & Setup 🛠️
### 1️⃣ Install Required Packages
```bash
pip install pandas google-generativeai matplotlib seaborn
```

### 2️⃣ Configure API Access
Create a configuration file named `config.py` with your API key:
```python
GEMINI_API_KEY = "your_gemini_api_key_here"
```

### 3️⃣ Run the Matching Engine
```python
from investmatch import InvestorMatcher

# Initialize the matching engine
matcher = InvestorMatcher()

# Load data
matcher.load_data('startups.csv', 'investors.csv')

# Calculate matches for a specific startup
matches = matcher.calculate_compatibility(startup_id=1)

# Display ranked results
matcher.display_matches(matches)

# Generate visualization
matcher.visualize_compatibility(matches)
```

## Sample Output 📋
```
=== INVESTMATCH AI RESULTS ===

Startup: FinTech SaaS Platform (Seed Stage)

Rank  Investor             Industry Fit      Stage Fit    Investment Range    Overall Score
---------------------------------------------------------------------------------
1     Techstars VC         Excellent         Ideal        Perfect Match       87%        
2     Fintech Partners     Excellent         Good         Acceptable          72%        
3     Angel Capital Group  Good              Ideal        Perfect Match       68%    
```

## Future Enhancements 🔮
- Integration with investor databases like Crunchbase and PitchBook
- Machine learning model to improve matching based on historical success
- Web interface for interactive use
- API endpoints for integration with other startup tools
