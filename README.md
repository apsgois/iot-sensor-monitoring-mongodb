# IoT Sensor Monitoring with MongoDB

Academic project developed during the **Database II** course as part of my Software Engineering studies.

The project simulates an **IoT temperature monitoring system** using Python threads and MongoDB. Multiple virtual sensors generate temperature readings independently, store their state in a MongoDB database, and trigger alerts when a temperature threshold is exceeded.

## 📚 Project Overview

The application simulates three independent temperature sensors using Python threads.

Each sensor periodically generates a random temperature between **30°C and 40°C** and stores its latest state in MongoDB.

When a sensor records a temperature above **38°C**, it enters an alarm state and stops generating new readings.

The application then reports a high-temperature warning for that sensor.

## ⚙️ How It Works

Each sensor stores information such as:

* Sensor name
* Current temperature
* Measurement unit
* Alarm status

The sensor lifecycle can be summarized as:

```text
Start Sensor
     │
     ▼
Generate Temperature
     │
     ▼
Store Reading in MongoDB
     │
     ▼
Temperature > 38°C?
     │
   ┌─┴─┐
   │   │
  No  Yes
   │   │
   │   ▼
   │  Trigger Alarm
   │   │
   │   ▼
   │  Stop Generating Readings
   │
   └──► Continue Monitoring
```

## 🛠️ Technologies

* Python
* MongoDB
* Python Threads
* JSON

## 📂 Project Structure

```text
.
├── db/
├── helper/
├── json/
├── main.py
└── README.md
```

## 💡 Concepts Explored

This project provided practical experience with:

* NoSQL databases
* MongoDB document operations
* Multithreading
* IoT sensor simulation
* Data persistence
* Threshold-based monitoring
* Application state management

## 🎓 Academic Context

This project was developed as an evaluated exercise for the **Database II** course.

It is maintained as part of my academic portfolio to document my experience integrating Python applications with MongoDB and simulating concurrent IoT sensor monitoring.
