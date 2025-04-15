# 🛰️ (Name To be found) – Augmented Object Mapping

> **Detect. Align. Map.**  
> A real-time collaborative mapping system using smartphones, sensors and video streams to identify and localize objects of interest (UAV).

---

## 🧠 Idea Summary

This project is inspired by a video recently realised by [ConsistentlyInconsistentyt](https://www.youtube.com/watch?v=m-b51C82-UE&pp=0gcJCX4JAYcqIYzv). The video show a proof of ocncept how two camera with known relative position + angles and basic image processign allow to detect very small object (from the size of a pixel) with good confidence.

The added value would be:
- Allow N sensor devices to gather the data without prior information about relative position/angles
- Allow sensor devices to disconenct/reconnect
- Allow M observator devices to see data in real time.

In order to do so:

We turn smartphones into decentralized, mobile detection units.  
Each phone:
- captures video
- reads orientation & location from sensors (GPS + IMU)
- sends probabilistic object detection data to a central backend

The backend:
- aggregates multiple viewpoints
- aligns them in space and time
- generates a **2D map of detection probabilities**.

Use cases: battleground intelligence, UAV scouting, RF-less plastic UAV scouting.

---

## 🎯 Goals for the Hackathon

- ✅ Build a minimal working prototype:
  - Mobile client: access camera & orientation sensors
  - Backend: receive + align detection data
  - Map view: visualize estimated object zones
- 🧪 Bonus: simulate multiple devices to test multi-angle fusion

---

## 📐 Architecture

```
📱 Mobile (Web or App) 
    ├── Camera feed 
    ├── Orientation sensors (accel, gyro, magneto) 
    └── GPS

📡 Sends data → Backend

🧠 Backend (NestJS / Python) 
    ├── Sync by timestamp 
    ├── Convert orientation + GPS to 3D cones 
    ├── Merge overlapping cones 
    └── Project on 2D plane

🗺️ Frontend (React / Leaflet) 
    └── Displays map with object probability zones
```


*(➡️ Tu peux ajouter ici un joli schéma SVG ou image)*

---

## 🧩 Modules

| Module | Stack | Owner | Status |
|--------|-------|--------|--------|
| 📱 Sensor & Camera Capture | Web APIs / React Native | TBD | ⚪ Not started |
| 📤 Data Sender | WebSocket / HTTP | You | 🟢 Boilerplate ready |
| 🧠 Data Fusion | Python or TS | You | ⚪ To define |
| 🗺️ Map View | Leaflet / Mapbox | TBD | ⚪ Not started |
| 🎯 Mock Detection | ML / Mocking | Pote ML ? | ⚪ Optional |

---

## 🧪 Tech Stack

- Front-end: **React / React Native** (web or mobile)
- Back-end: **NestJS/Express** (TypeScript) or **Flask** (Python)
- Visualisation: **Leaflet** or **Mapbox GL JS** ?
- Communication: **WebSocket + REST**
- Data fusion: home-made probabilistic system

---

## 👥 Team

Actuals skills needed and available:
    - System design [x]
    - Backend [x]
    - React [~]
    - Math & Sensor fusion [~]
    - Mobile (Website or Native) sensor data gathering [~]
    - UX []


---

## 🎁 Submission Checklist

TBD

---

## 📎 Useful Links

- [Project Architecture (Draw.io)](#) (TBD)
- [Figma UI Prototype](#) (TBD)
- [Sensor API Reference (MDN)](https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent) 
- [OpenStreetMap / Leaflet Docs](https://leafletjs.com/)

---

## 💬 Contact

Let’s build this together!  
Ping me on Discord: `@ery4z` or via email: `thomas.bolteau50@gmail.com`
