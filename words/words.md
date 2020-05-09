<div class="section">
    <div>
    	<iframe id="splash" width="960" height="480" src="banners/splash.html"></iframe>
        <div style="top: 70px;font-size: 75px;font-weight: bold;">
        	Apa Yang Terjadi Selanjutnya?
       	</div>
		<div style="font-weight: 500;top: 140px;left: 10px;font-size: 29px;">
			Masa Depan COVID-19, Dijelaskan Dengan Simulasi Interaktif
		</div>
		<div style="font-weight: 100;top: 189px;left: 10px;font-size: 19px;line-height: 21px;">
			<b>
				🕐 Waktu baca/interaksi: 30 menit
				&nbsp;&middot;&nbsp;
			</b>
			by
			<a href="https://scholar.google.com/citations?user=_wHMGkUAAAAJ&amp;hl=en">Marcel Salathé</a>
			(epidemiologis)
			&
			<a href="https://ncase.me/">Nicky Case</a>
			(desain/kode)
		</div>
	</div>
</div>

"Satu-satu hal yang ditakuti adalah rasa takut itu sendiri" adalah saran yang bodoh.

Tentu, tak perlu menimbun tisu toilet - namun jika pembuat kebijakan takut dengan rasa takutnya sendiri, mereka meremehkan bahaya sebenarnya untuk menghindari "kepanikan massal". Takut itu bukan masalahnya, namun bagaimana kita *menyalurkan* rasa takut kita. Takut memberikan kita kekuatan untuk menghadapi bahaya saat ini, dan mempersiapkan diri untuk bahaya di masa depan.

Sejujurnya, kami (Marcel, epidemiologis + Nicky, desain/kode) khawatir. Kami yakin Anda juga! Itu mengapa kami menyalurkan rasa takut kami dengan membuat **simulasi interaktif**, sehingga *Anda* bisa menyalurkan rasa takut dengan memahami:

* **Beberapa Bulan yang Lalu** (epidemiologi 101, mode SEIR, R & R<sub>0</sub>)
* **Beberapa Bulan yang Akan Datang** (karantina, pelacakan kontak, masker)
* **Beberapa Tahun yang Akan Datang** (hilangnya imunitas? tidak ada vaksin?)

Panduan ini (diterbitkan pada 1 Mei 2020. klik catatan kaki ini!→[^timestamp]) dibuat untuk memberimu harapan *dan* rasa takut. Untuk melawan COVID-19 **sekaligus melindungi kesehatan mental dan finansial kita**, kita perlu optimisme untuk membuat berbagai rencana, dan rasa pesimis untuk membuat rencana cadangan. Seperti yang Gladys Bronwyn Stern pernah katakan, *“The optimist invents the airplane and the pessimist the parachute.”* yang berarti *"Seseorang yang optimis menciptakan pesawat terbang dan yang pesimis hanya menciptakan parasut"*

[^timestamp]: Catatan kaki ini akan berisi sumber, tautan, dan komentar tambahan. Sukai komentar ini!
    
    **Panduan ini diterbitkan pada 1 Mei 2020.** Banyak rincian yang akan kedaluarsa, namun kami yakin panduan ini akan melingkupi 95% dari kemungkinan masa depan, dan Pengenalan Epidemologi akan tetap bermanfaat selamanya.
    
Jadi, bersiaplah: kita akan mulai perjalanan dengan turbulensi.

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>Beberapa Bulan yang Lalu</div>
    </div>
</div>

Pilot menggunakan simulator penerbangan untuk mempelajari bagaimana agar pesawat tidak jatuh.

**Ahli epidemiologi menggunakan simulator epidemi untuk mempelajari bagaimana agar ras manusia tidak jatuh**

Jadi, mari kita buat "simulator penerbangan epidemi" yang sangat, *sangat* sederhana! Dalam simulasi ini, <icon i></icon> Orang yang Menginfeksi dapat mengubah <icon s></icon> Orang yang Rentan menjadi lebih banyak <icon i></icon> Orang yang Menginfeksi:

![](pics/spread.png)

Diperkirakan bahwa, *pada awal* penjangkitan COVID-19, virus melompat dari <icon i></icon> ke <icon s></icon> setiap 4 hari, *rata-rata*.[^serial_interval] (ingat, ada banyak variasinya)

[^serial_interval]: “Interval [serial] rata-rata adalah 3,96 hari (95% CI 3,53–4,39 hari)”. [Du Z, Xu X, Wu Y, Wang L, Cowling BJ, Ancel Meyers L](https://wwwnc.cdc.gov/eid/article/26/6/20-0357_article) (Catatan: Artikel yang dirilis lebih awal tidak dianggap sebagai versi akhir)

Jika kita mensimulasikan "kasus menjadi ganda setiap 4 hari" *dan tidak ada lagi*, dalam sebuah populasi dimulai dengan hanya 0,001% <icon i></icon>, apa yang terjadi? 

**Klik "Mulai" untuk memainkan simulasi! Anda dapat memainkannya ulang nanti dengan pengaturan berbeda**
**Click "Start" to play the simulation! You can re-play it later with different settings:** (peringatan teknis: [^caveats])

[^caveats]: **Ingat: semua simulasi ini sudah sangat disederhanakan, untuk keperluan edukasi.**
    
    Satu penyederhanaan: Ketika Anda memberitahu simulasi ini "Infeksi 1 orang baru setiap X hari", ini sebenarnya meningkatkan jumlah dari yang Menginfeksi dengan 1/x setiap harinya. Hal yang sama untuk pengaturan masa depan dari simulasi ini - "Sembuh setiap X hari" sebenarnya mengurangi sejumlah orang Menginfeksi dalam 1/X setiap harinya.
    
    Hal ini *tentu* tidak sama persis, namun hampir mendekati, dan untuk keperluan edukasi ini tidak lebih samar daripada mengatur tingkat transmisi/pemulihan secara langsung.

<div class="sim">
		<iframe src="sim?stage=epi-1" width="800" height="540"></iframe>
</div>

Ini adalah **kurva pertumbuhan eksponensial.** Awalnya sedikit, kemudian meledak. Dari "Oh ini hanya flu kok" menjadi "Oh iya, flu tidak membuat *kuburan massal di kota-kota besar*". 

![](pics/exponential.png)

Tetapi, simulasi ini kurang tepat. Untungnya, pertumbuhan eksponensial tidak berjalan selamanya. Satu hal yang menghentikan virus untuk menyebar adalah jika orang-orang *sudah* terjangkiti virus:

![](pics/susceptibles.png)

Semakin banyak <icon i></icon> bermunculan, semakin cepat <icon s></icon> berubah menjadi <icon i></icon>, **namun semakin sedikit <icon s></icon>, semakin *lambat* <icon s></icon> berubah menjadi <icon i></icon>.**

Bagaimana ini mengubah pertumbuhan sebuah epidemi? Mari kita cari tahu:

<div class="sim">
		<iframe src="sim?stage=epi-2" width="800" height="540"></iframe>
</div>

Ini adalah **kurva S pertumbuhan logistik**. Awalnya kecil, meledak, kemudian kembali melambat.

Namun, simulasi ini *masih* keliru. Kita kehilangan fakta bahwa <icon i></icon> Orang yang Menginfeksi secara berkala akan berhenti menularkan, antara dengan menjadi 1) sembuh, 2) "sembuh" dengan kerusakan paru, atau 3) sekarat.

Untuk menyederhanakannya, kita anggap kalau semua <icon i></icon> orang yang Menginfeksi berubah menjadi <icon r></icon> Sembuh. (Cukup ingat bahwa kenyataannya, beberapa di antaranya meninggal dunia.) <icon r></icon> tidak dapat ditulari lagi, dan mari kita anggap - *untuk sekarang!* - bahwa mereka tetap imun sepanjang hidupnya.

Dengan COVID-19, diperkirakan Anda <icon i></icon> menjadi orang yang Menginfeksi dalam 10 hari, *rata-rata*.[^penularan] Ini berarti beberapa orang akan sembuh sebelum 10 hari, yang lainnya lebih dari itu. **Seperti ini lah tampilannya, dengan sebuah simulasi *dimulai* dengan 100% <icon i></icon>:**

