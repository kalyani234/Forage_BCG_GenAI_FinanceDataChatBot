# 💹 AI-Powered Financial Data Analysis & Chatbot

# 🧠 Overview
# ----------------------------------------------------------
# This project demonstrates two connected components:
#  1️⃣ Financial data analysis using Python & Pandas.
#  2️⃣ A simple AI-powered chatbot that responds to predefined
#     financial questions using the analyzed dataset.

# Both tasks were developed and executed in Google Colab.

# ----------------------------------------------------------
# 📂 Folder / File Structure
# ----------------------------------------------------------
financial_chatbot_project/
├── dataset/
│   └── companies_financial_data.csv        # Input dataset
├── task1_data_analysis.ipynb               # Task 1 notebook
├── task2_chatbot_logic.ipynb               # Task 2 notebook
└── README.md                               # Documentation

# (Optional for future work)
# ├── app.py
# └── templates/index.html                   # Flask front-end
# ----------------------------------------------------------


# 🧩 Task 1 — Financial Data Analysis
# ----------------------------------------------------------
# Objective:
#   • Clean and preprocess the dataset.
#   • Compute financial performance metrics.
#   • Summarize and visualize results.

# Step 1 – Load & inspect data
#   import pandas as pd
#   df = pd.read_csv('dataset/companies_financial_data.csv')
#   df.info()

# Step 2 – Data cleaning
#   • Remove missing rows in Fiscal Year.
#   • Convert revenue, income, assets, liabilities,
#     and cash-flow columns to float.
#   • Sort by Company and Fiscal Year.

# Step 3 – Feature engineering
#   • Revenue Growth (%)          = pct_change() × 100
#   • Net Income Growth (%)
#   • Debt Ratio (%)              = Liabilities / Assets × 100
#   • Cash-Flow-to-Revenue Ratio (%) = CFO / Revenue × 100
#   • Assets-to-Liabilities Ratio = Assets / Liabilities

# Step 4 – Aggregations
#   • Group by Company  → sum, mean, max of revenue & income
#   • Group by Year     → total revenue & income across firms

# Step 5 – Visualization
#   • Grouped bar chart: Total Revenue vs Year for each Company.
#   • Libraries used: matplotlib and numpy.

# Step 6 – Conclusions
#   • Apple dominates revenue & profit but growth is flattening.
#   • Microsoft shows consistent balanced performance.
#   • Tesla shows fastest revenue growth but volatile profit.
# ----------------------------------------------------------


# 🤖 Task 2 — Rule-Based Financial Chatbot
# ----------------------------------------------------------
# Objective:
#   Implement a basic chatbot using if-elif statements
#   to answer predefined queries derived from Task 1 metrics.

# Step 1 – Reuse cleaned DataFrame from Task 1.

# Step 2 – Define chatbot function
#   def simple_chatbot(user_query):
#       if user_query == "what is the total revenue?":
#           return ...
#       elif user_query == "which company has the highest net income?":
#           return ...
#       elif user_query == "which company has the highest debt ratio?":
#           return ...
#       ...
#       else:
#           return "Sorry, I can only answer predefined questions."

# Step 3 – Interactive loop
#   print("💬 Financial Chatbot Prototype (type 'exit' to quit)")
#   while True:
#       q = input("You: ")
#       if q.lower() == "exit":
#           break
#       print("Chatbot:", simple_chatbot(q))

# Step 4 – Example queries
#   • what is the total revenue?
#   • which company has the highest net income?
#   • which company has the highest debt ratio?
#   • what is the average assets to liabilities ratio?
#   • which company improved its cash flow the most?

# Step 5 – Example output
#   💬 Financial Chatbot Prototype (type 'exit' to quit)
#   You: what is the total revenue?
#   Chatbot: The total combined revenue of all companies is £2,099,880.
#   You: exit
#   Chatbot: Goodbye! 👋
# ----------------------------------------------------------


# ⚙️ Libraries Required
# ----------------------------------------------------------
pip install pandas numpy matplotlib
# (optional)
pip install flask
# ----------------------------------------------------------


# 🚀 Execution Workflow
# ----------------------------------------------------------
# 1️⃣ Upload dataset to Google Colab.
# 2️⃣ Run all cells in task1_data_analysis.ipynb.
# 3️⃣ Review visualizations and conclusions.
# 4️⃣ Run task2_chatbot_logic.ipynb.
# 5️⃣ Ask predefined questions in the Colab console.
# ----------------------------------------------------------


# 🌐 (Optional) Flask Web Extension
# ----------------------------------------------------------
#  • app.py  – wrap chatbot logic in Flask.
#  • templates/index.html  – simple HTML chat UI.
#  • Run with:
#        python app.py
#        # then open http://127.0.0.1:5000/
# ----------------------------------------------------------


# 🧮 Technologies U
