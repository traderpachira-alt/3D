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
- **Lazer kapı** (500 m'den sonra): yolu kesen bir kapı; her şeridin ışını sırayla açılıp kapanır, hep en az bir şerit açıktır. Kapanmadan önce ışın yanıp söner. Kapalı bir ışına girersen ölürsün.
- **Dönen testere** (350 m'den sonra): sana doğru yerden daha hızlı yuvarlanır (+11 m/s). Zıpla ya da şerit değiştir. 900 m'den sonra bazıları yolda sağa sola zikzak yapar.
- **Diken şeridi** (150 m'den sonra): bir şeritte 5 m'lik diken; üstünden zıpla. Üstünde kristal dizisi bekler, bazen iki şerit birden dikenli olur.
- **Avcı dron** (700 m'den sonra): önünde süzülür ve şeridini takip eder. Gözü kırmızıya dönüp ışın verdiği şeride 0,7 sn sonra mayın bırakır; 4–5 mayından kaç. Dron çalışırken yolda başka engel çıkmaz. Hepsini atlatırsan +6 kristal ve +120 puan.
- **Hızlandırıcı ped** (120 m'den sonra, yeşil oklu): üstüne basınca 1,7 sn boyunca dünya %45 hızlanır; arkasında kristal dizisi vardır.
- **Cam pano**: içinde kristaller donmuş şeffaf bir duvar. Çarpınca kırılır (+4 kristal, +40 puan), seni öldürmez ama ~1 sn yavaşlatır ve kombonu yarıya indirir. İstersen şeridini değiştirip kaçabilirsin. 250 m'den sonra duvarların bir kısmı cam olur.
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

## Hayalet (Rekoru kovala)
- Hayalet **en yüksek puanlı** koşunun kaydıdır; yalnızca kendi puanını geçen bir koşu onu değiştirir (eskiden "rekor kırılırsa" diye genel rekora bakılıyordu ve hayalet kayıp yeniden yazılabiliyordu).
- Her koşunun bir **tohumu** vardır ve pist yalnızca tohuma ve mesafeye bağlıdır: engeller, çatallar, viraj ve ters dönüşler, güçlendirmeler, Gözcü bölgeleri oyuncunun durumundan (güçlendirme, süre, hız) etkilenmez. Aynı tohum her seferinde aynı pisti verir.
- Hayalet o pistin kaydını taşır. Normal rastgele koşularda hayalet yoktur (başka pistte anlamsız olurdu). Menüdeki **Rekoru kovala** düğmesi rekor koşunun piste ve tohumuna döner; günlük meydan okuma da zaten her gün aynı pistte hayaletli koşulur.
- Yarışın ölçüsü artık puan farkıdır (kristal ve kombo): ekranda "Puan: +120 · hayalet 12 m önde" yazar. Art arda kristal toplamak hızı artırır (x2 = +3%, x5 = +12%), bu yüzden iyi oynayan hayaletin önüne geçer.
- En iyi hayalet Claude hesabına da yazılır (kendi belgesinde), başka cihazda da yarışabilirsin.

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

## Virajlar, U dönüşleri ve ters dönüşler
Yol artık düz değil. Oyun mantığı (şeritler, çarpışmalar) düz bir pist uzayında çalışır; bir vertex shader bu pisti yol boyunca büker ve kamera aynı yolu izler. Böylece:
- **Viraj**: 35–90° sağa ya da sola; kamera topla birlikte döner, güneş ve dağlar dünyaya sabit kalır.
- **U dönüşü** (1000 m'den sonra): 180° geri dönen viraj.
- **Ters dönüş** (450 m'den sonra): yol yarım tur dönüp tavana çıkar, ekran tersine döner; bir süre sonra eski haline döner.
- **Burgu** (1200 m'den sonra): yol tam tur döner ve virajla birleşir.
Özellik yaklaşmadan önce ekranda uyarı çıkar. Ayarlar'dan "Virajlar ve ters dönüşler" Kapalı / Viraj / Tam seçilebilir (baş dönmesi için). Hikaye modunda ilk iki bölüm düzdür, sonrası kademeli olarak virajlıdır.

## Yeni modlar (Modlar sekmesi)
| Mod | Kural |
| --- | --- |
| Zamana karşı | 60 sn. Çarpmak ve uçuruma düşmek 5 sn götürür, her kristal 1,5 sn ekler. Süre bitince koşu biter. |
| Hız çılgınlığı | 24 m/s ile başlar, hız çok çabuk artar (en çok 50). Kalkan yok, puan x2, engel yoğunluğu en yüksek. |
| Zen yolculuğu | Engel ve Gözcü yok, ölüm yok. 150 sn boyunca kristal topla; yol sık sık virajlanır ve ters döner. |
| Haftalık mutasyon | Haftaya göre değişen kural: Ay yürüyüşü (yarı yerçekimi), Kristal yağmuru, Karanlık hat (kısa görüş), Kalabalık yol (her sırada iki şerit kapalı). Harita herkes için aynıdır. |
Her mod için en iyi puan saklanır (hesap kaydıyla senkronlanır).

## Hesap verisi salt okunur gelir
Claude hesabından okunan kayıt (db anlık görüntüsü) dondurulmuş nesnelerdir. Oyun bu veriyi (görevler, istatistikler, günlük kayıt) değiştirdiği için, kayıt yüklenmiş bir oyunda görev tamamlanınca `Attempted to assign to readonly property` hatası her karede tekrarlanıyordu. Kayıt artık okunur okunmaz düz bir kopyaya çevrilir.

## Hata kurtarma ve güvenli mod
- Oyun döngüsünde bir hata olursa oyun durmaz; ekranda kısa bir "Hata" bildirimi çıkar. Aynı hata her karede tekrarlanırsa oyun menüye döner, bir hata paneli (mesaj, yığın, mesafe, yol durumu, cihaz bilgisi) gösterir ve hata yol ya da çizimle ilgiliyse virajları güvenlik için kapatır. Ayarlar'dan tekrar açılabilir.
- Oyun sırasında sayfa yakalanamayan bir çökmeyle kapanırsa (ör. telefonda bellek), bir sonraki açılışta "Önceki oturum kapandı" paneli çıkar ve yine virajlar kapatılır.
- Virajlar kapalıyken çizim eski, düz yoldaki gibi çalışır (bükme gölgelendiricisi hiç devreye girmez).

## Kristallerin kasaya geçişi
Kristaller artık koşu bitmeden, her birkaç saniyede bir ve duraklatınca, menüye dönünce, uygulamayı arka plana atınca kasaya yazılır. Çökme, çıkış ya da menüye dönüş kristal kaybettirmez. Oyun içinde sağ üstte canlı "Kasa" sayacı vardır.

## Riskli yol düzeni
Çatalda riskli şeritte şerit değiştiremediğin için engeller aralıklı gelir: zıpladıktan sonra yere inip bakmaya zaman kalacak kadar (zıplamadan sonra ~1,8 sn, eğilmeden sonra ~1,2 sn). Çatal hıza göre uzar (130–260 m).

## Çizim notu (nokta, çizgi ve etiketler)
Yol bükme gölgelendiricisi kamera matrisini kendi `uView` değişkeniyle alır. Three.js (r128) `viewMatrix`'i yalnızca mesh malzemelerine yüklediği için, ona güvenen nokta (iz, hava efekti), çizgi (engel kenarları, hız çizgileri) ve etiket (hayalet, rakip adı) nesneleri tek noktaya çöküp görünmez oluyordu.
