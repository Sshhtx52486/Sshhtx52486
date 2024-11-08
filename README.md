 import tkinter as tk
from tkinter import messagebox

# ایجاد پنجره اصلی
root = tk.Tk()
root.title("Login Form")

# تنظیم اندازه پنجره
root.geometry("300x200")

# تابع برای بررسی اطلاعات ورود
def login():
    username = entry_username.get()
    password = entry_password.get()
    if username == "admin" and password == "admin":
        messagebox.showinfo("Login", "Login Successful!")
    else:
        messagebox.showerror("Login", "Invalid Username or Password")

# ایجاد برچسب‌ها و ورودی‌ها
label_username = tk.Label(root, text="Username")
label_username.pack(pady=5)
entry_username = tk.Entry(root)
entry_username.pack(pady=5)

label_password = tk.Label(root, text="Password")
label_password.pack(pady=5)
entry_password = tk.Entry(root, show="*")
entry_password.pack(pady=5)

# ایجاد دکمه ورود
button_login = tk.Button(root, text="Login", command=login)
button_login.pack(pady=20)



# اجرای حلقه اصلی برنامه
root.mainloop()
