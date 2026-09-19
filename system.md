# SISU — Sistem

Bu dosya **nasıl** çalıştığını tanımlar. `identity.md` **niye** çalıştığını tanımlar.

---

## 1. Takvim

| | Tarih | İş |
|---|---|---|
| **Faz -1** | 16–20 Eylül | Sadece kalkış saati. Kaynaklar. Baseline ölçümleri. |
| **Faz 0** | 21–27 Eylül | Kurulum, repo, Project. Taban çalışıyor. 25'inde taşınma. |
| **Gün 1** | 28 Eylül | Sistem tam açılıyor. |
| **Gün 112** | 17 Ocak 2027 | Karar kapısı. Faz 2 kararı burada verilir. |

Ara kilometre taşları: Ay 1 → 28 Ekim · Ay 2 → 28 Kasım · Ay 3 → 28 Aralık

---

## 2. Taban

Dört madde. Her gün aynı. Zincir bunlardan sayılır.

1. **Kalkış saati tutuldu.** Yatış saati değil — kontrol edebildiğim şey bu.
2. **En az 10 dakika hareket.** Yürüyüş sayılır.
3. **En az 25 dakika odaklı iş.** Alan 3 veya 4'ten. Kesintisiz.
4. **Akşam log'u yazıldı.**

**Kalkış kuralı:** hafta içi kalkış ders programına göre sabitlenir. Hafta sonu, o saatin **en fazla 1 saat sonrası**. Asıl metrik hafta içi/hafta sonu farkıdır — okul takvimine bağımlı olmayan tek uyku ölçüsü budur.

**25 dakika ile 3 iş ilişkisi:** 25 dakika ek iş değil, **zemin**. Normal günde 3 işten biri zaten kapsar. Sadece çöken günde tek başına durur.

**Taban yapıldıysa gün geçerlidir.** Üstündeki her şey gerçek performanstır ve ayrı ölçülür.

**İzin günü yoktur.** Ne pazar, ne bayram, ne doğum günü. Taban zaten izin gerektirmeyecek kadar küçük, ve "izin günü" kavramı ilk delindiğinde genişler.

**Hastalık kuralı.** Ateş, grip, mide — gerçek hastalık gününde taban **sadece log'a** iner. Hareket ve odaklı iş düşer, zincir kırılmaz. Hasta olmak bir başarısızlık değil; hastayken antrenman yapmak aptallıktır. Kural: hastalık log'a yazılır, iki günü geçerse haftalık değerlendirmede konuşulur.

---

## 3. Günün 3 işi

Log şablonunda **fiziksel olarak üç satır** var. Dördüncü satır yok. Yeni bir şey eklemek için mevcut birini silmek gerekir.

**Takvimde sabit blok olan şeyler slot harcamaz.** Ders, gym (terfi ettikten sonra), koşu kulübü — bunlar randevu, karar değil. 3 slot isteğe bağlı emek içindir.

**Terfi mekaniği.** Bir şey üç hafta üst üste yapıldığında görev listesinden çıkar, takvime sabit blok olarak geçer ve slotu boşaltır. Yerleşenler dibe çöker, slotlar üstte kalır. Sistem büyümez, sıkışmaz.

> Gym ilk 3–4 hafta 3 işten biridir. Üç hafta üst üste tutunca terfi eder.

---

## 4. Kısıtlar

Üç tane. Dördüncüsü gelirse yanlış yoldayız.

**K1 — Telefon mesafesi.**
Telefon gece odada ama yataktan uzanılamayacak mesafede şarj olur. Alarm için ucuz çalar saat.
*Amacı telefon değil, kalkış saatidir.* Kalkış tutuyorsa mekanizma yeterlidir. **İki hafta üst üste kalkış kayarsa telefon odadan çıkar.** Kararı veri verir, tartışma vermez.

**K2 — Günde üç iş, dördüncü satır yok.**
Şablon sınırsız olsaydı sabah 8 madde yazılır, akşam 3'ü yapılır, gün "5 iş yapamamış gün" olarak kaydedilirdi. Üç slot, üçü bitince günü **tam** yapar.

**K3 — Haftalık değerlendirme yapılmadan yeni hafta başlamaz.**
Mekanizma: repoda sürümlenen pre-commit hook (`.githooks/pre-commit`, `core.hooksPath`). Geçen haftanın `weekly/wNN.md` dosyası yoksa veya Taban / Obstacle / Plan satırları boşsa günlük commit reddedilir. `--no-verify` ile atlamak K3 ihlalidir ve o haftanın weekly dosyasına yazılır.
*2. haftadan itibaren geçerli.*
Sebebi: haftalık değerlendirme ilk düşen şeydir ve düştüğünde sistem körleşir — sessiz kayma tam orada olur.

