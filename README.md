# Streamlit Session State Example

This repository demonstrates the practical use of Streamlit's session state mechanism.

## Overview

This Streamlit app reads data from a CSV file and displays it in a table. Users can dynamically adjust the number of rows displayed using "Increase" and "Decrease" buttons.

## Features

- **Dynamic Table Display:** The number of rows shown in the table can be increased or decreased.
- **Session State Management:** Maintains the state of the row count between interactions using Streamlit's session state.


## Code Summary

- **Session State Initialization:** Initializes the row count to 10 if not already set.
- **Data Loading:** Reads data from `data.csv`.
- **Table Display:** Shows the top rows of the dataframe based on the current row count.
- **Buttons:** "Increase" and "Decrease" buttons adjust the row count.
- **State Display:** Displays the current row count.

## License

This project is licensed under the MIT License.




# Streamlit Oturum Durumu Örneği

Bu depo, Streamlit'in oturum durumu mekanizmasının pratik kullanımını göstermektedir.

## Genel Bakış

Bu Streamlit uygulaması bir CSV dosyasından veri okur ve bir tabloda görüntüler. Kullanıcılar, "Artır" ve "Düşür" düğmelerini kullanarak görüntülenen satır sayısını dinamik olarak ayarlayabilir.

## Özellikler

- **Dinamik Tablo Görüntüleme:** Tabloda gösterilen satır sayısı artırılabilir veya azaltılabilir.
- **Oturum Durumu Yönetimi:** Streamlit'in oturum durumu kullanılarak satır sayısının durumu etkileşimler arasında korunur.


    ```

## Kod Özeti

- **Oturum Durumu Başlatma:** Satır sayısını 10'a başlatır eğer daha önce ayarlanmamışsa.
- **Veri Yükleme:** `data.csv` dosyasından veri okur.
- **Tablo Görüntüleme:** Mevcut satır sayısına göre dataframe'in üst satırlarını gösterir.
- **Düğmeler:** Satır sayısını ayarlayan "Artır" ve "Düşür" düğmeleri.
- **Durum Görüntüleme:** Mevcut satır sayısını gösterir.

## Lisans

Bu proje MIT Lisansı altında lisanslanmıştır.

