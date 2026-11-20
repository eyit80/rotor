# Rotor - Android uygulamasi (sunucusuz APK)

Bu uygulama tek basina calisir: bilgisayar, sunucu veya adres gerekmez.
Arayuz ve butun mantik (puanlama, ilan okuma, gecmis, favoriler, masraf hesabi) APK'nin icindedir.
Yapay zeka cagrilari telefondan dogrudan Google Gemini veya Anthropic Claude'a, SIZIN anahtarinizla yapilir.

## Kullanim
1. Ilk acilista cikan pencereye yapay zeka anahtarinizi yazin (Gemini icin ucretsiz anahtar: aistudio.google.com/apikey).
   Anahtar yalnizca bu telefonda saklanir. Sonradan degistirmek icin kenar cubugundaki "Yapay zeka anahtari" dugmesi.
2. Ilan linki, ilan metni, ekran goruntusu veya fotograf gonderin.
Hesap/giris yoktur; gecmis ve favoriler bu telefonda tutulur (uygulamayi silerseniz gider).

## APK'yi olusturma - Android Studio KURMADAN (kolay yol)
1. github.com'da ucretsiz hesap acin, sag ustte + > "New repository" ile bos bir depo olusturun (adi: rotor).
2. Depo sayfasinda "uploading an existing file" baglantisina tiklayin, bu klasorun ICINDEKI her seyi surukleyip birakin
   (app, gradle, .github klasorleri ve diger dosyalar), alttaki "Commit changes" dugmesine basin.
3. Ustteki "Actions" sekmesine gidin: "APK derle" calisir (3-5 dk). Yesil tik cikinca ilgili calismaya tiklayin,
   en altta "Artifacts" bolumundeki rotor-apk dosyasini indirin, zip'ten cikan app-debug.apk'yi telefona atip kurun.
   (".github" klasoru yuklenmediyse: Add file > Create new file > adina `.github/workflows/build.yml` yazip
   dosyanin icerigini yapistirin.)

## APK'yi olusturma - Android Studio ile (alternatif)
1. https://developer.android.com/studio adresinden Android Studio'yu kurun.
2. Android Studio > Open > bu `rotor_android` klasorunu secin (ilk acilista gerekli dosyalari indirir, internet gerekir).
3. Build > Build Bundle(s) / APK(s) > Build APK(s).
4. "locate" yazisina tiklayin: `app/build/outputs/apk/debug/app-debug.apk` -> telefona atip kurun
   (telefonda "bilinmeyen kaynaklardan yukleme" iznini verin).

## Rotor arayuzunu guncellediginizde
`python assets_guncelle.py ../rotor` komutu yeni arayuz dosyalarini APK'ya gomer, sonra APK'yi yeniden olusturun.

## Notlar
- Internet gerekir (yapay zeka ve ilan sayfalari icin).
- Bazi ilan siteleri uygulamadan gelen istegi de engelleyebilir (403); o zaman ilan metnini yapistirin veya ekran goruntusu yukleyin.
- Bu proje yazim sirasinda Android Studio'da derlenmemistir; derleme hatasi cikarsa hata mesajini iletin.
