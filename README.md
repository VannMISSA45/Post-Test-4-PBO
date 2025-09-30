# 🎣 Sistem Pencatatan Aktivitas Memancing

Fitur utama:
- Tambah Aktivitas (Ikan/Umpan)  
- Tampilkan Semua Aktivitas  
- Cari Aktivitas berdasarkan Lokasi  
- Hapus Aktivitas  
- Menu interaktif berbasis console


## Alur Program
1. User menjalankan program melalui **Main.java** pada package `main`.  
2. Menu akan tampil dan user memilih opsi (tambah, lihat, cari, hapus, keluar).  
3. Input user diproses oleh **AktivitasService.java** pada package `service`.  
4. Data disimpan dalam `ArrayList` sebagai objek `Ikan` atau `Umpan` dari package `model`.  
5. Program terus berjalan hingga user memilih menu keluar.
<img width="351" height="146" alt="image" src="https://github.com/user-attachments/assets/d68e1c4b-7f50-462b-84c6-1facc4006ce0" />


## Penerapan OOP

### 1. Encapsulation
- Atribut pada class `Aktivitas`, `Ikan`, dan `Umpan` bersifat **private**.  
- Menggunakan **getter** dan **setter** untuk mengakses dan mengubah data.  

### 2. Inheritance
- `Aktivitas` adalah **superclass**.  
- `Ikan` dan `Umpan` adalah **subclass** yang mewarisi atribut & method dari `Aktivitas`.  

### 3. Abstraction
- **Abstract Class:**  
  - `Aktivitas` di package `model` adalah **abstract class**.  
  - Method abstrak `deskripsi()` wajib diimplementasikan oleh subclass.  
- **Interface (opsional):**  
  - `Peralatan` adalah **interface**.  
  - Diimplementasikan oleh class `Joran` dengan method `gunakan()` dan `bersihkan()`.  

**Letak Abstraction:**  
- Abstract class → `model/Aktivitas.java`  
- Interface → `model/Peralatan.java` (diimplementasikan oleh `model/Joran.java`)  

### 4. Polymorphism
- **Overloading (Method Overloading):**  
  Di `AktivitasService.java` (package `service`):  
  ```java