---

## 5. Beş alan

### 1 — TEMEL · uyku + beslenme
Zaman rakibi değil, diğer dördünün ön koşulu.

**Ölçümler:** hafta içi/hafta sonu kalkış farkı ≤ 1 saat · haftada evde pişen öğün sayısı · haftada dışarıdan sipariş/fast food sayısı (baseline ilk hafta ölçülür, sonra azaltılır).

İlk ayın yemek hedefi sıkı diyet değil: **4–5 yemeği gerçekten pişirebilir hale gelmek, mutfağı dolu tutmak, dışarıdan beslenmeyi azaltmak.** Yediğine dikkat etmek buna dahil; gram saymak değil. Protein/kalori takibi şimdilik yok — istenirse bir haftalık değerlendirmede eklenir.

### 2 — VÜCUT · kuvvet + koşu tabanı + diz
Bu dönem **kuvvet baskın**. Skinny fat'in cevabı koşu hacmi değil, progresif ağırlık ve yeterli protein. Skinny fat'ken çok koşmak seni daha küçük yapar, daha iyi değil.

**Tek bacak çalışması zorunlu parça** (split squat, step-up, tek bacak RDL) — ACL geçmişi + kuvvet asimetrisi + artan hacim klasik sakatlık üçlüsü. Opsiyonel değil.

Basket ve voleybol eğlencedir, program değildir. Triathlon kuzey yıldızıdır, bu dönemin programı değildir.

**Ölçümler:** haftalık antrenman sayısı · ana hareketlerde yük ilerlemesi · tek bacak çalışması yapıldı mı.

### 3 — AKADEMİK & ERASMUS · öncelikli alan
Zaman çakışmasında kazanan alan.

**Birikimli dersler** (matematik, devreler, sinyal, programlama) haftalık takip edilir — bunlarda bilgi değil **beceri** ediniliyor ve beceri tekrar olmadan oluşmuyor; yığma fizik olarak çalışmaz. **Ezber/genişlik dersleri** kendi yöntemine bırakılır. Seçilen birikimli ders sayısı: 2–3.

**Dil sınavı hazırlığı Ekim–Aralık'ta yapılır, Ocak'ta yapılmaz.** Sınav finallerin ortasında (varsayım — tarih dönem içinde duyurulacak); o hafta Sınav Modu'nda olunacak ve İngilizce'ye zaman kalmayacak. Ocak'a bırakmak matematiksel olarak imkânsızdır.

**Ölçümler:** seçilen birikimli dersler o hafta bloğunu aldı mı (2–3 blok/hafta) · dil sınavı blokları (3/hafta).

### 4 — İNŞA · üretmek + Claude'da ustalaşmak
Tek alan, çünkü ayrılırsa "öğrenme" video izleyip hiçbir şey üretmemeye dönüşür.

"Para kazanan sistem" bu alanın içinde, dürüst kapsamla: 112 günde para kazanılmaz, **yayınlanır**.

**Haftalık prompt mekaniği.** Anthropic'in interaktif kursu 9 bölüm. Haftada bir bölüm okunur ve o hafta o teknik Claude ile bilinçli kullanılır. Haftalık değerlendirmede tek soru: *"bu teknik ne fark yarattı?"*

**Proje adayları:**
- Apple Watch/Health verisinden uyku ve antrenman çeken kişisel API — log'un ölçüm kısmını otomatikleştirir. **4–6. haftadan önce başlanmaz**: bir ay manuel yürütülmemiş bir formatı otomatikleştirmek, yanlış şeyi inşa etmektir.
- `state.json` üreteci — private log'dan sadece sayıları içeren public bir durum dosyası çıkaran script. Repo private'a geçerse gerekli olur.
- Pre-commit hook (K3) — Faz 0'ın küçük işi.

**Ölçümler:** haftalık commit sayısı · dönem sonunda yayınlanmış en az bir şey.

### 5 — ZİHİN · günlük + okuma + dikkat
**Günlük:** her gün. Kişisel günlük repo **dışında** kalır; log'a sadece "günlük yazıldı" olarak geçer. Ölçülen şeyle içini döktüğün şey karışırsa ikisi de bozulur.

