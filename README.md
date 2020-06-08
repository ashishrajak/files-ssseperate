# files-ssseperate

import tkinter as tk
from tkinter import ttk
ash=tk.Tk()
ash.title('ashsihe')
#lable

lable=ttk.Label(ash,text='enter your name=:')
lable.grid(row=0,column=0,sticky=tk.W)
age_lavel=ttk.Label(ash,text='youur age')
age_lavel.grid(row=1,column=0,sticky=tk.W)
#Variable
gender_=tk.StringVar()
name_var=tk.StringVar()
age_var=tk.IntVar()
#entry box

entryc=ttk.Entry(ash,width=12,textvariable=name_var,)
entryc.focus()

entryc.grid(row=0,column=1)
entry_age=ttk.Entry(ash,width=12,textvariable=age_var)
entry_age.grid(row=1,column=1)
#radiobutton
radiobutton=tk.StringVar()
radio1=ttk.Radiobutton(ash,text='student',value='student',variable=radiobutton)
radio1.grid(row=4,column=4)

#function
def rajak():
    user=name_var.get()
    age=age_var.get()
    gend=gender_.get()
    print(f'{user} and age is {age} and gehnder gender {gend}')

#combowbox
gender=ttk.Combobox(ash,width=19,textvariable=gender_,state='readonly')
gender['values']=('male','female','neutral')
gender.grid(row=2,column=0)
gender.current(0)
     

#button

button_a=tk.Button(ash,text='submit',command=rajak)
button_a.grid(row=1,column=3)

ash.mainloop()
