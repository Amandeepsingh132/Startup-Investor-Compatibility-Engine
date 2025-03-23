# Founder-Investor Matching AI Model 🚀


## Overview
This project is an AI-powered **Founder-Investor Matching System** that helps startup founders find the most compatible investors based on industry, funding stage, and business model. Using **Google's Gemini API**, the model calculates a **match score** between founders and investors to rank the best investment opportunities.

## Features ✨
- **Gemini API Integration**: Uses LLM-based analysis for investor-founder compatibility.
- **Structured Matching Process**: Compares startup traits with investor preferences.
- **Match Score Calculation**: Returns a ranked list of investors based on compatibility.
- **Custom Dataset Creation**: Synthetic data generated for founders and investors.
- **CSV-Based Data Handling**: Loads and processes structured startup and investor data.

## How It Works ⚙️
1. **Load Startup & Investor Data** 📊  
   - Founders provide details like **industry, stage, funding required, traction, and business model**.  
   - Investors specify their **preferred industries, investment range, and key focus areas**.

2. **Match Score Calculation** 🎯  
   - A structured **prompt** is sent to Gemini API, analyzing alignment between founder & investor profiles.
   - The API returns a **compatibility score (0-100)** based on key factors.

3. **Ranked Output** 📈  
   - A sorted list of investors is generated, ranked by compatibility.
   - Displayed in a structured format.

## Dataset Creation 🏗️
Since no predefined dataset was available, I **generated synthetic data** for testing. The dataset consists of:

- **`founders.csv`** 🏢  
  - 5 startup founders with attributes like **industry, stage, funding required, traction, and business model**.
  
- **`investors.csv`** 💰  
  - 5 investors with preferences such as **preferred industries, investment range, key focus areas, and previous investments**.

**Example Data Snippet:**
```
Founder 1 | Industry: FinTech | Stage: Seed | Funding: $500K | Model: B2B SaaS
Investor 1 | Prefers: FinTech | Range: $100K-$500K | Stage: Seed
```

## Installation & Usage 🛠️
### 1️⃣ Install Dependencies
```bash
pip install pandas google-generativeai
```
### 2️⃣ Set Up API Key (Gemini API)
Replace `API_KEY` with your actual Gemini API key:
```python
API_KEY = "your_gemini_api_key_here"
```

### 3️⃣ Run the Matching Model
```python
matcher = FounderInvestorMatcher(API_KEY)
matcher.load_data('founders.csv', 'investors.csv')
matches = matcher.calculate_match_score(founder_id=1)
matcher.display_matches(matches)
```

## Output Format 📋
```
# Founder-Investor Matching AI Model 🚀

## Overview
This project is an AI-powered **Founder-Investor Matching System** that helps startup founders find the most compatible investors based on industry, funding stage, and business model. Using **Google's Gemini API**, the model calculates a **match score** between founders and investors to rank the best investment opportunities.

## Features ✨
- **Gemini API Integration**: Uses LLM-based analysis for investor-founder compatibility.
- **Structured Matching Process**: Compares startup traits with investor preferences.
- **Match Score Calculation**: Returns a ranked list of investors based on compatibility.
- **Custom Dataset Creation**: Synthetic data generated for founders and investors.
- **CSV-Based Data Handling**: Loads and processes structured startup and investor data.

## How It Works ⚙️
1. **Load Startup & Investor Data** 📊  
   - Founders provide details like **industry, stage, funding required, traction, and business model**.  
   - Investors specify their **preferred industries, investment range, and key focus areas**.

2. **Match Score Calculation** 🎯  
   - A structured **prompt** is sent to Gemini API, analyzing alignment between founder & investor profiles.
   - The API returns a **compatibility score (0-100)** based on key factors.

3. **Ranked Output** 📈  
   - A sorted list of investors is generated, ranked by compatibility.
   - Displayed in a structured format.

## Dataset Creation 🏗️
Since no predefined dataset was available, I **generated synthetic data** for testing. The dataset consists of:

- **`founders.csv`** 🏢  
  - 5 startup founders with attributes like **industry, stage, funding required, traction, and business model**.
  
- **`investors.csv`** 💰  
  - 5 investors with preferences such as **preferred industries, investment range, key focus areas, and previous investments**.

**Example Data Snippet:**
```
Founder 1 | Industry: FinTech | Stage: Seed | Funding: $500K | Model: B2B SaaS
Investor 1 | Prefers: FinTech | Range: $100K-$500K | Stage: Seed
```

## Installation & Usage 🛠️
### 1️⃣ Install Dependencies
```bash
pip install pandas google-generativeai
```
### 2️⃣ Set Up API Key (Gemini API)
Replace `API_KEY` with your actual Gemini API key:
```python
API_KEY = "your_gemini_api_key_here"
```

### 3️⃣ Run the Matching Model
```python
matcher = FounderInvestorMatcher(API_KEY)
matcher.load_data('founders.csv', 'investors.csv')
matches = matcher.calculate_match_score(founder_id=1)
matcher.display_matches(matches)
```

## Output Format 📋
```
=== FOUNDER-INVESTOR MATCHES ===

Rank  Investor             Industry             Stage           Match Score
----------------------------------------------------------------------
1     Investor 2           FinTech              Seed            65        
2     Investor 3           FinTech              Series B        35        
3     Investor 1           EdTech               Series B        30  

```
