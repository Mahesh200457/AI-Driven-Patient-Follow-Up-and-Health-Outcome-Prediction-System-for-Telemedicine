# 🩺 Clinical Data Analytics Dashboard

An interactive web-based dashboard for analyzing clinical data, assessing patient risk based on symptoms, and scheduling consultations via Google Calendar integration. Built using **Dash**, **Plotly**, and **Google API**.

---

---



### 🔹 Dashboard Overview  
![Dashboard Main](https://github.com/Mahesh200457/Doctor-Patient-Dashboard/blob/main/Screenshot%20(98).png?raw=true)

### 🔹 Symptom & Disease Visualization  
![Charts](https://github.com/Mahesh200457/Doctor-Patient-Dashboard/blob/main/Screenshot%20(99).png)

### 🔹 High-Risk Filter & Appointment UI  
![Symptom Filter](https://github.com/Mahesh200457/Doctor-Patient-Dashboard/blob/main/Screenshot%20(100).png?raw=true)

### 🔹 Calendar Appointment Confirmation  
![Google Calendar](https://github.com/Mahesh200457/Doctor-Patient-Dashboard/blob/main/Screenshot%20(101).png?raw=true)

---

## 🧠 How It Works

1. User selects a **symptom category** and then filters by specific symptoms.
2. App displays **high-risk patients** who match all selected symptoms.
3. User selects a **date**, clicks **Schedule Appointment**, and the app:
   - Sends patient data to Google Calendar
   - Creates a consultation event from 10:00 AM to 10:30 AM for each match

---



## 🚀 Features

- 🔍 **Symptom-Based Risk Assessment**
- 📊 **Interactive Data Visualizations**
- 🧠 **High-Risk Patient Identification**
- 📅 **Google Calendar Appointment Scheduling**
- ☁️ **Word Cloud of Most Common Symptoms**

---

## 📦 Tech Stack

| Technology | Purpose |
|------------|---------|
| **Dash (Plotly)** | Web app & layout |
| **Dash Bootstrap Components** | UI styling |
| **Pandas** | Data processing |
| **Plotly Express** | Interactive visualizations |
| **Google Calendar API** | Appointment scheduling |
| **WordCloud & Base64** | Word cloud image generation |

---

## 📁 Data Structure

The data is loaded from a serialized `.pkl` file and contains:
- `symptoms` (List[str])
- `diseases` (List[str])
- `age` (int/float)
- `gender` (str)
- `serial_number` (str)
- `data` (Text summary)

---

## 📊 Dashboard Tabs

### 1. **Symptoms Analysis**
- 📌 Treemap of symptom distribution
- ☁️ Word Cloud of common symptoms

### 2. **Disease Analysis**
- 🌞 Sunburst chart of disease frequencies

### 3. **Demographics**
- 🧑‍⚕️ Gender vs Age scatter plot
- 📈 Violin plot for age distribution

---

## 🧠 Risk Assessment Workflow

1. Select a **symptom category** (e.g., Respiratory, Gastrointestinal).
2. Choose one or more **symptoms**.
3. The system filters and displays **high-risk patients**.
4. Optional: Select a date and click **Schedule Meeting** to automatically:
   - Schedule consultations in your Google Calendar.
   - Each event includes the patient ID and summary.

---

## 🔐 Google Calendar Integration

The app uses **OAuth 2.0** to authenticate Google Calendar API:
- Requires `client_secret.json` and stores `token.json` after login.
- Schedules meetings for filtered patients at 10:00 AM on the selected date.

> 📌 Note: API access must be enabled in your Google Cloud Project.

---
## ▶️ Run the App Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Mahesh200457/Doctor-Patient-Dashboard.git
cd Doctor-Patient-Dashboard

## 🧪 Installation & Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/clinical-dashboard.git
   cd clinical-dashboard
