# Streamlit101

This repository contains an educational application for rapid prototyping and learning various features of Streamlit. The application demonstrates basic and advanced functionalities of the Streamlit library, helping users develop their own data-driven web applications.

## Contents

- [About the Project](#about-the-project)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## About the Project

**Streamlit101** is an educational application designed to help users rapidly prototype with the Streamlit library. This project teaches essential Streamlit functions such as displaying text, playing multimedia, user interaction, layout management, program flow, and session state management.

The application covers the following scenarios:
- Displaying text and code in various formats
- Displaying images, videos, and audio files
- Collecting and processing user input
- Organizing and customizing the interface layout
- Saving user information to a JSON file
- Managing session state to store user preferences and data

## Installation

To run the project, you need to have Python installed on your computer. Follow these steps to set up the project:

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/Streamlit101.git
    cd Streamlit101
    ```

2. Create a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

To run the Streamlit application, use the following command:
```sh
streamlit run streamlit101.py
Features
1. Text Display
The application uses various Streamlit components to display text. These components support a wide range of text formats, from simple text to formatted text.

2. Multimedia Display
Users can display multimedia content such as images, videos, and audio files.

3. User Interaction
The application provides various interactive components to collect user data:

Buttons
Text Input Fields
Checkboxes
Radio Buttons
Sliders
File Uploader
4. Interface Layout
The application allows controlling the page layout using sidebars, tabs, and columns. This enables customizing the layout to improve user experience.

5. Program Flow
The application includes functionalities such as saving user information and performing calculations based on certain conditions. For example, user information is taken and saved to a file in JSON format.

6. Session State Management
The application manages session state to store and access specific information throughout the session. This is used to retain user preferences and status.

Project Structure
bash
Kodu kopyala
Streamlit101/
│
├── 1-image_sample.png         # Sample image file
├── 2-video_sample.mp4         # Sample video file
├── 3-audio_sample.mp3         # Sample audio file
├── data.csv                   # Sample data file
├── streamlit101.py            # Streamlit application file
└── requirements.txt           # List of required packages
Contributing
Contributions are welcome! Please create an issue first to discuss what you would like to change.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Streamlit101
Bu depo, hızlı prototipleme ve çeşitli Streamlit özelliklerini öğrenmek için bir eğitim uygulaması içermektedir. Uygulama, Streamlit kütüphanesinin temel ve ileri düzey işlevlerini göstererek kullanıcıların kendi veri odaklı web uygulamalarını geliştirmelerine yardımcı olur.

İçindekiler
Proje Hakkında
Kurulum
Kullanım
Özellikler
Proje Yapısı
Katkıda Bulunma
Lisans
Proje Hakkında
Streamlit101, kullanıcıların Streamlit kütüphanesini kullanarak hızlı prototipleme yapmalarını sağlayan bir eğitim uygulamasıdır. Bu proje, metin gösterme, multimedya oynatma, kullanıcı etkileşimi, arayüz yerleşimi, program akışı ve oturum durumu yönetimi gibi Streamlit'in temel işlevlerini öğretmek için tasarlanmıştır.

Uygulama, aşağıdaki senaryoları kapsar:

Farklı formatlarda metin ve kod gösterimi
Resim, video ve ses dosyalarını görüntüleme
Kullanıcı girdilerini toplama ve işleme
Arayüz bileşenlerini düzenleme ve özelleştirme
Kullanıcı bilgilerini JSON formatında dosyaya kaydetme
Oturum durumu yönetimi ile veri saklama
Kurulum
Projeyi çalıştırmak için bilgisayarınızda Python yüklü olmalıdır. Projeyi kurmak için aşağıdaki adımları izleyin:

Depoyu klonlayın:

sh
Kodu kopyala
git clone https://github.com/yourusername/Streamlit101.git
cd Streamlit101
Bir sanal ortam oluşturun:

sh
Kodu kopyala
python -m venv venv
source venv/bin/activate  # Windows için `venv\Scripts\activate`
Gerekli paketleri yükleyin:

sh
Kodu kopyala
pip install -r requirements.txt
Kullanım
Streamlit uygulamasını çalıştırmak için şu komutu çalıştırın:

sh
Kodu kopyala
streamlit run streamlit101.py
Bu komut uygulamayı başlatacak ve http://localhost:8501 adresinden web tarayıcınızda görüntüleyebilirsiniz.

Özellikler
1. Metin Gösterme
Uygulama, metin gösterimi için çeşitli Streamlit bileşenlerini kullanır. Bu bileşenler, basit metinlerden biçimlendirilmiş metinlere kadar geniş bir yelpazede metinleri destekler.

2. Multimedya Gösterme
Kullanıcılar, resimler, videolar ve ses dosyaları gibi multimedya içeriklerini görüntüleyebilirler.

3. Kullanıcı Etkileşimi
Uygulama, kullanıcıdan veri toplamak için çeşitli etkileşimli bileşenler sunar:

Butonlar
Metin Giriş Alanları
Checkbox'lar
Radyo Butonları
Slider'lar
Dosya Yükleyici
4. Arayüz Yerleşimi
Uygulama, yan menüler, sekmeler ve kolonlar kullanarak sayfanın düzenini kontrol etme yeteneği sunar. Bu, kullanıcı deneyimini iyileştirmek için düzenin özelleştirilmesini sağlar.

5. Program Akışı
Uygulama, kullanıcı bilgilerini kaydetme ve belirli koşullara göre hesaplama yapma gibi işlevleri içerir. Örneğin, kullanıcı bilgileri alınıp JSON formatında bir dosyaya kaydedilir.

6. Oturum Durumu Yönetimi
Uygulama, oturum durumu yönetimi ile kullanıcının belirli bilgilerini saklar ve bu bilgileri oturum boyunca erişilebilir kılar. Bu, kullanıcının tercihlerini ve durumunu saklamak için kullanılır.

Proje Yapısı
bash
Kodu kopyala
Streamlit101/
│
├── 1-image_sample.png         # Örnek resim dosyası
├── 2-video_sample.mp4         # Örnek video dosyası
├── 3-audio_sample.mp3         # Örnek ses dosyası
├── data.csv                   # Örnek veri dosyası
├── streamlit101.py            # Streamlit uygulama dosyası
└── requirements.txt           # Gerekli paketlerin listesi
Katkıda Bulunma
Katkılar memnuniyetle kabul edilir! Lütfen değiştirmek istediğiniz şeyi tartışmak için önce bir konu (issue) oluşturun.

Lisans
Bu proje MIT Lisansı altında lisanslanmıştır - detaylar için LICENSE dosyasına bakın.

Kodu kopyala

Bu metni README dosyanıza yapıştırarak kullanabilirsiniz.
