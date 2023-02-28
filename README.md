# Assigment-3---Sistem-Kendali
by Wahyu Micho Indrawan
---------------------------------------------------

>> Soal

Create a program code to determine stability using the Routh stability criteria. The 
program must be able to :
1. Returns the value of a polynomial
2. Displays the Routh table
3. Accepts a K value that can be changed via user input

>> Penjelasan
- Kode mengambil input dari pengguna dalam bentuk derajat dan koefisien polinomial karakteristik sistem. Fungsi pertama value_polynomial() menerima masukan dari pengguna berupa derajat dan koefisien polinomial. Ini memeriksa apakah tingkat input valid (yaitu bilangan bulat non-negatif) dan meminta pengguna untuk memasukkan koefisien yang sesuai. Ini kemudian mengembalikan daftar koefisien.

- Fungsi kedua routh() mengambil daftar koefisien yang diperoleh dari value_polynomial() sebagai input dan menghasilkan tabel Routh. Tabel Routh adalah array dua dimensi yang berisi koefisien polinomial karakteristik yang disusun dalam pola tertentu. Kolom pertama tabel berisi koefisien pangkat genap s, sedangkan kolom kedua berisi koefisien pangkat ganjil s. Kolom yang tersisa dihitung secara rekursif menggunakan sekumpulan rumus berdasarkan dua kolom pertama. Fungsi routh() menghitung tabel Routh dengan terlebih dahulu menginisialisasi dua kolom pertama tabel. Ini kemudian menggunakan perulangan for untuk menghitung kolom tabel yang tersisa berdasarkan rumus. Jika ada elemen di kolom pertama tabel yang nol, fungsi akan menggantinya dengan nilai kecil (eps) untuk menghindari pembagian dengan nol.

- Fungsi check_stability() memeriksa stabilitas sistem dengan memeriksa kolom pertama dari tabel Routh. Jika semua koefisien pada kolom pertama bertanda sama, maka sistem tersebut stabil. Jika ada koefisien pada kolom pertama adalah nol atau jika tanda-tanda koefisien berganti-ganti, maka sistem tersebut tidak stabil.

- Program utama menggunakan fungsi-fungsi ini untuk mendapatkan tabel Routh dan memeriksa stabilitas sistem. Ini meminta pengguna untuk memasukkan derajat dan koefisien polinomial dan menampilkan tabel Routh dan status stabilitas sistem. Pengguna juga dapat mengubah nilai koefisien (dalam hal ini, K) dan menghitung ulang tabel Routh dan status stabilitas.

- Dalam percobaannya, sangat sulit menemukan nilai untuk sistem stabil, sebab nilai K harus sama dengan 0. Sedangkan pada program ini, user menginputkan nilai derajat polinomial, koefisien polinomialnya dan nilai K. Sehingga, butuh perhitungan yang benar agar dapat mengisi nilai K. Secara konsep Routh, nilai K tidak harus diisikan (dibiarkan K) maka mudah untuk sistem stabil.

- Dalam kriteria stabilitas Routh, syarat perlu dan cukup agar sistem stabil adalah semua koefisien pada kolom pertama larik Routh memiliki tanda yang sama. Khususnya, jika semua koefisien pada kolom pertama dari larik Routh adalah positif, maka sistem tersebut stabil. Jika semua koefisiennya negatif, maka sistem tersebut juga stabil. Namun, jika ada perubahan tanda pada kolom pertama dari array Routh, maka sistem tidak stabil.

- Dalam kode Python yang diberikan untuk kriteria stabilitas Routh, derajat dan koefisien polinomial karakteristik dapat dimasukkan oleh pengguna. Untuk mendapatkan sistem yang stabil, pengguna harus memasukkan koefisien sedemikian rupa sehingga semua koefisien pada kolom pertama dari array Routh memiliki tanda yang sama (baik semua positif atau semua negatif).

- Hasil percobaan sebagai berikut, 
  1. <img width="277" alt="image" src="https://user-images.githubusercontent.com/126552366/221918697-8ccab613-8dad-4c27-9237-6a57cf534861.png">
  2. <img width="284" alt="image" src="https://user-images.githubusercontent.com/126552366/221919388-e7816805-1760-43c7-93e9-d010c5e6d79d.png">

