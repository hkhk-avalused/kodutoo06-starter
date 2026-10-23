# Kodutöö 06 — Minu koduvõrk

**Sinu nimi:** _______________________

Tunnis rääkisime kahest kihist:

- **2. kiht:** MAC-aadress, kommutaator (switch), lokaalne võrk, kaader (frame)
- **3. kiht:** IP-aadress, ruuter (router), IP-pakett, mitu võrku, default gateway

Selles kodutöös leiad need asjad **oma kodu võrgust**. Iga õpilase vastused on erinevad, sest igaühel on oma arvuti ja oma kodu.

📖 Kui midagi ei mäleta, loe [Peatükk 4: Andmesidekiht](https://optalvik.github.io/avalused/teooria/04_andmesidekiht.html) (2. kiht) ja [Peatükk 6: Võrgukiht](https://optalvik.github.io/avalused/teooria/06_vorgukiht.html), osad „Ruuter — võrkude vaheline teejuht" ja „Default gateway" (3. kiht).

Failid laed üles nii: **Add file → Upload files**, lohista failid, vajuta **Commit changes**. README täitmiseks vajuta pliiatsit (✏️ Edit).

## Vali oma olukord (loe kõigepealt!)

Kõigil on sama töö: **3 faili + 3 vastust**. Erineb ainult see, mida pildistad.

| Sinu olukord | `ipconfig.png` | `ruuter.jpg` | Joonisel on ruuter |
|---|---|---|---|
| **A. Kodus on ruuter / WiFi-karp** (Telia, Elisa vms) | kodus, oma arvutis | ruuteri kleebis (WiFi parool kinni kaetud) | kodu ruuter |
| **B. Internet tuleb telefonist** (hotspot, levijagamine) | arvutis, kui on telefoni hotspot'iga ühendatud | ekraanipilt telefoni seadetest, kus levijagamine on sees (Android: Seaded → Ühendused → Mobiilne kuumkoht; iPhone: Settings → Personal Hotspot) | sinu telefon |
| **C. Ühiselamu WiFi** | ühiselamus, oma arvutis | pilt WiFi-saatjast seinal või laes; kui seda ei näe, ekraanipilt WiFi nimest arvutis | ühiselamu ruuter (kirjuta küsimusse 1, et see on ühiselamu oma) |
| **D. Kodus pole internetti** | koolis, kooli arvutis või oma sülearvutis kooli võrgus | pilt klassi võrgupesast seinal või kommutaatorist; küsi õpetajalt, kus on kooli ruuter | kooli ruuter (kirjuta küsimusse 1, et see on kooli oma) |

Default gateway leiad igal juhul samamoodi: `ipconfig /all` (osa 1).


---

## 1. Sinu arvuti aadressid → `ipconfig.png`

Ühenda arvuti WiFi või kaabliga võrku (kodus, ühiselamus või koolis, vt tabelit). Ava **Command Prompt** (Start → kirjuta `cmd` → Enter) ja kirjuta:

```
ipconfig /all
```

Otsi välja see adapter, millega oled võrgus. WiFi puhul on see **Wireless LAN adapter Wi-Fi**, kaabli puhul **Ethernet adapter Ethernet**. Selle adapteri all on:

| Inglise keeles | Eesti keeles Windowsis | Mis see on | Kiht |
|---|---|---|---|
| Physical Address | Füüsiline aadress | sinu võrgukaardi MAC-aadress, nt `A4-5E-60-12-34-56` | 2 |
| IPv4 Address | IPv4-aadress | sinu arvuti IP-aadress, nt `192.168.1.23` | 3 |
| Default Gateway | Vaikelüüs | ruuteri IP-aadress, tavaliselt lõpeb `.1`, nt `192.168.1.1` | 3 |

Tee ekraanipilt (**Win + Shift + S**) nii, et need kolm rida on näha. Salvesta nimega `ipconfig.png`.

💡 **Kui sul on Mac või Linux:**

- **Mac:** System Settings → Network → Wi-Fi → Details. Seal on IP address, Router (see on default gateway) ja Hardware → MAC address.
- **Linux:** terminalis `ip a` (MAC on `link/ether` real, IP on `inet` real) ja `ip route` (gateway on `default via` järel).

💡 Kui adapteri all on Default Gateway tühi, siis see adapter ei ole võrgus. Otsi järgmine adapter.

## 2. Sinu ruuter → `ruuter.jpg`

Default gateway on kodus üks konkreetne seade. Tavaliselt on see Telia, Elisa või muu teenusepakkuja karp, mille küljes on kaablid ja tulukesed. Leia see ja pildista **kleebist**. Kleebis on tavaliselt karbi all või taga ja sellel on mudel, MAC-aadress või S/N.

⚠️ **Kata kinni WiFi parool** (näpu või paberiga), kui see on kleebisel. Parool ei tohi pildile jääda.

Kui sul on olukord B, C või D, tee pilt nii, nagu on kirjas tabelis „Vali oma olukord" lehe alguses.

## 3. Joonis käsitsi → `joonis.jpg`

Joonista **paberile pliiatsiga** (mitte arvutis) oma koduvõrk:

- sinu arvuti, telefon ja teised seadmed, mis on kodus võrgus
- ruuter (või telefon, kui kasutad hotspot'i)
- internet (pilv)
- jooned seadmete vahel; WiFi puhul katkendjoon

Kirjuta joonisele oma arvuti **IP-aadress** ja ruuteri **IP-aadress** (default gateway) ülesande 1 pildilt. Pildista joonis ja salvesta `joonis.jpg`.

💡 Vihje: kõik seadmed, mis on ühendatud sama ruuteriga, on üks **lokaalne võrk**. Internet on **teine võrk**. Ruuter on nende kahe vahel.

## 4. Küsimused (vasta oma andmetega, 1–2 lauset)

**1. Mis on sinu default gateway IP-aadress ja mis seade see sinu kodus on?**

> ...

**2. Kas sinu arvuti ja telefon on samas lokaalses võrgus? Kuidas sa seda tead?**

> ...

💡 Vihje: telefonis näed IP-aadressi WiFi seadetes (vajuta võrgu nimel). Kui IP-aadressi kolm esimest numbrit on samad kui arvutil, nt `192.168.1.x`, ja gateway on sama, siis on nad samas võrgus.

**3. Sinu arvutil on MAC-aadress ja IP-aadress. Kumb on 2. kihi ja kumb 3. kihi aadress? Kumba kasutab ruuter, kui pakett läheb internetti?**

> ...

---

## ✅ Kontrolli enne, kui lõpetad

- [ ] Nimi kirjas
- [ ] `ipconfig.png`: näha IPv4, MAC ja Default Gateway
- [ ] `ruuter.jpg`: kleebis, WiFi parool kinni kaetud (või hotspot / kooli WiFi)
- [ ] `joonis.jpg`: käsitsi joonistatud, IP-aadressid peal
- [ ] Kõik 3 vastust kirjas, `...` ei ole enam alles

Järgmise tunni alguses seletad oma joonise järgi, kuidas pakett sinu arvutist internetti läheb. Võta joonis kaasa.
