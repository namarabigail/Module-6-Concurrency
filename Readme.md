## Commit 1 Reflection notes
Fungsi `handle_connection` pada server ini bertujuan untuk membaca dan memproses data yang dikirimkan oleh browser (TCP Stream). 

Kita menggunakan `BufReader` untuk membaca aliran data tersebut baris per baris secara efisien. Kemudian, kode menggunakan metode seperti `.lines()`, `.map()`, dan `.take_while()` untuk memfilter teks HTTP request sampai menemukan baris kosong, lalu mengumpulkannya menjadi sebuah struktur data `Vec` (Vector) agar bisa dicetak di terminal.