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
- Dalam kriteria stabilitas Routh, syarat perlu dan cukup agar sistem stabil adalah semua koefisien pada kolom pertama larik Routh memiliki tanda yang sama. Khususnya, jika semua koefisien pada kolom pertama dari larik Routh adalah positif, maka sistem tersebut stabil. Jika semua koefisiennya negatif, maka sistem tersebut juga stabil. Namun, jika ada perubahan tanda pada kolom pertama dari array Routh, maka sistem tidak stabil.

- Dalam kode Python yang diberikan untuk kriteria stabilitas Routh, derajat dan koefisien polinomial karakteristik dapat dimasukkan oleh pengguna. Untuk mendapatkan sistem yang stabil, pengguna harus memasukkan koefisien sedemikian rupa sehingga semua koefisien pada kolom pertama dari array Routh memiliki tanda yang sama (baik semua positif atau semua negatif).

- Dalam percobaannya, sangat sulit menemukan nilai untuk sistem stabil, sebab nilai K harus sama dengan 0. Sedangkan pada program ini, user menginputkan nilai derajat polinomial, koefisien polinomialnya dan nilai K. Sehingga, butuh perhitungan yang benar agar dapat mengisi nilai K. Secara konsep Routh, nilai K tidak harus diisikan (dibiarkan K) maka mudah untuk sistem stabil.

- Contohnya pada gambar berikut, 
  1. <img width="277" alt="image" src="https://user-images.githubusercontent.com/126552366/221918697-8ccab613-8dad-4c27-9237-6a57cf534861.png">
  2. <img width="284" alt="image" src="https://user-images.githubusercontent.com/126552366/221919388-e7816805-1760-43c7-93e9-d010c5e6d79d.png">

