📝 Description

This is a simple countdown timer written in Python. It takes user input in seconds and then counts down to zero, displaying the remaining time in the format MM:SS. Once the countdown reaches zero, it prints "Time's up!" to notify the user.

This project demonstrates basic usage of Python’s time module and how to format and display a live updating timer in the terminal.


---

🚀 Features

Accepts user input for countdown duration

Displays time in a live countdown format (MM:SS)

Real-time updates in the terminal

User-friendly input validation

Written in clean and readable Python



---

🛠️ Requirements

Python 3.x (recommended: Python 3.6 or later)


No external libraries are required — this project uses only built-in Python modules.


---

📂 Project Structure

countdown_timer/
├── countdown_timer.py   # Main Python script
└── README.md            # Project documentation (this file)


---

🔧 How to Run the Program

1. Clone or Download the Repository

If you're using Git:

git clone https://github.com/yourusername/countdown_timer.git
cd countdown_timer

Or manually download and extract the ZIP file.

2. Run the Script

Make sure Python is installed on your system. Then run the script:

python countdown_timer.py

You’ll be prompted to enter the number of seconds for the countdown. For example:

Enter time in seconds: 10
00:10
00:09
...
00:01
Time's up!


---

💡 Code Breakdown

Here’s a simplified version of the core logic:

import time

def countdown_timer():
    total_seconds = int(input("Enter time in seconds: "))
    while total_seconds:
        mins, secs = divmod(total_seconds, 60)
        print('{:02d}:{:02d}'.format(mins, secs), end='\r')
        time.sleep(1)
        total_seconds -= 1
    print("Time's up!")

🔍 Key Functions Used:

input() – for taking user input

int() – to convert input into an integer

divmod() – to separate minutes and seconds

time.sleep(1) – pauses execution for 1 second

end='\r' – rewrites the same line in the terminal
