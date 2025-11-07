# 🧠 HOSi: Human Operating System Index

> *Quantifying Coherence for Human Regulation in the Age of AI*  
> Developed by **Christopher Salvador Ponce** & collaborators  
> Website: [https://humanosindex.org](https://humanosindex.org)

---

### 🪶 Overview

**HOSi (Human Operating System Index)** is a multidimensional framework and web application that helps individuals, teams, and researchers measure and improve *human coherence*—a state of balanced functioning across seven key dimensions of human regulation:

1. **Self-Awareness** (GABA / Cognitive Regulation)  
2. **Connection** (Oxytocin / Social Bonding)  
3. **Purpose** (Dopamine / Motivation & Flow)  
4. **Health** (Cortisol / Physical Regulation)  
5. **Belief** (Serotonin / Existential Resilience)  
6. **Joy** (Endorphins / Creative Energy)  
7. **Stability** (Adrenaline / Grounding)

Built at the intersection of neuroscience, systems thinking, and spiritual psychology, **HOSi** provides users with:
- A scientifically grounded self-assessment,
- Personalized micro-interventions,
- Real-time coherence analytics, and
- A research-backed path to neurochemical and energetic balance.

---

## 📖 Reference: The HOSi White Paper

**The Human Operating System Index (HOSi): Quantifying Coherence for Human Regulation in the Age of AI**  
By **Christopher Salvador Ponce**  
Collaborators:  
- Dr. Robert Gutzwiller — *Human Systems Engineering, ASU*  
- Bob Beard — *Center for Science and the Imagination, ASU*  
- Shawn Banzhaf, MA — *Pat Tillman Veterans Center, ASU*  
- Wanda Wright — *Office for Veteran and Military Academic Engagement, ASU*  
- Pearla White — *MS Psychology Candidate, ASU*  

> **Abstract:**  
> This paper introduces the Human Operating System Index (HOSi)—a replicable framework for quantifying human coherence across neurochemical and energetic dimensions. Built at the intersection of neuroscience, systems thinking, and spirituality, HOSi operationalizes self-regulation as the prerequisite for ethical and creative leadership in the age of AI.  
>  
> It posits that before optimizing artificial intelligence, humanity must optimize human intelligence—achieving neurochemical balance, energetic alignment, and systemic coherence. Using seven measurable dimensions—Self-Awareness, Connection, Purpose, Health, Belief, Joy, and Stability—HOSi generates a Coherence Score that visualizes the state of an individual’s system. Early results from the prototype assessment suggest this model can help identify “energy leaks,” predict burnout risk, and support leadership development across sectors.

📄 **Read the full white paper:** [https://humanosindex.org](https://humanosindex.org)

---

## ⚙️ Repository Structure

<details>
<summary>📂 Expand Repository Overview</summary>

### 1. **Core Entities (Data Models)**
These JSON/TypeScript models define the backbone of HOSi’s data schema:

| Entity | Description |
|---------|-------------|
| **Assessment** | Stores user assessment results, dimension scores, reflections, and opt-in research data. |
| **Intervention** | Manages micro-interventions for improving target dimensions and tracks streaks. |
| **CheckIn** | Daily/weekly self-tracking for interventions with mood and completion status. |
| **Team** | Defines team info, invite codes, and admin settings. |
| **TeamMembership** | Links users to teams with role and data-consent flags. |
| **Achievement** | Tracks earned badges and milestones. |
| **UserStats** | Aggregated XP, level, and progress metrics. |
| **LearningResource** | Curated educational content mapped to specific dimensions. |
| **LearningPath** | Structured paths combining multiple learning resources. |
| **LearningProgress** | Monitors user advancement through resources or paths. |
| **User** | Base user entity extended with demographic and personalization data. |

---

### 2. **Frontend Pages (UI Routes)**
Each page corresponds to a React route under `/pages`:

| Page | Function |
|------|-----------|
| **Home** | Introductory overview and CTA to take assessment. |
| **Assessment** | 7-dimension questionnaire with live progress and reflections. |
| **MyResults** | Radar charts, trend analytics, gamified stats, and sharing options. |
| **Interventions** | Hub for personalized actions and micro-interventions. |
| **Teams / TeamDashboard** | Collective coherence visualization for organizations. |
| **Research** | Aggregated, anonymized data with insights and methodology. |
| **About** | Scientific and philosophical foundation of the HOSi model. |
| **Profile** | Manage account, demographics, and data consent. |
| **Learning** | Discover and follow learning paths. |
| **AdminDashboard** | Admin-only portal for research exports and analytics. |
| **SharedResults / SharedCoachInsights** | Public, read-only links for shared content. |

---

### 3. **UI Components**
Modular, reusable components built with React + Tailwind CSS.

| Category | Components |
|-----------|-------------|
| **Assessment UI** | `QuestionSlider`, `PrivacyConsent`, `CoachModal` |
| **Visualization** | `RadarChart`, `DimensionHeatmap`, `TrendForecast`, `ComparativeAnalytics` |
| **Results & Dimensions** | `DimensionCard`, `DimensionExplainer`, `ResultsPanel`, `PrintableReport` |
| **Gamification** | `BadgeCard`, `LevelProgress` |
| **Learning** | `ResourceCard`, `LearningPathCard` |
| **Forms** | `DemographicsForm` |

---

### 4. **Backend Functions**
Serverless functions for secure processing and analytics:

- `getResearchAggregates()` → Aggregates anonymized assessment data for research dashboards.  
- *(Future modules)*: `saveAssessment`, `generateReportPDF`, `suggestIntervention`, `logCoachConversation`.

---

### 5. **AI Agents**
Located in `/agents/`.

| Agent | Purpose |
|--------|----------|
| **hosi_coach.json** | Core multi-role AI agent that guides assessment, interprets trends, and suggests interventions. |

---

### 6. **Layout**
Defined in `AppLayout.tsx`:
- Global header, mobile nav, footer  
- Light/dark theme toggle  
- Context providers for auth/session state

</details>

---

## 🧩 Tech Stack

| Layer | Tools |
|-------|-------|
| **Frontend** | React + TypeScript + Tailwind CSS |
| **Backend** | Serverless (Vercel / Supabase / Firebase Functions) |
| **Database** | JSON / Firestore / Supabase tables aligned with data models |
| **Visualization** | Chart.js / Recharts for radar and trend visualizations |
| **AI Layer** | Modular JSON-configured agents with explainable outputs |
| **CI/CD** | GitHub Actions → Vercel or Cloud Run Deployment |

---

## 🧬 Theoretical Foundation

HOSi conceptualizes the *Human Operating System* as a tri-layer model:

- **Biological Hardware:** brain, body, and sensory network  
- **Cognitive Software:** thoughts, emotions, and behavioral patterns  
- **Spiritual Network:** meaning, connection, and collective consciousness  

Each of the seven coherence dimensions maps to a **primary neurochemical** axis and **core human function**, enabling the quantification of inner balance and “energy leaks.”

---

## 🧑‍🔬 Research & Validation

HOSi’s interdisciplinary validation is supported by collaborators at **Arizona State University**:

| Contributor | Role |
|--------------|------|
| Dr. Robert Gutzwiller | Human Systems Engineering, HCI & methodology |
| Bob Beard | Narrative design & leadership storytelling |
| Shawn Banzhaf, MA | Veteran resilience & purpose recovery |
| Wanda Wright, MPA | Systems change & academic engagement |
| Pearla White, MS Candidate | Neuropsychology & statistical validation |

### Pilot Study Goals
- Collect anonymous HOSi data from 200+ participants  
- Test internal consistency (Cronbach’s α) and inter-dimension correlations  
- Evaluate pre/post micro-intervention effects  
- Thematically code qualitative reflections  

---

## 🧘 Applications

| Domain | Application |
|--------|--------------|
| **Individuals** | Personal reflection, coherence mapping, and micro-interventions |
| **Teams** | Organizational alignment and burnout risk analysis |
| **Researchers** | Data for cross-domain coherence studies |
| **AI Ethics** | Modeling “Human-AI Coherence Systems” grounded in human regulation |

---

## 🔮 Future Directions
- Integrate physiological measures (HRV, sleep, cortisol)  
- Expand to mobile with offline micro-intervention logging  
- Build open research APIs for cross-lab collaboration  
- Train coherence-based recommendation models for leadership development  

---

## 🧾 Citation

If referencing HOSi in research or publications:

> Ponce, C. S., Gutzwiller, R., Beard, B., Banzhaf, S., Wright, W., & White, P. (2025). *The Human Operating System Index (HOSi): Quantifying Coherence for Human Regulation in the Age of AI.* Arizona State University. Retrieved from [https://humanosindex.org](https://humanosindex.org)

---

## 🪴 License
© 2025 HOSi Project Team. All rights reserved.  
Licensed for research and educational use under an open science agreement (non-commercial distribution only).

---

## 💡 Acknowledgment
> “Before optimizing machines, we must regulate humans.  
> Dysregulated humans build dysregulated systems.”  
> — *Christopher Salvador Ponce, HOSi White Paper (2025)*

---
