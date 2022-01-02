# Traffic-light2


 
from tkinter import *
class TrafficLights:
    def __init__(self):
        window = Tk()
        window.title("Traffic Light")
        self.canvas = Canvas(window, width = 450, height = 300, bg = "white")
        self.canvas.pack()
        frame = Frame(window)
        frame.pack()
        self.v1 = IntVar()
        rbRed = Radiobutton(frame, text = "Red", bg = "red",
                variable = self.v1, value = 1,
                command = self.processRadiobutton)
        rbYellow = Radiobutton(frame, text = "Yellow", bg = "yellow",
                variable = self.v1, value = 2,
                command = self.processRadiobutton)              
        rbGreen = Radiobutton(frame, text = "Green", bg = "green",
                variable = self.v1, value = 3,              
                command = self.processRadiobutton)
        rbRed.grid(row = 10, column = 1)
        rbYellow.grid(row = 10, column = 2)
        rbGreen.grid(row = 10, column = 3)
        window.mainloop()
    def processRadiobutton(self):
            if self.v1.get() == 'R':
                self.lbl["fg"] = "red"
            elif self.v1.get() == 'Y':
                  self.lbl["fg"] = "yellow"
            elif self.v1.get() == 'G':
                  self.v1.lbl["fg"] = "Green"
    id = self.canvas.create_rectangle(200, 67, 265, 60)
    def displayRectangle(self):
          self.canvas.create_rectangle(200, 67, 265, 60, tags = "rect")
    def displayOval(self):
          self.canvas.create_oval(10, 10, 10, 10, fill='red')
    def displayOval(self):
          self.canvas.create_oval(20, 20, 20, 20, fill='yellow')
    def displayOval(self):
          self.canvas.create_oval(30, 30, 30, 30, fill='green')
TrafficLights()   
