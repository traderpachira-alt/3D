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
| M | Müziği aç / kapat |

Dokunmatik: sağa/sola kaydır şerit, yukarı kaydır ya da dokun zıpla, aşağı kaydır eğil.

## Engeller
- **Kırmızı blok**: üzerinden zıpla
- **Turuncu bariyer**: altından eğilerek geç
- **Mor duvar**: şerit değiştir
- **Kristal**: +10 puan
- **Yeşil kalkan**: bir çarpmayı emer

## Güçlendirmeler
- **Mıknatıs** (8 sn): yakındaki kristalleri her şeritten çeker
- **2x Puan** (10 sn): mesafe ve kristal puanı ikiye katlanır
- **Ağır çekim** (5 sn): dünya yavaşlar, tepki süren artar

## Kombo
Kristalleri 2 saniye içinde art arda topla. Her 5 kristalde çarpan bir artar (en fazla x5).

## Bölgeler
Her 1000 metrede yeni bölge: Gün Batımı → Gece Mavisi → Buz Vadisi → Lav Kanyonu. Her bölgenin renkleri, engel dağılımı ve müzik tonu farklıdır.

## Toplar
Koşularda topladığın kristaller kasada birikir. Menüden yeni toplar aç: Buz, Lav, Zümrüt, Nebula, Altın.

## Müzik
Oyun içinde üretilen, hızla birlikte temposu artan müzik. `M` tuşu ya da menüdeki düğmeyle aç/kapat.

Puan = mesafe + kristal puanları (kombo ve 2x dahil). Rekor, kasa ve toplar tarayıcıda saklanır.
