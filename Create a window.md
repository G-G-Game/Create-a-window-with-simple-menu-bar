Create-a-window-with-simple-menu-bar
====================================

Create a window with a simple menu bar

import pygame
from Tkinter import *

# create the root window
root = Tk()

# modify the window
root.title("Create a window")
root.geometry("640x380")

# create a menu
def callback():
    print "New game!"

menu = Menu(root)
root.config(menu=menu)

filemenu = Menu(menu)
menu.add_cascade(label="File", menu=filemenu)
filemenu.add_command(label="New", command=callback)
filemenu.add_command(label="Open...", command=callback)
filemenu.add_separator()
filemenu.add_command(label="Exit", command=callback)

helpmenu = Menu(menu)
menu.add_cascade(label="Help", menu=helpmenu)
helpmenu.add_command(label="About...", command=callback)

# Start the window's event-loop
root.mainloop()
