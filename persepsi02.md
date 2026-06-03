## Bab 2 Pengolahan sinyal auditori

sistem pendengaran:
1. telinga bagian luar
2. telinga bagian tengah
3. telinga bagian dalam

### telinga bagian luar
Komponen telinga bagian luar:
- pinna (daun telinga)
- concha
- ear canal

Fungsi: untuk menekankan suara frekuensi tinggi
yang penting untuk pendengaran spasial (menentukan 
sumber suara dll)


anatomi vs fisiologis sistem pendengaran?
Anatomy approach can be used to organize and name the components.
Physiology approach is used to understand the function of each component.

Suara diindera oleh telinga sebagai tekanan suara (perbedaan tekanan udara), 
informasi ini dikonversi oleh ear drum menjadi vibrasi mekanik menjadi 
basilar membrane motion (BMM) dan akhirnya pulse train (neural firing) di 
auditory nerve.

Elevation dan azimuth (cone of confusion)
A cone-shaped set of points, radiating outwards from a location midway between an organism's ears, from which a sound source produces identical phase delays and transient disparities, making the use of such binaural cues useless for sound localization. Any cross-section of the cone represents a set of points that are equidistant from the left ear and equidistant from the right ear.

Desibel?
Desibel (dB) adalah satuan logaritmik untuk menyatakan rasio antara dua besaran,
misalnya daya atau intensitas suara. Awalan "desi" berarti sepersepuluh (1/10),
sehingga 1 bel = 10 desibel. Skala logaritmik dipakai karena rentang pendengaran
manusia sangat lebar dan persepsi loudness mendekati logaritmik.

Untuk rasio daya/intensitas:
dB = 10 log_{10} (P / P_ref)

dengan P_ref adalah daya/intensitas referensi (misal ambang dengar). Untuk rasio
tekanan suara digunakan faktor 20 karena daya sebanding dengan kuadrat tekanan:
dB = 20 log_{10} (p / p_ref).

Telinga bagian tengah
Fungsi telinga bagian tengah = impedance matching antara air-filled compartment (ear canal) dengan water-filled compartment (cochlea)
So, what is impedance?
Impedansi adalah ukuran hambatan suatu medium terhadap aliran energi (gerak).
Udara memiliki impedansi rendah, sedangkan cairan dalam cochlea memiliki
impedansi tinggi. Tanpa penyesuaian, sebagian besar energi suara akan dipantulkan
pada batas udara-cairan. Telinga tengah (tulang pendengaran dan perbedaan luas
membran timpani vs oval window) berfungsi menyesuaikan kedua impedansi ini agar
energi suara ditransfer secara efisien.
Analogi 1: Rangkaian listrik, impedansi seperti hambatan yang menentukan seberapa
besar arus (energi) yang dapat mengalir; transfer daya maksimum terjadi saat
impedansi sumber dan beban sesuai (matched).
Analogi 2: Berbicara dengan seseorang yang sedang menyelam; suara dari udara sulit
masuk ke air karena perbedaan impedansi yang besar, sehingga sebagian besar
energinya dipantulkan di permukaan air.

Cochlea
In one tube there are two rooms: scala vestibuli dan scala tympani. Di antara
keduanya dipisahkan oleh basilar membrane, di dalam basilar membrane terdapat
organ corti. Di dalam organ corti, terdapat inner hair cell dan outer hair cell.
Oval window and round window saling berhubungan terbalik.

Organ corti
Dua komponen penting organ corti: hair cells dan tectorial membrane.
Rambut yang menyentuh tectorial membrane disebut outer hair cell, sedangkan yang tidak menyentuhnya disebut inner hair cell.
inner hair cell: mengkonversi getaran basilar membrane menjadi neural firing.
Outer hair cell berfungsi untuk stretching ketika basilar membrane aktif (bergetar). Sehingga Outer hair cell bertindak sebagai gain 
atau amplifier dari getaran basilar membrane.

Telinga bagian dalam
Fungsi cochlea --> frequency decomposition
Basilar membrane wave
Traveling wave through high frequency on the base and low frequency on the end.
Analogi, dua orang A dan B memegang tali. Si A menggerakkan tali, agar getaran sampai 
pada B, maka A mengayunkan tali dengan cepat sehingga timbul gelombang berjalan frekuensi tinggi.
Sebaliknya, jika A mengayunkan tali dengan pelan, gelombang tali akan sampai pada B dengan frekuensi rendah.

BBM --> variasi tekanan of 2 rooms
Tuning bassilar membrane motion. Kebalikan dari tuning BMM ini merupakan bandpass filter.
Gammatone filter? Karena distribusi impulse responsenya (transfer function) menyerupai distribusi gamma.

Dari telinga ke otak
Afferent: Peripheral ke auditori korteks
Efferent: otak ke peripheral

Fletcher-Munson curve
Kurva Fletcher-Munson menggambarkan kontur loudness yang sama. Telinga manusia
tidak memiliki sensitivitas yang sama untuk semua frekuensi: pada level rendah,
frekuensi menengah sekitar 2-5 kHz terdengar lebih mudah dibanding frekuensi
sangat rendah atau sangat tinggi. Karena itu, dua suara dengan SPL yang sama
belum tentu dipersepsi sama lantangnya.

Produksi suara
sinyal suara yang kita persepsi terdiri atas tiga: glottis (sumber), resonansi (filter) dan radiasi
F0 berasal glottis
F1, F2 and F3 berasal dari vocal tract

Persepsi suara
Mode pertama dari getaran 100 Hz adalah 200 Hz, mode kedua 300 Hz, dst
Mode-mode itu dinamakan harmonik, jika kita menerapkan inverse Fourier Transform maka akan kita dapatkan x(t)
x(t)=F^{-1} F(\omega) 
Contoh aplikasi: bunyi vokal (A,I, U, E, O) bisa dikenali dari F2-nya.

STFT mengaplikasikan FT pada rentang integral tertentu.

Rujukan visual yang berguna untuk bagian ini adalah animasi sistem auditori,
terutama animasi gelombang berjalan pada basilar membrane dan perubahan tekanan
pada oval window serta round window.
