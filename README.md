

# Calorie Calculator - Java Application

## Overview
This Java application calculates a person's Basal Metabolic Rate (BMR) and estimated daily calorie needs based on personal information including gender, age, weight, height, and activity level.

## Features
- Calculates BMR using the Mifflin-St Jeor Equation
- Estimates daily calorie requirements based on activity level
- Validates all user inputs
- Clean, object-oriented design with separation of concerns

## Class Structure

### 1. `CalorieCalculator`
**Purpose**: Handles all business logic for calorie calculations  
**Key Methods**:
- `calculateBMR()`: Computes Basal Metabolic Rate using gender-specific formulas
- `calculateDailyCalorieNeeds()`: Adjusts BMR based on activity level

### 2. `UserData`
**Purpose**: Data Transfer Object to hold user information  
**Fields**:
- Gender (M/F)
- Age (years)
- Weight (kg)
- Height (cm)
- Activity Level (sedentary/moderate/active)

### 3. `UserInputHandler`
**Purpose**: Handles all user input with validation  
**Key Methods**:
- `gatherUserData()`: Orchestrates collection of all user data
- Validation methods for each input type (gender, age, etc.)

### 4. `ResultDisplay`
**Purpose**: Presents calculation results to the user  
**Key Methods**:
- `displayResults()`: Shows formatted BMR and calorie needs

### 5. `MainApp`
**Purpose**: Application entry point and workflow coordinator  
**Key Responsibilities**:
1. Collects user data
2. Performs calculations
3. Displays results

## How to Use
1. Run the `MainApp` class
2. Follow the prompts to enter your:
   - Gender (M/F)
   - Age (in years)
   - Weight (in kilograms)
   - Height (in centimeters)
   - Activity level (sedentary/moderate/active)
3. View your calculated BMR and daily calorie needs

## Calculation Methodology
### BMR Calculation
- **Male**:  
  `BMR = 88.362 + (13.397 × weight in kg) + (4.799 × height in cm) - (5.677 × age in years)`
  
- **Female**:  
  `BMR = 447.593 + (9.247 × weight in kg) + (3.098 × height in cm) - (4.330 × age in years)`

### Activity Multipliers
- **Sedentary**: BMR × 1.2
- **Moderate activity**: BMR × 1.55
- **Active**: BMR × 1.725

## Requirements
- Java 8 or higher

## Example Output
```
Calorie Calculator
Enter your gender (M/F): M
Enter your age (in years): 30
Enter your weight (in kilograms): 75
Enter your height (in centimeters): 180
Enter your activity level (sedentary/moderate/active): moderate

Your Basal Metabolic Rate (BMR) is: 1685 calories per day.
Your estimated daily calorie needs are: 2612 calories per day.
```

## Design Principles
- Single Responsibility Principle (each class has one clear purpose)
- Separation of concerns (input, calculation, display logic separated)
- Input validation
- Immutable data transfer object
- Proper resource management (Scanner cleanup)
