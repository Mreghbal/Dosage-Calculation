import tkinter as tk

def calculate_heart_rate(age):
    max_heart_rate = 220 - age
    target_min = 0.5 * max_heart_rate
    target_max = 0.85 * max_heart_rate
    return target_min, target_max

def get_user_condition(heart_rate, target_min, target_max):
    if heart_rate < target_min:
        return "Below target range"
    elif heart_rate >= target_min and heart_rate <= target_max:
        return "Within target range"
    else:
        return "Above target range"

def calculate_button_clicked():
    age = int(age_entry.get())
    target_min, target_max = calculate_heart_rate(age)
    heart_rate = int(heart_rate_entry.get())
    user_condition = get_user_condition(heart_rate, target_min, target_max)
    target_heart_rate_label.config(text=f"Target Heart Rate Range: {target_min} - {target_max}")
    heart_rate_label.config(text=f"Your Heart Rate: {heart_rate}")
    condition_label.config(text=f"Condition: {user_condition}")

# Create the main window
window = tk.Tk()
window.title("Heart Rate Calculator")

# Age input label and entry
age_label = tk.Label(window, text="Enter your age:")
age_label.pack()
age_entry = tk.Entry(window)
age_entry.pack()

# Heart rate input label and entry
heart_rate_label = tk.Label(window, text="Enter your heart rate:")
heart_rate_label.pack()
heart_rate_entry = tk.Entry(window)
heart_rate_entry.pack()

# Calculate button
calculate_button = tk.Button(window, text="Calculate", command=calculate_button_clicked)
calculate_button.pack()

# Result labels
target_heart_rate_label = tk.Label(window, text="")
target_heart_rate_label.pack()
heart_rate_label = tk.Label(window, text="")
heart_rate_label.pack()
condition_label = tk.Label(window, text="")
condition_label.pack()

# Start the main GUI loop
window.mainloop()
