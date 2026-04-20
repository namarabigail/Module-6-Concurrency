## Commit 1 Reflection notes
Fungsi `handle_connection` pada server ini bertujuan untuk membaca dan memproses data yang dikirimkan oleh browser (TCP Stream). 

Kita menggunakan `BufReader` untuk membaca aliran data tersebut baris per baris secara efisien. Kemudian, kode menggunakan metode seperti `.lines()`, `.map()`, dan `.take_while()` untuk memfilter teks HTTP request sampai menemukan baris kosong, lalu mengumpulkannya menjadi sebuah struktur data `Vec` (Vector) agar bisa dicetak di terminal.

## Commit 2 Reflection notes
Pada versi ini, kita meng-upgrade `handle_connection` agar bisa membaca isi file `hello.html` dan mengembalikannya sebagai respons ke browser. 

Kita juga menambahkan header `Content-Length`. Header ini sangat penting karena memberi tahu browser ukuran pasti dari data (file HTML) yang dikirimkan. Dengan begitu, browser tahu kapan seluruh data telah selesai diunduh dan bisa langsung merendernya ke layar tanpa harus menunggu *connection timeout*.

![Commit 2 screen capture](assets/images/commit2.png)