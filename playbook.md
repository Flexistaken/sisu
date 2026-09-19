# SISU — Playbook

Gün 1'e kadar ne yapılacağı, kurulum talimatları ve şablonlar. Bu dosya bir kez kullanılır ve sonra referans olarak durur.

---

## FAZ -1 · 16–20 Eylül · Tek iş: uyku

Bu beş günün tek amacı var: **28 Eylül'de sistem açıldığında uyku düzeninin oturmuş olması.** Kalkış saatinin yerleşmesi 4–7 gün alır. 21'inde başlarsan 25'inde taşınırken hâlâ ayarlanıyor olursun.

### Her gün

- [ ] **08:00'de kalk.** Yatış saatini düşünme, kontrol edemezsin. Kalkışı kontrol edersin.
- [ ] **Gündüz uyuma.** Bu kritik — gündüz uykusu tüm süreci sıfırlar.
- [ ] Telefon yataktan uzanılamayacak mesafede şarj olsun.

İlk gece 02:00'de uyursun, ikinci 01:00, üçüncü 00:30. Uyku basıncı işi kendisi halleder. "Yatağa girdim ama uyuyamadım" bir başarısızlık değil, sürecin normal parçası.

### 16–20 Eylül içinde bir kez

- [ ] **Baseline ölçümleri** → `baseline.md` (aşağıda liste var). Bu şimdi yapılmazsa bir daha yapılamaz.
- [ ] Miessler'ın yazısını oku: `danielmiessler.com/blog/personal-ai-infrastructure` → Bakılacak: üç katmanlı hafıza ayrımı ve ISC fikri
- [ ] Bir Obsidian + Claude Code videosu izle: `youtube.com/watch?v=glAoiBWVkmU` → Bakılacak: günlük kullanımda nasıl göründüğü. Kurulum adımlarını ezberleme.
- [ ] Obsidian'ı indir, boş bir vault aç, 20 dakika kurcala. Okumak değil, dokunmak.

---

## BASELINE ÖLÇÜMLERİ · `baseline.md`

20 dakikalık iş. 17 Ocak'ta "değiştim" diyebilmenin tek yolu.

**Vücut**

- Kilo (sabah, aç karnına)
- Boy
- Ölçüler: bel, göğüs, kol, uyluk
- Fotoğraf: ön / yan / arka — aynı ışık, aynı yer, aynı saat. 17 Ocak'ta aynısı çekilecek.
- Şu an kaldırdığın ağırlıklar (biliyorsan): squat, bench, deadlift, row
- Sol/sağ bacak farkı hissi — tek bacak squat kaç tekrar, hangi taraf zayıf

**Uyku**

