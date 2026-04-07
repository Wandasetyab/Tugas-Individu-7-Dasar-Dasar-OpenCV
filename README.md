# Tugas Individu 7 Dasar Dasar OpenCV

**Mata Kuliah:** Praktikum Machine Learning (Computer Vision)  
**Dosen Pengampu:** Herfandi, Ph.D. — Informatika — Universitas Teknologi Sumbawa (UTS)

---

## Profil Mahasiswa
* **Nama:** Wanda Setya Budi
* **NIM:** 231001008
* **Kelas:** Informatika

---

## Deskripsi Proyek
Repositori ini berisi dokumentasi teknis mengenai implementasi dasar **OpenCV (Open Source Computer Vision Library)**. Praktikum ini bertujuan untuk memahami bagaimana komputer membaca gambar dan video sebagai matriks angka (NumPy Array), melakukan manipulasi channel warna, serta menangani input stream dari file video maupun kamera (webcam).

Materi ini merupakan fondasi utama sebelum melangkah ke tahap *Image Pre-processing* yang lebih lanjut dalam alur kerja *Machine Learning*.

---

## Lingkungan Pengembangan (Environment)
* **Bahasa Pemrograman:** Python 3.x
* **Library Utama:** * `opencv-python` (cv2)
    * `numpy` (Manipulasi matriks)
    * `matplotlib` (Visualisasi data)
    * `os` & `sys` (Manajemen sistem & file)
* **Editor:** Jupyter Notebook / VS Code

---

## Cakupan Praktikum
Tahapan koding yang dilakukan mencakup:

1.  **I/O Citra Digital:** Membaca gambar (`cv2.imread`), menampilkan jendela GUI (`cv2.imshow`), dan menyimpan hasil olahan (`cv2.imwrite`).
2.  **Analisis Matriks Gambar:** Membedah properti gambar melalui `.shape` (dimensi), `.size` (total elemen), dan `.nbytes` (alokasi memori RAM), serta membandingkan ukuran file terkompresi (JPEG) dengan data mentah (RAW).
3.  **Ruang Warna (Color Spaces):** Memahami standar BGR di OpenCV dan cara mengonversinya ke RGB untuk visualisasi yang benar di Matplotlib, baik menggunakan metode *Numpy Slicing* `[::-1]` maupun fungsi `cv2.cvtColor`.
4.  **Manipulasi Pixel & Channel:** Mengakses koordinat pixel tertentu dan memisahkan layer warna (Blue, Green, Red) untuk melihat karakteristik intensitas cahaya pada tiap channel.
5.  **Pemrosesan Video:** Membaca file video, mengatur resolusi kamera, dan mengimplementasikan fungsi *real-time* seperti *frame capturing* (screenshot) dan penyimpanan stream video menggunakan *FourCC Codec*.

---

## 🔍 Analisis & Kesimpulan Teknis

Berdasarkan hasil praktikum, berikut adalah poin-poin analisis teknis:

1.  **Representasi Data:** Gambar dalam OpenCV diproses sebagai array multidimensi NumPy. Pemahaman tentang *Slicing* pada NumPy sangat krusial karena manipulasi gambar (seperti cropping atau pengubahan warna) pada dasarnya adalah operasi aritmatika pada matriks.
2.  **Efisiensi Memori:** Terdapat perbedaan signifikan antara ukuran file di disk (terkompresi) dengan ukuran file saat dimuat di RAM (`img.nbytes`). Hal ini penting diperhatikan saat membangun model Machine Learning agar tidak terjadi *Memory Error* ketika menangani dataset gambar berskala besar.
3.  **Perbedaan Standar Warna:** Transisi antara BGR (OpenCV) dan RGB (Matplotlib/Standard) adalah tahap yang sering menyebabkan kesalahan visualisasi. Penggunaan `cv2.cvtColor` lebih disarankan untuk menjaga integritas data daripada manual slicing untuk proyek yang lebih kompleks.
4.  **Karakteristik Video:** Video adalah urutan frame (gambar) yang ditampilkan cepat. Pengaturan `cv2.waitKey()` tidak hanya berfungsi sebagai jeda, tetapi juga sebagai penangkap input *keyboard* yang memungkinkan interaksi pengguna selama program berjalan (seperti menekan 's' untuk simpan foto).

---

## 📽️ Presentasi Video
Demonstrasi lengkap mengenai langkah-langkah praktikum, bedah kodingan baris demi baris, serta simulasi pemrosesan gambar dan video dapat diakses melalui tautan berikut:

👉 [https://youtu.be/y3MRtGKLg18]
