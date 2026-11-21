# Kehribar Hattı

Three.js ile yazılmış, tarayıcıda çalışan 3D sonsuz koşu oyunu. Tek dosya: `index.html`.

## Çalıştırma
`index.html` dosyasını bir tarayıcıda açın (Three.js CDN'den yüklenir).

## Kontroller
| Tuş | Eylem |
| --- | --- |
| ← / → (A / D) | Şerit değiştir |
| ↑ / Boşluk (W) | Zıpla |
| ↓ (S) | Eğil, havadayken hızlı in |
| P / Esc | Duraklat |

Dokunmatik: sağa/sola kaydır şerit, yukarı kaydır ya da dokun zıpla, aşağı kaydır eğil.

## Engeller
- **Kırmızı blok**: üzerinden zıpla
- **Turuncu bariyer**: altından eğilerek geç
- **Mor duvar**: şerit değiştir
- **Kristal**: +10 puan
- **Yeşil kalkan**: bir çarpmayı emer

Puan = mesafe (m) + kristal × 10. Rekor tarayıcıda saklanır.
