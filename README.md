# 🏙️ Smart City Transportation Network Optimization - Greater Cairo

This repository contains the implementation of the Smart City Transportation Network Optimization Project , designed for the Greater Cairo metropolitan area Developed for the Design and Analysis of Algorithms course (CSE112) at Alamein International University (AIU) , this comprehensive system integrates graph theory, dynamic programming, greedy approaches, and machine learning to solve real-world urban transportation challenges.

---

## 🌟 Key Features

### 1. Infrastructure Network Design
* **Minimum Spanning Tree (MST):** Utilizes Kruskal's or Prim's algorithm to compute a cost-efficient road network.
* **Strategic Connectivity:** Prioritizes vital connections between high-population residential zones and critical infrastructure, such as hospitals and government centers.

### 2. Traffic Flow & Route Optimization
* **Smart Navigation:** Implements Dijkstra's algorithm for accurate route planning across Cairo's 25 nodes, which includes 15 neighborhoods and 10 facilities.
* **Context-Aware Routing:** Customizes standard Dijkstra's by implementing time-varying weights (adjusting for morning/evening rush hours) and applying penalties for poor road conditions.
* **Performance Optimization:** Employs memoization techniques to cache repeated route queries, improving search speeds to O(1).

### 3. Emergency Response Planning
* **Priority Ambulance Routing:** Deploys the A* search algorithm for rapid emergency vehicle routing.
* **Targeted Focus:** Uses GPS coordinates as a heuristic to guide the search directly toward medical facilities like Qasr El Aini and Maadi Military Hospitals.
* **Traffic Bypass:** Emergency routes are calculated using raw distance metrics, completely ignoring congestion factors and road condition penalties to find the absolute fastest physical route.

### 4. Public Transit & Resource Allocation
* **Transit Scheduling:** Applies Dynamic Programming (DP) to optimize operating schedules across public transportation vehicles like metro and bus lines.
* **Maintenance Budgeting:** Uses DP to dynamically allocate resources for road maintenance in areas with poor road conditions.
* **Intersection Management:** Implements a greedy approach for real-time traffic signal optimization at major Cairo intersections and emergency vehicle preemption during high congestion periods.

### 5. AI Integration & Visual Analytics
* **Traffic Forecasting:** Uses ML-based traffic prediction (scikit-learn or TensorFlow) trained on the provided temporal traffic data to forecast congestion.
* **Algorithm Racing UI:** Features a side-by-side algorithm comparison visualizer (e.g., Dijkstra vs A* race animation).

---

## 📊 Dataset Overview

The system is powered by a custom dataset mapping the intricacies of Greater Cairo:
* **Geographic Nodes:** Coordinates, types, and population data for 15 districts (e.g., New Cairo, Shubra, Giza) and 10 key facilities (e.g., Cairo International Airport, Cairo University).
* **Road Network:** Data on existing connecting roads with attributes for distance (km), current capacity (vehicles/hour), and condition ratings from 1 to 10.
* **Traffic Fluctuations:** Granular traffic volume patterns divided into Morning Peak, Afternoon, Evening Peak, and Night phases.
* **Public Transit:** Ridership demand, routing, and station data for 3 Metro Lines and 10 standard Bus Routes.

---

## 🚀 Installation & Setup

**1. Clone the repository:**
`bash
git clone https://github.com/yourusername/Cairo-Traffic-Optimization.git
cd Cairo-Traffic-Optimization
`

**2. Create a virtual environment (Recommended):**
`bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
`

**3. Install dependencies:**
`bash
pip install -r requirements.txt
`
*(Ensure you have `scikit-learn`, `tensorflow`, `networkx`, and your preferred visualization libraries installed).*

---

## 💻 Usage & Demo

Run the main dashboard to launch the simulation framework and UI:
`bash
python main.py
`

**Demo Scenarios Included:**
* **Scenario A:** Standard commute from Maadi to Downtown during the Morning Peak.
* **Scenario B:** Emergency ambulance routing from Cairo International Airport to Qasr El Aini Hospital.
* **Scenario C:** Side-by-side visualization of routing algorithms under heavy congestion.

---

## 📁 Repository Structure

* `data/`: Contains the parsed Cairo transportation dataset.
* `src/algorithms/`: Implementations of MST, Dijkstra, A*, DP, and Greedy algorithms.
* `src/ml_models/`: ML-based traffic prediction models.
* `src/visualization/`: Code for the UI and side-by-side algorithm race animations.
* `docs/`: Contains the comprehensive Technical Report (PDF) detailing system architecture, complexity analysis, and performance evaluations.
* `main.py`: Entry point for the interactive demonstration.

---

## 👥 Contributors
* **[Moataz Moamen 23102156]** 
* **[Farah Ghassan 23101583]** 
* **[Yomna Mohamed Fekry 23101506]** 
* **[Wesam Kamal 23101501]** 
* **[Habiba Hamada 23101382]** 
* **[Rawan Osama 23101891]** 


* *Algorithms & UI Development* - Alamein International University (AIU).

## 📄 License
This project is submitted as academic coursework for CSE112.
