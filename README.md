import tkinter as tk
from tkinter import messagebox
def hitung():
try:
panjang = float(input_panjang.get())
lebar = float(input_lebar.get())
luas = panjang * lebar
keliling = 2 * (panjang * lebar)
hasil_luas.config(text=f"luas: {luas:.2f}")
hasil_keliling.config(text=f"keliling: {keliling:.2f}")
except ValueError:
messagebox.showerror("error", "masukan angka yang validi")
# membuat window utama
window = tk.Tk()
window.title("kalkulator persegi panjang")
window.geometry("300x200")
#label dan entry untuk panjang
label_panjang = tk.Label(window, text="panjang:")
label_panjang.pack()
input_panjang = tk.Entry(window)
input_panjang.pack()
#label dan entry untuk lebar
label_lebar = tk.Label(window, text="lebar:")
label_lebar.pack()
input_lebar = tk.Entry(window)
input_lebar.pack()
#tombol hitung
button_hitung = tk.Button(window, text="hitung", command=hitung)
button_hitung.pack()
#label untuk menampilkan hasil
hasil_luas = tk.Label(window, text="luas: ")
hasil_luas.pack()
hasil_keliling = tk.Label(window, text="keliling: ")
hasil_keliling.pack()
# menjalankan aplikasi
window.mainloop()
