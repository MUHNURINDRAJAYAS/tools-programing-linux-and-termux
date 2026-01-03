# Materi Lengkap

## Bahasa Pemrograman untuk Membuat Tools Linux + Compiler

Dokumen ini berisi **bahasa pemrograman yang umum digunakan untuk membuat tools Linux**, lengkap dengan **fungsi, kelebihan, dan cara compile / menjalankannya**. Cocok untuk **belajar, menentukan stack, dan dokumentasi GitHub**.

---

## 1. C (Paling Dasar & Powerful)

### Kegunaan:

* Tools sistem Linux
* Kernel, driver, utilitas core (`ls`, `cp`, `ps`)

### Compiler:

* `gcc`

### Compile:

```bash
gcc tool.c -o tool
./tool
```

### Kelebihan:

* Sangat cepat
* Akses langsung ke sistem
* Dipakai di hampir semua Linux

---

## 2. C++ (Tool Modern & Cepat)

### Kegunaan:

* CLI tools
* Aplikasi sistem
* Software performa tinggi

### Compiler:

* `g++` / `clang++`

### Compile:

```bash
g++ tool.cpp -o tool
./tool
```

### Kelebihan:

* Lebih rapi dari C
* Mendukung OOP
* Cocok untuk Linux CLI tools

---

## 3. Bash (Shell Script)

### Kegunaan:

* Otomasi Linux
* Admin sistem
* Script ringan

### Interpreter:

* `bash`

### Jalankan:

```bash
chmod +x tool.sh
./tool.sh
```

### Kelebihan:

* Tidak perlu compile
* Sangat cepat dibuat
* Native Linux

---

## 4. Python (Paling Populer)

### Kegunaan:

* CLI tools
* Networking tools
* Security tools

### Interpreter:

* `python3`

### Jalankan:

```bash
python3 tool.py
```

### Optional Build (Executable):

```bash
pip install pyinstaller
pyinstaller --onefile tool.py
```

### Kelebihan:

* Mudah dipelajari
* Banyak library
* Cepat develop

---

## 5. Go (Modern & Single Binary)

### Kegunaan:

* Linux tools modern
* Network & cloud tools

### Compiler:

* `go`

### Compile:

```bash
go build tool.go
./tool
```

### Kelebihan:

* Binary tunggal
* Cepat
* Cocok distribusi Linux

---

## 6. Rust (Aman & Cepat)

### Kegunaan:

* System tools
* Security tools
* Performance critical apps

### Compiler:

* `rustc` / `cargo`

### Compile:

```bash
cargo build --release
./target/release/tool
```

### Kelebihan:

* Aman memory
* Performa tinggi
* Alternatif C/C++

---

## 7. Java

### Kegunaan:

* Cross-platform tools
* Server & service

### Compiler:

* `javac`

### Compile & Run:

```bash
javac Tool.java
java Tool
```

---

## 8. Node.js (JavaScript)

### Kegunaan:

* CLI tools modern
* Automation tools

### Runtime:

* `node`

### Jalankan:

```bash
node tool.js
```

### Build Binary:

```bash
npm install -g pkg
pkg tool.js
```

---

## 9. Perbandingan Singkat

| Bahasa | Compile | Cocok untuk       |
| ------ | ------- | ----------------- |
| C      | Ya      | System tools      |
| C++    | Ya      | CLI tools cepat   |
| Bash   | Tidak   | Automation        |
| Python | Tidak   | General tools     |
| Go     | Ya      | Distribusi binary |
| Rust   | Ya      | Secure tools      |
| Java   | Ya      | Cross-platform    |
| JS     | Tidak   | CLI modern        |

---

## 10. Rekomendasi Belajar (Step by Step)

1. Bash
2. C++ / Python
3. Go atau Rust
4. System & Security tools

---

## 11. Cara Membuat File dengan Nano (Wajib untuk Linux)

