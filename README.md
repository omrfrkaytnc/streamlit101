# Streamlit101

This repository demonstrates basic and advanced usage of Streamlit, focusing on creating interactive web applications with dynamic content and session state management.

## Overview

This project is divided into two main files:
1. `app.py`: Demonstrates basic Streamlit functionalities such as text display, multimedia display, user interactions, and layout management.
2. `session.py`: Demonstrates session state management in Streamlit.

## Features

### app.py
1. **Importing Streamlit Library**:
    ```python
    import streamlit as st
    ```

2. **Starting Streamlit Application**:
    Placeholder for initializing Streamlit application.

3. **Page Configuration**:
    ```python
    st.set_page_config(page_title="Streamlit 101", page_icon=":robot_face:")
    ```

4. **Displaying Text**:
    - Various methods for displaying text such as `st.write`, `st.markdown`, `st.header`, `st.subheader`, `st.code`, and `st.latex`.

5. **Displaying Multimedia**:
    - Methods for displaying images, videos, and audio files using `st.image`, `st.video`, and `st.audio`.

6. **User Interaction**:
    - Widgets such as `st.button`, `st.radio`, `st.checkbox`, `st.slider`, `st.number_input`, and `st.file_uploader`.

7. **Layout Management**:
    - Using `st.sidebar` for sidebar content and `st.tabs` for tabbed content.

8. **Program Flow with Streamlit Components**:
    - Demonstrates how to capture and process user inputs, and how to save data to a file.

