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
| E / Shift | Topun yeteneği |

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
Her 1000 metrede yeni bölge, yedi bölge döngüsü:
Gün Batımı → Gece Mavisi → Çöl Fırtınası → Buz Vadisi → Sualtı → Lav Kanyonu → Uzay Boşluğu.
Her bölgenin renkleri, engel dağılımı, müzik tonu ve hava efekti (kum, kar, kabarcık, kül, yıldız) farklıdır.
- **Çöl Fırtınası**: üç şeridi süpüren kum hortumu
- **Sualtı**: inip çıkan denizanaları
- **Uzay Boşluğu**: işaretli şeride düşen meteorlar, düşük yerçekimi

## Çatallanan yollar ve köprüler
- Yol arada ortadaki uzun bir duvarla ikiye ayrılır. Tabela riskli ve güvenli tarafı gösterir. Riskli tarafta blok, bariyer ve küçük uçurumlar arasında bolca kristal var; güvenli taraf sakin.
- Uçurumlarda tek şeritte raylı köprü kalır, art arda köprüler şerit değiştirir. Uçuruma düşmek koşuyu bitirir (kalkan bir kez seni sektirir).

## Yetenekler
Her kristal enerji çubuğunu %4 doldurur (Gözcü'yü atlatmak %40). Dolunca `E` / `Shift` ya da alttaki düğme:
| Top | Yetenek |
| --- | --- |
| Kehribar | Nova: öndeki 30 m engeli patlatır |
| Buz | Dondur: zaman 4 sn neredeyse durur |
| Lav | Erit: 5 sn engelleri eritir, uçurumda süzülür |
| Zümrüt | Hasat: üç şeride kristal yağar, 6 sn mıknatıs |
| Nebula | Işınlan: 40 m ileri |
| Altın | Midas: öndeki engeller kristale döner, 6 sn x3 kristal |

## Hayalet ve istatistikler
En iyi koşun kaydedilir ve sonraki koşularda yarı saydam "REKOR" hayaleti olarak yanında koşar; sağ üstte kaç metre önde/geride olduğu yazar. Günlük meydan okumada o günün en iyi koşusu hayalettir. Menüden kapatılabilir.
İstatistik sekmesi: toplam koşu, mesafe, kristal, zıplama, Gözcü, yetenek, oyun süresi, en sevdiğin top ve en çok neye çarptığın.

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

## Hikaye modu
10 bölüm, her birinin bitiş çizgisi ve kristal hedefleri var: bitirmek ★, ikinci hedef ★★, üçüncü hedef ★★★. Her yeni yıldız kasaya 15 kristal ekler; bir bölümü bitirmek sonrakini açar. 7. bölümde Gözcü, 10. bölümde Büyük Gözcü (24 sn, hızlanan ateş) var.

## Ayarlar
Grafik kalitesi (Düşük / Orta / Yüksek), parlama (bloom) efekti, hız çizgileri, ekran sarsıntısı, ana ses / müzik / efekt seviyeleri ve renk körlüğü modu (Okabe-Ito paletiyle engel renkleri).

## Hesaba kayıt
claude.ai'de açıldığında ilerleme (kasa, toplar, başarımlar, yıldızlar, istatistikler, ayarlar) oturum açan kişinin Claude hesabına da kaydedilir ve başka cihazda aynı hesapla açınca geri yüklenir. Google/Gmail girişi sayfa içinde desteklenmez. Yerel dosya olarak açıldığında yalnızca tarayıcıda saklanır.

## Çok oyunculu
claude.ai'de, sayfaya erişimi olan oturum açmış kişiler bir yarış odası açar ya da koda katılır. "Yarışı başlat" ile herkese aynı tohum gönderilir, 3 sn geri sayımdan sonra herkes aynı engel dizisinde koşar. Rakipler pistte isimleriyle görünür, sağ üstte canlı sıralama, sonunda en yüksek puan kazanır.
