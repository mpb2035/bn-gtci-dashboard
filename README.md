# BN GTCI Dashboard - 2023 vs 2025 Comparison

🚀 **Intelligent Global Talent Competitiveness Index Dashboard for Brunei Darussalam**

## Overview

This is a comprehensive, AI-powered dashboard for analyzing and comparing Global Talent Competitiveness Index (GTCI) indicators between 2023 and 2025. It features an intelligent natural language query system with agentic AI capabilities for self-hosted deployment.

## Features

### 🤖 Agentic AI Capabilities
- **Intelligent Query Engine**: Ask questions in natural language about GTCI data
- **Automated Data Analysis**: Generate reports on improved/declined indicators
- **Smart Filtering**: Multi-dimensional filtering by pillar, status, and data owner
- **Predictive Insights**: Analyze trends across government agencies and data sources

### 📊 Dashboard Features
- **Real-time Data Visualization**: Interactive charts using Chart.js
- **Comprehensive Data Input**: Edit 83+ indicators across 6 pillars
- **Advanced Filtering**: Filter by status, pillar, and search terms
- **Government Agency Mapping**: Track data ownership across Brunei ministries
- **Responsive Design**: Works on desktop, tablet, and mobile devices

### 🔄 Data Pillars
1. **Enable**: Regulatory, market, and business landscapes
2. **Attract**: External and internal openness
3. **Grow**: Formal education, lifelong learning, growth opportunities
4. **Retain**: Sustainability and lifestyle factors
5. **Vocational & Technical Skills**: Mid-level skills and employability
6. **Global Knowledge Skills**: High-level skills and talent impact

## 🚀 Quick Start

### Online Access (GitHub Pages)
Visit: **http://www.mpb-dashboard.com/**

### Local Development
1. Clone the repository
2. Open `index.html` in your web browser
3. No build process or dependencies required!

### Self-Hosting

#### Docker Deployment
```bash
# Build the Docker image
docker build -t bn-gtci-dashboard .

# Run the container
docker run -p 8080:80 bn-gtci-dashboard

# Access at http://localhost:8080
```

#### Node.js/Express Server
```bash
# Install dependencies
npm install

# Start the server
node server.js

# Access at http://localhost:3000
```

#### Static HTTP Server
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx http-server
```

## 📱 Usage Guide

### Intelligent Queries
Try asking:
- "How many indicators improved from 2023 to 2025?"
- "Which ministry manages education indicators?"
- "Show indicators with missing data"
- "List all data sources"
- "Compare 2023 vs 2025 performance"

### Data Entry
1. Unlock the input panel (click 🔓 Unlock)
2. Enter 2023 and 2025 scores for each indicator
3. Add data source and website information
4. Changes update charts and summary automatically

### Filtering & Sorting
- **Search**: Find indicators by code or name
- **Status Filters**: All, Improved, Declined, Missing Data
- **Pillar Select**: Filter by specific pillar
- **Sort**: Click column headers to sort

## 🏗️ Architecture

### Client-Side Stack
- **HTML5**: Semantic markup and responsive layout
- **CSS3**: Modern styling with CSS variables
- **Vanilla JavaScript**: No dependencies for core functionality
- **Chart.js**: Data visualization library
- **Local Storage**: Client-side data persistence

### Key Components

#### 1. Data Model (`detailedIndicators`)
- 83 GTCI indicators with 2023/2025 scores
- Metadata: data owners, sources, government agencies
- Indicator status: new, replaced, code-changed

#### 2. Intelligent Query System
```javascript
// Query Parser
parseQuery(query) // Identifies intent, code, pillar

// Response Generator
generateResponse(parseResult) // Generates contextual responses

// Patterns Supported:
- Indicator scores: "What's the score for 1.1.1?"
- Pillar analysis: "How's the Enable pillar?"
- Trend analysis: "Show improved indicators"
- Missing data: "Which indicators have no 2025 data?"
```

#### 3. Agentic Features
- **Autonomous Insights**: Generate reports without explicit queries
- **Data Validation**: Check data consistency across sources
- **Trend Detection**: Identify patterns and anomalies
- **Ministry Coordination**: Track cross-agency data responsibilities

## 📊 Data Structure

### Indicator Object
```javascript
{
  code: "1.1.1",
  name: "Government effectiveness",
  pillar: "Enable",
  subpillar: "1.1 Regulatory Landscape",
  score2023: 79.14,
  score2025: 80.06,
  dataOwner: "Prime Minister's Office (PMO)",
  source: "World Bank, Worldwide Governance Indicators",
  website: "www.govindicators.org",
  indicatorStatus: null // 'new', 'replaced', 'code-changed'
}
```

## 🔐 Security & Privacy

- **Client-Side Processing**: All data processing happens in your browser
- **No Server Required**: Static HTML/CSS/JS deployment
- **Local Storage**: Data stored locally, not transmitted
- **HTTPS Ready**: Can be deployed on HTTPS servers

## 🌐 Deployment Options

### Option 1: GitHub Pages (Recommended)
- Already configured and live at: http://www.mpb-dashboard.com/
- Free hosting, automatic HTTPS
- Edit `index.html` to push updates instantly

### Option 2: Traditional Web Server
- Copy files to any web server (Apache, Nginx, IIS)
- No special configuration needed
- Supports custom domain

### Option 3: Containerized Deployment
- Docker support included
- Kubernetes-ready
- Cloud platform compatible (AWS, GCP, Azure)

### Option 4: Local/Intranet
- Python HTTP server
- Node.js Express server
- Perfect for Brunei government intranet deployment

## 💾 Data Persistence

The dashboard uses Browser Local Storage to persist user edits:
```javascript
// Data is automatically saved when you modify inputs
localStorage.setItem('gtci-dashboard', JSON.stringify(indicators));

// Clear local data
localStorage.removeItem('gtci-dashboard');
```

## 📈 API Integration (Future)

Ready for external data source integration:
```javascript
// Example: Fetch real-time data from government sources
async function fetchIndicatorData(code) {
  const response = await fetch(`/api/indicators/${code}`);
  return response.json();
}
```

## 📞 Support & Contact

- **Data Issues**: Contact relevant ministry (listed in dataOwner field)
- **Technical Support**: Create an issue in the repository
- **Feature Requests**: Suggest improvements via GitHub Issues

## 📜 License

Public repository for Brunei government GTCI data analysis.

## 🙌 Acknowledgments

- **World Economic Forum**: Global Talent Competitiveness Index framework
- **Data Sources**: World Bank, UNESCO, ILO, OECD, and partner organizations
- **Brunei Agencies**: All participating government departments and ministries

---

**Last Updated**: December 2025
**Version**: 2.0 (AI-Enhanced)
**Status**: Production Ready ✅
