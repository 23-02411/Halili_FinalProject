Fitness Tracker Application

This is a simple fitness tracker application built using Python and Tkinter. It helps users log their daily steps, calories, and workouts. Users can edit and save their fitness data for better tracking and management.

Features

Login Screen: Simulates a login interface with placeholders for username and password.

Main Fitness Tracker Interface: Allows users to log steps, calories, and workouts.

Edit Entries: Users can edit their logged data.

Save Data: Saves fitness data to a JSON file.

Reset Data: Resets all logged fitness data.

Interactive Listbox: Displays total steps, calories, and workouts.

Prerequisites

Python 3.x

Required Libraries:

Tkinter (Standard Python library for GUI development)

PIL (Python Imaging Library for handling images)

JSON (For saving and loading data)

Setup Instructions

Clone or download the repository to your local machine.

Install the required libraries if not already installed:

pip install pillow

Place the background image (bg.jpg) in the same directory as the script.

Run the script:

python fitness_tracker.py

File Structure

fitness_tracker.py: The main application script.

bg.jpg: Background image for the login screen.

fitness_data.json: File for storing fitness data (created after saving data).

How to Use

Login:

Enter username: user

Enter password: password

Click "Login" to access the main screen.

Log Data:

Use the input fields to log steps, calories, and workouts.

Click the corresponding buttons to save the entries.

Edit Data:

Select an entry from the listbox.

Click the "Edit Selected" button to modify the entry.

Save Data:

Click the "Save Data" button to save all entries to fitness_data.json.

Reset Data:

Click the "Reset Data" button to clear all logged data.

Code Highlights

Login Screen

The show_login_screen function creates a simple login interface with placeholder functionality for username and password fields.

def show_login_screen():
    # Example snippet for creating the login screen
    login_window = tk.Toplevel(root)
    login_window.title("Login")
    login_window.geometry("500x500")
    ...

Main Screen

The show_main_screen function creates the main interface, allowing users to log and manage their fitness data.

def show_main_screen():
    global data, main_window, listbox
    main_window = tk.Toplevel(root)
    main_window.title("Byte Me Fitness Tracker")
    main_window.geometry("600x600")
    ...

Save Data

The save_data function writes the fitness data to a JSON file.

def save_data():
    try:
        with open("fitness_data.json", "w") as file:
            json.dump(data, file, indent=4)
        messagebox.showinfo("Save Data", "Data has been saved successfully!")
    except Exception as e:
        messagebox.showerror("Save Error", f"Failed to save data: {e}")

Future Enhancements

User Authentication: Integrate actual user authentication with database support.

Graphical Reports: Add graphs and charts to visualize fitness progress.

Mobile Compatibility: Create a mobile-friendly version of the application.

Multi-User Support: Allow multiple users to log in and track their individual fitness data.

License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it.

Acknowledgments

Tkinter Documentation for GUI development.

Pillow Library for image handling.

The open-source community for inspiration and support.

