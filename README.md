alu-AirBnB_clone – The Console

This project is the beginning of the AirBnB clone developed at African Leadership University (ALU).
The goal is to build a simplified version of the AirBnB platform step by step, starting with a command-line console to manage objects and store them persistently.

Eventually, this project will evolve into:

A command interpreter (the console)

A website (front-end)

A storage system (JSON & MySQL)

An API for communication between front-end and storage

alu-AirBnB_clone/
│
├─ console.py            # Entry point for the command interpreter
├─ models/               # All classes (BaseModel, User, State, City, Place, etc.)
│   ├─ base_model.py     # Base class for all models
│   ├─ user.py           # User model
│   ├─ state.py          # State model
│   ├─ city.py           # City model
│   ├─ place.py          # Place model
│   ├─ amenity.py        # Amenity model
│   ├─ review.py         # Review model
│   └─ engine/           # Storage engines
│       └─ file_storage.py
│
├─ tests/                # Unit tests for all classes and the console
├─ web_static/           # Static web files (HTML, CSS, images)
├─ AUTHORS               # Project contributors
└─ README.md             # Project description
⚡ Features

Command-line Console

Create, show, update, and destroy objects

List all objects or filter by class

Data persists across sessions via file.json

Models Implemented

BaseModel (common parent class with id, created_at, updated_at)

User, State, City, Place, Amenity, Review

Storage Engine

File storage system (FileStorage)

Serializes objects to JSON

Deserializes JSON back into Python objects

🛠️ Technologies Used

Python 3.8+

JSON (for serialization)

Unittest (for testing)

Object-Oriented Programming (OOP)

🚀 Getting Started

git clone https://github.com/YOUR_USERNAME/alu-AirBnB_clone.git
cd alu-AirBnB_clone

Run the console
python3 console.py

Example Commands

(hbnb) create BaseModel
(hbnb) show BaseModel 1234-5678
(hbnb) all
(hbnb) update User 1234-5678 email "me@alu.edu"
(hbnb) destroy City 9876-5432

Run tests

python3 -m unittest discover tests

📦 JSON File Storage

Objects are stored in file.json using JSON serialization.

{
  "BaseModel.1234": {
    "id": "1234",
    "created_at": "2025-09-13T21:00:00.000000",
    "updated_at": "2025-09-13T21:10:00.000000",
    "name": "My First Model"
  }
}

✨ Future Improvements

Add MySQL storage engine

Build RESTful API

Develop dynamic front-end with Flask/Jinja

Enable client-side interaction with JavaScript

👩‍💻 Authors

Ineza Manzi Arnaud 

Leila Abbie Adoyo Omol 