`nano` adalah **text editor terminal** yang paling umum di Linux dan sangat cocok untuk pemula.

---

### 11.1 Membuat File Baru dengan Nano

Contoh membuat file C++:

```bash
nano tool.cpp
```

Contoh membuat file Bash:

```bash
nano tool.sh
```

Contoh membuat file Python:

```bash
nano tool.py
```

Setelah perintah dijalankan, editor **nano** akan terbuka.

---

### 11.2 Menyimpan & Keluar dari Nano

Di bagian bawah nano terdapat shortcut penting:

* **CTRL + O** → Simpan file
* **Enter** → Konfirmasi nama file
* **CTRL + X** → Keluar dari nano

📌 Shortcut penting lain:

* **CTRL + K** → Cut baris
* **CTRL + U** → Paste
* **CTRL + W** → Cari teks

---

### 11.3 Contoh Kode (Ditulis di Nano)

#### Contoh C++:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Linux Tool C++" << endl;
    return 0;
}
```

Simpan lalu compile:

```bash
g++ tool.cpp -o tool
./tool
```

---

#### Contoh Bash:

```bash
#!/bin/bash
echo "Linux Tool Bash"
```

Simpan lalu jalankan:

```bash
chmod +x tool.sh
./tool.sh
```

---

#### Contoh Python:

```python
print("Linux Tool Python")
```

Jalankan:

```bash
python3 tool.py
```

---

## 12. Struktur Repo GitHub (Contoh)

```
Linux-Tools/
├── bash/
│   └── tool.sh
├── cpp/
│   └── tool.cpp
├── python/
│   └── tool.py
├── go/
├── rust/
└── README.md
```

---

---

## 13. Penggunaan di Termux (Android)

Bagian ini khusus untuk **user Termux (Android)** agar bisa membuat **Linux Tools langsung dari HP** menggunakan workflow yang sama seperti Linux desktop.

---

### 13.1 Install Termux (WAJIB BENAR)

📌 **Gunakan Termux dari F-Droid (bukan Play Store)** karena versi Play Store sudah usang.

---

### 13.2 Update & Install Package Dasar

```bash
pkg update && pkg upgrade
pkg install nano clang make git python
```

📌 Keterangan:

* `nano` → editor teks
* `clang` → compiler C / C++ di Termux
* `make` → build automation
* `git` → GitHub
* `python` → tools Python

---

### 13.3 Membuat File dengan Nano (Termux)

Contoh C++:

```bash
nano tool.cpp
```

Contoh Bash:

```bash
nano tool.sh
```

Contoh Python:

```bash
nano tool.py
```

Shortcut nano (sama seperti Linux):

* **CTRL + O** → Simpan
* **Enter** → OK
* **CTRL + X** → Keluar

---

### 13.4 Compile & Jalankan Tools di Termux

#### C++ (clang++)

```bash
clang++ tool.cpp -o tool
./tool
```

#### Bash

```bash
chmod +x tool.sh
./tool.sh
```

#### Python

```bash
python tool.py
```

---

### 13.5 Contoh Mini Linux Tool di Termux (C++)

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Linux Tool via Termux" << endl;
    return 0;
}
```

Compile:

```bash
clang++ tool.cpp -o tool
./tool
```

---

### 13.6 Struktur Repo GitHub (Termux Friendly)

```
Linux-Tools/
├── cpp/
│   └── tool.cpp
├── bash/
│   └── tool.sh
├── python/
│   └── tool.py
├── Makefile
└── README.md
```

---

### 13.7 Tips Penting User Termux

* Gunakan **keyboard tambahan Termux**
* Biasakan coding full CLI
* Jangan takut error (clang error sangat jelas)
* Cocok untuk belajar **system & security tools**

---

🔥 Dengan Termux, HP kamu sudah setara **Linux development environment**.
🔥 Dengan **nano + clang + git**, kamu siap jadi **Linux Tools Developer**.
