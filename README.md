import tkinter
from tkinter import *

root = Tk()
root.title('calculator')
root.resizable(width=0, height=0)
# -----------------------------------------------------------------------------------------------------
add_text = StringVar()
x = 4
y = 1
bcol = 'red'
fcol = 'white'
display = ''
# -------------------------------------------------------------------------------------------------------


def btnclick(num):
    global display
    display = display+str(num)
    add_text.set(display)


def clear_button():
    global display
    display = ""
    add_text.set(display)


def equal():
    global display
    eq = str(round(eval(display), 5))
    add_text.set(eq)
    display = eq


screen = Entry(root, bg='purple', width=13, bd=3,
               textvariable=add_text, font=('Times New Roman', 25, 'bold'), fg='white')

button_7 = Button(root, text='7', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(7))
button_8 = Button(root, text='8', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(8))
button_9 = Button(root, text='9', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(9))
button_4 = Button(root, text='4', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(4))
button_5 = Button(root, text='5', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(5))
button_6 = Button(root, text='6', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(6))
button_1 = Button(root, text='1', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(1))
button_2 = Button(root, text='2', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(2))
button_3 = Button(root, text='3', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(3))
button_0 = Button(root, text='0', font=('Times New Roman', 20, 'bold'),
                  bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick(0))

button_point = Button(root, text='.', font=('Times New Roman', 20, 'bold'),
                      bg=bcol, width=x, height=y, fg=fcol, command=lambda: btnclick('.'))

button_plus = Button(root, text='+', font=('Times New Roman', 20, 'bold'),
                     bg='black', width=x, height=y, fg=fcol, command=lambda: btnclick('+'))
button_minus = Button(root, text='-', font=('Times New Roman', 20, 'bold'),
                      bg='black', width=x, height=y, fg=fcol, command=lambda: btnclick('-'))
button_multiply = Button(root, text='X', font=('Times New Roman', 20, 'bold'),
                         bg='black', width=x, height=y, fg=fcol, command=lambda: btnclick('*'))
button_div = Button(root, text='/', font=('Times New Roman', 20, 'bold'),
                    bg='black', width=x, height=y, fg=fcol, command=lambda: btnclick('/'))

button_equal = Button(root, text='=', font=('Times New Roman', 20, 'bold'),
                      bg='blue', width=x, height=y, fg='black', command=lambda: equal())

button_clear = Button(root, text='C', font=('Times New Roman', 20, 'bold'),
                      bg='tomato', width=9, padx=1, height=y, fg='black', command=lambda: clear_button())


screen.grid(row=0, column=0, columnspan=3)
button_7.grid(row=1, column=0)
button_8.grid(row=1, column=1)
button_9.grid(row=1, column=2)
button_4.grid(row=2, column=0)
button_5.grid(row=2, column=1)
button_6.grid(row=2, column=2)
button_1.grid(row=3, column=0)
button_2.grid(row=3, column=1)
button_3.grid(row=3, column=2)
button_0.grid(row=4, column=1)
button_plus.grid(row=4, column=0)
button_minus.grid(row=5, column=0)
button_multiply.grid(row=4, column=2)
