# ⚡ EcoPulse EV - Smart Load Balancing Algorithm Logic

## 🎯 Goal
Prevent EV charging station congestion by dynamically analyzing queue length and rerouting users to nearby underutilized stations.

## 🧮 Congestion Formula
Congestion Ratio = Queue Count / Total Chargers

## 📜 Decision Logic
1. If Congestion Ratio > 0.8:
   - Mark Station Status as "HIGH_TRAFFIC" / "CONGESTED"
   - Trigger alert on Frontend: "Station is busy! Redirect to nearby station for 10% off & zero wait time."
   - Suggest nearest alternative station within 3 km radius.

2. Else:
   - Mark Station Status as "AVAILABLE" / "NORMAL"
   - Allow direct slot booking.