# You're a Wizard, Harry

## Overview

Build a **Flask REST API** in **Python** that calls the public **Wizard World API** (`https://wizard-world-api.herokuapp.com/swagger/index.html`) via the **requests** library. Your API must expose **three endpoints** and use a **multitier architecture** (controller → service → repository) with **OOP concepts** (classes, abstract classes, inheritance, attributes/properties).

> **Deliverables:** runnable Flask API + a short README.

---

## Learning Goals

* Build HTTP endpoints with Flask (routing, JSON I/O).
* Separate concerns with controller/service/repository layers.
* Apply OOP (domain models, abstract repositories, inheritance).
* Integrate with an external REST API using `requests`.

---

## Endpoints to Implement (design your own response schema)

1. **POST `/api/v1/house-quiz`**
   Accept user trait scores (e.g., bravery, loyalty, intellect, ambition, optional name) and **assign a house** using your sorting logic. Optionally enrich with house metadata fetched from Wizard World API.

2. **POST `/api/v1/house-mates`**
   Given a wizard’s name and house, return **two compatible best friends**. Fetch characters from Wizard World API and apply your compatibility rule.

3. **GET `/api/v1/random-spell`**
   Return **one random spell** and its info, retrieved from Wizard World API.

---

## Architecture & OOP Requirements

* **Layers:** Controller (Flask routes) → Service (business logic) → Repository (HTTP integration).
* **Repository:** Define an abstract base class; implement a concrete HTTP repository using `requests`.
* **Models:** Create small classes (e.g., `House`, `Wizard`, `Spell`) with attributes/properties.

---

## README Must Include

* How to run the API (brief).
* Short description of each endpoint and its request format.
* Your **house-quiz logic** and **house-mate compatibility rule**.

---

## Grading (100 pts)

* **Adding the 3 endpoints correctly:** 40 pts
* **Calling the external API correctly:** 30 pts
* **OOP concepts (classes, ABCs, inheritance, properties):** 15 pts
* **Error handling (status codes, graceful failures):** 10 pts
* **README quality (clarity, completeness):** 5 pts
