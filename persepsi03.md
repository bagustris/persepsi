Ini adalah catatan kuliah I645 Human Perceptual
Systems and its Models yang saya transkrip ketika kuliah berlangsung, pertemuan ketiga.

Sound representations and signal processing

Apakah pendengaran merupakan sistem linear? Tidak
Bagaimana mempelajari pendengaran?
1. Fisiologi auditori
2. Psikoakustik

Auditori Fisiologi
Tentang bagaimana suara diproses oleh sell dan struktur dalam otak dan telinga

Psikoakustik
studi perilaku dari pendengaran, responden diminta memberikan respon atas suara yang diberikan (stimuli)
Pentingnya psikoakustik: Untuk mengkombinasikan eksperimen fisiologis dengan eksperimen 
yang melibatkan perilaku terhadap respon

Suara
Dua pengertian suara yakni sebagai gelombang (waveform) dan sensasi pendengaran (arti psikologis)

Karakteristik suara:
Frekuensi, Amplitudo, Fase

$$ x(t) = A \sin (2 \pi f t + \phi ) $$

Speech vs Voice
Speech (suara ucap/sinyal wicara), suara ucap yang memiliki arti.
Voice (suara), suara yang diproduksi oleh laring.

Persepsi pitch absolute
Musisi bisa mengenali ketidak-adaan satu frekuensi yang hilang dari suatu susunan
Pada telefon, meski terfilter, penerima bisa merasakan sensasi pitch penelfon.

Dekomposisi impulse dan fungsi rektangular
Sinyal apa pun dapat dipandang sebagai penjumlahan (superposisi) dari sinyal-sinyal
sederhana. Pada dekomposisi impulse, sinyal diuraikan menjadi deretan impulse
(delta) tergeser dan terskala; keluaran sistem linear kemudian menjadi penjumlahan
respon impulse-nya (konvolusi). Fungsi rektangular (pulsa persegi) sering dipakai
sebagai window untuk memotong sinyal pada rentang waktu tertentu; spektrum sebuah
fungsi rektangular adalah fungsi sinc, sehingga pemilihan lebar window memengaruhi
resolusi frekuensi pada analisis spektral.

Karakteristik suara
Daya: energi yang ditransmisikan per detik.
Yang dapat kita rasakan adalah daya, bukan energi.
Intensitas suara
Intensitas: daya suara yang ditransmisikan per unit area tiap detik.
Satuannya watt per meter persegi ($$\text{W/m}^2$$).
Referensi ambang dengar: $$I_0 = 10^{-12}~\text{W/m}^2$$, setara dengan tekanan RMS
sekitar $$2 \times 10^{-5}~\text{N/m}^2$$ atau 20 µPa.

$$I = k P^2$$

Sound level dalam dB
60 dB SPL --> 60 dB lebih tinggi daripada referensi (0 dB, intensitas $$10^{-12}~\text{W/m}^2$$).

Fourier Transform
Fourier Transform digunakan untuk mengubah representasi sinyal dari domain waktu
ke domain frekuensi. Dengan transformasi ini, sinyal kompleks dapat dilihat
sebagai penjumlahan komponen sinusoidal dengan frekuensi, amplitudo, dan fase
tertentu.

Untuk sinyal suara yang berubah terhadap waktu, Fourier Transform biasa tidak
cukup karena informasi waktunya hilang. Oleh karena itu digunakan Short-Time
Fourier Transform (STFT), yaitu menerapkan Fourier Transform pada potongan sinyal
pendek menggunakan window.

Filter
Filter digunakan untuk memilih atau menekan komponen frekuensi tertentu.
Jenis-jenis filter yang umum:
- low-pass filter: melewatkan frekuensi rendah dan menekan frekuensi tinggi
- high-pass filter: melewatkan frekuensi tinggi dan menekan frekuensi rendah
- band-pass filter: melewatkan rentang frekuensi tertentu
- band-stop/notch filter: menekan rentang frekuensi tertentu

Dalam sistem pendengaran, basilar membrane dapat dimodelkan sebagai filterbank
yang memisahkan komponen frekuensi suara sebelum diteruskan ke saraf auditori.
