# Kodutöö 06 — Minu koduvõrk

**Sinu nimi:** _______________________

Tunnis rääkisime kahest kihist:

- **2. kiht:** MAC-aadress, kommutaator (switch), lokaalne võrk, kaader (frame)
- **3. kiht:** IP-aadress, ruuter (router), IP-pakett, mitu võrku, default gateway

Selles kodutöös leiad need asjad **oma arvutist ja kodust**. Aega kulub umbes **1 tund**.

Failid laed üles nii: **Add file → Upload files**, lohista failid, vajuta **Commit changes**. README täitmiseks vajuta pliiatsit (✏️ Edit), kirjuta vastused `...` asemele ja vajuta **Commit changes**.

## Vali oma olukord

| Sinu olukord | Kus teed `ipconfig`-i | Joonisel on ruuter |
|---|---|---|
| **A. Kodus on ruuter / WiFi-karp** (Telia, Elisa vms) | kodus, oma arvutis | kodu ruuter |
| **B. Internet tuleb telefonist** (hotspot) | arvutis, kui see on telefoni hotspot'iga ühendatud | sinu telefon |
| **C. Ühiselamu WiFi** | ühiselamus, oma arvutis | ühiselamu ruuter |
| **D. Kodus pole internetti** | koolis, kooli arvutis või oma sülearvutis kooli WiFi-s | kooli ruuter |

---

## 1. Sinu arvuti aadressid → `ipconfig.png`

Ava **Command Prompt** (Start → kirjuta `cmd` → Enter). Kirjuta kõigepealt oma nimi, siis käsk:

```
echo Mari Maasikas
ipconfig /all
```

Otsi adapter, millega oled võrgus: WiFi puhul **Wireless LAN adapter Wi-Fi**, kaabli puhul **Ethernet adapter Ethernet**. Kui adaptereid on mitu (VPN, vEthernet), vali see, mille all on **Default Gateway** täidetud. Selle adapteri all leia neli rida: **Physical Address**, **IPv4 Address**, **Subnet Mask**, **Default Gateway**.

**Näide** (nimi sinine, otsitavad read kollased):

![Näide: ipconfig /all ekraanipilt koos nimega](naited/ipconfig-naide.png)

Tee ekraanipilt **kogu aknast**: **Win + Shift + S** → vali ülevalt **Window mode** → klõpsa käsuaknale. Pildil peavad olema näha sinu nimi ja kõik neli rida. Ära kärbi pilti ja ära pildista ekraani telefoniga. Salvesta `ipconfig.png`.

💡 **Mac:** System Settings → Network → Wi-Fi → Details (IP address, Router, MAC address). **Linux:** `ip a` ja `ip route`. Nime näitamiseks kirjuta terminali `echo Mari Maasikas`.

### Mida käsk teeb?

Igal Windowsi käsul on sisseehitatud abi. Kirjuta käsu järele `/?`, näiteks `ipconfig /?` või `ping /?`. Abi näitab, mida käsk teeb ja mis võtmed sellel on.

**1. Mida teeb käsk `ipconfig` ja mida lisab võti `/all`? Kirjuta abi põhjal oma sõnadega.**

> ...

### Täida tabel oma väljundi järgi

| Rida ipconfig'is | Sinu väärtus | Mis see on ja milleks seda vaja on? | Kiht (2 või 3) |
|---|---|---|---|
| Physical Address | ... | ... | ... |
| IPv4 Address | ... | ... | ... |
| Subnet Mask | ... | ... | ... |
| Default Gateway | ... | ... | ... |

📖 **Kust vastused leiad:**

