Catatan kuliah "Human perceptual model and its system", pertemuan ke-11.

Pitch dan pemodelannya

Pure tone 100 Hz
Periodic complex tone --> fundamental frequency.

Periodik kompleks tone adalah jumlahan dari tones

Misal, suatu kompleks tone terdiri dari 200, 400, 600 dan 800 Hz.
Sehingga ketika didekomposisi ada lebih dari satu frekuensi: f0, f1, f2, f3, ..., fN.
Frekuensi tersebut dinamakan harmonik. Harmonik berkaitan dengan pitch.

Absolute pitch --> kemampuan telinga musisi untuk menentukan pitch/frekuensi dari suatu nada.

Harmonik
Satu diantara komponen frekuensi pembentuk kompleks tone. Harmonik tidak sama dengan formant.
Harmonik dihasilkan oleh vocal folds, sedangkan formant dihasilkan oleh vocal tract.
Harmonik selalu berulang, sedangkan formant tidak.

Teori persepsi pitch
- Teori tempat (place/spectral): pitch diperkirakan dari lokasi eksitasi pada
  basilar membrane atau dari pola spektral harmonik.
- Teori temporal: pitch diperkirakan dari periode firing atau sinkronisasi
  aktivitas saraf terhadap periode stimulus.

Dalam domain waktu, periode adalah cue yang penting. 
Pada domain frekuensi, bisa saja f0 tidak muncul, sebaliknya hanya frekuensi tengah yang muncul. 
Dalam hal ini, f0 bisa dihitung sebagai selisih antara frekuensi pertama dengan frekuensi kedua.


Periode sinyal dihitung dari selisih antara dua puncak harmonik, misal untuk 500 Hz adalah 2 ms, sedangkan untuk 550 Hz adalah sekitar 1,8 ms.

Limen dinyatakan sebagai persentase dari frekuensi acuan:

$$\text{limen} = \frac{\Delta f}{f} \times 100\%$$

Frekuensi diskriminan
1000 Hz dengan 1002 Hz secara sekuensial maka dapat dibedakan antara frekuensi pertama dengan frekuensi kedua.
Pada frekuensi rendah, misal 150 Hz, perbedaan frekuensi antara dua tone kecil bisa dibedakan, yakni 0.5 Hz.
Sedang pada frekuensi tinggi dibutuhkan beda frekuensi yang besar agar bisa dibedakan.


Phase locking
Penguncian frekuensi yang bisa terjadi pada stimulus dengan frekuensi rendah dan pada temporal envelope.

Missing fundamental
Secara fisis tidak ada frekuensi dasar, tapi bisa dipersepsi.

Mistune
Memindahkan fN lebih tinggi atau lebih rendah (halaman 17). Dari gambar
tersebut yang paling dominan adalah memindah f2 dan f3 agar pitch yang
dipersepsi berbeda.

Apakah ada hubungan antara loudness dengan pitch?
Tidak ada, namun ada penelitian yang mengarah pada hal itu.

Bagaimana mengekstrak f0?
- autokorelasi, jika input merupakan sinyal periodik maka kita bisa mengekstrak periodenya
- zero-crossing, jika input hanya pure tone maka mengekstrak titik di mana $$y = 0$$ dan menghitung selisih antar titik bisa digunakan untuk mencari f0.
- FFT + (autokorelasi)
- peak picking
- cepstrum atau harmonic product spectrum untuk menonjolkan periodisitas harmonik

Namun semua metode tersebut tidak akan bekerja pada sinyal kompleks semisal, speech.
Untuk speech, metode yang baik adalah untuk mengeliminasi efek vocal tract,
sehingga estimasi f0 lebih merepresentasikan sumber glottis. Dalam praktik,
algoritma f0 juga perlu menangani voiced/unvoiced decision, noise, dan formant
yang dapat mengganggu peak picking sederhana.
