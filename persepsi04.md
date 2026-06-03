# persepsi4: Human perceptual system and its model, 4th meeting

Suara yang dihasilkan microphone bukan murni suara kita, 
namun suara kita dikalikan dengan respon microphone (yang tidak flat)

How to analyze signal?
Non-parametric analysis
Untuk mendapatkan sinyal target digunakan metode tanpa mengasumsikan model tertentu.
Contoh: Y(z) = H(z)X(z) + N(z)
Contoh dalam analisa suara:
- short term autocorrelation analysis
- short term spectral analysis
- cepstrum analysis
- band pass filter bank
- zero cross analysis


Analisis Parametrik
Untuk mendapatkan sinyal target, digunakan model tertentu dimana sinyal target 
bergantung pada model.
Contoh: Y = f(a, b, c, ...)
a, b, c, ... adalah parameter
Contoh dalam analisa suara: source filter model
Suara yang didengar manusia lainnya merupakan gabungan (perkalian) dari
sumber (glottis), filter (resonance) dan radiasi.
Pada sumber suara (glottis) respon yang dihasilkan adalah -12 dB/octave, sedang 
pada radiasi terjadi peningkatan 6 dB/octave, sehingga suara yang diobservasi 
masih menyisakan sekitar -6dB/octave. Dibutuhkan pre-emphasis untuk menganalisa 
suara yang terobservasi ini.

Short term spectral analysis
Resolusi frekuensi waktu:
window lebar: fine structure (source)
window sempit: temporal envolope (filter)

TFS, ENV dan Hilbert
TFS: Temporal Fine Structure
ENV: Temporal Envelope
Hilbert (transform): Untuk memisahkan sinyal suara kedalam TFS dan ENV

Analisis Kepstrum
Kepstrum merupakan spectrum dikalikan dengan log scale
dengan notasi yang sama, maka frekuensi menjadi quefrency, filter menjadi lifter

Analisa Parametrik
AbS: Analysis-by-Synthesis
LPC: Linear Predictive Coding

Analysis/Synthesis system
Vocoder: voice coder

Karasu, naze naku no
Hatsunemiku
It used concatenate speech processing
Ex: /ohayou/ --> /o/ /ha/ /yo/ /u/

data != speech
Data suara mentah belum tentu merepresentasikan struktur produksi wicara. Dalam
analisis wicara, sinyal perlu dipisahkan antara sumber, filter, dan radiasi agar
parameter yang diukur benar-benar berkaitan dengan mekanisme produksi suara.
