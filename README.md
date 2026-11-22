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
- **Pembe kayan blok**: iki şerit arasında gidip gelir, zamanla
- **Sarkaç**: üç şeridi de süpürür; zıpla ya da boşluğu bekle
- **Rampa**: üstünden geçince havalanırsın, gökyüzündeki kristal yayını topla
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

## Gözcü (boss)
Her bölgenin 760. metresinde Gözcü gelir. 11 saniye boyunca şeritlere ateş eder; önce şerit kırmızı yanıp söner, sonra küre gelir. Hayatta kalırsan bonus kristal ve 250 puan.

## Toplar ve izler
Koşularda topladığın kristaller kasada birikir. Menüden yeni toplar aç; her topun kendi izi var:
Kehribar (kıvılcım), Buz (kar tanesi), Lav (kor), Zümrüt (yaprak), Nebula (yıldız tozu), Altın (altın para).

## Görevler ve başarımlar
Aynı anda 3 görev açıktır (tek koşuda N kristal, N m, seri, rampa, Gözcü...). Tamamlayınca kristal ödülü kasaya eklenir ve yeni görev gelir. 11 kalıcı başarım vardır; her biri +15 kristal.

## Yükseltmeler
Mıknatıs, 2x puan ve ağır çekim sürelerini 5 seviyeye kadar uzat (her seviye +%25). Başlangıç kalkanı ile her koşuya kalkanla başla.

## Günlük meydan okuma
Haritası tarihe göre belirlenir, gün boyunca herkes aynı diziyle koşar. Günün en iyi puanı saklanır; günde bir kez 500 m koşunca +40 kristal.

## Müzik
Oyun içinde üretilen, hızla birlikte temposu artan müzik. `M` tuşu ya da menüdeki düğmeyle aç/kapat.

Puan = mesafe + kristal puanları (kombo ve 2x dahil). Rekor, kasa ve toplar tarayıcıda saklanır.