**Okuma:** günde 10 sayfa. Küçük görünüyor ama %15'lik günde de yapılabilir olması şart. 112 gün × 10 sayfa ≈ 1120 sayfa ≈ 3–4 kitap. Kitap Faz 0'da seçilir.

**Dikkat:** ölçülen şey **toplam ekran süresi değil**, sosyal medya ve kısa video süresi (Instagram, TikTok, Shorts). Kod yazmak, ders çalışmak, Claude ile konuşmak ekran süresidir ama sorun değildir; toplam süreyi hedeflemek iyi kullanımı da cezalandırır.

**Baseline (19 Eylül, son 3 hafta ortalaması):** günlük 7 saat toplam ekran, bunun **~4 saati** TikTok + Instagram.

Kademeli hedef, **haftalık ortalama** üzerinden (günlük sapma gürültüdür):

| Hafta | Sosyal medya + kısa video, günlük ortalama |
|---|---|
| 1–2 | ≤ 3 saat |
| 3–4 | ≤ 2 saat |
| 5+ | ≤ 1,5 saat |

**Ölçümler:** günlük yazıldı mı · okuma günleri · sosyal medya haftalık ortalaması.

### Çakışma sırası
**Akademik > Vücut > İnşa > Zihin.**
Temel bu sıranın dışında, çünkü rakip değil koşul.
Vücut, İnşa'nın önünde: sakatlanır veya çökersen diğer üçü de düşer.

---

## 6. Sınav Modu

Vize ve final haftaları **önceden** takvime işaretlenir.

O haftalarda sadece **taban** çalışır. Vücut haftada 2 minimuma iner, İnşa durur, Zihin sadece günlüğe iner. Zincir kırılmaz.

**Önceden ilan edilir, o gün ilan edilemez.** Salı günü yorgun olduğun için Sınav Modu'na geçilmez. Bu, "%15'lik gün" açığını kapatan mekanizmadır.

**Süre sınırı: bir sınav dönemi için en fazla 2 hafta.** Üçüncü haftaya taşıyorsa bu sınav modu değil, çöküştür.

> Sınav Modu'nda en çok kayan taban maddesi **hareket**tir. 10 dakika yürüyüş, 10 saat çalışmanın içine sığar.

---

## 7. Ritim

### Günlük — 5 + 3 dakika
**Sabah (5 dk):** log dosyası açılır, 3 iş yazılır, brief alınır.
**Akşam (3 dk):** taban tiklenir, ne çalıştı / ne çalışmadı yazılır, commit atılır.
**Claude en fazla 5 cümle döner.** Uzun analiz haftalıkta.

### Haftalık — Pazar akşamı, ~30 dakika
Yeni konuşma (Opus). O haftanın 7 günlük dosyası + geçen haftanın `weekly` dosyası yapıştırılır.

1. Sayılar
2. **Sadece-taban günleri kaç taneydi ve neden.** Üst üste 3 tane = sistem alarmı
3. Desenler — hangi gün tipleri sistematik kötü
4. **WOOP:** Wish → Outcome → **Obstacle** (içsel) → Plan (eğer X olursa ben Y yapacağım)
5. Gelecek haftanın prompt tekniği
6. `weekly/wNN.md` yazılır — bu dosya yazılmadan pazartesi commit'i geçmez

### Aylık — ~1 saat
Trendler, `areas/` güncellemesi, alan ağırlıklarının yeniden ayarlanması, gerekirse taban revizyonu.

### Gösterim kuralı
**Günlük görünümde sadece zincir var.** "Gün 48. Taban 48/48." Başka sayı yok.
Hedef oranı sadece **haftalık**'ta görünür. Trend sadece **aylık**'ta.
Her katmanda sadece o katmanda işe yarayan bilgi.

---

## 8. Claude ile çalışma protokolü

**Claude konuşmaları hatırlamaz.** Süreklilik dosyalarda, Claude'da değil. Tasarım buna göre kurulmuştur.

**Project bilgisine konacaklar** (sabit, küçük, her konuşmada yüklü):
`identity.md` · `system.md`
`areas/*.md` ilk aylık değerlendirmeden (28 Ekim) sonra eklenir — o zamana kadar system.md'nin kopyasıdır, yaşayan durum tutmaz.
`playbook.md` ve `baseline.md` konmaz: biri tek kullanımlık, diğeri sadece aylık/kapanışta gerekir, gerektiğinde yapıştırılır.

