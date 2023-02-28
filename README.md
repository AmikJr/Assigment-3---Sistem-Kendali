# Assigment-3---Sistem-Kendali
Nama : Wahyu Micho Indrawan
NIM  : 21/475378/PA/20573

---------------------------------------------------

>> Soal
Create a program code to determine stability using the Routh stability criteria. The 
program must be able to :
1. Returns the value of a polynomial
2. Displays the Routh table
3. Accepts a K value that can be changed via user input

>> Penjelasan
- Dalam kriteria stabilitas Routh, syarat perlu dan cukup agar sistem stabil adalah semua koefisien pada kolom pertama larik Routh memiliki tanda yang sama. Khususnya, jika semua koefisien pada kolom pertama dari larik Routh adalah positif, maka sistem tersebut stabil. Jika semua koefisiennya negatif, maka sistem tersebut juga stabil. Namun, jika ada perubahan tanda pada kolom pertama dari array Routh, maka sistem tidak stabil.

- Dalam kode Python yang diberikan untuk kriteria stabilitas Routh, derajat dan koefisien polinomial karakteristik dapat dimasukkan oleh pengguna. Untuk mendapatkan sistem yang stabil, pengguna harus memasukkan koefisien sedemikian rupa sehingga semua koefisien pada kolom pertama dari array Routh memiliki tanda yang sama (baik semua positif atau semua negatif).

- Dalam percobaannya, sangat sulit menemukan nilai untuk sistem stabil, sebab nilai K harus sama dengan 0. Sedangkan pada program ini, user menginputkan nilai derajat polinomial, koefisien polinomialnya dan nilai K. Sehingga, butuh perhitungan yang benar agar dapat mengisi nilai K. Secara konsep Routh, nilai K tidak harus diisikan (dibiarkan K) maka mudah untuk sistem stabil.
