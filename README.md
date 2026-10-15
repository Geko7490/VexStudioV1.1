# VexEdit Studio

Android için çevrimdışı öncelikli, modüler yaratıcı video/ses editörü. (Offline-first modular creative editor for Android.)

## Özellikler / Features
- Tamamen yerel video & ses düzenleme (fully local editing)
- Modüler mimari, Modül Merkezi, gerçek indirme yöneticisi
- Çok katmanlı zaman çizelgesi, efektler, presetler, Undo/Redo
- MP4 dışa aktarma, ses miksajı
- Türkçe/İngilizce

## Derleme / Build
### Web (demo)
```
npm install
npm run build
```
### Android
Android Studio veya Gradle ile:
```
./gradlew :app:assembleDebug
```
APK: `app/build/outputs/apk/debug/`

## GitHub Actions
`.github/workflows/android-build.yml` push/PR/dispatch üzerinde otomatik derleme yapar ve APK artifact üretir. Release imzalama için repository secrets: `KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS`, `KEY_PASSWORD`.

## Lisanslar / Licenses
- Uygulama kodu: MIT (LICENSE)
- Üçüncü taraf bağımlılıklar: THIRD_PARTY_LICENSES.md
- FFmpeg (kullanılırsa): LGPL/GPL koşullarına tabidir; kullanılan sürüm ve codec desteği ayrıca belgelenmelidir.

## Bilinen sınırlamalar / Known limitations
- Android medya motoru (MediaCodec/OpenGL) bu iskelette placeholder'dır; tam uygulama aşamalı geliştirilecektir.
- Web demo, Android uygulamasının UI/akış prototipidir.