**Project'e konmayacaklar** (hacimli, gerektiğinde yapıştırılır):
`daily/` · `weekly/` · `monthly/`

**Model bölüşümü:** günlük check-in → Sonnet. Haftalık, aylık, tasarım → Opus.

**Konuşma hijyeni:** haftada bir yeni konuşma. Tek dev thread'de 112 gün gidilirse her mesajda tüm geçmiş yeniden yüklenir ve maliyet katlanır.

**Devir teslim:** `weekly/wNN.md`, hafızası olmayan bir Claude'un okuyacağı varsayımıyla yazılır. "Kararlar ve açık konular" bölümü süreklilik mekanizmasıdır.

**Sayaç Claude'un işi değil.** Zincir kaç gün, hangi gün kaçtı — repo'nun işi. Claude yorum, desen ve karar için.

**Otomasyon sınırı:** Girdi asla otomatikleşmez. Teslimat ve analiz otomatikleşebilir. Analiz soru olarak döner.

**Repo public'tir ama ilan edilmemiştir.** Link paylaşılmaz, proje anlatılmaz. İhlal repo ayarı değil, sosyal paylaşımdır.
> Risk: okunabileceğini bildiğin bir dosyaya "ne çalışmadı" yazarken yumuşatma ihtimali. Kendini yumuşatırken yakalarsan private'a geçilir ve `state.json` çözümü devreye alınır.

---

## 9. Çöküş protokolü

40–50. gün, bu tür projelerde bırakmanın en yoğun olduğu aralıktır. Motivasyon bitmiş, son hâlâ uzaktır. Bu protokol **o an yazılamaz**, o yüzden şimdi yazılıyor.

**Bir gün kaçtığında:** hiçbir şey olmaz. Ertesi gün taban yapılır. Geriye dönüp telafi edilmez, ileriye taşınmaz. Sayaç "47/48" olur ve devam eder.

**Üç gün üst üste sadece taban olduğunda:** sistem alarmı. Haftalıkta tek soru — bu yorgunluk mu, yoksa alanlardan biri yanlış mı kurulmuş?

**Bir hafta boyunca taban bile kaçtığında:** proje bitmemiştir. O hafta `weekly/` dosyasına "çöküş" olarak yazılır, sebebi aranır, ve **taban tek maddeye indirilir** (sadece kalkış saati) ta ki zincir tekrar kurulana kadar. Küçültmek bırakmaktan iyidir.

**"Bu projeyi bırakayım" düşüncesi geldiğinde:** bu düşünce 40–50. gün aralığında istatistiksel olarak beklenen bir olaydır, kişisel bir yetersizlik sinyali değildir. **O gün hiçbir karar verilmez.** Karar sadece pazar akşamı, veriye bakarak verilir.

**Plato normaldir.** 5–8. haftada ilerleme düzleşecek. Gerçek ilerleme doğrusal değildir — plato yapar, düşer, sonra sıçrar. Günde %1 beklentisi bu platoyu başarısızlık diye okutur.

---

## 10. Dosya yapısı

```
sisu/                      (public repo, ilan edilmemiş)
├── identity.md            Kim olmaya çalışıyorum
├── system.md              Bu dosya
├── playbook.md            Zamanlı eylem listesi + kurulum
├── baseline.md            16-20 Eylül ölçümleri (bir kez yazılır, değişmez)
├── CLAUDE.md              Claude Code için talimat (identity.md'den türetilir)
├── .gitignore
├── areas/
│   ├── 1-temel.md
│   ├── 2-vucut.md
│   ├── 3-akademik.md
│   ├── 4-insa.md
│   └── 5-zihin.md
├── templates/
│   ├── daily.md
│   └── weekly.md
├── daily/YYYY-MM-DD.md
├── weekly/wNN.md
└── monthly/mN.md
```

`areas/` dosyaları **yaşayan durum** tutar, başlangıç sayılarını değil. Başlangıç için `baseline.md`'ye referans verilir; güncel sayılar aylık değerlendirmede yenilenir.

Kişisel günlük bu reponun dışındadır.

---

## 11. Günlük log şablonu

```markdown

## Taban
- [ ] Kalkış HH:MM        (gerçek: __:__)
- [ ] Hareket ≥ 10 dk
- [ ] 25 dk odaklı iş
- [ ] Bu log yazıldı

## Bugünün 3 işi
1.
2.
3.

## Akşam
Ne çalıştı:
Ne çalışmadı:
Yatış planı:
```
