"""
NAMA = VIOLA WULAN AZ ZAHRO
INA ver
Konversi sistem bilangan digital adalah proses mengubah representasi angka dari satu sistem bilangan ke sistem bilangan lainnya. Terdapat beberapa sistem bilangan digital yang umum digunakan, yaitu sistem bilangan biner (basis 2), sistem bilangan oktal (basis 8), sistem bilangan desimal (basis 10), dan sistem bilangan heksadesimal (basis 16).

ENG ver
The conversion of digital number systems is the process of changing the representation of numbers from one number system to another. There are several commonly used digital number systems, namely the binary number system (base 2), the octal number system (base 8), the decimal number system (base 10), and the hexadecimal number system (base 16).
"""

"""
Pastikan Library Tkinter terinstall, biasanya sudah terinstal secara otomatis bersamaan dengan instalasi 
Python pada sistem operasi Windows dan macOS. Kalau menggunakan Linux, mungkin perlu 
menginstalnya terpisah. cara untuk install Tkinter  :

Windows dan macOS:

        jalankan perintah ini di command prompt atau terminal:

        python -m tkinter

Linux:
        Untuk Debian dan Ubuntu:

        Buka terminal dan jalankan perintah :
        sudo apt-get update
        sudo apt-get install python3-tk


        Untuk Fedora:

        Buka terminal dan jalankan perintah berikut:
        sudo dnf install python3-tkinter

        Untuk CentOS:

        Buka terminal dan jalankan perintah :
        sudo yum install python3-tkinter
"""
import tkinter as tk


def desimal_ke_biner(desimal):
    return format(desimal, "b")


def desimal_ke_oktal(desimal):
    return format(desimal, "o")


def desimal_ke_heksa(desimal):
    return format(desimal, "x")


def biner_ke_desimal(biner):
    return int(biner, 2)


def biner_ke_oktal(biner):
    desimal = int(biner, 2)
    return format(desimal, "o")


def biner_ke_heksa(biner):
    desimal = int(biner, 2)
    return format(desimal, "x")


def oktal_ke_desimal(oktal):
    return int(oktal, 8)


def oktal_ke_biner(oktal):
    desimal = int(oktal, 8)
    return format(desimal, "b")


def oktal_ke_heksa(oktal):
    desimal = int(oktal, 8)
    return format(desimal, "x")


def heksa_ke_desimal(heksa):
    return int(heksa, 16)


def heksa_ke_biner(heksa):
    desimal = int(heksa, 16)
    return format(desimal, "b")


def heksa_ke_oktal(heksa):
    desimal = int(heksa, 16)
    return format(desimal, "o")


def konversi_pilihan(pilihan):
    try:
        if pilihan == "1":
            nilai_desimal = int(input_nilai.get())
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, desimal_ke_biner(nilai_desimal))
        elif pilihan == "2":
            nilai_desimal = int(input_nilai.get())
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, desimal_ke_oktal(nilai_desimal))
        elif pilihan == "3":
            nilai_desimal = int(input_nilai.get())
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, desimal_ke_heksa(nilai_desimal))
        elif pilihan == "4":
            nilai_biner = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, biner_ke_desimal(nilai_biner))
        elif pilihan == "5":
            nilai_biner = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, biner_ke_oktal(nilai_biner))
        elif pilihan == "6":
            nilai_biner = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, biner_ke_heksa(nilai_biner))
        elif pilihan == "7":
            nilai_oktal = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, oktal_ke_desimal(nilai_oktal))
        elif pilihan == "8":
            nilai_oktal = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, oktal_ke_biner(nilai_oktal))
        elif pilihan == "9":
            nilai_oktal = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, oktal_ke_heksa(nilai_oktal))
        elif pilihan == "10":
            nilai_heksa = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, heksa_ke_desimal(nilai_heksa))
        elif pilihan == "11":
            nilai_heksa = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, heksa_ke_biner(nilai_heksa))
        elif pilihan == "12":
            nilai_heksa = input_nilai.get()
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, heksa_ke_oktal(nilai_heksa))
        else:
            entry_hasil.delete(0, tk.END)
            entry_hasil.insert(0, "Pilihan tidak valid")
    except ValueError:
        entry_hasil.delete(0, tk.END)
        entry_hasil.insert(0, "Masukkan nilai yang valid")


# Membuat tampilan GUI
root = tk.Tk()
root.title("Konverter Bilangan")

# Frame utama
frame_utama = tk.Frame(root)
frame_utama.pack(pady=20)

# Label untuk jenis konversi
label_jenis_konversi = tk.Label(frame_utama, text="Pilihan konversi:")
label_jenis_konversi.grid(row=0, column=0, padx=10, pady=5, sticky=tk.W)

# Dropdown menu untuk pilihan konversi
pilihan_konversi = tk.StringVar()
dropdown_konversi = tk.OptionMenu(
    frame_utama,
    pilihan_konversi,
    "1. Desimal ke Biner",
    "2. Desimal ke Okta",
    "3. Desimal ke Heksadesimal",
    "4. Biner ke Desimal",
    "5. Biner ke Okta",
    "6. Biner ke Heksadesimal",
    "7. Okta ke Desimal",
    "8. Okta ke Biner",
    "9. Okta ke Heksadesimal",
    "10. Heksadesimal ke Desimal",
    "11. Heksadesimal ke Biner",
    "12. Heksadesimal ke Okta",
)
dropdown_konversi.config(bg="black", fg="white")
dropdown_konversi.grid(row=0, column=1, padx=10, pady=5, sticky=tk.W)

# Label dan Entry untuk input nilai
label_input = tk.Label(frame_utama, text="Masukkan nilai:")
label_input.grid(row=1, column=0, padx=10, pady=5, sticky=tk.W)

input_nilai = tk.StringVar()
entry_nilai = tk.Entry(frame_utama, textvariable=input_nilai)
entry_nilai.grid(row=1, column=1, padx=10, pady=5, sticky=tk.W)

# Button untuk konversi
tombol_konversi = tk.Button(
    frame_utama,
    text="Konversi",
    command=lambda: konversi_pilihan(pilihan_konversi.get().split(".")[0]),
)
tombol_konversi.grid(row=2, columnspan=2, pady=10)

# Label dan Entry untuk hasil konversi
label_hasil = tk.Label(frame_utama, text="Hasil konversi:")
label_hasil.grid(row=3, column=0, padx=10, pady=5, sticky=tk.W)

entry_hasil = tk.Entry(frame_utama)
entry_hasil.grid(row=3, column=1, padx=10, pady=5, sticky=tk.W)

root.mainloop()
