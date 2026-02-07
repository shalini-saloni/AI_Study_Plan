# SmartStudy AI - Engineering Study Planner

> An AI-powered study planner specifically designed for engineering students to study smarter, not harder.


## Demo Video

**[Watch the Full Demo Video Here](YOUR_DEMO_VIDEO_LINK)**

https://user-images.githubusercontent.com/yourusername/demo.mp4


## Problem Statement

Engineering students struggle to efficiently allocate limited study time across complex subjects while maintaining consistent progress, meeting deadlines, and achieving deep conceptual understanding.

### Key Challenges:
- **Cognitive Load Imbalance** - Different subjects demand different mental effort levels
- **Prerequisite Dependencies** - Foundational gaps block progress in advanced topics
- **Dynamic Prioritization** - Shifting deadlines and unexpected difficulties
- **Inefficient Study Patterns** - Cramming leads to poor retention and high stress
- **Lack of Personalization** - Generic tools don't adapt to individual needs

## Solution

SmartStudy AI is an intelligent study planner that:

Analyzes subjects, deadlines, prerequisites, and cognitive load  
Creates personalized, adaptive study schedules  
Balances deep learning with timely completion  
Evolves dynamically as priorities and performance change  

## Key Features

### 1. AI-Powered Scheduling Algorithm
- **Smart Time Allocation**: Credits, confidence levels, and difficulty weighted
- **Cognitive Load Optimization**: High-focus topics scheduled during peak hours
- **Prerequisite-Aware**: Weak areas and foundations prioritized early
- **Adaptive Rebalancing**: Schedule adjusts based on progress

### 2. Visual, Actionable Schedules
- **Color-Coded Calendar**: High/Medium/Low cognitive load indicators
- **2-Week Planning View**: Clear daily breakdown with time blocks
- **Subject-Wise Allocation**: Percentage and hour-based distribution
- **Progress Tracking**: Weekly confidence checkpoints

### 3. Intelligent Insights
- Priority focus recommendations
- Prerequisite gap identification
- Study pattern optimization
- Buffer time for unexpected challenges

### 4. User-Friendly Interface
- Clean, modern design with dark theme
- Intuitive form inputs
- Real-time validation
- Mobile-responsive layout

## Tech Stack

- **Frontend**: React (via CDN), HTML5, CSS3
- **Styling**: Custom CSS with modern gradients and animations
- **Fonts**: Google Fonts (Outfit, JetBrains Mono)
- **Algorithm**: Custom JavaScript scheduling engine
- **Hosting**: GitHub Pages / Netlify / Vercel

## Installation & Setup

### Option 1: Direct Usage (No Installation)
Simply open `index.html` in any modern browser:

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-study-planner.git

# Navigate to project folder
cd ai-study-planner

# Open in browser
open index.html  # macOS
start index.html # Windows
xdg-open index.html # Linux
```

### Option 2: Local Development Server

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server

# Then open http://localhost:8000
```

### Option 3: Deploy to GitHub Pages

1. Fork this repository
2. Go to Settings → Pages
3. Select main branch
4. Your site will be live at `https://yourusername.github.io/ai-study-planner`

## Usage Guide

### Step 1: Enter Student Details
- Name, College, Branch, Year, Email
- **Name is required**

### Step 2: Add Subjects
- Subject name and credits
- Strong areas (comma-separated)
- Weak areas (comma-separated)
- Confidence level (1-5 slider)
- Add multiple subjects using "+ Add Another Subject"
- **At least one subject name is required**

### Step 3: Configure Study Time
- Weekday hours per day (default: 3, minimum: 1)
- Weekend hours per day (default: 6, minimum: 1)
- Preferred study time (Morning/Afternoon/Evening/Night)
- **Target completion date (REQUIRED - must be future date)**

### Step 4: Generate Plan
Click "🚀 Generate My Study Plan" to get:
- Personalized 2-week schedule
- Subject-wise time allocation
- AI-powered insights and recommendations
- Cognitive load-optimized study blocks

