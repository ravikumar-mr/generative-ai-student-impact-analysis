# Generative AI & Student Impact Analysis

An interactive **Power BI data analytics project** exploring how Generative AI usage relates to students' academic performance, skill retention, burnout, wellbeing, and institutional AI policies.

## 📊 Project Overview

Generative AI tools are increasingly being used by students for learning, research, coding, writing, and academic assistance.

This project analyzes **50,000 student records** to explore patterns between AI usage and:

* Academic performance
* GPA change
* Skill retention
* AI dependency
* Exam anxiety
* Burnout risk
* Prompt engineering skills
* Institutional AI policies

The goal is to transform the dataset into an interactive dashboard that helps users explore these relationships from multiple perspectives.

##Dashboard
<img width="1337" height="790" alt="image" src="https://github.com/user-attachments/assets/9b9ec1ee-078d-4bc7-b89d-c31d214c4f02" />
<img width="1346" height="787" alt="image" src="https://github.com/user-attachments/assets/2b866422-495b-49f5-9127-eb7223ed3ac0" />
<img width="1352" height="782" alt="image" src="https://github.com/user-attachments/assets/7e57e1a4-ae82-4d82-98cf-b24d81d61f28" />
<img width="1352" height="792" alt="image" src="https://github.com/user-attachments/assets/819fecce-b9e4-45f8-abc1-7fe3c634c260" />
<img width="1362" height="791" alt="image" src="https://github.com/user-attachments/assets/e8fc7de3-83db-490f-be26-8ba9172a8489" />





## 🎯 Key Questions

The dashboard focuses on four major questions:

1. How does Generative AI usage relate to GPA change?
2. How does AI usage relate to skill retention?
3. How does burnout risk vary across different AI-usage levels?
4. How do different institutional AI policies compare?

## 📌 Dataset

The dataset contains **50,000 student records** with variables covering:

* Student ID
* Major category
* Year of study
* Pre-semester GPA
* Post-semester GPA
* Weekly Generative AI usage
* Primary AI use case
* Prompt engineering skill
* Tool diversity
* Paid AI subscription
* Traditional study hours
* Perceived AI dependency
* Institutional AI policy
* Exam anxiety
* Skill retention score
* Burnout risk level
* GPA change
* AI usage bucket

## 📈 Dashboard Structure

### 🏠 1. Home

The landing page introduces the project and provides navigation to the analytical sections.

Includes:

* Project overview
* Dataset size
* Key questions
* Navigation buttons

### 📊 2. Executive Overview

Provides a high-level summary of the dataset.

Key visuals include:

* Total Students
* Average GPA Change
* Average AI Usage
* High Burnout %
* Average Skill Retention
* AI Usage Distribution
* GPA Change by AI Usage
* Students by Major
* Skill Retention by AI Usage

### 🎓 3. Academic Impact

Focuses on the relationship between Generative AI usage and academic outcomes.

Visuals include:

* AI Hours vs GPA Change
* Prompt Engineering Skill vs GPA Change
* Prompt Engineering Skill vs Skill Retention
* AI Usage vs Skill Retention

### 🧠 4. Burnout & Wellbeing

Explores student wellbeing across different levels of AI usage.

Visuals include:

* High Burnout % by AI Usage
* Burnout Risk Distribution
* Anxiety vs AI Dependency
* AI Usage × Burnout Risk
* Burnout and Skill Retention comparison

### 🏛️ 5. Institutional Policy Comparison

Compares different institutional AI policies using:

* GPA Change
* Skill Retention
* High Burnout %
* Average AI Usage

Policies are compared side-by-side using interactive Power BI visuals.

## 🔢 Key DAX Measures

The dashboard uses a focused set of DAX measures:

```DAX
Total Students =
COUNTROWS('Student_Data')
```

```DAX
Avg GPA Change =
AVERAGE('Student_Data'[GPA_Change])
```

```DAX
Avg AI Hours =
AVERAGE('Student_Data'[Weekly_GenAI_Hours])
```

```DAX
Avg Skill Retention =
AVERAGE('Student_Data'[Skill_Retention_Score])
```

```DAX
High Burnout Students =
CALCULATE(
    COUNTROWS('Student_Data'),
    'Student_Data'[Burnout_Risk_Level] = "High"
)
```

```DAX
High Burnout % =
DIVIDE(
    [High Burnout Students],
    [Total Students],
    0
)
```

```DAX
Avg Anxiety =
AVERAGE('Student_Data'[Anxiety_Level_During_Exams])
```

```DAX
Avg AI Dependency =
AVERAGE('Student_Data'[Perceived_AI_Dependency])
```

## 🎨 Dashboard Design

The dashboard follows a consistent modern BI design system:

* Light neutral background
* White analytical cards
* Blue primary navigation
* Purple academic indicators
* Red/orange wellbeing indicators
* Green low-risk indicators
* Interactive navigation buttons
* Consistent KPI cards and visual hierarchy

## 🛠️ Tools & Technologies

* **Power BI**
* **DAX**
* **Microsoft Excel / CSV**
* **Data Visualization**
* **Data Analysis**

## 📊 Key Analytical Areas

The dashboard enables exploration of:

**AI Usage → Academic Performance → Skill Retention → Wellbeing → Institutional Policy**

Rather than focusing on a single metric, the project provides a multi-dimensional view of Generative AI usage among students.

## 🚀 How to Use

1. Download or clone this repository.
2. Open the `.pbix` file using Power BI Desktop.
3. Navigate through the Home page.
4. Use the available slicers to filter the analysis.
5. Explore the four analytical dashboard pages.

## ⚠️ Data Interpretation

The dashboard presents patterns and relationships observed in the dataset. These results should be interpreted as **dataset-level associations**, not as proof that AI usage directly causes a particular academic or wellbeing outcome.

## 👨‍💻 Author

**Ravi Kumar**

Data Analyst | Business Analytics

### Connect

* LinkedIn: [Ravi Kumar](https://www.linkedin.com/in/ravi-kumar-7b0602310/)
* Portfolio: [theravi.vercel.app](https://theravi.vercel.app/)
* GitHub: [ravikumar-mr](https://github.com/ravikumar-mr)

---

⭐ If you find this project useful, consider giving the repository a star.
