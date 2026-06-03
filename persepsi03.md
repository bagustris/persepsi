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

Karakteristik suara
Daya : energi yang ditransmisikan per detik
yang dapat kita rasakan adalah daya, bukan energi.
Intensitas suara
intensitas: daya suara yang ditransmisikan per unit area tiap detik
unit = watt per square meter (w/m^2)
Referensi ambang dengar: I0 = 10^{-12} W/m^2, setara dengan tekanan RMS
sekitar 2 x 10^{-5} N/m^2 atau 20 micro Pa.
 
I = k P^2

Sound level dalam dB
60 dB SPL --> 60 dB lebih tinggi daripada referensi (0dB, intensity of 10^{-6} W/m^2)

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