### Important Notes
- **Target date MUST be in the future** (not today or past)
- **Fill in at least the subject name** for each subject
- The more details you provide (strong/weak areas), the better the recommendations
- If you see zeros (0 hours, 0 days), check that your target date is set correctly

## Troubleshooting

### "Showing 0 Total Study Hours"
**Cause**: Target date is not set or is in the past  
**Solution**: 
1. Make sure you selected a target date
2. Ensure the date is in the FUTURE (not today or yesterday)
3. Try selecting a date at least 1 week from today

### "0 Days to Target"
**Cause**: Same as above - target date issue  
**Solution**: Select a future date (e.g., 2 weeks or 1 month from today)

### "Schedule shows nothing / No study blocks"
**Cause**: Subject names not filled in  
**Solution**: 
1. Make sure each subject has a NAME entered
2. Add at least 2 subjects for best results
3. Fill in weak areas for better scheduling

### "AI Insights not clear"
**Cause**: Missing subject details  
**Solution**: 
1. Fill in strong and weak areas for each subject
2. Set realistic confidence levels (1-5)
3. The more information you provide, the better the insights

### "Can't generate plan"
**Checklist**:
- [ ] Name is filled in
- [ ] Target date is selected AND in the future
- [ ] At least one subject has a name
- [ ] Study hours are at least 1 hour per day
- [ ] Using a modern browser (Chrome, Firefox, Safari, Edge)

### Still Having Issues?
1. Try the sample data in QUICKSTART.md
2. Check browser console (F12) for errors
3. Refresh the page and try again
4. Make sure JavaScript is enabled
5. Use a recent browser version

## Algorithm Explanation

### Time Allocation Formula

```javascript
weight = creditWeight × (0.4 + confidenceWeight × 0.3 + difficultyWeight × 0.3)
```

Where:
- `creditWeight` = subject credits / total credits
- `confidenceWeight` = (6 - confidence) / 5
- `difficultyWeight` = 1.2 if weak areas exist, else 1.0

### Scheduling Logic

1. **Phase 1 (Week 1)**: Focus on weak areas and low-confidence subjects
2. **Phase 2 (Week 2+)**: Balanced practice and revision
3. **Cognitive Load Distribution**:
   - High-load: Confidence ≤ 2 (weak subjects)
   - Medium-load: Confidence = 3
   - Low-load: Confidence ≥ 4 (strong subjects)

### Smart Prioritization

- Weak topics scheduled first
- High-focus work during preferred study times
- Light revision in low-energy slots
- Buffer time for spillovers

## Sample Input/Output

### Input Example:
```
Student: Aman
Subjects:
  - Data Structures (4 credits, Confidence: 3/5)
    Strong: Arrays, Linked Lists
    Weak: Trees, Graphs
  
  - Operating Systems (3 credits, Confidence: 2/5)
    Strong: Processes, Threads
    Weak: Deadlocks, Memory Management

Study Time: 3h weekday, 6h weekend
Target: March 15, 2026
```

### Output Includes:
- **Stats**: 126 total hours, 42 days, 2 subjects
- **Allocation**: DS (55%), OS (45%)
- **2-Week Schedule**: Color-coded daily blocks
- **AI Insights**: 5 personalized recommendations

## Why This Solution Wins

### 1. Impact (20%) 
- Generates personalized plan in under 2 minutes
- Realistic, actionable schedules
- Addresses real engineering student pain points

### 2. Innovation (20%) 
- Unique cognitive load-based scheduling
- Prerequisite-aware time allocation
- Adaptive algorithm that evolves with progress

### 3. Technical Execution (20%) 
- Clean, modular code structure
- Efficient scheduling algorithm
- Comprehensive documentation
- Production-ready quality

### 4. User Experience (25%) 
- Intuitive input flow
- Clear visual outputs
- Beautiful, modern UI
- Mobile-responsive design
- **Hosted solution** for easy access

