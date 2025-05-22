# 🚗 Autonomous Vehicle Simulation Framework

This project presents an integrated simulation framework for adaptive path planning, V2X communication, and energy-aware WSN routing in autonomous vehicles. The system combines Deep Reinforcement Learning (DRL), classical path planning algorithms, 5G-based V2X groupcasting, and WSN optimization using MOISA. It is designed to run within high-fidelity simulation environments like CARLA and SUMO.

---

## 📌 Features

- DRL-based adaptive motion planning using PPO/SAC
- Baseline path generation using A* and RRT*
- Real-time replanning with Model Predictive Control (MPC)
- 5G-based V2X communication using groupcasting and IR-HARQ
- Comfort-aware control using Full Velocity Difference (FVD) model
- Signal Temporal Logic (STL) for safety verification
- Energy-efficient WSN routing via MOISA and RL clustering
- Simulation integration via CARLA, SUMO, and NS-3 (optional)

---

## 🧱 Project Structure

```plaintext
AutonomousVehicleProject/
├── CARLA_SUMO_Integration/
│   ├── CARLA/                         # CARLA simulator
│   ├── SUMO/                          # SUMO network and routing files
│   ├── integration/                   # Bridge scripts between CARLA & SUMO
│   ├── config/                        # Simulation parameters
│   └── logs/                          # Synchronization output
│
├── ObstacleDetectionSimulation/
│   ├── simulation/                    # Entry-point simulation script
│   ├── sensors/                       # LIDAR and detection modules
│   ├── communication/                # V2X message handling
│   ├── decision_engine/              # Behavioral response logic
│   ├── evaluation/                   # Metrics and visualization
│   └── config/                       # Communication and reaction settings
│
├── env/                               # Python virtual environment
├── requirements.txt                   # Python dependencies
└── README.md






🛠️ Setup Instructions
1. Clone the repository
                        git clone https://github.com/Pushpak1203/V2X-Communication.git
cd V2X-Communication




2. Set up a virtual environment (Python 3.10 recommended)
python -m venv env
.\env\Scripts\activate  # Windows
pip install -r requirements.txt



3. Download and set up CARLA Simulator
Download CARLA 0.9.13 for Windows from CARLA Releases

Extract to CARLA_SUMO_Integration/CARLA/

Launch using:
           CARLA_SUMO_Integration\CARLA\CarlaUE4.exe -carla-rpc-port=2000


4. Run CARLA-SUMO Integration

cd CARLA_SUMO_Integration/integration
python run_carla_sumo.py


5. Run Obstacle Detection Simulation

cd ObstacleDetectionSimulation/simulation
python run_sim.py


🧠 Algorithms and Techniques Used
DRL: Proximal Policy Optimization (PPO), Soft Actor Critic (SAC)

Path Planning: A*, RRT*, MPC

Comfort Modeling: Full Velocity Difference (FVD)

Formal Verification: Signal Temporal Logic (STL)

Communication: Groupcasting, IR-HARQ over V2X

WSN Optimization: MOISA (Multi-Objective Improved Seagull Algorithm)




📊 Tools & Technologies
CARLA

SUMO

Python

TensorFlow, PyTorch, OpenCV, Stable-Baselines3

NS-2/NS-3 (optional for WSN)
