# Capstone_3
Sebagai Capstone Project Machine Learning 
## **Business Understanding**
### **Konteks**
Banyak jenis produk finansial yang ditawarkan oleh perbankan. salah satu produk finansial yang cukup populer adalah deposito berjangka. Mekanisme deposito berjangka adalah jumlah uang yang didepositokan oleh nasabah dapat diambil kembali setelah satu periode waktu berlalu. Sebagai kompensasi, nasabah diberikan bunga tetap sesuai dengan nominal uang yang didepositokan. Sebagai entitas bisnis dengan produk finansial, perbankan masih harus berkompetisi untuk tidak kehilangan nasabahnya. salah satu caranya adalah dengan melakukan kampanye pemasaran (marketing campaign)
Target :
- 0 : Nasabah yang tidak membuka rekening tabungan deposito berjangka.
- 1 : Nasabah yang membuka rekening tabungan deposito berjangka.

#### **Definisi Deposito Berjangka**
Deposito adalah simpanan yang pencairannya hanya dapat dilakukan pada jangka waktu tertentu dan syarat-syarat tertentu. Karakteristik deposito dari antara lain adalah deposito dapat dicairkan setelah jangka waktu berakhir, deposito yang akan jatuh tempo dapat diperpanjang secara otomatis atau automatic roll over (ARO), deposito dapat dalam mata uang rupiah maupun dalam mata uang asing.
Deposito Berjangka Merupakan simpanan yang pencairannya dilakukan berdasarkan jangka waktu tertentu. Umumnya mempunyai jangka waktu mulai dari 1, 3, 6, dan 12 sampai dengan 24 bulan. Diterbitkan dengan mencantumkan nama pemilik deposito baik perorangan maupun lembaga. [https://sikapiuangmu.ojk.go.id/FrontEnd/CMS/Category/121]

#### **Problem Statement**
Sebagai badan usaha, perbankan harus tetap berkompetisi untuk tidak kehilangan nasabahnya. salah satu cara untuk mendapatkan nasabah baru adalah dengan melakukan marketing campaign. Hal yang menjadi permasalahan utama adalah bagaimana perbankan mengetetahui nasabah mana yang akan membuka rekening deposito atau tidak. Untuk meminimalisir biaya marketing campaign, perusahaan harus mengenal karakteristik nasabah mana yang sekiranya akan membuka rekening deposito sehingga kampanye yang dilakukan menjadi tepat sasaran. Berdasarkan dataset yang dimiliki, apakah proses marketing campaign ini memerlukan peran machine learning atau tidak untuk menentukan nasabah yang akan diberikan marketing campaign. maka problem statement ini dapat disimpulkan kedalam beberapa pertanyaan :

- Siapa saja nasabah yang berpotensial untuk melakukan pembukaan rekening tabungan deposito berjangka?
- Lebih baik melakukan marketing campaign ke seluruh nasabah atau hanya kepada nasabah yang menurut machine learning berpotensial untuk membuka tabungan deposito berjangka? 

#### **Goals**
Tujuan yang ingin dicapai adalah menjawab problem statement diatas yakni :
- Mengetahui nasabah mana saja yang berpotensial untuk melakukan pembukaan rekening tabungan deposito berjangka.
- Mengetahui apakah harus melakukan marketing campaign ke seluruh nasabah atau kepada nasabah yang berpotensial saja.


#### **Analytic Approach**
Berikut ini merupakan tahapan pendekatan analisa ang akan dilakukan :
1. business understanding, memahami proses bisnis yang terjadi.
2. berdasarkan permasalahan yang terjadi, dibutuhkan peran machine learning dalam memprediksi nasabah yang akan membuka rekening deposito atau tidak.
3. Menentukan apakah marketing campaign yang akan dilakukan perlu dilakukan kepada seluruh nasabah atau hanya nasabah yang diprediksi oleh machine learning untuk membuka rekening atau tidak.

#### **Evaluation Metric**
Matrik evaluasi yang akan digunakan adalah `f1 score` karena baik marketing campaign fee dan opportunity cost dianggap sama pentingnya maka `f1 score` digunakan.

- False Positive : Nasabah yang diprediksi akan deposito namun ternyata tidak. False positive menyebabkan kita mengeluarkan biaya marketing campaign padahal nasabah tersebut tidak akan membuka tabungan rekening deposito.
- False Negative : Nasabah yang diprediksi tidak akan deposito namun ternyata melakukan deposito. False negative menyebabkan bank mengealami opportunity cost atau profit loss.



<table>
<h2><b> Conclusion Summary </b></h2>
  <tr>
    <th>ML Usage</th>
    <th>Total Revenue</th>
    <th>Total Cost</th>
    <th>Total Profit</th>
  </tr>
  <tr>
    <td>Tidak Menggunakan Machine Learning</td>
    <td>$37300</td>
    <td>$5307</td>
    <td>$31993</td>
  </tr>
    <tr>
    <td>Menggunakan Machine Learning</td>
    <td>$22500</td>
    <td>$2216.8</td>
    <td>$20283</td>
  </tr>
</table>


Hal-hal yang direkomendasikan adalah sebagai berikut ini :
- Bagian administratif yang mengumpulkan data untuk memperbaiki kualitas pengumpulan datanya sehingga data yang dikumpulkan dpaat menjadi dataset yang akurat, karena pada salah satu kolom (`contact`) terdapat nilai unknown yang cukup banyak sehingga dapat mempengaruhi baik hasil klasifikasi maupun hasil feature importancenya.  
- Menambahkan fitur baru supaya dapat meningkatkan akurasi klasifikasi, karena berdasarkan 10 model algoritma yang digunakan, nilai akurasi terbaik hanya 67% saja. diharapkan dengan menambah fitur baru, dapat meningkatkan nilai akurasi klasifikasinya hingga mencapai 80%. 
- Melakukan `root-cause analysis` mengapa machine learning dapat mengklasifikasikan nasabah secara tidak akurat sehingga pada akhirnya kita dapat memprediksi dengna fitur mana yang sebaiknya digunakan yang dapat mempengaruhi hasil prediksi machiine learning. 
