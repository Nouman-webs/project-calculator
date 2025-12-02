import tkinter as tk
from tkinter import messagebox

# --- Functions for buttons ---
def add_student():
    messagebox.showinfo("Add", "Add Student button clicked")

def view_students():
    messagebox.showinfo("View", "View Students button clicked")

def update_student():
    messagebox.showinfo("Update", "Update Student button clicked")

def delete_student():
    messagebox.showinfo("Delete", "Delete Student button clicked")

# --- Main Window ---
root = tk.Tk()
root.title("Student Management System")
root.geometry("400x500")
root.resizable(False, False)

# ----------- Labels -------------
title_label = tk.Label(root, text="Student Management System",
                       font=("Arial", 16, "bold"))
title_label.pack(pady=20)

name_label = tk.Label(root, text="Name", font=("Arial", 12))
name_label.pack(pady=10)

age_label = tk.Label(root, text="Age", font=("Arial", 12))
age_label.pack(pady=10)

gender_label = tk.Label(root, text="Gender", font=("Arial", 12))
gender_label.pack(pady=10)

# ----------- Buttons ------------
button_frame = tk.Frame(root)
button_frame.pack(pady=20)

btn_width = 20

add_btn = tk.Button(button_frame, text="Add Student", width=btn_width,
                    command=add_student)
add_btn.pack(pady=5)

view_btn = tk.Button(button_frame, text="View Students", width=btn_width,
                     command=view_students)
view_btn.pack(pady=5)

update_btn = tk.Button(button_frame, text="Update Student", width=btn_width,
                       command=update_student)
update_btn.pack(pady=5)

delete_btn = tk.Button(button_frame, text="Delete Student", width=btn_width,
                       command=delete_student)
delete_btn.pack(pady=5)

# Run the GUI
root.mainloop()
