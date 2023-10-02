import tkinter as tk
import time
import math

class AdvancedAnalogClock(tk.Tk):
    def __init__(self):
        super().__init__()
        self.title("Advanced Analog Clock")
        self.geometry("400x400")
        self.canvas = tk.Canvas(self, bg='white', height=400, width=400)
        self.canvas.pack(fill='both', expand=True)
        self.update_clock()

    def update_clock(self):
        self.canvas.delete("all")
        width = self.canvas.winfo_width()
        height = self.canvas.winfo_height()
        size = min(width, height) - 20
        center_x = width // 2
        center_y = height // 2
        current_time = time.localtime()
        hours = current_time.tm_hour
        minutes = current_time.tm_min
        seconds = current_time.tm_sec

        # Draw clock face
        self.canvas.create_oval(center_x - size // 2, center_y - size // 2, center_x + size // 2, center_y + size // 2, fill='light gray')
        for i in range(1, 13):
            angle = math.radians(i * (360 / 12) - 90)
            x = center_x + (size // 2 - 20) * math.cos(angle)
            y = center_y + (size // 2 - 20) * math.sin(angle)
            self.canvas.create_text(x, y, text=str(i), font=('Times New Roman', 20, 'bold'))

        # Draw tick marks
        for i in range(60):
            angle = math.radians(i * (360 / 60) - 90)
            start_x = center_x + (size // 2 - 10) * math.cos(angle)
            start_y = center_y + (size // 2 - 10) * math.sin(angle)
            end_x = center_x + (size // 2) * math.cos(angle)
            end_y = center_y + (size // 2) * math.sin(angle)
            self.canvas.create_line(start_x, start_y, end_x, end_y, width=1 if i % 5 else 2)

        # Draw hour hand
        hour_angle = math.radians((hours % 12 + minutes / 60) * (360 / 12) - 90)
        hour_x = center_x + (size // 4) * math.cos(hour_angle)
        hour_y = center_y + (size // 4) * math.sin(hour_angle)
        self.canvas.create_line(center_x, center_y, hour_x, hour_y, width=6, fill='black')

        # Draw minute hand
        minute_angle = math.radians(minutes * (360 / 60) - 90)
        minute_x = center_x + (size // 3) * math.cos(minute_angle)
        minute_y = center_y + (size // 3) * math.sin(minute_angle)
        self.canvas.create_line(center_x, center_y, minute_x, minute_y, width=4, fill='blue')

        # Draw second hand
        second_angle = math.radians(seconds * (360 / 60) - 90)
        second_x = center_x + (size // 2 - 20) * math.cos(second_angle)
        second_y = center_y + (size // 2 - 20) * math.sin(second_angle)
        self.canvas.create_line(center_x, center_y, second_x, second_y, fill='red')

        # Schedule the function to be called after 1000ms
        self.after(1000, self.update_clock)

if __name__ == "__main__":
    app = AdvancedAnalogClock()
    app.mainloop()
