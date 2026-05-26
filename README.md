# Türkpatent LaTeX Şablonu (Temel Sürüm)

Bu depo, Türkpatent (Türk Patent ve Marka Kurumu) format kurallarına tam uyumlu patent veya faydalı model başvuruları hazırlamak için kullanıma hazır bir LaTeX şablonu sunmaktadır. Akademik bir dizin yapısı kullanılarak tasarlanmış olup, buluş sahiplerinin şekilsel gereksinimlerle uğraşmadan yalnızca içeriğe odaklanmasını sağlar.

## Özellikler

Bu şablon, Türkpatent tarafından zorunlu tutulan aşağıdaki kısıtlamaları otomatik olarak uygular:
- **Kenar Boşlukları**: Metin sayfalarında Üst/Sol 2.5-4 cm, Sağ 2-3 cm, Alt 2 cm olacak şekilde optimize edilmiştir. Çizimlerin yer aldığı resim sayfalarında ise kenar boşlukları otomatik olarak Üst/Sol 2.5 cm, Sağ 1.5 cm ve Alt 1 cm olarak değiştirilir. 
- **Satır Aralığı ve Numaralandırması**: Metin kısımlarında 1.5 satır aralığı kullanılır [3]. *Tarifname* ve *İstemler* bölümlerinde sol kenarda her 5 satırda bir satır numarası eklenir [1]. Resim sayfalarında satır numaralandırması otomatik olarak kapatılır. 
- **Sayfa Numaralandırması**: Metin sayfalarının alt-orta kısmında sürekli sayfa numaralandırması yapılır. *Resimler* bölümünde ise Türkpatent kuralları gereği "Mevcut Sayfa / Toplam Resim Sayfası" (örn. 1/3, 2/3) formatına otomatik geçiş yapılır.
- **Bölüm Geçişleri**: *Tarifname*, *İstemler*, *Özet* ve *Resimler* bölümlerinin her biri zorunlu olduğu üzere otomatik olarak yeni bir sayfadan başlar.

## Dizin Yapısı

Proje dosyaları, LaTeX ayarları ile patent metnini birbirinden ayırmak için şu şekilde yapılandırılmıştır:

turkpatent-latex-template/
│
├── main.tex                 # Derlenecek ana kök dosya.
├── preamble.tex             # Paketler, kenar boşlukları ve format ayarları.
│
├── bolumler/                # Başvuru metninin yer aldığı alt dizin.
│   ├── 01-tarifname.tex     # TARİFNAME
│   ├── 02-istemler.tex      # İSTEMLER
│   ├── 03-ozet.tex          # ÖZET
│   └── 04-resimler.tex      # RESİMLER (Şekillerin eklendiği dosya)
│
└── sekiller/                # Teknik çizimlerinizi koyacağınız dizin.

Nasıl Kullanılır?

    Bu depoyu bilgisayarınıza klonlayın.
    Derleme hatası almamak için sekiller/ klasörünün içine sekil1.png adında örnek bir resim (placeholder) ekleyin.
    Kendi buluş detaylarınızı bolumler/ dizinindeki ilgili .tex dosyalarına yazın. 01-tarifname.tex dosyası, zorunlu alt başlıklarla (Teknik Alan, Önceki Teknik vb.) önceden doldurulmuştur.
    Teknik çizimlerinizi (.png, .jpg, .pdf) sekiller/ dizinine yükleyin ve 04-resimler.tex dosyası içerisinden çağırın.
        Not: Türkpatent kuralları gereği çizimlerde antet veya çerçeve bulunmamalı; renk ve gölgelendirme yerine tarama çizgileri kullanılmalıdır.
    İşletim sisteminizdeki terminalden pdflatex main.tex komutunu çalıştırarak veya favori LaTeX editörünüzü (TeXstudio, VS Code vb.) kullanarak belgeyi derleyin.

Not: Türkçe babel paketinden kaynaklanan özel karakter (=) hatası preamble.tex içerisinde kalıcı olarak çözülmüştür.
