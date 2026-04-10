# Smart Elevator Control System - ER Diagram

This project presents the Entity-Relationship (ER) diagram for a smart elevator control system used in large multi-building infrastructures such as corporate towers, malls, and residential complexes.

## 📌 Overview

The system manages multiple buildings, elevators, floors, and real-time ride requests. It supports efficient elevator allocation, status monitoring, maintenance tracking, and ride logging for performance analysis.

---

## 🧩 Entities Included

* **Buildings** – Stores building details
* **Floors** – Represents floors within each building
* **Elevators** – Elevator units assigned to buildings
* **Elevator_Floors** – Junction table to map elevators to multiple floors
* **Floor_Requests** – Tracks user requests from floors
* **Ride_Assignments** – Assigns requests to elevators
* **Ride_Logs** – Records completed rides for analytics
* **Elevator_Status** – Tracks real-time elevator state (idle, moving, maintenance)
* **Maintenance_Logs** – Stores maintenance history of elevators

---

## 🔗 Key Relationships

* A building has multiple floors and elevators
* Elevators can serve multiple floors (many-to-many via elevator_floors)
* Floor requests are generated from floors
* Each request is assigned to an elevator
* Elevators handle multiple ride logs
* Elevator status and maintenance are tracked separately

---

## 🧠 Design Decisions

* **Separation of Dynamic Data:**
  Ride logs, requests, and status are stored separately from elevator configuration.

* **Flexible Floor Mapping:**
  A junction table allows elevators to serve multiple floors and floors to be served by multiple elevators.

* **Request → Assignment → Ride Flow:**
  Requests are handled through a structured pipeline for better tracking and analytics.

* **Maintenance Tracking:**
  Maintenance logs preserve history without overwriting elevator data.

---

## 🛠️ Tools Used

* Eraser (for ER diagram design)

---

## 📷 Output

The ER diagram is included in this repository as an image.

---

## 👨‍💻 Author

Shashikant Mane
