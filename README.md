<h1>KONVERSI SISTEM BILANGAN DIGITAL/THE CONVERSION OF DIGITAL NUMBER SYSTEM IN PYTHON GUI</h1>

<p style="text-align: justify;">INA Ver
Konversi sistem bilangan digital adalah proses mengubah representasi angka dari satu sistem bilangan ke sistem bilangan lainnya. Terdapat beberapa sistem bilangan digital yang umum digunakan, yaitu sistem bilangan biner (basis 2), sistem bilangan oktal (basis 8), sistem bilangan desimal (basis 10), dan sistem bilangan heksadesimal (basis 16).</p>

<p style="text-align: justify;">ENG Ver
The conversion of digital number systems is the process of changing the representation of numbers from one number system to another. There are several commonly used digital number systems, namely the binary number system (base 2), the octal number system (base 8), the decimal number system (base 10), and the hexadecimal number system (base 16).</p>

<p style="text-align: justify;">Pastikan Library Tkinter terinstall, biasanya sudah terinstal secara otomatis bersamaan dengan instalasi 
Python pada sistem operasi Windows dan macOS. Kalau menggunakan Linux, mungkin perlu 
menginstalnya terpisah. cara untuk install Tkinter  :</p>


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



# Membuat tampilan GUI
root = tk.Tk()
root.title("Konverter Bilangan")

# Dropdown Menu pilihan konversi
Dropdown menu untuk pilihan konversi
        
    "1. Desimal ke Biner"<br>
    "2. Desimal ke Okta"<br>
    "3. Desimal ke Heksadesimal"<br>
    "4. Biner ke Desimal"<br>
    "5. Biner ke Okta"<br>
    "6. Biner ke Heksadesimal"<br>
    "7. Okta ke Desimal"<br>
    "8. Okta ke Biner"<br>
    "9. Okta ke Heksadesimal"<br>
    "10. Heksadesimal ke Desimal"<br>
    "11. Heksadesimal ke Biner"<br>
    "12. Heksadesimal ke Okta"<br>
