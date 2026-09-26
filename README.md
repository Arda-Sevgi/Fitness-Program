# Fitness Tracker 🏋️

A Python-based fitness tracking application designed to help users record physical activities, monitor nutrition, set fitness goals and review their overall progress.

The application uses a menu-driven command-line interface and stores user, activity, nutrition and goal data in CSV files. It also includes user authentication, password hashing, calorie calculations and progress tracking.

## 📌 Features

### 👤 User Authentication

- Create a personal user account
- Secure password hashing using SHA-256
- Existing user login
- Username validation
- Password confirmation during registration
- Maximum of three failed login attempts
- User session management

### 🏃 Physical Activity Tracking

Users can record different types of physical activity, including:

- Running
- Cycling
- Swimming
- Weight Training
- Walking
- Yoga
- Dancing

For each activity, users can enter:

- Activity duration
- Exercise intensity
- Date

The application calculates estimated calories burned based on the selected activity, duration and intensity.

### 🥗 Nutrition Tracking

Users can record their daily food and nutrition information.

Supported meal types include:

- Breakfast
- Lunch
- Dinner
- Snack

Each nutrition entry records:

- Food or meal name
- Calories
- Carbohydrates
- Protein
- Fat
- Date

### 🎯 Fitness Goals

Users can create personalised fitness goals, including:

- Weight Loss
- Weight Gain
- Total Calories Burned
- Weekly Workouts
- Daily Steps
- Running Distance

Goals include a target value and target date, allowing users to monitor their progress over time.

### 📊 Progress Monitoring

The application calculates and displays progress towards fitness goals.

Progress information includes:

- Target value
- Current value
- Percentage completed
- Target date
- Visual progress indicator

Activity-based goals such as total calories burned and weekly workouts are automatically updated from recorded activity data.

### 📈 Fitness Summary

Users can view an overall fitness summary containing:

- Total calories burned
- Total calories consumed
- Net calories
- Total workouts recorded
- Total nutrition entries
- Today's activities
- Recent goal progress

This provides a consolidated overview of the user's recorded fitness data.

## 🧮 Calorie Calculation

The application estimates calories burned using predefined calorie-per-minute values for each activity.

The calculation also considers exercise intensity:

| Intensity | Multiplier |
|---|---:|
| Low | 0.8× |
| Medium | 1.0× |
| High | 1.2× |

The estimated calories burned are calculated using the activity's base calorie rate, duration and intensity multiplier.

## 💾 Data Storage

The application uses **CSV files** for persistent data storage rather than a traditional database.

Four CSV files are automatically created when required:

```text
users.csv
activities.csv
nutrition.csv
goals.csv
```

### `users.csv`

Stores:

- Username
- Password hash
- Join date

### `activities.csv`

Stores:

- Username
- Date
- Activity type
- Duration
- Intensity
- Calories burned

### `nutrition.csv`

Stores:

- Username
- Date
- Meal type
- Food item
- Calories
- Carbohydrates
- Protein
- Fat

### `goals.csv`

Stores:

- Username
- Goal type
- Target value
- Current value
- Target date
- Created date

## 🔐 Password Security

Passwords are not stored as plain text.

When an account is created, the password is processed using Python's `hashlib` library and stored as a SHA-256 hash.

During login, the entered password is hashed using the same method and compared with the stored hash.

> **Note:** SHA-256 without a password-specific key derivation function is not considered sufficient for production authentication systems. This project uses it as a learning implementation of password hashing.

## 🛠️ Technologies Used

- **Python 3**
- **CSV**
- **OS / File System**
- **datetime**
- **hashlib**
- Object-Oriented Programming

## 📁 Project Structure

```text
Fitness_Program/
│
├── Program_Fitness/
│   └── Fitness.py
│
├── users.csv
├── activities.csv
├── nutrition.csv
└── goals.csv
```

The CSV files are created automatically by the application if they do not already exist.

## 🚀 Getting Started

### Requirements

- Python 3.x

No external Python packages are required.

### Run the Application

Navigate to the project directory and run:

```bash
python Fitness.py
```

The application will display the welcome screen and prompt you to log in or create a new account.

## 🎮 Main Menu

After logging in, users can access:

```text
1. Log Physical Activity
2. Track Nutrition
3. View Progress
4. Set Fitness Goals
5. View Fitness Summary
6. Exit
```

Each option provides a separate part of the fitness tracking system.

## 🧠 Programming Concepts Demonstrated

This project was developed to practise and apply several Python programming concepts, including:

- Object-oriented programming
- Classes and methods
- File handling
- CSV data processing
- Dictionaries
- Lists
- Loops
- Conditional statements
- Exception handling
- User input validation
- Date and time processing
- Data calculations
- Password hashing
- State management
- Modular application design

## 🎯 Learning Objectives

The main purpose of this project was to develop practical experience building a larger Python application rather than isolated programming exercises.

Key learning areas included:

- Designing a menu-driven application
- Managing persistent data using CSV files
- Implementing user authentication
- Handling user sessions
- Working with structured data
- Performing calculations from stored data
- Connecting multiple application features together
- Validating user input
- Handling file and runtime errors
- Applying object-oriented programming principles

## 🔄 Application Workflow

```text
Start Application
       │
       ▼
Welcome Screen
       │
       ▼
Login / Create Account
       │
       ▼
User Authentication
       │
       ▼
Main Menu
       │
       ├── Log Physical Activity
       │
       ├── Track Nutrition
       │
       ├── View Progress
       │
       ├── Set Fitness Goals
       │
       ├── View Fitness Summary
       │
       └── Exit
```

## 🔮 Possible Future Improvements

Potential improvements to the application include:

- Replacing CSV storage with a relational database
- Using a stronger password hashing solution such as Argon2 or bcrypt
- Adding graphical data visualisation
- Adding weekly and monthly reports
- Supporting more activity types
- Adding more detailed nutrition calculations
- Implementing BMI and body composition tracking
- Adding user profile management
- Adding exportable fitness reports
- Developing a graphical or web-based interface

## 📚 Project Purpose

Fitness Tracker was created as a practical Python project to demonstrate how multiple programming concepts can be combined into a single application.

The project goes beyond simple calculations by implementing **authentication, persistent data storage, activity and nutrition management, goal tracking and progress analysis** within one application.

## 👨‍💻 Author

**Arda Sevgi**

Developed as a Python programming and application development project.