[^penularan]: “Angka median periode komunikasi \[...\] adalah 9,5 hari.” [Hu, Z., Song, C., Xu, C. et al](https://link.springer.com/article/10.1007/s11427-020-1661-4) Ya, kita tahu "angka median" tidak sama dengan "rata-rata". Untuk keperluan edukasi sederhana, ini cukup mendekati.

<div class="sim">
		<iframe src="sim?stage=epi-3" width="800" height="540"></iframe>
</div>

Ini adalah **kurva kehilangan eksponensial**, lawan dari pertumbuhan eksponensial.

Sekarang, apa yang terjadi jika Anda mensimulasikan kurva S logistik pertumbuhan *dengan* kesembuhan?

![](pics/graphs_q.png)

Mari kita cari tahu.

<b style='color:#ff4040'>Kurva merah</b> adalah kasus *saat ini* <icon i></icon>,    
<b style='color:#999999'>Kurva abu</b> adalah kasus *total* (kasus saat ini + kasus sembuh <icon r></icon>),
dimulai dengan hanya 0,001% <icon i></icon>:

<div class="sim">
		<iframe src="sim?stage=epi-4" width="800" height="540"></iframe>
</div>

Dan *itulah* asal di mana kurva terkenal tersebut muncul! Ini bukan kurva lonceng, bahkan bukan kurva "log-normal". Kurva ini tidak ada namanya. Tetapi Anda sudah melihatnya berjuta-juta kali, dan memohon-mohon agar kurva menjadi rata.

Ini adalah **Model SIR**,[^sir]    
(<icon s></icon>**S**usceptible/Kelas Rentan <icon i></icon>**I**nfectious/Kelas Terinfeksi <icon r></icon>**R**ecovered/Kelas Sembuh)      
gagasan paling penting kedua di Pengenalan Epidemiologi:

[^sir]: Untuk penjelasan Model SIR yang lebih teknis, lihat [the Institute for Disease Modeling](https://www.idmod.org/docs/hiv/model-sir.html#) dan [Wikipedia](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SIR_model)

![](pics/sir.png)

**CATATAN: Simulasi yang menginformasikan kebijakan itu jauh, *jauh* lebih canggih daripada ini!** Namun model SIR masih dapat menjelaskan temuan umum, walaupun jika kehilangan nuansanya.

Sebenarnya, mari kita tambahkan satu nuansa lain: sebelum seorang <icon s></icon> berubah menjadi <icon i></icon>, pertama-tama mereka berubah menjadi <icon e></icon> orang yang Terekspos. Ini adalah ketika mereka memiliki virus di tubuhnya namun belum dapat mengopernya ke orang lain - *ter*infeksi namun belum dapat *meng*infeksi.

![](pics/seir.png)

(Varian ini disebut sebagai **model SEIR**[^seir], di mana "E" berarti <icon e></icon> "Kelas Terekspos". Mohon dicatat bahwa ini *bukan* arti umum dari "terekspos", ketika Anda mungkin atau tidak memiliki virus. Dalam pengertian teknis, "Terekspos" berarti Anda benar-benar memiliki virusnya. Terminologi sains memang buruk.)

[^seir]: Untuk penjelasan Model SEIR yang lebih teknis, lihat, lihat [the Institute for Disease Modeling](https://www.idmod.org/docs/hiv/model-seir.html) dan [Wikipedia](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SEIR_model)

Untuk COVID-19, diperkirakan bahwa Anda menjadi <icon e></icon> orang yang terinfeksi namun belum menginfeksi dalam waktu 3 hari, *dalam rata-rata*.[^latent] Apa yang terjadi jika kita menambahkannya ke dalam simulasi?

[^latent]: “Dengan asumsi distribusi periode inkubasi rata-rata 5,2 hari dari studi terpisah kasus COVID-19 awal, kami menyimpulkan bahwa infeksi dimulai dari 2,3 hari (95% CI, 0,8-3,0 hari) sebelum timbulnya gejala” (translation: Dengan asumsi gejala dimulai pada 5 hari, infeksi dimulai 2 hari sebelumnya = Infeksi dimulai pada 3 hari) [He, X., Lau, E.H.Y., Wu, P. et al.](https://www.nature.com/articles/s41591-020-0869-5)

<b style='color:#ff4040'>Kurva Merah <b style='color:#FF9393'>+ Merah Muda</b></b> adalah kasus *saat ini* (Kelas Terinfeksi <icon i></icon> + Kelas Terekspos <icon e></icon>),    
<b style='color:#888'>Kurva Abu</b> adalah kasus *total* (saat ini + Kelas Sembuh <icon r></icon>):

<div class="sim">
		<iframe src="sim?stage=epi-5" width="800" height="540"></iframe>
</div>

Tidak banyak pengubahan! Seberapa lama Anda tetap menjadi <icon e></icon> Kelas Terekspos mengubah laju pengubahan dari <icon e></icon>-ke-<icon i></icon>, dan *ketika* kasus saat ini memuncak... tetapi *ketinggian* puncak, dan total kasus pada akhirnya, tetap sama.

Mengapa bisa begitu? Ini dikarenakan oleh gagasan *pertama* dan paling penting dalam Pengenalan Epidemiologi:

![](pics/r.png)

Kependekan dari "angka Reproduksi". Ini adalah angka *rata-rata* orang yang seorang <icon i></icon> infeksi *sebelum* mereka sembuh (atau meninggal dunia).

![](pics/r2.png)

**R** berubah selama wabah, sepanjang kita mendapatkan lebih banyak imunitas & intervensi.

**R<sub>0</sub>** (diucapkan sebagai R-nought) adalah nilai R *pada permulaan penyebaran wabah, sebelum imunitas atau intervensi*. R<sub>0</sub> secara lebih dekat merefleksikan kekuatan virus itu sendiri, namun masih dapat berubah dari lokasi ke lokasi. Sebagai contoh, R<sub>0</sub> di kota-kota berkepadatan tinggi lebih tinggi daripada area pedesaan berkepadatan rendah.

(Mayoritas artikel berita – dan bahkan beberapa artikel ilmiah! – kebingungan antara R dan R<sub>0</sub>. Sekali lagi, terminologi sains memang buruk.)

R<sub>0</sub> untuk flu musiman itu sekitar 1,28[^r0_flu]. Ini berarti, pada saat *permulaan* wabah flu, setiap <icon i></icon> menginfeksi 1,28 orang lainnya *rata-rata* (Jika ini terdengar aneh bahwa ini bukan angka bulat, ingat bahwa "rata-rata" seorang ibu memiliki 2,4 anak. Hal ini bukan berarti ada setengah anak di tengah masyarakat.)

[^r0_flu]: “Angka R median untuk influenza musiman adalah 1,28 (IQR: 1,19–1,37)” [Biggerstaff, M., Cauchemez, S., Reed, C. et al.](https://bmcinfectdis.biomedcentral.com/articles/10.1186/1471-2334-14-480)

Nilai R<sub>0</sub> untuk COVID-19 diperkirakan sekitar 2,2 ,[^r0_covid] walaupun sebuah studi *yang belum difinalisasi* memperkirakan nilainya 5,7(!) di Wuhan.[^r0_wuhan]

[^r0_covid]: “Kami memperkirakan angka reproduksi dasar R0 dari 2019-nCoV berkisar 2,2 (90% interval berkepadatan tinggi: 1,4–3,8)” [Riou J, Althaus CL.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7001239/)

[^r0_wuhan]: “kami menghitung nilai median R0 sebesar 5,7 (95% CI 3,8–8,9)” [Sanche S, Lin YT, Xu C, Romero-Severson E, Hengartner N, Ke R.](https://wwwnc.cdc.gov/eid/article/26/7/20-0282_article)

Dalam simulasi kami - *pada permulaan & rata-rata* – seorang <icon i></icon> menginfeksi orang lain setiap 4 hari, selama 10 hari. "4 hari" dalam "10 hari" menjadi dua-setengah kali. Ini berarti - *pada permulaan & rata-rata* - setiap <icon i></icon> menginfeksi 2,5 orang lainnya. Sehingga, nilai R<sub>0</sub> = 2,5. (caveats:[^r0_caveats_sim])

[^r0_caveats_sim]: Ini berpura-pura bahwa Anda sama-sama menular di seluruh "periode menular" Anda. Sekali lagi, penyederhanaan untuk tujuan pendidikan.

**Mainkan dengan kalkulator R<sub>0</sub> ini, untuk melihat bagaimana R<sub>0</sub> bergantung pada waktu penyembuhan dan waktu infeksi baru:**

<div class="sim">
		<iframe src="sim?stage=epi-6a&format=calc" width="285" height="255"></iframe>
</div>

Tapi ingat, semakin sedikit <icon s></icon> berada, semakin *melambat* <icon s></icon> berubah menjadi <icon i></icon>. Angka reproduksi *saat ini* (R) bergantung tidak hanya pada angka reproduksi *dasar* (R<sub>0</sub>), namun *juga* bergantung pada berapa banyak orang yang tidak lagi termasuk <icon s></icon> Kelas Rentan. (Contohnya, mereka yang sembuh & mendapatkan imunitas secara alami.)

<div class="sim">
		<iframe src="sim?stage=epi-6b&format=calc" width="285" height="390"></iframe>
</div>

Ketika cukup banyak orang yang memiliki kekebalan, R<1, dan virusnya terkandung! Ini disebut ***herd immunity*** atau **kekebalan kawanan**. Untuk flu, kekebalan kawanan dicapai *dengan vaksin*. Usaha untuk mencapai "kekebalan kawanan alami" dengan membiarkan orang terinfeksi adalah gagasan *mengerikan*. (Tapi tidak untuk alasan yang mungkin kau pikirkan! Kami akan menjelaskannya nanti.)

Sekarang, mari kita mainkan Model SEIR lagi, namun sekarang menampilkan nilai R<sub>0</sub>, R sepanjang waktu, dan ambang batas kekebalan kawanan:

<div class="sim">
		<iframe src="sim?stage=epi-7" width="800" height="540"></iframe>
</div>

**CATATAN: Angka total kasus *tidak berhenti* pada kekebalan kawanan, namun melampaui dari itu!** Dan angka tersebut melewati ambang batas *tepat* ketika kasus saat ini memuncak. (Hal ini akan terjadi bagaimanapun Anda mengubah pengaturannya - coba saja sendiri!)

Ini karena ketika ada lebih banyak orang non-<icon s></icon> daripada ambang batas kekebalan kawanan, Anda mendapati R < 1. Dan ketika R < 1, kasus baru berhenti bertambah: inilah puncak.

**Jika ada hanya satu pelajaran yang bisa Anda petik dari panduan ini, ini dia** - ini adalah diagram yang sangat amat rumit sehingga silakan ambil waktu Anda untuk memahami sepenuhnya:
**If there's only one lesson you take away from this guide, here it is** – it's an extremely complex diagram so please take time to fully absorb it:

![](pics/r3.png)

**Ini berarti: kita TIDAK perlu menangkap semua penularan, atau hampir mendekat semua penularan, untuk menghentikan COVID-19!**

Ini adalah sebuah paradoks. COVID-19 sangatlah menular, bahkan untuk mengekangnya, kita "hanya" perlu menghentikan lebih dari 60% infeksi. 60%?! Jika angka itu dianggap nilai rapor sekolah, pasti tergolong nilai D-. Tetapi jika R<sub>0</sub> = 2,5, memotongnya hingga 61% dapat menghasilkan nilai R = 0,975, yang berarti R < 1, virus berhasil dikekang! (rumus tepatnya:[^rumus_tepat])

[^rumus_tepat]: Ingat R = R<sub>0</sub> * rasio penularan yang dibolehkan. Ingat juga bahwa rasio penularan yang dibolehkan = 1 - rasio penularan yang *dihentikan*.
    
    Sehingga, untuk mendapatkan R < 1, Anda perlu untuk mendapatkan R<sub>0</sub> * PenularanYangDiperbolehkan < 1. 
    
    Maka, PenularanYangDiperbolehkan < 1/R<sub>0</sub>
    
    Maka, 1 - PenularanYangDihentikan < 1/R<sub>0</sub>
    
    Maka, PenularanYangDihentikan > 1 - 1/R<sub>0</sub>
    
    Maka, Anda perlu menghentikan lebih dari **1 - 1/R<sub>0</sub>** dari penularan untuk mendapatkan R < 1 dan virus dikekang!
    
![](pics/r4.png)

(Jika Anda pikir R<sub>0</sub> atau angka lainnya di dalam simulasi kami terlalu rendah/tinggi, pertanda bagus karena Anda menantang asumsi kami! Nanti akan ada "Mode Sandbox" pada akhir panduan ini, di mana Anda bisa mematok angka Anda *sendiri*, dan mensimulasikan apa yang terjadi.)

*Setip* intervensi COVID-19 yang Anda dengar - cuci tangan dengan sabun, jaga jarak, karantina wilayah, isolasi mandiri, pelacakan kontak, penggunaan masker, bahkan "imunitas kawanan" - itu *semua* dilakukan untuk hal yang sama:

Mendapatkan nilai R < 1.

Jadi sekarang, mari kita gunakan "simulasi penerbangan epidemi" kami untuk memecahkan masalah ini: Bagaimana kita bisa mendapatkan nilai R < 1 dengan cara **yang sekaligus melindungi kesehatan mental *dan* finansial kita?**

Siapkan diri Anda untuk pendaratan darurat...

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>Beberapa Bulan Kemudian</div>
    </div>
</div>

...bisa menjadi lebih buruk. Inilah jagad raya paralel yang kita hindari:

###Skenario 0: Tidak Melakukan Apa-apa

Sekitar 1 dari 20 orang yang terinfeksi COVID-19 perlu dibawa ke ICU (Intensive Care Unit).[^icu_covid] Di negara makmur seperti AS, ada 1 kasur ICU per 3400 orang.[^icu_us] Oleh karena itu, AS dapat menangani 20 dari 3400 orang yang *secara simultan* terinfeksi - atau, 0,6% dari total populasi.

[^icu_covid]: ["Persentase kasus COVID-19 di Amerika Serikat pada 12 Februari hingga 16 Maret 2020 yang dimasukkan ke *intensive care unit*, menurut kelompok umur"](https://www.statista.com/statistics/1105420/covid-icu-admission-rates-us-by-age-group/). Antara 4,9% hingga 11,5% dari *semua* kasus COVID-19 memerlukan ICU. Between 4.9% to 11.5% of *all* COVID-19 cases required ICU. Dengan murah hati memilih kisaran yang lebih rendah, yaitu 5% atau 1 dari 20. Perhatikan bahwa total ini khusus untuk struktur usia AS, dan akan lebih tinggi di negara-negara dengan populasi yang lebih tua, lebih rendah di negara-negara dengan populasi yang lebih muda.

[^icu_us]: “Total kasur ICU = 96.596”. Dari [the Society of Critical Care Medicine](https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19) Populasi AS adalah 328.200.000 pada tahun 2019. 96.596 dari 328.200.000 = sekitar 1 per 3400. 

Bahkan jika kita *lebih dari tiga kali lipatkan* kapasitas itu menjadi 2%, inilah apa yang terjadi *jika kita tidak melakukan apa-apa:*

<div class="sim">
		<iframe src="sim?stage=int-1&format=lines" width="800" height="540"></iframe>
</div>

Tidak bagus.

Itulah apa yang [laporan Imperial College per 16 Maret](http://www.imperial.ac.uk/mrc-global-infectious-disease-analysis/covid-19/report-9-impact-of-npis-on-covid-19/) temukan: tidak melakukan apa-apa, dan kita kehabisan slot ICU, dengan lebih dari 80% terinfeksi. 
(ingat: total kasus *melampaui* imunitas kawanan)

Bahkan jika hanya 0,5% yang terinfeksi meninggal dunia - sebuah asumsi murah hari ketika tidak ada lagi ICU - di negara besar seperti AS, dengan 300 juta orang, 0,5% dari 80% dari 300 juta = masih ada 1,2 juta orang meninggal dunia... *JIKA kita tidak melakukan apa-apa*

(Banyak sekali berita & media sosial mengabarkan "80% akan terinfeksi" *tanpa* "JIKA KITA TIDAK MELAKUKAN APA-APA". Rasa takut disalurkan melalui setiap kliknya, bukan dalam setiap pemahaman beritanya. *Heu.*)

###Skenario 1: Ratakan Kurvanya / Imunitas Kawanan

Rencana "Ratakan Kurvanya" digaungkan oleh setiap organisasi kesehatan masyarakat, sementara rencana awal "imunitas kawanan" milik Inggris Raya dicemooh banyak orang. Keduanya adalah *rencana yang sama*. Hanya saja mereka mengomunikasikannya dengan sangat buruk.[^yong]

[^yong]: “Dia mengatakan bahwa tujuan sebenarnya adalah sama dengan tujuan negara lain: ratakan kurva dengan cara mengejutkan infeksi. Sebagai konsekuensinya, bangsa dapat mencapai kekebalan kelompok; itu adalah efek samping, bukan tujuan. [...] Rencana tindakan coronavirus aktual pemerintah, tersedia online, tidak menyebutkan kekebalan kawanan sama sekali. "
    
    Dari sebuah [artikel The Atlantic oleh Ed Yong](https://www.theatlantic.com/health/archive/2020/03/coronavirus-pandemic-herd-immunity-uk-boris-johnson/608065/)

Mesikpun begitu, kedua rencana benar-benar memiliki kelemahan yang fatal.

Pertama, mari kita lihat pada dua cara utama untuk "meratakan kurva": cuci tangan dengan sabun dan menjaga jarak.

Rajin mencuci tangan dapat memotong kasus flu & demam di negara berpenghasilan tinggi hingga ~25%[^handwashing], sementara karantina satu kota penuh di London memotong interaksi kontak dekat menjadi ~70%[^london]. Jadi, mari kita asumsikan tindakan cuci tangan dapat mengurangi nilai R *hingga* 25%, dan menjaga jarak dapat menurunkan nilai R *hingga* 70%:

[^handwashing]: “Semua delapan studi yang memenuhi syarat melaporkan bahwa mencuci tangan menurunkan risiko infeksi pernapasan, dengan pengurangan risiko berkisar dari 6% hingga 44% [nilai gabungan 24% (95% CI 6–40%)].” Kami mengumpulkan nilai gabungan hingga 25% dalam simulasi ini untuk penyederhanaan. [Rabie, T. dan Curtis, V.](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1365-3156.2006.01568.x) Catatan: seperti yang ditunjukkan oleh meta-analisis ini, kualitas studi untuk mencuci tangan (setidaknya di negara-negara berpenghasilan tinggi) sangat buruk.

[^london]: “Kami menemukan pengurangan 73% dalam rata-rata jumlah kontak harian yang diamati per peserta. Ini akan cukup untuk mengurangi R0 dari nilai dari 2,6 sebelum penguncian ke 0,62 (0,37 - 0,89) selama penguncian ". Kami membulatkannya menjadi 70% dalam simulasi ini untuk penyederhanaan. [Jarvis dan Zandvoort et al](https://cmmid.github.io/topics/covid19/comix-impact-of-physical-distance-measures-on-transmission-in-the-UK.html)

**Coba mainkan dengan kalkulator ini untuk melihat berapa % dari non-<icon s></icon>, mencuci tangan, dan menjaga jarak mengurangi nilai R:** (kalkulator ini memvisualisasikan efek *relatifnya*, itulah sebabnya meningkatkan salah satu *terlihat* seperti itu mengurangi efek lainnya.[^log_caveat])

[^log_caveat]: Distorsi ini akan hilang jika kita merencanakan R pada skala logaritmik .. tetapi kemudian kita malah harus menjelaskan *skala logaritmik.*

<div class="sim">
		<iframe src="sim?stage=int-2a&format=calc" width="285" height="260"></iframe>
</div>

Sekarang, mari kita simulasikan apa yang terjadi pada epidemi COVID-19 jika, mulai Maret 2020, kita telah meningkatkan cuci tangan tetapi hanya *menjaga jarak* tingkat ringan - sehingga nilai R lebih rendah, tetapi masih di atas 1:

<div class="sim">
		<iframe src="sim?stage=int-2&format=lines" width="800" height="540"></iframe>
</div>

Tiga catatan:

1. Hal ini *mengurangi* total kasus! **Bahkan jika Anda tidak mendapati nilai R < 1, mengurangi nilai R masih dapat menyelamatkan banyak jiawa, dengan mengurangi 'pelampauan' di atas imunitas kawanan.** Banyak kawan berpikir usaha "Meratakan Kurva" menyebarkan kasus tanpa menurunkan nilai total. Hal ini tidak mungkin terjadi di model Pengenalan Epidemiologi *manapun*. Namun karena berita mengabarkan "80%+ akan terinfeksi" tak dapat dihindari, kawan-kawan berpikiran bahwa total kasus akan tetap sama apapun yang terjadi. *Sigh.*

2. Dikarenakan intervensi ekstra, kasus saat ini memuncak *sebelum* imunitas kawanan dicapai. Faktanya, dalam simulasi ini, total kasus hanya melampaui *sedikit saja* di atas imunitas kawanan - sesuai rencana Inggris Raya! Pada titik itu, nilai R < 1, Anda dapat melepaskan segala macam intervensi, dan COVID-19 tetap dikekang! Yah, kecuali ada satu masalah...

3. Anda masih kekurangan ruang ICU. Untuk beberapa bulan. (dan ingat, kita *sudah* menambahkan jumlah ICU hingga tiga kali lipat untuk simulasi-simulasi ini.

Itu adalah temuan lapin dari laporan Imperial College tanggal 16 Maret, yang menyakinkan Inggris Raya untuk mengabaikan rencana awalnya. Segala usaha **mitigasi** (mengurangi nilai R, namun R > 1) akan gagal. Satu-satunya jalan keluar adalah **penekanan** (mengurangi nilai R hingga R < 1).

![](pics/mitigation_vs_suppression.png)

Artinya, jangan hanya "meratakan" kurva, *hancurkan* kurvanya. Misalnya, dengan ...

###Skenario 2: Karantina Wilayah Berbulan-bulan

Mari kita lihat apa yang terjadi jika kita *rusak* kurvanya dengan karantina wilayah selama 5 bulan, mengurangi <icon i></icon> sampai habis, kemudian akhirnya - *akhirnya* - kembali ke kehidupan yang normal:

<div class="sim">
		<iframe src="sim?stage=int-3&format=lines" width="800" height="540"></iframe>
</div>

Oh.

Inilah "gelombang kedua" yang dibicarakan banyak orang. Segera setelah kita mengakhiri karantina wilayah, kita akan mendapatkan nilai R > 1 lagi. Jadi, sedikit sisa kelompok <icon i></icon> (atau kelompok <icon i></icon> yang diimpor dari tempat lagi) dapat menyebabkan lonjakan dalam kasus yang hampir seburuk dengan jika kita melakukan Skenario 0: Tidak Melakukan Apa-apa.

**Karantina wilayah bukanlah obatnya, hanya sebuah pengulangan kembali.**

Jadi, apakah, kita perlu lakukan karantina wilayah lagi dan lagi?

###Skenario 3: Karantina Wilayah Berselang-seling

Solusi ini pertama kali disarankan oleh laporan Imperial College per tanggal 16 Maret, dan diusulkan lagi oleh sebuah artikel ilmiah dari Harvard.[^lockdown_harvard]

[^lockdown_harvard]: “Tidak ada intervensi lain, metrik kunci untuk keberhasilan pembatasan sosial adalah apakah kapasitas perawatan kritis terlampaui. Untuk menghindari ini, pembatasan sosial yang lama atau berselang mungkin diperlukan hingga tahun 2022.” [Kissler dan Tedijanto et al](https://science.sciencemag.org/content/early/2020/04/14/science.abb5793)

**Ini simulasinya:** (Setelah memainkan sebuah "skenario terekam", Anda dapat coba mensimulasikan jadwal karantina wilayah Anda *sendiri*, dengan mengubah slider *ketika* simulasi berjalan! Ingat, Anda dapat menjeda & melanjutkan simulasi, dan mengubah kecepatan simulasi)

<div class="sim">
		<iframe src="sim?stage=int-4&format=lines" width="800" height="540"></iframe>
</div>

Hal ini *akan* menjaga jumlah kasus di bawah kapasitas ICU! Dan ini *lebih* baik daripada pelaksanaan karantina wilayah selama 18 bulan sampai vaksin tersedia. Kita hanya perlu untuk... menutup beberapa bulan, membuka kembali beberapa bulan, dan mengulanginya lagi sampai vaksin ditemukan. (Dan jika tidak ada vaksin ditemukan, ulangi hingga imunitas kawanan dicapai... pada tahun 2022.)

Lihat, sangat menarik untuk menarik garis bertuliskan "kapasitas ICU", namun banyak hal penting yang kita *tidak dapat* simulasikan di sini. Seperti:

**Kesehatan Mental:** Kesepian adalah salah satu faktor risiko terbesar dari depresi, kecemasan, dan aksi bunuh diri. Dan ini diasosiasikan dengan kematian yang cepat seperti menghisap 15 batang rokok setiap hari.[^loneliness]

[^loneliness]: Lihat [Gambar 6 dari Holt-Lunstad & Smith 2010](https://journals.sagepub.com/doi/abs/10.1177/1745691614568352). Tentu saja, penolakan besar bahwa mereka menemukan *korelasi*. Tetapi kecuali jika Anda ingin mencoba secara acak menugaskan orang untuk kesepian seumur hidup, bukti pengamatan adalah semua yang akan Anda dapatkan.

**Kesehatan Finansial:** "Bagaimana dengan ekonomi" terdengar seperti Anda lebih peduli pada pundi-pundi uang daripada nyawa, namun "ekonomi" tidak hanya sebatas saham: ini adalah kemampuan masyarakat untuk menyediakan pangan dan tempat tinggal untuk keluarga yang disayangi, berinvestasi untuk masa depan anak-anaknya, dan menikmati seni, makanan, gim - hal-hal yang membuat hidup amat berarti. Dan di samping itu, kemiskinan *itu sendiri* memiliki dampak mengerikan kepada kesehatan mental dan fisik.

Bukan berarti kita *tidak perlu* melakukan karantina wilayah lagi! Kita akan lihat pada karantina "pemutusan arus" nanti. Namun masih saja, ini tidak ideal.

Tapi tunggu... bukankah Taiwan dan Korea Selatan *sudah berhasil* mengekang COVID-19? Untuk 4 bulan penuh, *tanpa* karantina wilayah jangka panjang?

Bagaimana mungkin?

###Skenario 4: Tes, Lacak, Isolasi

*"Tentu, kita \*juga dapat\* melakukan apa yang Taiwan dan Korea Selatan lakukan sejak awal, namun sekarang sudah terlambat. Kita melewatkan permulaannya.*

Tapi memang seperti itu! "Karantina wilayah bukanlah obatnya, hanya sebuah pengulangan kembali."... **dan sebuah permulaan yang barulah yang kita perlukan.**

Untuk memahami bagaimana Taiwan & Korea Selatan mengekang COVID-19, kita perlu memahami linimasa sesungguhnya dari infeksi umum COVID-19[^timeline]:

[^timeline]: **3 hari rata-rata terjadi infeksi:** "Dengan asumsi distribusi periode inkubasi rata-rata 5,2 hari dari studi terpisah kasus COVID-19 awal, kami menyimpulkan bahwa infeksi dimulai dari 2,3 hari (95% CI, 0,8-3,0 hari) sebelum timbulnya gejala" (terjemahan: Gejala asumsi dimulai pada 5 hari, infeksi mulai 2 hari sebelumnya = Infeksi dimulai pada 3 hari) [He, X., Lau, E.H.Y., Wu, P. et al.](https://www.nature.com/articles/s41591-020-0869-5)  
    
    **4 hari rata-rata menginfeksi orang lain:** “Interval [serial] rata-rata adalah 3,96 hari (95% CI 3,53–4,39 hari)” [Du Z, Xu X, Wu Y, Wang L, Cowling BJ, Ancel Meyers L](https://wwwnc.cdc.gov/eid/article/26/6/20-0357_article)
    
    **5 hari rata-rata merasakan gejala-gejala:** “Masa inkubasi rata-rata diperkirakan 5,1 hari (95% CI, 4,5 hingga 5,8 hari)” [Lauer SA, Grantz KH, Bi Q, et al](https://annals.org/AIM/FULLARTICLE/2762808/INCUBATION-PERIOD-CORONAVIRUS-DISEASE-2019-COVID-19-FROM-PUBLICLY-REPORTED)

![](pics/timeline1.png)

Jika pasien hanya mengisolasi diri ketika mereka tahu mereka sakit (yaitu, mereka merasakan gejala), virus masih dapat menyebar:

![](pics/timeline2.png)

Dan faktanya, 44% dari semua penularan itu seperti ini: *pre* simptomatik atau *sebelum adanya* gejala! [^pre_symp]

[^pre_symp]: “Kami memperkirakan bahwa 44% (interval kepercayaan 95%, 25-69%) dari kasus sekunder terinfeksi selama tahap presimptomatik kasus indeks” [He, X., Lau, E.H.Y., Wu, P. et al](https://www.nature.com/articles/s41591-020-0869-5)

Namun, jika kita menemukan *dan mengkarantina* kerabat terdekat dari pasien kasus bergejala... kita menghentikan penyebaran, dengan tetap satu langkah lebih maju!

![](pics/timeline3.png)

Inilah yang disebut sebagai **pelacakan kontak**. Idenya sudah lama, digunakan pada skala yang tidak bisa diprediksi sebelumnya untuk mengekang Ebola[^ebola], dan sekarang menjadi bagian inti dalam bagaimana Taiwan & Korea Selatan mengekang COVID-19!

[^ebola]: “Pelacakan kontak adalah intervensi penting di Liberia dan merupakan salah satu upaya penelusuran kontak terbesar selama epidemi dalam sejarah.” [Swanson KC, Altare C, Wesseh CS, et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6152989/)

(Ini pun membolehkan kita gunakan tes terbatas lebih efisien, untuk menemukan kelompok <icon i></icon> presimptomatik tanpa perlu melakukan tes hampir ke semua orang.)

Secara tradisional, kontak ditemukan dengan wawancara langsung, namun tindakan itu *sendiri* terlalu lamban untuk jendela 48 jam dari COVID-19. Itulah mengapa pelacak kontak membutuhkan bantuan, dan akan didukung oleh - *TIDAK* digantikan oleh - aplikasi pelacakan kontak.

(Gagasan isi tidak dapat dari para "pegiat teknologi": menggunakan aplikasi untuk melawan COVID-19 pertama kali diusulkan oleh [sebuah tim epidemiologis dari Oxford](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936).)

Tunggu, aplikasi yang melacak dengan siapa saja Anda telah kontak sebelumnya?... Apakah ini berarti kita merelakan privasi kita, untuk dipantau oleh pihak berwenang?

Tentu tidak! **[DP-3T](https://github.com/DP-3T/documents#decentralized-privacy-preserving-proximity-tracing)**, sebuah tim epidemiologis & kriptografer (termasuk salah satu dari kami, Marcel Salathé) *telah* membuat sebuah aplikasi pelacakan kontak - dengan kode yang tersedia untuk umum - yang **tidak mengungkap apapun tentang identitas, lokasi Anda, siapa yang Anda hubungi, atau bahkan *berapa banyak kontak* yang telah Anda lakukan.**

Inilah bagaimana aplikasi itu bekerja:

![](pics/dp3t.png)

(& [inilah komik selengkapnya](https://ncase.me/contact-tracing/))

Bersamaan dengan tim serupa seperti TCN Protocol[^tcn] dan MIT PACT[^pact], mereka menginspirasi Apple & Google untuk menghasilkan pelacakan kontak yang mengutamakan privasi langsung ke dalam Android/iOS.[^gapple] (Tidak percaya Google/Apple? Bagus! Keindahan dari sistem ini adalah ini tidak *memerlukan* kepercayaan!) Kelak, kantor kesehatan masyarakat lokal Anda mungkin meminta Anda untuk mengunduh sebuah aplikasi. Jika aplikasi tersebut mengutamakan privasi dengan kode yang tersedia untuk umum, mohon segara unduh!

[^tcn]: [*Temporary Contact Numbers* atau Nomor Kontak Sementara, sebuah protokol pelacakan kontak yang terdesentralisasi dan mengutamakan privasi](https://github.com/TCNCoalition/TCN#tcn-protocol)

[^pact]: [PACT: Private Automated Contact Tracing](https://pact.mit.edu/)

[^gapple]: [Apple dan Google bermitra dengan teknologi pelacakan kontak COVID-19](https://www.apple.com/ca/newsroom/2020/04/apple-and-google-partner-on-covid-19-contact-tracing-technology/). Dicatat bahwa mereka tidak membuat aplikasinya *oleh mereka sendiri*, hanya membuat sistem yang dapat *mendukung* aplikasi sejenisnya.

Lalu bagaimana dengan masyarakat yang tidak menggunakan ponsel pintar? Atau yang terinfeksi melalui gagang pintu? Atau kasus tanpa gejala "sebenarnya"? Aplikasi pelacakan kontak tidak dapat menangkap semua kasus penularan... *dan itu tidak apa-apa!* Kita tidak perlu menangkap *semua* penularan, hanya 60%+ saja diperlukan untuk mendapatkan nilai R < 1.

(Ocehan tentang kebingungan tentang pra-gejala vs kasus tanpa gejala "sebenarnya". Kasus tanpa gejala "sebenarnya" jarang terjadi:[^rant])

[^rant]: Banyak laporan berita - dan sejujurnya, banyak makalah penelitian - tidak membedakan antara "kasus yang tidak menunjukkan gejala ketika kami mengujinya" (pra-gejala) dan "kasus yang tidak menunjukkan gejala *sama sekali*" (tanpa gejala yang sebenarnya). Satu-satunya cara Anda mengetahui perbedaannya adalah dengan menindaklanjuti kasus-kasus nanti.
   
    Yang sebenarnya apa yang [studi ini](https://wwwnc.cdc.gov/eid/article/26/8/20-1274_article) telah lakukan. (Penafian: "Artikel rilis awal tidak dianggap sebagai versi final.") Di sebuah pusat panggilan di Korea Selatan yang memiliki wabah COVID-19, "hanya 4 (1,9%) yang tetap tanpa gejala dalam waktu 14 hari karantina, dan tidak satu pun dari kontak dalam satu rumah mereka memperoleh infeksi sekunder. "
    
    Jadi itu berarti "kasus tanpa gejala sejati" jarang terjadi, dan tertular penyakit dari kasus tanpa gejala sejati bahkan mungkin lebih jarang!
    
Mengisolasi kasus *bergejala* dapat menurunkan R hingga 40%, dan mengkarantina kontak mereka yang *belum/tanpa gejala* dapat menurunkan R hingga 50%[^oxford]:

[^oxford]: Dari penelitian Oxford yang sama yang pertama merekomendasikan aplikasi untuk melawan COVID-19: [Luca Ferretti & Chris Wymant et al](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936/tab-figures-data) Lihat Gambar 2. Asumsikan R<sub>0</sub> = 2,0, mereka menemukan bahwa:    
    
    * Kasus bergejala berkontribusi pada R = 0,8 (40%)
    * Kasus yang belum bergejala berkontribusi pada R = 0,9 (45%)
    * Kasus bergejala berkontribusi pada R = 0,1 (5%, meskipun model mereka memiliki ketidakpastian dan bisa jadi jauh lebih rendah)
    * Benda sekitar seperti gagang pintu berkontribusi pada R = 0,2 (10%)

    Dan tambahkan kontak yang belum & tanpa gejala (45% + 5%) fan Anda akan mendapatkan 50% dari R!

<div class="sim">
		<iframe src="sim?stage=int-4a&format=calc" width="285" height="340"></iframe>
</div>

Jadi, bahkan tanpa 100% mengkarantina kontak, kita dapat meraih nilai R < 1 *tanpa karantina wilayah!* Jauh lebih baik untuk kesehatan mental & finansial kita. (Adapun biaya untuk mereka yang harus mengisolasi/karantina diri, *pemerintah harus memberi dukungan kepada mereka* - membayar tes, perlindungan kerja, cuti berbayar yang disubsidi, dan lain-lain. Masih jauh lebih murah daripada karantina wilayah berselang-seling.)

Kemudian kita tetap menjaga nilai R < 1 sampai kita menemukan vaksinnya, yang dapat mengubah kelompok rentan <icon s></icon> menjadi kelompok yang imun <icon r></icon>. Inilah imunitas kawanan dengan cara yang *benar*:

<div class="sim">
		<iframe src="sim?stage=int-4b&format=calc" width="285" height="230"></iframe>
</div>

(Catatan: kalkulator ini berpura-pura vaksinnya 100% efektif. Ingatlah bahwa pada kenyataannya, Anda harus menggantinya dengan cara memvaksinasi *lebih banyak* daripada mencapai "imunitas kawanan", untuk *benar-benar* mendapatkan imunitas kawanan)

OK, cukup bicaranya. Ini dia simulasi dari:

1. Karantina wilayah selama beberapa bulan, sampai kita bisa ...
2. Beralih ke "Tes, Lacak, Isolasi" sampai kita bisa ...
3. Vaksinasi cukup banyak orang, yang berarti ...
4. Kita menang.

<div class="sim">
		<iframe src="sim?stage=int-5&format=lines" width="800" height="540"></iframe>
</div>

Jadi begitu! Begitulah cara kita melakukan pendaratan darurat di pesawat ini.

Itulah cara kita mengalahkan COVID-19.

...

Tetapi bagaimana jika ternyata *masih* bermasalah? Hal-hal buruk telah terjadi. Itulah rasa takut, dan itu bagus! Rasa takut memberi kita energi untuk membuat *rencana cadangan*.

Pesimis menciptakan parasut.

###Skenario 4+: Masker Untuk Semua, Musim Panas, Karantina Pemutus Arus

Bagaimana jika nilai R<sub>0</sub> jauh lebih tinggi dari yang kita duga, dan tindakan di atas, bahkan dengan menjaga jarak secara nyaman, *masih* kurang cukup untuk meraih nilai R < 1?

Ingat, bahkan jika kita tidak dapat meraih nilai R < 1, mengurangi R masih dapat menurunkan "lonjakan" pada total kasus, jadi nyawa bisa diselamatkan. Namun tetapi, R < 1 itu ideal, jadi inilah beberapa cara lainnya untuk mengurangi nilai R:

**Masker Untuk Semua:**

*"Tunggu,"* mungkin Anda bertanya, *"Saya pikir masker tidak menghentikan kita dari kemungkinan menjadi sakit?"*

Anda benar. Masker tidak menghentikan kita dari kemungkinan untuk sakit[^incoming]... tapi masker menghentikan Anda untuk membuat *orang lain* menjadi sakit.

[^incoming]: “Tidak satu pun dari masker bedah ini yang memperlihatkan kinerja filter yang memadai dan karakteristik kecocokan wajah untuk dipertimbangkan sebagai alat perlindungan pernapasan.” [Tara Oberg & Lisa M. Brosseau](https://www.sciencedirect.com/science/article/pii/S0196655307007742)

[^outgoing]: “Keseluruhan pengurangan 3,4 kali lipat [pengurangan 70%] dalam jumlah salinan aerosol yang kami amati dikombinasikan dengan penghilangan semprotan tetesan besar yang hampir lengkap yang ditunjukkan oleh Johnson et al. menunjukkan bahwa masker bedah yang dikenakan oleh orang yang terinfeksi dapat memiliki dampak yang signifikan secara klinis pada penularan.” [Milton DK, Fabian MP, Cowling BJ, Grantham ML, McDevitt JJ](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3591312/)

[^homemade]: [Davies, A., Thompson, K., Giri, K., Kafatos, G., Walker, J., & Bennett, A](https://www.cambridge.org/core/journals/disaster-medicine-and-public-health-preparedness/article/testing-the-efficacy-of-homemade-masks-would-they-protect-in-an-influenza-pandemic/0921A05A69A9419C862FA2F35F819D55) Lihat Tabel 1: T-shirt berbahan 100% katun memiliki sekitar 2/3 efisiensi penyaringan layaknya masker bedah, berdasarkan dua aerosol bakteri yang mereka uji.

![](pics/masks.png)

Bila kita ukur: masker bedah *yang dipakai orang sakit* menurunkan jumlah virus flu & demam berbentuk aerosol hingga 70%.[^outgoing] Mengurangi penularan hingga 70% memberi dampak yang besarnya seperti pelaksanaan karantina wilayah!

Walaupun begitu, kami belum tahu dengan yakin dampak masker pada COVID-19 *secara spesifik*. Di dalam sains, seseorang seharusnya bisa mempublikasikan sebuah temuan jika sudah 95% yakin dengan temuan tersebut. (...seharusnya.[^replication]) Masker, hingga 1 Mei 2020, masih kurang dari "95% yakin".

[^replication]: Ilmuwan sebenarnya mana pun yang membaca kalimat terakhir itu mungkin sedang tertawa saat ini. Lihat: [p-hacking](https://en.wikipedia.org/wiki/Data_dredging), [krisis replikasi](https://en.wikipedia.org/wiki/Replication_crisis))

Walaupun begitu, pandemi layaknya seperti poker. **Membuat taruhan hanya jika Anda sudah 95% yakin, dan Anda akan kehilangan segalanya yang dipertaruhkan.** Seperti yang disebutkan pada sebuah artikel tentang masker di British Medical Journal,[^precautionary] kita *harus* membuat analisis manfaat biaya di bawah ketidakpastian. Seperti itu:

[^precautionary]: “Sudah waktunya untuk menerapkan prinsip kehati-hatian” [Trisha Greenhalgh et al \[PDF\]](https://www.bmj.com/content/bmj/369/bmj.m1435.full.pdf)

Biaya: Jika masker kain rumahan (yang ~2/3 seefektif masker bedah[^homemade]), sangat murah. Jika masker bedah, lebih mahal tapi tetap cukup murah.

Manfaat: Bahkan jika itu adalah peluang 50-50 masker bedah mengurangi penularan sebesar 0% atau 70%, rata-rata "nilai yang diharapkan" masih 35%, sama dengan setengah dampak karantina wilayah! Jadi mari kita menerka dan perkirakan bahwa masker bedah mengurangi nilai R hingga 35%, dipotong oleh ketidakpastian kita. (Sekali lagi, Anda dapat menantang asumsi kami dengan memutar slider ke atas/bawah)

<div class="sim">
		<iframe src="sim?stage=int-6a&format=calc" width="285" height="380"></iframe>
</div>

(argumen lainnya untuk mendukung/menolak penggunaan masker:[^mask_args])

[^mask_args]: **"Kita perlu menyelamatkan persediaan untuk rumah sakit."** *Sangat setuju.* Tetapi itu lebih kepada argumen untuk meningkatkan produksi masker, bukan pendistribusiannya. Untuk sementara waktu, kita bisa membuat masker kain.

   **"Mereka sulit menggunakannya dengan benar."** Juga sangat sulut untuk mencuci tangan mengikuti Panduan WHO - serius, "Langkah 3) telapak tangan kanan ke arah dorsum kiri"?! – tapi kami tetap merekomendasikan cuci tangan, karena tidak sempurna masih lebih baik daripada tidak sama sekali.
      
   **"Itu akan membuat orang lebih gegabah dengan mencuci tangan & menjaga jarak."** Tentu, dan sabuk pengaman membuat orang mengabaikan tanda berhenti, dan benang gigi membuat orang tetap makan batu. Tapi serius, kami berpendapat sebaliknya: masker adalah *pengingat fisik yang konstan* untuk berhati-hati - dan di Asia Timur, masker juga merupakan simbol solidaritas!

Masker *sendiri* tidak akan mendapatkan nilai R < 1. Namun jika tindakan cuci tangan & "Tes, Lacak, Isolasi" hanya membantu kita meraih nilai R = 1,10, hanya dengan 1/3 dari seluruh orang memakai masker bisa mengubah nilai R menjadi < 1, virus berhasil dikekang!

**Musim Panas:**

OK, ini bukan sebuah "tindakan" yang tidak dapat kita kendalikan, namun ini dapat membantu! Beberapa media pemberitaan melaporkan bahwa musim panas tidak membantu apa-apa pada situasi COVID-19. Situasi ini setengah bermanfaat: musim panas tidak dapat menjadikan nilai R < 1, tetapi *akan* menurunkan nilai R.

Untuk COVID-19, setiap penambahan suhu 1° Celsius (2,2° Fahrenheit) akan menurukan nilai hingga 1,2%.[^heat] Perbedaan musim panas-musim dingin di New York City adalah 15°C (60°F), sehingga musim panas dapat menurunkan nilai R menjadi 18%.

[^heat]: “Peningkatan temperatur sebesar satu-derajat Celsius [...] menurunkan nilai R sebesar 0,0225” dan “Rata-rata nilai R dari 100 kota ini adalah 1,83”. 0,0225 ÷ 1,83 = ~1,2%. [Wang, Jingyuan dan Tang, Ke dan Feng, Kai dan Lv, Weifeng](https://papers.ssrn.com/sol3/Papers.cfm?abstract_id=3551767)

<div class="sim">
		<iframe src="sim?stage=int-6b&format=calc" width="285" height="220"></iframe>
</div>

Musim panas saja tidak akan membuat R < 1, tetapi jika kami memiliki sumber daya yang terbatas, kami dapat mengurangi beberapa tindakan di musim panas - sehingga kami dapat meningkatkan skalanya *lebih tinggi* di musim dingin.

**Karantina "Pemutusan Arus":**

Dan jika semua itu *masih* tidak cukup untuk mendapatkan R < 1 ... kita bisa melakukan karantina wilayah lainnya.

But we wouldn't have to be 2-months-closed / 1-month-open over & over! Because R is reduced, we'd only need one or two more "circuit breaker" lockdowns before a vaccine is available. (Singapore had to do this recently, "despite" having controlled COVID-19 for 4 months. That's not failure: this *is* what success takes.)

Here's a simulation a "lazy case" scenario:

1. Lockdown, then
2. A moderate amount of hygiene & "Test, Trace, Isolate", with a mild amount of "Masks For All", then...
3. One more "circuit breaker" lockdown before a vaccine's found.

<div class="sim">
		<iframe src="sim?stage=int-7&format=lines&height=620" width="800" height="620"></iframe>
</div>

Not to mention all the *other* interventions we could do, to further push R down:

* Travel restrictions/quarantines
* Temperature checks at malls & schools
* Deep-cleaning public spaces
* [Replacing hand-shaking with foot-bumping](https://twitter.com/V_actually/status/1233785527788285953)
* And all else human ingenuity shall bring

. . .

We hope these plans give you hope. 

**Even under a pessimistic scenario, it *is* possible to beat COVID-19, while protecting our mental and financial health.** Use the lockdown as a "reset button", keep R < 1 with case isolation + privacy-protecting contract tracing + at *least* cloth masks for all... and life can get back to a normal-ish!

Sure, you may have dried-out hands. But you'll get to invite a date out to a comics bookstore! You'll get to go out with friends to watch the latest Hollywood cash-grab. You'll get to people-watch at a library, taking joy in people going about the simple business of *being alive.*

Even under the worst-case scenario... life perseveres.

So now, let's plan for some *worse* worst-case scenarios. Water landing, get your life jacket, and please follow the lights to the emergency exits:

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Next Few Years</div>
    </div>
</div>

You get COVID-19, and recover. Or you get the COVID-19 vaccine. Either way, you're now immune...

...*for how long?*

* COVID-19 is most closely related to SARS, which gave its survivors 2 years of immunity.[^SARS immunity]
* The coronaviruses that cause "the" common cold give you 8 months of immunity.[^cold immunity]
* There's reports of folks recovering from COVID-19, then testing positive again, but it's unclear if these are false positives.[^unclear]
* One *not-yet-peer-reviewed* study on monkeys showed immunity to the COVID-19 coronavirus for at least 28 days.[^monkeys]

But for COVID-19 *in humans*, as of May 1st 2020, "how long" is the big unknown.

[^SARS immunity]: “SARS-specific antibodies were maintained for an average of 2 years [...] Thus, SARS patients might be susceptible to reinfection ≥3 years after initial exposure.” [Wu LP, Wang NC, Chang YH, et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2851497/) "Sadly" we'll never know how long SARS immunity would have really lasted, since we eradicated it so quickly.

[^cold immunity]: “We found no significant difference between the probability of testing positive at least once and the probability of a recurrence for the beta-coronaviruses HKU1 and OC43 at 34 weeks after enrollment/first infection.” [Marta Galanti & Jeffrey Shaman (PDF)](http://www.columbia.edu/~jls106/galanti_shaman_ms_supp.pdf)

[^unclear]: “Once a person fights off a virus, viral particles tend to linger for some time. These cannot cause infections, but they can trigger a positive test.” [from STAT News by Andrew Joseph](https://www.statnews.com/2020/04/20/everything-we-know-about-coronavirus-immunity-and-antibodies-and-plenty-we-still-dont/)

[^monkeys]: From [Bao et al.](https://www.biorxiv.org/content/10.1101/2020.03.13.990226v1.abstract) *Disclaimer: This article is a preprint and has not been certified by peer review (yet).* Also, to emphasize: they only tested re-infection 28 days later. 

For these simulations, let's say it's 1 year.
**Here's a simulation starting with 100% <icon r></icon>**, exponentially decaying into susceptible, no-immunity <icon s></icon>s after 1 year, on *average*, with variation:

<div class="sim">
		<iframe src="sim?stage=yrs-1&format=lines&height=600" width="800" height="600"></iframe>
</div>

Return of the exponential decay!

This is the **SEIRS Model**. The final "S" stands for <icon s></icon> Susceptible, again.

![](pics/seirs.png)

Now, let's simulate a COVID-19 outbreak, over 10 years, with no interventions... *if immunity only lasts a year:*

<div class="sim">
		<iframe src="sim?stage=yrs-2&format=lines&height=600" width="800" height="600"></iframe>
</div>

In previous simulations, we only had *one* ICU-overwhelming spike. Now, we have several, *and* <icon i></icon> cases come to a rest *permanently at* ICU capacity. (Which, remember, we *tripled* for these simulations)

R = 1, it's **endemic.**

Thankfully, because summer reduces R, it'll make the situation better:

<div class="sim">
		<iframe src="sim?stage=yrs-3&format=lines&height=640" width="800" height="640"></iframe>
</div>

Oh.

Counterintuitively, summer makes the spikes worse *and* regular! This is because summer reduces new <icon i></icon>s, but that in turn reduces new immune <icon r></icon>s. Which means immunity plummets in the summer, *creating* large regular spikes in the winter.

Thankfully, the solution to this is pretty straightforward – just vaccinate people every fall/winter, like we do with flu shots:

**(After playing the recording, try simulating your own vaccination campaigns! Remember you can pause/continue the sim at any time)**

<div class="sim">
		<iframe src="sim?stage=yrs-4&format=lines" width="800" height="540"></iframe>
</div>

But here's the scarier question:

What if there's no vaccine for *years*? Or *ever?*

**To be clear: this is unlikely.** Most epidemiologists expect a vaccine in 1 to 2 years. Sure, there's never been a vaccine for any of the other coronaviruses before, but that's because SARS was eradicated quickly, and "the" common cold wasn't worth the investment. 

Still, infectious disease researchers have expressed worries: What if we can't make enough?[^vax_enough] What if we rush it, and it's not safe?[^vax_safe]

[^vax_enough]: “If a coronavirus vaccine arrives, can the world make enough?” [by Roxanne Khamsi, on Nature](https://www.nature.com/articles/d41586-020-01063-8)

[^vax_safe]: “Don’t rush to deploy COVID-19 vaccines and drugs without sufficient safety guarantees” [by Shibo Jiang, on Nature](https://www.nature.com/articles/d41586-020-00751-9)

Even in the nightmare "no-vaccine" scenario, we still have 3 ways out. From most to least terrible:

1) Do intermittent or loose R < 1 interventions, to reach "natural herd immunity". (Warning: this will result in many deaths & damaged lungs. *And* won't work if immunity doesn't last.)

2) Do the R < 1 interventions forever. Contact tracing & wearing masks just becomes a new norm in the post-COVID-19 world, like how STI tests & wearing condoms became a new norm in the post-HIV world.

3) Do the R < 1 interventions until we develop treatments that make COVID-19 way, way less likely to need critical care. (Which we should be doing *anyway!*) Reducing ICU use by 10x is the same as increasing our ICU capacity by 10x:

**Here's a simulation of *no* lasting immunity, *no* vaccine, and not even any interventions – just slowly increasing capacity to survive the long-term spikes:**

<div class="sim">
		<iframe src="sim?stage=yrs-5&format=lines" width="800" height="540"></iframe>
</div>

Even under the *worst* worst-case scenario... life perseveres.

. . .

Maybe you'd like to challenge our assumptions, and try different R<sub>0</sub>'s or numbers. Or try simulating your *own* combination of intervention plans!

**Here's an (optional) Sandbox Mode, with *everything* available. (scroll to see all controls) Simulate & play around to your heart's content:**

<div class="sim">
		<iframe src="sim?stage=SB&format=sb" width="800" height="540"></iframe>
</div>

This basic "epidemic flight simulator" has taught us so much. It's let us answer questions about the past few months, next few months, and next few years.

So finally, let's return to...

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Now</div>
    </div>
</div>

Plane's sunk. We've scrambled onto the life rafts. It's time to find dry land.[^dry_land]

[^dry_land]: Dry land metaphor [from Marc Lipsitch & Yonatan Grad, on STAT News](https://www.statnews.com/2020/04/01/navigating-covid-19-pandemic/)

Teams of epidemiologists and policymakers ([left](https://www.americanprogress.org/issues/healthcare/news/2020/04/03/482613/national-state-plan-end-coronavirus-crisis/), [right](https://www.aei.org/research-products/report/national-coronavirus-response-a-road-map-to-reopening/ ), and [multi-partisan](https://ethics.harvard.edu/covid-roadmap)) have come to a consensus on how to beat COVID-19, while protecting our lives *and* liberties.

Here's the rough idea, with some (less-consensus) backup plans:

![](pics/plan.png)

So what does this mean for YOU, right now?

**For everyone:** Respect the lockdown so we can get out of Phase I asap. Keep washing those hands. Make your own masks. Download a *privacy-protecting* contact tracing app when those are available next month. Stay healthy, physically & mentally! And write your local policymaker to get off their butt and...

**For policymakers:** Make laws to support folks who have to self-isolate/quarantine. Hire more manual contact tracers, *supported* by privacy-protecting contact tracing apps. Direct more funds into the stuff we should be building, like...

**For builders:** Build tests. Build ventilators. Build personal protective equipment for hospitals. Build tests. Build masks. Build apps. Build antivirals, prophylactics, and other treatments that aren't vaccines. Build vaccines. Build tests. Build tests. Build tests. Build hope. 

Don't downplay fear to build up hope. Our fear should *team up* with our hope, like the inventors of airplanes & parachutes. Preparing for horrible futures is how we *create* a hopeful future.

The only thing to fear is the idea that the only thing to fear is fear itself.