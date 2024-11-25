# Minggu 12
## Brilyan Satria Wahyuda - TI 3H - 2241720019
<p>
letak Konsep Pola BLoC<br>
Pola BLoC diterapkan melalui beberapa komponen:<br>

1. Logika Bisnis Terpisah di RandomNumberBloc<br>

- Input Stream: _generateRandomController menerima event dari UI untuk memulai proses pembuatan angka acak.
- Output Stream: _randomNumberController menyalurkan angka acak yang dihasilkan ke UI.
- Transformasi Data: Event dari Stream input diproses untuk menghasilkan angka acak dan dikirimkan ke Stream output.

2. Interaksi UI dengan Stream

- Input Event: Tombol (FloatingActionButton) memanggil _bloc.generateRandom.add(null) untuk memberikan event ke Stream input.
- Output Display: Widget StreamBuilder mendengarkan perubahan data pada Stream output (_bloc.randomNumber) dan memperbarui UI dengan angka terbaru.

3. Pengelolaan Resource dengan dispose

- Metode dispose di RandomNumberBloc memastikan StreamController ditutup saat tidak digunakan lagi, sehingga menghindari kebocoran memori.</p>

Berikut adalah hasil run
![hasilrun](hasilrun.gif)#   b l o c _ r a n d o m _ B r i l y a n  
 