import tkinter as tk
from tkinter import messagebox

def myclick(number):
    entry.insert(tk.END, number)

def equal():
    try:
        result = str(eval(entry.get()))
        entry.delete(0, tk.END)
        entry.insert(0, result)
    except:
        messagebox.showinfo("Error", "Syntax Error")

def clear():
    entry.delete(0, tk.END)

window = tk.Tk()
frame = tk.Frame(master=window, bg="deep pink", padx=30, pady=30)
frame.pack()

entry = tk.Entry(master=frame, relief=tk.SUNKEN, borderwidth=5, width=40)
entry.grid(row=0, column=0, columnspan=3, ipady=15, pady=15)

button_specs = [
    (1, 0, '1'), (1, 1, '2'), (1, 2, '3'),
    (2, 0, '4'), (2, 1, '5'), (2, 2, '6'),
    (3, 0, '7'), (3, 1, '8'), (3, 2, '9'),
    (4, 1, '0')
]

for (row, col, text) in button_specs:
    button = tk.Button(master=frame, text=text, padx=15, pady=5, width=3, command=lambda num=text: myclick(num))
    button.grid(row=row, column=col, pady=5)

operator_specs = [
    (5, 0, '+'), (5, 1, '-'), (5, 2, '*'), (6, 0, '/'),(4, 2,'.')
]

for (row, col, text) in operator_specs:
    operator_button = tk.Button(master=frame, text=text, padx=15, pady=5, width=3, command=lambda op=text: myclick(op))
    operator_button.grid(row=row, column=col, pady=5)

button_clear = tk.Button(master=frame, text="Clear", padx=15, pady=5, width=12, command=clear)
button_clear.grid(row=6, column=1, columnspan=2, pady=5)

button_equal = tk.Button(master=frame, text="=", padx=15, pady=5, width=9, command=equal)
button_equal.grid(row=7, column=0, columnspan=3, pady=5)

window.mainloop()