- Physical Address: [Peatükk 4, „MAC-aadress — seadme isikukood"](https://optalvik.github.io/avalused/teooria/04_andmesidekiht.html#mac-aadress-seadme-isikukood) ja [„MAC vs IP-aadress"](https://optalvik.github.io/avalused/teooria/04_andmesidekiht.html#mac-vs-ip-aadress)
- IPv4 Address: [Peatükk 4, „MAC vs IP-aadress"](https://optalvik.github.io/avalused/teooria/04_andmesidekiht.html#mac-vs-ip-aadress) ja [Peatükk 6, „Ruuter"](https://optalvik.github.io/avalused/teooria/06_vorgukiht.html#ruuter-vorkude-vaheline-teejuht)
- Subnet Mask ja Default Gateway: [Peatükk 6, „Default gateway"](https://optalvik.github.io/avalused/teooria/06_vorgukiht.html#default-gateway-uks-valismaailma). Seal on sama väljund näitena.

## 2. Mõtle ise (1–3 lauset)

**2. Võrdle oma IPv4-aadressi ja Default Gateway't. Mis on neil sama ja miks?**

> ...

**3. Sinu telefonil on kodus aadress `192.168.1.40`. Sõbra telefonil on tema kodus samuti `192.168.1.40`. Kas see on viga? Miks?**

> ...

**4. Viid oma sülearvuti kooli ja ühendad kooli WiFi-ga. Kumb aadress muutub, MAC või IP? Miks?**

> ...

💡 Vihje küsimustele 3 ja 4: mõtle, kumb aadress on seotud **seadmega** ja kumb **võrguga**, kus seade parasjagu on.

## 3. Joonis käsitsi → `joonis.jpg`

Joonista **paberile pliiatsiga** (mitte arvutis) oma koduvõrk:

- sinu arvuti, telefon ja teised seadmed, mis on võrgus
- ruuter (vaata tabelit „Vali oma olukord")
- internet (pilv)
- jooned seadmete vahel; WiFi puhul katkendjoon
- **ring ümber lokaalse võrgu**: mis on sees ja mis väljas?

Kirjuta joonisele oma arvuti IP-aadress ja gateway IP-aadress (osa 1). Lehe ülaserva kirjuta **oma nimi**. Pildista **kogu leht** valges ruumis, nii et kõik kirjad on loetavad. Salvesta `joonis.jpg`.

**Näide** (sinu joonis on käsitsi ja sinu aadressidega):

![Näide: koduvõrgu joonis](naited/joonis-naide.png)

## 4. Milline ruuter osta?

Sa töötad IT-toes. Klient küsib, millise ruuteri ta peaks ostma, ja ütleb, mida ruuter **peab toetama**. Leia tootelehtedelt (osa **Specifications**), milline mudel sobib.

Koduruuter on mitu seadet ühes karbis: **ruuter** (ühendab kodu võrgu internetiga), **kommutaator** (juhtmega pordid kodu seadmetele) ja **WiFi-saatja**.

**Sinu klient sõltub sinu eesnime esitähest:**

| Eesnime esitäht | Klient | Ruuter peab toetama |
|---|---|---|
| A–H | **1. Pere** | vähemalt **5 juhtmega gigabit-porti** (internet + arvuti, teler, mängukonsool, printer) ja **WiFi 6** |
| I–P | **2. Suvila** | **WiFi 6**; ainult telefon ja sülearvuti, seega piisab **2,4 GHz** sagedusest; **kõige odavam** |
| R–Ü (ka Õ, Ä, Ö) | **3. Väike kontor** | **5 juhtmega gigabit-porti** ja WiFi ka **5 GHz** sagedusel; WiFi 6 pole vaja; **kõige odavam**, mis sobib |

**Valikus on 3 MikroTiki ruuterit:**

| Mudel | Tooteleht |
|---|---|
| hAP ax lite | <https://mikrotik.com/product/hap_ax_lite> |
| hAP ac² | <https://mikrotik.com/product/hap_ac2> |
| hAP ax² | <https://mikrotik.com/product/hap_ax2> |

💡 Mis rida tootelehel otsida:

- juhtmega pordid: `10/100/1000 Ethernet ports`
- WiFi: `Wireless 2.4 GHz standards`, `Wireless 5 GHz standards`. Kui 5 GHz rida puudub, ei toeta seade 5 GHz sagedust. `ax` = WiFi 6, `ac` = WiFi 5
- hind: `Suggested price` (tootja soovitushind)

**5. Mis number on sinu klient ja millise ruuteri valid? Kirjuta iga nõude kohta rida tootelehelt, mis seda tõestab (nt `10/100/1000 Ethernet ports = 5`), ja hind.**

> ...

**6. Vali üks teine mudel. Millise nõude järgi see sinu kliendile ei sobi? Too tootelehe rida.**

> ...

---

## ⭐ BOONUS: sinu ruuter ja selle juhend (lisapunktid õpetajalt)

Seda osa ei pea tegema. Kui teed, saad õpetajalt lisapunkte.

**Pilt → `ruuter.jpg`:** pildista oma ruuteri **kleebist** (tavaliselt karbi all või taga, seal on mudel). Pildil peab olema ka paberitükk sinu **nime ja kuupäevaga**. ⚠️ **Kata WiFi parool kinni**, kui see on kleebisel. Kui sul on olukord B, C või D, kasuta juhendi jaoks mudelit **MikroTik hAP ax²** ja pilti ei pea tegema.

**Kuidas juhendi leiad:** otsi `<mudel> user manual`, ava **tootja enda leht** (mitte pood või foorum). Teenusepakkuja karbi juhend on Telia või Elisa abilehel. Juhendit ei pea lugema algusest lõpuni: vajuta **Ctrl+F** ja otsi `192.168`, `default`, `reset`. MikroTik hAP ax² juhend: <https://help.mikrotik.com/docs/display/UM/hAP+ax%C2%B2>

**B1. Mis mudel see on? Pane link juhendile.**

> (boonus)

**B2. Mis aadressil avaneb juhendi järgi ruuteri seadistusleht? Kas see on sama mis sinu Default Gateway? Kui ei ole, siis miks võib see erineda?**

> (boonus)

**B3. Kuidas taastada tehaseseaded (reset)? Kirjuta sammud juhendi järgi.**

> (boonus)

---

## ✅ Kontrolli enne, kui lõpetad

- [ ] Nimi kirjas
- [ ] `ipconfig.png`: sinu nimi ja neli rida näha, kogu aken
- [ ] Tabel täidetud sinu andmetega
- [ ] `joonis.jpg`: käsitsi, nimi peal, lokaalne võrk ringiga
- [ ] Küsimused 1–6 vastatud, `...` ei ole enam alles
- [ ] (Boonus) `ruuter.jpg` ja B1–B3

Järgmise tunni alguses seletad oma joonise järgi, kuidas pakett sinu arvutist internetti läheb. Võta joonis kaasa.
