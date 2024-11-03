<a name="readme-top"></a>

> [!NOTE]
> <b>DeltaGroup_JC_DS_FT_JKT_24_RemedialFinalProject</b>

<h1 align="center">
  <span style="color: #627254; font-size: 44px; font-weight: bold;">
    Flipkart E-commerce Customer Churn: Analisis dan Prediksi untuk Efisiensi Biaya Akuisisi dan Retensi
  </span>
</h1>

---

<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; font-style: italic; display: inline-block;">Remedial Final Project: Data-Driven Analysis and Supervised Learning Classification</h2>
</div>

> [!IMPORTANT]
> `Disclaimer:
This remedial final project serves as a final crucial component of the educational and assessment sequence in Job Connector Data Science and Machine Learning Program at Purwadhika Digital Technology School. Please kindly download the notebook to your local environment to read the Jupyter Notebook.`

**Author:** [Arief Luqman Hakiem](https://www.linkedin.com/in/ariefluqman/) dan [Samuel Semaya](https://www.linkedin.com/in/samuelsemaya/) <br>
**Batch:** JCDS 2404 <br>
**Date Submitted and Last Updated:** `2024-11-04` <br>
**Data Source:** [Kaggle E-commerce Customer Churn Dataset](https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction) <br>

<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block;">Sumber Daya Pendukung</h2>
</div>

---

 **Github:** [Repository](https://github.com/arluqmann/DeltaGroup_JC_DS_FT_JKT_24_RemedialFinalProject) <br>
 **Tableau:** [Dashboard](https://public.tableau.com/app/profile/samuelsemaya/viz/final-project-ver2-fix/Dash_CP) <br>

<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block; font-size: 30px">Konteks</h2>
</div>

---

<div style='text-align: justify'>

<strong>Customer churn atau kehilangan pelanggan menjadi tantangan signifikan bagi industri e-commerce, termasuk Flipkart.</strong> Dalam industri ini, di mana persaingan sangat ketat dan pilihan konsumen semakin beragam, mempertahankan pelanggan menjadi lebih sulit. <strong>Churn berdampak langsung pada pendapatan dan profitabilitas perusahaan</strong>, karena biaya untuk mendapatkan pelanggan baru sering kali lebih tinggi daripada mempertahankan yang sudah ada. Dengan semakin banyaknya pilihan platform dan peningkatan ekspektasi pelanggan terhadap layanan, e-commerce seperti Flipkart harus <strong>mengembangkan strategi yang efektif untuk memahami penyebab churn serta mencari solusi inovatif untuk meningkatkan retensi dan efisiensi biaya perusahaan.</strong>

<strong>Dari perspektif bisnis</strong>, efisiensi biaya akuisisi dan retensi pelanggan sangat penting dalam menjaga profitabilitas dan keberlanjutan perusahaan e-commerce seperti Flipkart. <strong>Nilai Customer Spend per Month (CSPM) yang mencapai ₹17.550</strong> menunjukkan potensi pendapatan rata-rata yang dapat dihasilkan dari setiap pelanggan aktif dalam satu bulan. Di sisi lain, <strong>Customer Acquisition Cost (CAC) sebesar ₹6.500</strong> untuk menyoroti biaya yang diperlukan untuk menarik pelanggan baru. Biaya Retensi Pelanggan atau <strong>Customer Retention Cost (CRC), yang sekitar ₹4.000</strong>, juga menjadi metrik penting, karena menggambarkan biaya yang diperlukan untuk mempertahankan pelanggan. Dengan membandingkan nilai-nilai ini, Flipkart dapat <strong>menyusun strategi efisiensi biaya yang optimal, di mana biaya retensi yang relatif tinggi dibandingkan biaya akuisisi menunjukkan pentingnya menjaga pelanggan agar menghasilkan keuntungan jangka panjang.</strong> Menggunakan analisis ini, Flipkart dapat membuat keputusan yang lebih tepat dalam alokasi anggaran untuk akuisisi dan retensi, sekaligus memaksimalkan nilai seumur hidup pelanggan bagi perusahaan.

</div>



<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block; font-size: 30px">Pernyataan Permasalahan</h2>
</div>

---

<div style='text-align: justify'>

Sebagai salah satu platform leading e-commerce di India, Flipkart menghadapi tantangan churn pelanggan yang signifikan, di mana <strong>sekitar 16.8% pelanggan—948 dari total 5,630—berhenti menggunakan layanan.</strong> Tingginya churn ini <strong>mempengaruhi nilai Customer Spend per Month (CSPM)</strong>, karena berkurangnya jumlah pelanggan aktif mengurangi pendapatan potensial yang dapat dihasilkan setiap bulannya. Dengan penurunan CSPM, Flipkart harus menghadapi konsekuensi finansial yang semakin besar, terutama dalam menjaga stabilitas pendapatan yang dibutuhkan untuk mendukung pertumbuhan jangka panjang.

Selain itu, <strong>churn yang tinggi berdampak</strong> langsung pada <strong>Customer Acquisition Cost (CAC) dan Customer Retention Cost (CRC).</strong> Untuk menggantikan pelanggan yang churn, Flipkart perlu meningkatkan biaya akuisisi, yang sering kali jauh lebih tinggi dibandingkan mempertahankan pelanggan yang sudah ada. Di sisi lain, upaya menekan churn juga memerlukan investasi pada biaya retensi yang menguras anggaran. Ketidakstabilan ini menuntut Flipkart untuk mencari solusi yang dapat <strong>menyeimbangkan antara nilai CAC, CRC, dan CSPM, sehingga biaya operasional tetap efisien di tengah tingginya tingkat churn.</strong>

</div>



<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block; font-size: 30px">Tujuan Permasalahan</h2>
</div>

---

<div style='text-align: justify'>

Berdasarkan pernyataan permasalahan tersebut dan peran dari pemangku kebijakan, berikut merupakan tujuan yang ingin dicapai:
1. <strong>Mengidentifikasi Faktor Churn Pelanggan:</strong> Memahami secara mendalam faktor-faktor yang mendorong pelanggan untuk berhenti menggunakan layanan merupakan langkah penting bagi perusahaan. Dengan mengetahui penyebab utama churn, perusahaan dapat melakukan evaluasi menyeluruh terhadap elemen-elemen yang paling berpengaruh, sehingga upaya retensi dapat lebih efektif dan tepat sasaran.
2. <strong>Mengidentifikasi Pola dan Meningkatkan Pengalaman Pengguna:</strong> Pemahaman mendalam tentang pola perilaku dan alasan di balik churn memungkinkan perusahaan untuk menyempurnakan aspek-aspek tertentu dari pengalaman pengguna. Langkah ini penting untuk memastikan kepuasan pelanggan tetap terjaga dan meminimalisir peluang hilangnya pelanggan karena aspek-aspek yang dapat diperbaiki.
3. <strong>Memproyeksikan Pelanggan Berpotensi Churn:</strong> Melalui prediksi yang akurat terhadap pelanggan yang berpotensi churn, perusahaan dapat mengambil tindakan preventif yang tepat guna mempertahankan pelanggan. Pendekatan ini tidak hanya mengurangi tingkat churn, tetapi juga mengoptimalkan anggaran dengan meminimalkan kerugian yang timbul dari kehilangan pelanggan serta menekan biaya yang dikeluarkan untuk akuisisi pelanggan baru.

</div>



<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block; font-size: 30px">Evaluasi Metrik</h2>
</div>

---

<div style='text-align: justify'>

text

</div>



<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block; font-size: 30px">Pemahaman Dataset</h2>
</div>

---

<div style='text-align: justify'>

| Variabel                     | Deskripsi                                                                          |
|----------------------------  |------------------------------------------------------------------------------------|
| `CustomerID`                 | ID pelanggan unik                                                                  |
| `Churn`                      | Status churn                                                                       |
| `Tenure`                     | Lama keanggotaan pelanggan dalam organisasi (bulan)                                |
| `PreferredLoginDevice`       | Perangkat login yang paling sering digunakan oleh pelanggan                        |
| `CityTier`                   | Tingkatan kota                                                                     |
| `WarehouseToHome`            | Jarak antara gudang ke rumah pelanggan (km)                                        |
| `PreferredPaymentMode`       | Metode pembayaran yang paling sering digunakan oleh pelanggan                      |
| `Gender`                     | Jenis kelamin pelanggan                                                            |
| `HourSpendOnApp`             | Jumlah jam yang dihabiskan pada aplikasi seluler atau situs web                    |
| `NumberOfDeviceRegistered`   | Total jumlah perangkat yang terdaftar pada pelanggan tertentu                      |
| `PreferredOrderCat`          | Kategori pesanan yang paling disukai oleh pelanggan dalam sebulan terakhir         |
| `SatisfactionScore`          | Skor kepuasan pelanggan terhadap layanan                                           |
| `MaritalStatus`              | Status pernikahan pelanggan                                                        |
| `NumberOfAddress`            | Total jumlah alamat yang ditambahkan pada pelanggan tertentu                       |
| `Complain`                   | Apakah ada keluhan yang diajukan dalam sebulan terakhir                            |
| `OrderAmountHikeFromlastYear`| Persentase kenaikan jumlah pesanan dari tahun lalu                                 |
| `CouponUsed`                 | Total jumlah kupon yang digunakan dalam sebulan terakhir                           |
| `OrderCount`                 | Total jumlah pesanan yang dilakukan dalam sebulan terakhir                         |
| `DaySinceLastOrder`          | Jumlah hari sejak pesanan terakhir oleh pelanggan                                  |
| `CashbackAmount`             | Rata-rata cashback dalam sebulan terakhir (rupee)                                  |

</div>



<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block; font-size: 30px">Pembersihan Data</h2>
</div>

---

<div style='text-align: justify'>

text

</div>


Data yang dibersihkan terlampir dalam repositori ini dengan nama
`ecommerce_churn_cleaned.csv`.



<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block; font-size: 30px">Pemodelan</h2>
</div>

---

<div style='text-align: justify'>
For this guest prediction cancellation project, we will separate the dataset into features (independent variables) and target (dependent variable). Features include columns excluding 'is_canceled', such as 'agent', 'company', and others. <strong>Our target is the 'is_canceled' column</strong>, which indicates whether a guest canceled or not. This separation is crucial for training the model to predict canceled based on guest characteristics.

To be precise, there are 19 columns used as features, listed below:
* Categorical features: `hotel`, `agent`, `company`, `customer_type`, `deposit_type`, `distribution_channel`, `market_segment`, `meal`, `is_local`, `was_in_waiting_list`, `is_repeated_guest`;
* Numerical features: `adr_third_quartile_deviation`, `adults`, `booking_changes`, `lead_time`, `previous_cancellation_ratio`, `total_of_special_requests`, `duration_of_stay`, `arrival_date_week_number`.
</div>


<div style='text-align: justify'>
The dataset <strong>will be split into training and testing data with an 80:20 ratio</strong>. The training data will be used to train the model, while the testing data will be used to evaluate the model's performance. This split is important for assessing the model's ability to generalize to new, unseen data.
</div>

Based on the cross-validating and model evaluation, the model chosen for this case is **the hyperparameter tuned model of XGBoost Classifier using Random Oversampling** as the resample method. Using F2-score as the main metric, its F2-score was as high as 81%. This model also **has a very high recall of 95%**. Other than precision, the other metrics also seem okay from this team rule of thumb, with accuracy of 74%, precision of 52%, and F1-score of 0.67%. The model has been saved as an pickle object, and ready to be deployed.


<div style="text-align: left;">
  <h2 style="background-color: #2C3E3D; color: white; padding: 10px 20px; margin-bottom: 20px; border-radius: 8px; font-weight: bold; display: inline-block; font-size: 30px">Limitasi Model</h2>
</div>

---

This model was trained using Xtreme Gradient Booster model for classification, with the train data were resampled using Random Oversampling method. While the model may perform well, there are several limitations while inputting data to be used as features, listed below:
* `lead_time` must be inbetween 0 and 709;
* `duration_of_stay` must be inbetween 1 and 57;
* `previous_cancellation_ratio` must be in between 0 and 1;
* `booking_changes` must be in between 0 and 21;
* `total_of_special_requests` must be in between 0 and 5.

<br><hr>
[🔼 Back to top](#readme-top)
