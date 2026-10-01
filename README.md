# Pixel 7 · Donanım Testi (PWA)

Pixel 7 / Android 14 hedef alınarak geliştirilmiş, **Web Tabanlı Mobil Uygulama Geliştirme**
dersi laboratuvarı için hazırlanmış çok amaçlı donanım test PWA'sı.

## Test Edilenler
| Modül      | Kullanılan Web API |
|------------|--------------------|
| Ekran      | Fullscreen API, Screen Wake Lock, `screen.*`, `devicePixelRatio`, rAF (Hz ölçümü) |
| Dokunmatik | Pointer Events, `navigator.maxTouchPoints`, Canvas 2D |
| Hoparlör   | Web Audio API (`OscillatorNode`, `StereoPannerNode`, `GainNode`) |
| Mikrofon   | `getUserMedia`, Web Audio `AnalyserNode`, `MediaRecorder` |
| Titreşim   | Vibration API |
| İnternet   | `navigator.onLine`, Network Information API, Fetch + Streaming |

## GitHub Pages'e Yayınlama
1. Yeni bir repo aç: `pixel7-donanim-testi`
2. Dosyaları yükle (bkz. `kur.sh`)
3. **Settings → Pages → Source: Deploy from a branch → main / (root)**
4. Adres: `https://<kullanıcı>.github.io/pixel7-donanim-testi/`

> PWA için HTTPS şarttır. GitHub Pages otomatik HTTPS sunar. ✅

## Önemli Notlar
- **Mikrofon** ve **Wake Lock** yalnızca HTTPS'te çalışır.
- **Titreşim (Vibration API)** yalnızca Android Chrome'da desteklenir.
- **iOS Safari**'de Vibration API ve `beforeinstallprompt` yoktur (bu proje Android hedeflidir).
- Renk turundayken ekran kapanmasın diye Wake Lock istenir.

## Dosya Yapısı