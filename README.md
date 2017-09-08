from Tkinter import *

class Application(Frame):
    def say_hi(self):
        print "hi there, everyone!"

    def createWidgets(self):
        self.QUIT = Button(self)
        self.QUIT["text"] = "QUIT"
        self.QUIT["fg"]   = "red"
        self.QUIT["command"] =  self.quit

        self.QUIT.pack({"side": "left"})

        self.hi_there = Button(self)
        self.hi_there["text"] = "Hello",
        self.hi_there["command"] = self.say_hi

        self.hi_there.pack({"side": "left"})

    def __init__(self, master=None):
        Frame.__init__(self, master)
        self.pack()
        self.createWidgets()

root = Tk()
app = Application(master=root)
app.mainloop()
root.destroy()
 110       while self.letras.match(ch):
 111         s += ch
 112         ch = self.entrada.read(1)
 113       self.str_value = s
 114       self.cur_tok = Calc.TOK_NOME
 115     elif len(ch) == 0:
 116       self.cur_tok = Calc.TOK_FIM
 117     else:
 118       self.cur_tok = ch
 119       if ch == '\n':
 120         if hasattr(self,'ch'):
 121           del self.ch
 122         return
 123       ch = sys.stdin.read(1)
 124 
 125     while ch in (' ', '\t'):
 126       ch = sys.stdin.read(1)
 127       
 128     self.ch = ch
 129 
 130 if __name__ == "__main__":
 131   import sys
 132   calc = Calc(sys.stdin)
 133   calc.run()
