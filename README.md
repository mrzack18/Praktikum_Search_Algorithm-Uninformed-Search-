# Algoritma Pencarian Graf dan Pohon

Repository ini berisi implementasi berbagai algoritma pencarian yang digunakan dalam pencarian jalur pada graf dan pohon. Algoritma yang disertakan adalah:

- **Depth-First Search (DFS)**
- **Breadth-First Search (BFS)**
- **Uniform Cost Search (UCS)**
- **Greedy Best-First Search**
- **A* (A-Star) Search (Tree & Graph)**

## 1. Depth-First Search (DFS)
### Deskripsi
DFS adalah algoritma pencarian yang menelusuri cabang **sedalam mungkin** sebelum kembali.

### Fitur
- Menggunakan **stack (versi iteratif)** atau **rekursi (versi rekursif)**.
- Cocok untuk eksplorasi hierarki dan analisis graf.
- Bisa mengalami **dead-end**, sehingga perlu strategi backtracking.

### Penggunaan
- Penyelesaian teka-teki seperti Sudoku.
- Pencarian dalam game dan AI.
- Analisis struktur pohon dalam compiler.

---

## 2. Breadth-First Search (BFS)
### Deskripsi
BFS adalah algoritma pencarian yang bekerja dengan menjelajahi **seluruh level** sebelum berpindah ke level berikutnya.

### Fitur
- Menggunakan **struktur queue (FIFO)**.
- Menjamin menemukan **jalur terpendek dalam graf tak berbobot**.
- Mencegah eksplorasi ulang dengan menyimpan node yang telah dikunjungi.

### Penggunaan
- Pencarian jalur dalam labirin atau peta.
- Sistem rekomendasi berbasis hubungan pengguna.

---

## 3. Uniform Cost Search (UCS)
### Deskripsi
UCS mencari jalur dengan biaya total paling kecil tanpa menggunakan heuristik.

### Fitur
- Mirip dengan BFS, tetapi mempertimbangkan **biaya sebenarnya (g(n))**.
- Menjamin jalur **optimal** dalam graf berbobot.
- Menggunakan **priority queue** untuk memilih node dengan biaya terendah.

### Penggunaan
- Algoritma Dijkstra untuk pencarian jalur terpendek.
- Navigasi robot dan perencanaan logistik.

---

## 4. Greedy Best-First Search
### Deskripsi
Greedy Best-First Search memilih **node dengan nilai heuristik terkecil** tanpa mempertimbangkan biaya jalur sebelumnya.

### Fitur
- Menggunakan **heuristik (h(n))** untuk menentukan arah pencarian.
- Lebih cepat dalam beberapa kasus tetapi bisa terjebak di **local minima**.
- Implementasi menggunakan **priority queue**.

### Penggunaan
- Navigasi berbasis AI.
- Sistem rekomendasi berbasis preferensi pengguna.

---

## 5. A* (A-Star) Search (Tree & Graph)
### Deskripsi
A* adalah algoritma pencarian jalur yang menggabungkan **biaya sebenarnya (g(n))** dan **heuristik (h(n))** untuk memperkirakan biaya tersisa ke tujuan. Algoritma ini menggunakan fungsi evaluasi:

\[ f(n) = g(n) + h(n) \]

### Fitur
- Menggunakan **priority queue** untuk memilih node dengan nilai \( f(n) \) terkecil.
- Implementasi dalam **struktur pohon** dan **graf berbobot**.
- Heuristik yang dapat disesuaikan, seperti **jarak Euclidean atau Manhattan**.
- Menampilkan jalur terpendek dan total biaya.

### Penggunaan
- Navigasi dan pathfinding dalam game.
- Perencanaan rute dalam sistem transportasi.

---

## Perbandingan Algoritma

| Algoritma | Karakteristik | Kelebihan | Kekurangan |
|-----------|--------------|-----------|------------|
| **DFS** | Menelusuri secara mendalam terlebih dahulu | Efisien dalam struktur hierarki | Bisa masuk ke loop tak terbatas |
| **BFS** | Mencari jalur secara level-by-level | Menemukan jalur terpendek dalam graf tak berbobot | Tidak efisien pada graf besar |
| **UCS** | Menggunakan biaya aktual tanpa heuristik | Menemukan jalur optimal | Bisa lebih lambat dibandingkan A* |
| **Greedy Best-First** | Memilih berdasarkan nilai heuristik | Cepat dalam kasus tertentu | Tidak selalu menemukan jalur optimal |
| **A*** | Menggunakan biaya jalur + heuristik | Optimal & efisien | Perlu heuristik yang baik |

---

## Cara Menggunakan

1. Pastikan Anda memiliki **Jupyter Notebook** dan Python terinstal.
2. Buka salah satu notebook yang ingin dijalankan, misalnya `bfs.ipynb`.
3. Jalankan sel kode secara berurutan untuk melihat bagaimana algoritma bekerja.
4. Ubah parameter graf atau pohon untuk menguji berbagai skenario.

---
