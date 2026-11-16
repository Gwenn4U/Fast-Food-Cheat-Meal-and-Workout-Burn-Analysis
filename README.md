# Fast-Food-Cheat-Meal-and-Workout-Burn-Analysis
An Exploratory Data Analysis (EDA) project
# 🍔 Fast Food Cheat Meals and Workout Plan Analysis

**Fast food တစ်နပ်စားလိုက်ရင် လေ့ကျင့်ခန်း ဘယ်လောက်လုပ်ရမလဲ၊ ဘယ်လိုစားသင့်သလဲ?**

A comprehensive data analysis project exploring the caloric and nutritional burden of fast-food cheat meals, evaluating required workout durations to offset caloric surplus, and providing portion-control strategies for non-exercisers.

---

## 👥 Project Team (Group 3)

* **Kaung Khant Lynn** 
* **Hsu San Lwin** 
* **Phyo Thiha Kyaw** 
* **Thadar Hsu(Gwenn)** 

**Project Guidance:** Ko Kyaw Kyaw Htut *(Founder of Ace of Data)*

---

## 📊 Dataset Overview

* **Source:** [Fast Food Calorie Shock: Food vs Workout Burn (Kaggle)](https://www.kaggle.com/datasets/samartalwar/fast-food-calorie-shock-food-vs-workout-burn)
* **Size:** 8,000 fast-food orders across 23 columns (0 missing values, 0 duplicate rows).
* **Privacy:** Contains no personally identifiable information (PII).
* **Core Attributes:**
  * **Consumer Demographics:** `consumer_age`, `consumer_weight_kg`, `fitness_level` (*Sedentary, Moderately Active, Highly Trained*).
  * **Meal & Nutrition:** `fast_food_chain` (9 chains), `meal_category` (6 categories), `total_calories`, `fat_grams`, `saturated_fat_grams`, `carb_grams`, `sugar_grams`, `sodium_mg`, `daily_calorie_allowance_pct`.
  * **Energy & Workout Burden:** `net_caloric_surplus`, `workout_shock_tier`, and burn duration (in minutes) across four modalities (`walking`, `cycling`, `running`, `hiit`).

---

## 🎯 Project Objectives

This analysis addresses two practical decision-making frameworks:
1. **Decision 1 — Exercise Plan:** Determines the appropriate workout modality and duration required to burn off a cheat meal's net caloric surplus based on consumer age, weight, and fitness level.
2. **Decision 2 — Dietary Risk & Portion Control:** Assesses nutritional risks (saturated fat, sodium, sugar, calories) against daily reference limits for sedentary individuals and calculates optimal portion reductions (100%, 75%, 50%).

---

## 🔍 Key Findings & Insights

### 1. Consumer Profile & Demographics
* **Age Distribution:** Working-age adults (`31–50`) represent the largest segment at **41.3%**, followed by seniors (`51+`) at **31.3%**, and young adults (`18–30`) at **27.5%**.
* **Weight Distribution:** Nearly 9 out of 10 consumers weigh over 60 kg (`60–80 kg`: **46.1%**, `>80 kg`: **43.3%**, `<60 kg`: **10.6%**).
* **Fitness Level:** Almost half (**45.3%**) are **Sedentary**, highlighting the critical need for dietary portion control alongside exercise planning.

### 2. Decision 1: Exercise Plan & Workout Shock
* **Caloric Surplus:** The average `net_caloric_surplus` per meal is **1,481.0 kcal** (median: 1,367.0 kcal; max: 3,429.2 kcal). Surplus levels remain consistent across age, weight, and fitness brackets, proving that meal size—not consumer profile—drives caloric overload.
* **Workout Shock Tiers:** **45.1%** of Sedentary consumers fall into the highest burden tier (*Extreme / Half-Marathon Toll*), compared to **31.3%** of Highly Trained individuals.
* **Average Burn Time Required:**
  * **HIIT:** ~100.5 mins (most time-efficient)
  * **Running:** ~117.9 mins (~2 hours)
  * **Cycling:** ~165.0 mins (~2.75 hours)
  * **Walking:** ~350.2 mins (nearly 6 hours; up to 21+ hours for extreme orders)
* **Body Weight vs. Fitness Impact:** Body weight affects calculated burn time far more significantly (**64% difference** between `<60 kg` and `>80 kg` groups) than fitness level (**18% difference** between Sedentary and Highly Trained).

### 3. Decision 2: Dietary Risk & Portion Control
* **Single-Meal Overload:** On average, a single fast-food meal consumes **80.1%** of daily calories (1,602.6 kcal) while exceeding daily limits for **Saturated Fat (160%)**, **Sugar (125%)**, **Total Fat (123%)**, and **Sodium (104%)**.
* **Hidden Compound Risk:** While only **25.4%** of orders exceed the 2,000 kcal daily calorie limit, **75.6%** exceed the saturated fat limit (>20g), **46.0%** exceed the sodium limit (>2,300mg), and **45.7%** exceed *both* simultaneously.
* **Chain & Category Uniformity:** Nutritional averages vary by less than 1.5% across all 6 meal categories and ~3% across all 9 fast-food chains—switching chains or meal types alone does not mitigate nutritional risk.
* **Portion Reduction Impact:**
  * **At 75% Portion:** Fat, sugar, and sodium drop below daily limits, but saturated fat remains at **120%**.
  * **At 50% Portion:** All average nutrient metrics fall within daily reference limits (saturated fat drops to **80%**). However, on an order-by-order basis, **24.3%** of meals still exceed daily limits even when cut in half, primarily due to saturated fat.

---

## ⚠️ Limitations of the Study

1. **Formula-Derived Burn Times:** Exercise burn durations appear algorithmically estimated via standard MET formulas (e.g., `MET * 3.5 * weight / 200`), which explains why heavier individuals show shorter required durations.
2. **Simulated Data Characteristics:** The minimal variance across different fast-food chains and meal categories, alongside hard upper caps (e.g., 3,600 kcal, 5,800 mg sodium, 75 g saturated fat), suggests the dataset is synthetically generated rather than real-world POS data.
3. **Strict Daily Benchmarks:** Comparing a single meal against full-day reference limits (`2,000 kcal`, `20 g` saturated fat, `2,300 mg` sodium) serves as a strict baseline indicator rather than an individualized clinical diet plan.

---

## 💡 Recommendations

* **For Consumers:** Relying solely on exercise to offset fast-food meals requires hours of high-intensity effort. Combine **portion control (reducing meals to 50%–75%)** with workouts matched to personal fitness levels, prioritizing lower saturated fat items.
* **For Food Retailers:** Increase menu transparency by displaying saturated fat, sodium, and estimated exercise burn-time equivalents alongside standard calorie counts.

```[cite: 1, 2, 3, 4, 6, 7, 8, 9, 10, 12, 13, 14, 15, 16, 18, 20, 21, 22, 24, 25]