- Son 7 günün yatış ve kalkış saatleri (Apple Watch'tan çek)
- Ortalama uyku süresi

**Dikkat**

- Son 7 günün günlük ekran süresi ortalaması
- Bunun içinde Instagram + TikTok + Shorts payı

**Akademik**

- GANO: 2.64
- Bu dönem alınan dersler ve kredileri (21 Eylül'de eklenir)

**İnşa**

- GitHub'daki mevcut repo sayısı ve son 30 günün commit sayısı
- Yayında olan şey sayısı: 0

**Ve bir yazı** Bugün nerede olduğunu kendi kelimelerinle 10 satır yaz. 17 Ocak'ta bunu okuyacaksın. Süslemeden yaz.

---

## FAZ 0 · 21–27 Eylül · Kurulum

Bu hafta **taban çalışıyor** ama başka hiçbir şey yok. Amaç: taban bir şehir değişikliğinden sağ çıkabiliyor mu?

### 21 Eylül · Pazartesi

- [ ] Ders seçimi
- [ ] Ders programını not et → hafta içi kalkış saatleri buna göre sabitlenir
- [ ] GitHub'da `sisu` reposunu oluştur (public)
- [ ] `identity.md`, `system.md`, `playbook.md`, `baseline.md` commit
- [ ] **Taban bugün başlıyor.** İlk `daily/2026-09-21.md` dosyası.

### 22 Eylül · Salı

- [ ] `areas/` altındaki 5 dosyayı yaz (şablon aşağıda)
- [ ] Claude Project'i kur (talimat aşağıda)
- [ ] Taban

### 23 Eylül · Çarşamba

- [ ] Pre-commit hook'u yaz (K3) — 2. haftadan itibaren devreye girecek
- [ ] Okunacak kitabı seç
- [ ] Taban

### 24 Eylül · Perşembe

- [x] ~~Özekes'e dil sınavı tarihini sor~~ — sorulmuştu: tarih dönem içinde duyurulacak. Varsayım: finallerin ortası. Duyuruyu takip et.
- [ ] Taban

### 25 Eylül · Cuma — İSTANBUL'A TAŞINMA

- [ ] **Sadece taban.** Başka hiçbir şey. Bu günün tek testi bu.
- [ ] **Taha ile üç konuyu konuş** (Taha 27 gecesi geliyor — telefonda, en geç 27'de; eve girmeden önce):
    - Gece evde ışık ve ses düzeni — saat kaçtan sonra ne olur
    - Mutfakta ne bulunacak, alışveriş nasıl yapılacak
    - Gym: hangi salon, hangi günler, kim kimi bekler

### 26–27 Eylül · Cumartesi–Pazar

- [ ] Ev kurulumu, telefonun şarj yeri belirlenir, çalar saat alınır
- [ ] Gym kararı (üyelik 28 Eylül'e kaydı — Taha 27 gecesi geliyor)
- [ ] Markete git, mutfağı doldur
- [ ] **Deneme haftalık değerlendirmesi:** `weekly/faz0.md` yaz. Faz 0'ın 7 günü üzerinden. Amaç şablonu test etmek. (Numaralandırmanın dışında — `w01` 28 Eylül–4 Ekim haftasının değerlendirmesidir.)
- [ ] Taban

### 28 Eylül · Pazartesi — **GÜN 1**

---

## KURULUM · Claude Project

1. Claude'da yeni bir Project aç, adı: **SISU**
2. Project talimatlarına (custom instructions) `identity.md`'nin **"Claude'a talimat"** bölümünü yapıştır
3. Project bilgisine (knowledge) şu dosyaları yükle:
    - `identity.md`
    - `system.md`
    - (`areas/` ilk aylık değerlendirmeden sonra — bkz. system.md §8)
4. `daily/`, `weekly/`, `monthly/` **yüklenmez** — her mesajda yüklenir ve token yakar. Gerektiğinde yapıştırılır.
5. `identity.md` / `system.md` değiştiğinde Project'teki kopyayı da güncelle. `areas/` ilk aylık değerlendirmede (28 Ekim) eklenir.

---

## KURULUM · Repo

```bash
mkdir sisu && cd sisu
git init
mkdir -p areas daily weekly monthly
# identity.md, system.md, playbook.md, baseline.md dosyalarını buraya koy
git add .
git commit -m "SISU başlangıç"
# GitHub'da public repo aç, sonra:
git remote add origin git@github.com:Flexistaken/sisu.git
git push -u origin main
```

### Pre-commit hook (K3)

> **Güncel sürüm `.githooks/pre-commit`'te** (19 Eylül): içerik kontrolü eklendi, repoya dahil. Kurulum: `git config core.hooksPath .githooks`. Aşağıdaki ilk sürüm tarihçe olarak duruyor.

`.git/hooks/pre-commit` dosyası, çalıştırılabilir yap (`chmod +x`):

```bash
#!/bin/sh
# 2. haftadan itibaren: geçen haftanın değerlendirmesi yoksa commit reddedilir.
START="2026-09-28"
TODAY=$(date +%Y-%m-%d)
DAYS=$(( ( $(date -d "$TODAY" +%s) - $(date -d "$START" +%s) ) / 86400 ))
WEEK=$(( DAYS / 7 ))

[ "$WEEK" -lt 1 ] && exit 0

PREV=$(printf "weekly/w%02d.md" "$WEEK")
if [ ! -f "$PREV" ]; then
  echo "K3 ihlali: $PREV yok. Haftalık değerlendirme yapılmadan yeni hafta başlamaz."
  exit 1
fi
exit 0
```

> Bu senin ilk İnşa çıktın. Çalışmazsa düzeltmek de İnşa'ya dahil.

---

## KURULUM · Sabah brief'i

Repo public olduğu için zamanlanmış bir görev her sabah son `daily/` dosyasını okuyup brief üretebilir.

Kurulumu Gün 1'den sonra, ilk hafta içinde yapılır — önce log'un gerçekten her gün yazıldığından emin olunur. Yazılmayan bir log'un brief'i olmaz; **otomatik olan, manuel olana bağımlıdır.**

Kurulumu birlikte yapacağız. Gerekli olan: repo adresi ve brief'in saati.

---

## ŞABLON · `areas/N-ad.md`

```markdown
# Alan N — AD

## Bu dönemki hedef

## Ölçümler

## Mevcut durum
(son güncelleme: TARİH)

## Program / kurallar

## Açık konular
```

---

## ŞABLON · `weekly/wNN.md`

Bu dosya, **hafızası olmayan** bir Claude'un okuyacağı varsayımıyla yazılır.

```markdown
# Hafta N — TARİH – TARİH

## Sayılar
Taban: __/7
3 işin tamamlandığı gün: __/7
Sadece-taban günü: __  (üst üste en fazla: __)

Temel:     kalkış farkı __ | evde pişen öğün __ | dışarıdan sipariş __
Vücut:     antrenman __ | tek bacak __ | yük ilerlemesi:
Akademik:  birikimli ders bloğu __/__ | dil sınavı bloğu __/3
İnşa:      commit __ | bu haftanın tekniği: ___ → ne fark yarattı:
Zihin:     günlük __/7 | okuma __/7 | sosyal medya ort. __ sa (hedef __)

## Desenler
Hangi gün tipleri kötü geçti, ortak noktaları ne:

## WOOP — gelecek hafta
Wish:
Outcome:
Obstacle (içsel, dışsal değil):
Plan: eğer ______ olursa, ben ______ yapacağım.

## Kararlar ve açık konular
Bu hafta verilen kararlar:
Sonraki haftaya taşınanlar:
Sistemde değişmesi gereken bir şey:

## Gelecek haftanın prompt tekniği
```

---

## İLK DÖRT HAFTA · kaba yön

Detay haftalık değerlendirmelerde çıkar. Bu sadece yön.

**Hafta 1 (28 Eylül–4 Ekim)** — Hiçbir şeyi optimize etme. Tek hedef taban 7/7. Gym başlar, hafif. Dil sınavı bloğu başlar.

**Hafta 2** — Birikimli dersler seçilir. Pre-commit hook devreye girer. Sosyal medya hedefi `system.md` §5'teki merdivene göre (hafta 1–2: ≤3 sa).

**Hafta 3** — Gym terfi kontrolü (3 hafta üst üste tuttuysa sabit bloğa geçer). Okuma ritmi oturmuş olmalı.

**Hafta 4** — İlk aylık değerlendirme (28 Ekim). Apple Health projesi burada masaya gelir. Vize takvimi netleşmiş olur, Sınav Modu haftaları takvime işaretlenir.

---

## KAPANIŞ · 17 Ocak 2027

Bitiş değil, **karar kapısı.**

O gün yapılacaklar:

- Baseline fotoğrafının aynısı çekilir, yan yana konur
- `baseline.md`'deki 10 satırlık yazı okunur
- Tüm sayılar karşılaştırılır
- `identity.md`'deki beş cümle tek tek işaretlenir: oldu / olmadı / kısmen (dil sınavı ve dönem ortalaması cümleleri sonuç gelince)
- **Faz 2 kararı verilir:** devam, değiştir, veya dur

Faz 2 kararı o gün verilir — öncesinde değil.