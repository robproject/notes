### Root window
```
import tkinter

if __name__ = '__main__':
	root = tkinter.Tk()
	rootwindow.mainloop()
```
	
### Button
button = tkinter.Button(rootwindow, text="click me")
button.pack()

### Button command
button = tkinter.Button(rootwindow, text="click me", command = my_function)

### Background color
rootwindow.config(background="red")

### Pack
Adds vertical axis padding in pixels:
artifact.pack(pady=10)
