# QR-code-genrator
import tkinter
from tkinter import ttk
from tkinter import messagebox
import qrcode as qr


def enter_data():
    a=entry.get()
    sal=qr.make(a)

    sal.save("C:\mywork\python\experiment_dl\QR.png")


window=tkinter.Tk()
window.title("QR Genaroator")

QR=tkinter.LabelFrame(text="QR")
QR.grid(row=0,column=0,padx=20,pady=10)

name=tkinter.Label(QR,text="QR Genaroator")
name.grid(row=0,column=1)
entry=tkinter.Entry(QR)
entry.grid(row=0,column=1,padx=20,pady=20)


button=tkinter.Button(QR,text="Button",command=enter_data)
button.grid(row=0,column=3,sticky="news",padx=20,pady=10)




window.mainloop()
