# persepsi4: Human perceptual system and its model, 4th meeting

Suara yang dihasilkan microphone bukan murni suara kita, namun suara kita
dikalikan dengan respon microphone (yang tidak flat). Karena sinyal yang
terobservasi selalu merupakan hasil interaksi sumber dengan berbagai sistem
(microphone, ruang akustik, dan organ produksi suara), kita memerlukan metode
analisis untuk memisahkan sinyal target dari pengaruh sistem-sistem tersebut.

How to analyze signal?

Analisis non-parametrik
Untuk mendapatkan sinyal target digunakan metode tanpa mengasumsikan model
tertentu. Sebagai contoh, sinyal terobservasi dapat dituliskan dalam domain-z
sebagai

$$Y(z) = H(z)X(z) + N(z)$$

dengan $$X(z)$$ adalah sinyal sumber, $$H(z)$$ respon sistem/kanal, dan $$N(z)$$
derau (noise). Contoh metode non-parametrik dalam analisis suara:
- short-term autocorrelation analysis
- short-term spectral analysis
- cepstrum analysis
- band-pass filter bank
- zero-crossing analysis


Analisis Parametrik
Untuk mendapatkan sinyal target, digunakan model tertentu di mana sinyal target
bergantung pada model:

$$Y = f(a, b, c, \ldots)$$

dengan $$a, b, c, \ldots$$ adalah parameter. Contoh dalam analisis suara adalah
source-filter model. Suara yang didengar manusia lain merupakan gabungan
(perkalian) dari sumber (glottis), filter (resonance), dan radiasi. Pada sumber
suara (glottis) respon yang dihasilkan adalah -12 dB/octave, sedangkan pada
radiasi terjadi peningkatan 6 dB/octave, sehingga suara yang diobservasi masih
menyisakan kemiringan sekitar -6 dB/octave. Karena itu dibutuhkan pre-emphasis
(penguatan frekuensi tinggi) untuk menganalisis suara yang terobservasi ini.

Short term spectral analysis
Analisis spektral jangka pendek dilakukan dengan menerapkan transformasi Fourier
pada potongan sinyal yang dipotong oleh window. Lebar window menentukan trade-off
antara resolusi waktu dan resolusi frekuensi:
- Window lebar (panjang dalam domain waktu) memberi resolusi frekuensi yang halus
  sehingga harmonik individual tampak terpisah. Inilah fine structure yang
  berkaitan dengan sumber (source), misalnya periodisitas getaran glottis.
- Window sempit (pendek dalam domain waktu) memberi resolusi waktu yang baik
  tetapi resolusi frekuensi yang kasar, sehingga yang terlihat adalah selubung
  (envelope) yang berkaitan dengan filter (resonansi vocal tract).

Dengan kata lain, memilih lebar window sama dengan memilih apakah kita ingin
melihat detail sumber atau bentuk umum filter.

TFS, ENV dan Hilbert
- TFS (Temporal Fine Structure): struktur halus sinyal, yaitu osilasi cepat
  (carrier) yang membawa informasi frekuensi sesaat.
- ENV (Temporal Envelope): selubung amplitudo yang berubah lambat dan membungkus
  osilasi cepat tersebut.

Sebuah sinyal suara dapat dipandang sebagai perkalian antara envelope yang lambat
dengan fine structure yang cepat. Transformasi Hilbert dipakai untuk memisahkan
keduanya: dari sinyal asli dibentuk sinyal analitik (analytic signal), magnitude-
nya memberikan envelope sedangkan fase sesaatnya memberikan temporal fine
structure. Pemisahan ini penting secara perseptual karena ENV banyak membawa
informasi untuk pemahaman wicara (terutama pada implan koklea), sedangkan TFS
berperan pada persepsi pitch dan lokalisasi sumber suara.

Analisis Kepstrum
Kepstrum (cepstrum) diperoleh dengan mengambil transformasi Fourier balik dari
logaritma magnitude spektrum sinyal. Operasi log mengubah perkalian antara sumber
dan filter (yang pada spektrum tampak sebagai harmonik rapat termodulasi oleh
selubung formant) menjadi penjumlahan, sehingga komponen sumber dan filter dapat
dipisahkan. Pada kepstrum, komponen filter (selubung spektrum yang berubah lambat)
muncul pada quefrency rendah, sedangkan periodisitas sumber (harmonik) muncul
sebagai puncak pada quefrency tinggi. Karena domainnya "terbalik" dari spektrum,
istilah-istilahnya pun dibalik sebagai permainan kata: spectrum menjadi cepstrum,
frequency menjadi quefrency, filter menjadi lifter (liftering), dan harmonic
menjadi rahmonic.

Analisis parametrik: AbS dan LPC
Pada analisis parametrik, sinyal direpresentasikan oleh sejumlah parameter dari
sebuah model.
- AbS (Analysis-by-Synthesis): parameter dicari dengan cara mensintesis ulang
  sinyal dari model lalu membandingkannya dengan sinyal asli; parameter
  disesuaikan secara iteratif sampai selisih (error) antara sinyal sintesis dan
  sinyal asli sekecil mungkin.
- LPC (Linear Predictive Coding): memodelkan tiap sampel suara sebagai kombinasi
  linear dari beberapa sampel sebelumnya. Koefisien prediksi linear ini
  menggambarkan filter vocal tract (all-pole), sedangkan residu (selisih
  prediksi) merepresentasikan sumber eksitasi. LPC banyak dipakai untuk coding dan
  sintesis wicara karena efisien merepresentasikan source-filter model.

Analysis/Synthesis system
Sistem analysis/synthesis bekerja dalam dua tahap: tahap analisis menguraikan
sinyal suara menjadi parameter (misal parameter eksitasi/sumber dan selubung
spektrum/filter), lalu tahap sintesis membangun kembali suara dari parameter
tersebut. Vocoder (voice coder) adalah contoh klasiknya: ia mengkodekan suara
menjadi parameter yang ringkas untuk transmisi atau penyimpanan, lalu
merekonstruksinya kembali di sisi penerima. Selain untuk coding, vocoder juga
banyak dipakai untuk efek suara dan musik.

Concatenative synthesis: "Karasu, naze naku no" dan Hatsune Miku
"Karasu, naze naku no" (烏 なぜ鳴くの, "gagak, mengapa engkau bersuara") adalah
penggalan lirik lagu anak Jepang (七つの子, Nanatsu no Ko) yang sering dipakai
sebagai contoh sintesis suara nyanyian. Hatsune Miku, perangkat lunak penyanyi
virtual (Vocaloid), menghasilkan suaranya dengan concatenative speech processing,
yaitu menyambung-nyambungkan unit-unit suara terekam (fonem atau suku kata)
menjadi ucapan atau nyanyian yang utuh. Contohnya, kata /ohayou/ dipecah menjadi
unit /o/ /ha/ /yo/ /u/, lalu unit-unit itu disambung kembali dengan penyesuaian
pitch dan durasi sesuai melodi.

data != speech
Data suara mentah belum tentu merepresentasikan struktur produksi wicara. Dalam
analisis wicara, sinyal perlu dipisahkan antara sumber, filter, dan radiasi agar
parameter yang diukur benar-benar berkaitan dengan mekanisme produksi suara.