### session.py
9. **Session State Management**:
    - Demonstrates how to use session state to maintain state between user interactions.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/streamlit101.git
    ```

2. Navigate to the project directory:

    ```bash
    cd streamlit101
    ```

3. Ensure `data.csv` is in the project directory.

4. Install Streamlit if not already installed:

    ```bash
    pip install streamlit
    ```

5. Run the app:

    ```bash
    streamlit run app.py
    ```

## Code Summary

### app.py

- **Session State Initialization**:
    ```python
    import streamlit as st 
    ```

- **Page Configuration**:
    ```python
    st.set_page_config(page_title="Streamlit 101", page_icon=":robot_face:")
    ```

- **Text Display**:
    ```python
    # st.write("En yaygın metin gösterme yöntemi")
    # st.markdown("_Biçimlendirilmiş Metin_")
    # st.header("Bu bir header örneği")
    # st.subheader("Bu ise bir subheader örneği")
    # st.code('for i in range(10): my_function()')
    # st.latex(r''' e^{i\pi} + 1 = 0 ''')
    ```

- **Multimedia Display**:
    ```python
    # st.image(image="1-image_sample.png")
    # st.video(data="2-video_sample.mp4")
    # st.audio(data="3-audio_sample.mp3")
    ```

- **User Interaction**:
    ```python
    # st.write("Lütfen Bilgilerinizi Girin")
    # st.text_input(label="Lütfen e-posta adresinizi giriniz:")
    # st.text_input(label="Lütfen şifrenizi giriniz:", type="password")
    # st.checkbox(label="Şifremi Unuttum")
    # st.divider()
    # st.number_input(label="Lütfen yaşınızı giriniz:", min_value=18, max_value=40, value=22)
    # st.slider(label="Lütfen yaşınızı giriniz:", min_value=18, max_value=40, value=22)
    # st.divider()
    # st.radio(label="Statünüz Nedir?", options=["Öğrenci", "Mezun"])
    # st.button(label="Giriş Yap")
    # st.divider()
    # st.file_uploader(label="Dosya Yüklemek İçin Tıklayınız")
    ```

- **Layout Management**:
    ```python
    # st.sidebar.markdown("<h4>Uygulamamıza Hoşgeldin!</h4>", unsafe_allow_html=True)
    # st.sidebar.image("1-image_sample.png")

    # tab1, tab2 = st.tabs(["Kullanıcı Bilgileri", "Kullanım Tercihleri"])

    # with tab1:
    #     st.text_input(label="E-Posta Adresinizi Giriniz:")
    #     st.text_input(label="Şifrenizi Giriniz", type="password")
    #     st.checkbox(label="Şifremi Unuttum")
    #     st.divider()
    #     st.button(label="Kaydet")

    # with tab2:
    #     st.radio(label="Hesap Türü", options=["Öğrenci", "Mezun"])
    #     st.slider(label="Zaman Aşımı Süresi (saniye)", min_value=3, max_value=30, value=5)
    #     st.file_uploader(label="Güncel Özgeçmişinizi Yükleyiniz")
    ```

- **Program Flow**:
    ```python
    import json

    st.sidebar.markdown("<h4>Uygulamamıza Hoşgeldin!</h4>", unsafe_allow_html=True)
    st.sidebar.image("1-image_sample.png")

    tab1, tab2 = st.tabs(["Kullanıcı Bilgileri", "Kullanım Tercihleri"])

    with tab1:
        eposta = st.text_input(label="E-Posta Adresinizi Giriniz:")
        sifre = st.text_input(label="Şifrenizi Giriniz", type="password")
        st.checkbox(label="Şifremi Unuttum")
        st.divider()
        kaydet_btn = st.button(label="Kaydet")

    with tab2:
        hesap_turu = st.radio(label="Hesap Türü", options=["Öğrenci", "Mezun"])
        st.slider(label="Zaman Aşımı Süresi (saniye)", min_value=3, max_value=30, value=5)
        st.file_uploader(label="Güncel Özgeçmişinizi Yükleyiniz")

    if kaydet_btn:
        data = []
        data.append({"eposta": eposta})
        data.append({"sifre": sifre})

        if hesap_turu == "Öğrenci":
            gecerlilik_suresi = 365
        elif hesap_turu == "Mezun":
            gecerlilik_suresi = 30

        data.append({"geçerlilik süresi": gecerlilik_suresi})

        with open("kullanici.txt", "w") as file:
            file.write(json.dumps(data))
        
        st.balloons()
        st.success("Dosyanız kaydedildi")
        st.write(f"Belirlenen geçerlilik süresi: {gecerlilik_suresi}")
    ```

### session.py

- **Session State Mechanism**:
    ```python
    import streamlit as st
    import pandas as pd

    st.header("Session State Mekanizması: Pratik Kullanım")

    if "satir_sayisi" not in st.session_state:
        st.session_state.satir_sayisi = 10

    dataframe = pd.read_csv("data.csv", sep=",")

    st.table(dataframe.head(st.session_state.satir_sayisi))

    def artir():
        st.session_state.satir_sayisi += 1

    def dusur():
        st.session_state.satir_sayisi -= 1

    artir_btn = st.button(label="Artır 👆", on_click=artir)
    dusur_btn = st.button(label="Düşür 👇", on_click=dusur)

    st.divider()
    st.header(st.session_state.satir_sayisi)
    ```

## License

This project is licensed under the MIT License.

---

# Streamlit101

Bu depo, Streamlit'in temel ve ileri düzey kullanımını, dinamik içerik ve oturum durumu yönetimi ile etkileşimli web uygulamaları oluşturma konularına odaklanarak göstermektedir.

## Genel Bakış

Bu proje iki ana dosyaya ayrılmıştır:
1. `app.py`: Metin gösterme, multimedya gösterme, kullanıcı etkileşimleri ve ara yüz yerleşimi gibi temel Streamlit işlevlerini göstermektedir.
2. `session.py`: Streamlit'te oturum durumu yönetimini göstermektedir.

## Özellikler

### app.py
1. **Streamlit Kütüphanesini Ekleme**:
    ```python
    import streamlit as st
    ```

2. **Streamlit Uygulamasını Başlatma**:
    Streamlit uygulamasını başlatma için yer tutucu.

3. **Sayfa Konfigürasyonu**:
    ```python
    st.set_page_config(page_title="Streamlit 101", page_icon=":robot_face:")
    ```

4. **Metin Gösterme**:
    - `st.write`, `st.markdown`, `st.header`, `st.subheader`, `st.code`, ve `st.latex` kullanarak çeşitli metin gösterme yöntemleri.

5. **Multimedya Gösterme**:
    - `st.image`, `st.video`, ve `st.audio` kullanarak görüntü, video ve ses dosyalarını gösterme yöntemleri.

6. **Kullanıcı Etkileşimi**:
    - `st.button`, `st.radio`, `st.checkbox`, `st.slider`, `st.number_input`, ve `st.file_uploader` gibi widget'lar.

7. **Ara Yüz Yerleşimi**:
    - Yan çubuk içeriği için `st.sidebar` ve sekmeli içerik için `st.tabs` kullanma.

8. **Streamlit Bileşenleriyle Program Akışı**:
    - Kullanıcı girdilerini yakalama ve işleme, ve verileri bir dosyaya kaydetme yöntemleri.

### session.py
9. **Oturum Durumu Yönetimi**:
    - Kullanıcı etkileşimleri arasında durumu korumak için oturum durumunun nasıl kullanılacağını gösterir.

## Kurulum

1. Depoyu klonlayın:

    ```bash
    git clone https://github.com/your-username/streamlit101.git
    ```

2. Proje dizinine gidin:

    ```bash
    cd streamlit101
    ```

3. `data.csv` dosyasının proje dizininde olduğundan emin olun.

4. Streamlit yüklü değilse yükleyin:

    ```bash
    pip install streamlit
    ```

5. Uygulamayı çalıştırın:

    ```bash
    streamlit run app.py
    ```

## Kod Özeti

### app.py

- **Oturum Durumu Başlatma**:
    ```python
    import streamlit as st 
    ```

- **Sayfa Konfigürasyonu**:
    ```python
    st.set_page_config(page_title="Streamlit 101", page_icon=":robot_face:")
    ```

- **Metin Gösterme**:
    ```python
    # st.write("En yaygın metin gösterme yöntemi")
    # st.markdown("_Biçimlendirilmiş Metin_")
    # st.header("Bu bir header örneği")
    # st.subheader("Bu ise bir subheader örneği")
    # st.code('for i in range(10): my_function()')
    # st.latex(r''' e^{i\pi} + 1 = 0 ''')
    ```

- **Multimedya Gösterme**:
    ```python
    # st.image(image="1-image_sample.png")
    # st.video(data="2-video_sample.mp4")
    # st.audio(data="3-audio_sample.mp3")
    ```

- **Kullanıcı Etkileşimi**:
    ```python
    # st.write("Lütfen Bilgilerinizi Girin")
    # st.text_input(label="Lütfen e-posta adresinizi giriniz:")
    # st.text_input(label="Lütfen şifrenizi giriniz:", type="password")
    # st.checkbox(label="Şifremi Unuttum")
    # st.divider()
    # st.number_input(label="Lütfen yaşınızı giriniz:", min_value=18, max_value=40, value=22)
    # st.slider(label="Lütfen yaşınızı giriniz:", min_value=18, max_value=40, value=22)
    # st.divider()
    # st.radio(label="Statünüz Nedir?", options=["Öğrenci", "Mezun"])
    # st.button(label="Giriş Yap")
    # st.divider()
    # st.file_uploader(label="Dosya Yüklemek İçin Tıklayınız")
    ```

- **Ara Yüz Yerleşimi**:
    ```python
    # st.sidebar.markdown("<h4>Uygulamamıza Hoşgeldin!</h4>", unsafe_allow_html=True)
    # st.sidebar.image("1-image_sample.png")

    # tab1, tab2 = st.tabs(["Kullanıcı Bilgileri", "Kullanım Tercihleri"])

    # with tab1:
    #     st.text_input(label="E-Posta Adresinizi Giriniz:")
    #     st.text_input(label="Şifrenizi Giriniz", type="password")
    #     st.checkbox(label="Şifremi Unuttum")
    #     st.divider()
    #     st.button(label="Kaydet")

    # with tab2:
    #     st.radio(label="Hesap Türü", options=["Öğrenci", "Mezun"])
    #     st.slider(label="Zaman Aşımı Süresi (saniye)", min_value=3, max_value=30, value=5)
    #     st.file_uploader(label="Güncel Özgeçmişinizi Yükleyiniz")
    ```

- **Program Akışı**:
    ```python
    import json

    st.sidebar.markdown("<h4>Uygulamamıza Hoşgeldin!</h4>", unsafe_allow_html=True)
    st.sidebar.image("1-image_sample.png")

    tab1, tab2 = st.tabs(["Kullanıcı Bilgileri", "Kullanım Tercihleri"])

    with tab1:
        eposta = st.text_input(label="E-Posta Adresinizi Giriniz:")
        sifre = st.text_input(label="Şifrenizi Giriniz", type="password")
        st.checkbox(label="Şifremi Unuttum")
        st.divider()
        kaydet_btn = st.button(label="Kaydet")

    with tab2:
        hesap_turu = st.radio(label="Hesap Türü", options=["Öğrenci", "Mezun"])
        st.slider(label="Zaman Aşımı Süresi (saniye)", min_value=3, max_value=30, value=5)
        st.file_uploader(label="Güncel Özgeçmişinizi Yükleyiniz")

    if kaydet_btn:
        data = []
        data.append({"eposta": eposta})
        data.append({"sifre": sifre})

        if hesap_turu == "Öğrenci":
            gecerlilik_suresi = 365
        elif hesap_turu == "Mezun":
            gecerlilik_suresi = 30

        data.append({"geçerlilik süresi": gecerlilik_suresi})

        with open("kullanici.txt", "w") as file:
            file.write(json.dumps(data))
        
        st.balloons()
        st.success("Dosyanız kaydedildi")
        st.write(f"Belirlenen geçerlilik süresi: {gecerlilik_suresi}")
    ```

### session.py

- **Oturum Durumu Mekanizması**:
    ```python
    import streamlit as st
    import pandas as pd

    st.header("Session State Mekanizması: Pratik Kullanım")

    if "satir_sayisi" not in st.session_state:
        st.session_state.satir_sayisi = 10

    dataframe = pd.read_csv("data.csv", sep=",")

    st.table(dataframe.head(st.session_state.satir_sayisi))

    def artir():
        st.session_state.satir_sayisi += 1

    def dusur():
        st.session_state.satir_sayisi -= 1

    artir_btn = st.button(label="Artır 👆", on_click=artir)
    dusur_btn = st.button(label="Düşür 👇", on_click=dusur)

    st.divider()
    st.header(st.session_state.satir_sayisi)
    ```

## Lisans

Bu proje MIT Lisansı altında lisanslanmıştır.
