# Praktikum Search Algorithm (Search Algorithm)

## 🔎 Deskripsi  
Repository ini berisi implementasi berbagai algoritma pencarian dalam **Python**, meliputi:  

- **Uninformed Search**: DFS, BFS, UCS  
- **Informed Search**: Greedy Best-First Search, A* Tree Search, A* Graph Search  

## 📂 File dalam Repository  
- `dfs.py` → Implementasi Depth First Search  
- `bfs.py` → Implementasi Breadth First Search  
- `ucs.py` → Implementasi Uniform Cost Search  
- `greedy_best_first.py` → Implementasi Greedy Best-First Search  
- `a_star_tree.py` → Implementasi A* Tree Search  
- `a_star_graph.py` → Implementasi A* Graph Search  

## 🚀 Cara Menjalankan di Google Colab  
1. **Clone repository ini ke Google Colab atau komputer lokal**:  


---
## Penjelasan Singkat
## 1. Depth-First Search (DFS)
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
