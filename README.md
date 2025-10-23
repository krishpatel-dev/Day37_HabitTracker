# 🐍 Habit Tracker with Pixela - Day 37

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/krishpatel-dev/Day37_habit_tracker/graphs/commit-activity)

A Python-based habit tracker that uses the Pixela API to track and visualize your daily coding habits. This project helps you maintain consistency in your coding routine by allowing you to log your daily coding hours and visualize your progress over time.

## 📋 Table of Contents
- [Features](#-features)
- [Prerequisites](#-prerequisites)
- [Setup](#-setup)
- [Usage](#-usage)
- [API Reference](#-api-reference)
- [Contributing](#-contributing)

## ✨ Features

- 📊 Track daily coding hours
- 📅 Automatic date tracking
- 🔄 Update or delete previous entries
- 📱 Simple command-line interface
- 🌈 Visual progress tracking with Pixela graphs

## 🛠 Prerequisites

- Python 3.8 or higher
- A Pixela account (free to create)
- `requests` library (install via `pip install requests`)

## 🚀 Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/krishpatel-dev/Day37_habit_tracker.git
   cd Day37_habit_tracker
   ```

2. **Install dependencies**
   ```bash
   pip install requests
   ```

3. **Configure your Pixela account**
   - Sign up at [Pixela](https://pixe.la/)
   - Create a new token in your account settings
   - Create a new graph for tracking your habit

4. **Update the configuration**
   Open `Proj37_habit_tracker.py` and update the following variables:
   - `USERNAME`: Your Pixela username
   - `TOKEN`: Your Pixela API token
   - `GRAPH_ID`: The ID of your created graph

## 🖥 Usage

### Track Daily Coding
```bash
python Proj37_habit_tracker.py
```
The script will prompt you to enter the number of hours you coded today.

### Update an Entry
Uncomment and modify the following section in the code:
```python
update_endpoint = f"{pixela_endpoint}/{USERNAME}/graphs/{GRAPH_ID}/{today.strftime('%Y%m%d')}"
new_pixel_data = {
    "quantity": "3.5"  # Update with your new value
}
response = requests.put(url=update_endpoint, json=new_pixel_data, headers=headers)
print(response.text)
```

### Delete an Entry
Uncomment and modify the following section in the code:
```python
delete_endpoint = f"{pixela_endpoint}/{USERNAME}/graphs/{GRAPH_ID}/{today.strftime('%Y%m%d')}"
response = requests.delete(url=delete_endpoint, headers=headers)
print(response.text)
```

## 🌐 API Reference

This project uses the [Pixela API](https://docs.pixe.la/) for habit tracking and visualization. The API allows you to:
- Create and manage user accounts
- Create custom graphs
- Post, update, and delete pixel data
- View your progress through a web interface

## 🤝 Contributing

Contributions are welcome! Here's how you can contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

<div align="center">
  Made with ❤️ and ☕ by <b>Krish</b>
</div>
