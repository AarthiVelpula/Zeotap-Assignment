Zeotap Intern Assignment Submission 

Table of Contents 
Overview 
Project Structure 
Prerequisites 
How to Run the Applications 
Rule Engine with AST 
Weather Monitoring System 
Test Cases 
Bonus Features References

Overview 
This repository contains two applications for the Zeotap intern assignment: Rule Engine with Abstract Syntax Tree (AST) to evaluate user eligibility based on configurable rules. Real-Time Weather Monitoring System to retrieve, process, and visualize weather data from OpenWeatherMap API.

Project Structure 
zeotap_assignment/ │ ├── rule_engine.ipynb
├── weather_monitoring.ipynb
├── README.md
├── .env (optional)
└── requirements.txt

Prerequisites 
Python 3.x installed on your machine or use Google Colab. API Key from OpenWeatherMap – Sign up here. GitHub account to clone/push code.

How to Run the Applications 
Option 1: Run on Google Colab Upload the notebooks (rule_engine.ipynb and weather_monitoring.ipynb) to Colab. For weather monitoring, add your OpenWeatherMap API key.
Option 2: Run Locally on Jupyter Install Jupyter:

pip install notebook jupyter notebook Open the notebooks in the Jupyter interface and follow the steps provided in the cells.

Rule Engine with AST 
Description The Rule Engine application allows you to:

Create complex eligibility rules using AST. Evaluate user attributes (age, department, salary, etc.) against the rules. How It Works AST Structure: Each rule is parsed into an AST with operators (AND, OR) and operands (conditions like age > 30). API Functions: create_rule(): Parse a rule string into an AST. evaluate_rule(): Evaluate a rule using input data.

Weather Monitoring System 
Description The Weather Monitoring System retrieves real-time weather data from the OpenWeatherMap API for major Indian cities. It processes the data to provide:

Current temperature (in Celsius) Weather condition (e.g., Rain, Clear) Time of data update Features Temperature Conversion: From Kelvin to Celsius. API Integration: Uses OpenWeatherMap’s API for real-time weather data. Data Visualization: Plots temperature trends for different cities. How to Add API Key Option 1: Add your key directly in the code:

API_KEY = "your_openweathermap_api_key" Option 2: Use a .env file to securely store the key.

Test Cases 
Rule Engine Test Case 1: Create a rule "age > 30 AND department = 'Sales'". Test Case 2: Evaluate the rule with: {"age": 35, "department": "Sales", "salary": 60000} Expected Output: True Weather Monitoring Test Case 1: Retrieve weather data for Mumbai. Test Case 2: Simulate weather data breaching a threshold (e.g., temperature > 35°C).

Bonus Features Error Handling: 
Handles invalid rules and API responses gracefully. Alerts: Allows setting thresholds for temperature and weather conditions. Scalable Design: Modular functions for easy expansion.

References 
OpenWeatherMap API Documentation: https://openweathermap.org/ Python Requests Library: https://pypi.org/project/requests/
