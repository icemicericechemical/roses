# roses
example reposiyory
# pip install tkinter
import tkinter as tk
import tkinter.messagebox
from tkinter.constants import SUNKEN
 
window = tk.Tk()
window.title('Calculator-')
frame = tk.Frame(master=window, bg="skyblue", padx=10)
frame.pack()
entry = tk.Entry(master=frame, relief=SUNKEN, borderwidth=4, width=54)
entry.grid(row=8, column=1, columnspan=4, ipady=7, pady=7)
 
 
def myclick(number):
    entry.insert(tk.END, number)
 
 
def equal():
    try:
        y = str(eval(entry.get()))
        entry.delete(0, tk.END)
        entry.insert(0, y)
    except:
        tkinter.messagebox.showinfo("Error", "Syntax Error")
