[README.md](https://github.com/user-attachments/files/28057861/README.md)[README.md](https://github.com/user-attachments/files/28057860/README.md)
# ⏱️ Štoperica — Flowcode Projekat

<div align="center">

![Flowcode](https://img.shields.io/badge/Flowcode-2.0-blue?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNk+M9QDwADhgGAWjR9awAAAABJRU5ErkJggg==)
![Status](https://img.shields.io/badge/Status-Završeno-brightgreen?style=for-the-badge)
![Škola](https://img.shields.io/badge/Školski_Projekat-2024%2F2025-orange?style=for-the-badge)
![Jezik](https://img.shields.io/badge/Jezik-Flowcode-purple?style=for-the-badge)

**Digitalna štoperica izrađena u Flowcode razvojnom okruženju kao školski projekat.**

</div>

---

## 📋 Sadržaj

- [O Projektu](#-o-projektu)
- [Funkcionalnosti](#-funkcionalnosti)
- [Snimci Ekrana](#-snimci-ekrana)
- [Pokretanje Projekta](#-pokretanje-projekta)
- [Kako Koristiti](#-kako-koristiti)
- [Dijagram Toka](#-dijagram-toka)
- [Struktura Projekta](#-struktura-projekta)
- [Autor](#-autor)

---

## 📖 O Projektu

Ovaj projekat predstavlja **digitalnu štopericu** razvijenu u **Flowcode** vizuelnom programskom okruženju. Cilj projekta je bio demonstrirati razumijevanje osnovnih programskih koncepta kao što su:

- Upravljanje stanjem programa (start, pauza, reset)
- Rad sa tajmerima i vremenskim funkcijama
- Evidentiranje međurezultata (krugovi / lapovi)
- Dizajn korisničkog interfejsa

Projekat je realiziran kao dio nastavnog predmeta **[PRAKTIČNA NASTAVA]** u školskoj godini **2025/2026**.

---

## ✨ Funkcionalnosti

| Funkcija | Opis | Dugme |
|----------|------|-------|
| ▶️ **Start** | Pokreće mjerenje vremena | `START` |
| ⏸️ **Pauza** | Pauzira mjerenje (nastavlja se ponovnim pritiskom) | `PAUZA` |
| 🔄 **Reset** | Vraća štopericu na `00:00:00` | `RESET` |
| 🏁 **Lap** | Bilježi trenutno vrijeme kao međurezultat | `LAP` |

### Detalji implementacije

- **Prikaz vremena** u formatu `MM:SS:ms` (minute : sekunde : milisekunde)
- **Lista lapova** — svaki lap se prikazuje sa rednim brojem i vremenom
- **Stanje pauze** — štoperica pamti ukupno proteklo vrijeme čak i nakon pauziranja
- **Višestruki lapovi** — moguće zabilježiti neograničen broj međurezultata

---

## 📸 Snimci Ekrana

> *Dodaj snimke ekrana svog projekta ovdje.*

```
screenshots/
├── main_screen.png       ← Glavni ekran štoperice
├── running_state.png     ← Štoperica u toku mjerenja
├── paused_state.png      ← Štoperica pauzirana
└── lap_list.png          ← Prikaz liste lapova
```

*Da dodaš snimak: `Uredi README → Zamijeni ovu sekciju sa slikom`*

---

## 🚀 Pokretanje Projekta

### Preduvjeti

- Instalirano **Flowcode** razvojno okruženje (verzija 2.0 ili novija)
- Windows operativni sistem (Flowcode je Windows aplikacija)

### Koraci

1. **Kloniraj repozitorij**
   ```bash
   git clone https://github.com/[tvoje-korisnicko-ime]/stoperica-flowcode.git
   ```

2. **Otvori projekt u Flowcode-u**
   ```
   File → Open → stoperica.fcfx
   ```

3. **Pokreni simulaciju**
   ```
   Compile → Simulate (F5)
   ```

4. **(Opcionalno) Kompajliraj za mikrokontroler**
   ```
   Compile → Build (F7)
   ```

---

## 🎮 Kako Koristiti

```
1. Pritisni [START]  → štoperica počinje mjeriti
2. Pritisni [LAP]    → bilježi se trenutni međurezultat
3. Pritisni [PAUZA]  → mjerenje se zaustavlja
4. Pritisni [START]  → mjerenje se nastavlja od gdje je stalo
5. Pritisni [RESET]  → sve se vraća na nulu
```

> ⚠️ **Napomena:** Dugme `LAP` funkcioniše samo dok štoperica mjeri (nije pauzirano).

---

## 🔄 Dijagram Toka

```
         ┌─────────────┐
         │   POČETAK   │
         └──────┬──────┘
                │
         ┌──────▼──────┐
         │  Prikaz 00  │◄────────────────────┐
         └──────┬──────┘                     │
                │                            │
         [START pritisnuto]                  │
                │                       [RESET]
         ┌──────▼──────┐                     │
    ┌───►│  MJERENJE   │─────────────────────┘
    │    └──────┬──────┘
    │           │
    │    ┌──────┴──────────────┐
    │    │                     │
    │  [PAUZA]               [LAP]
    │    │                     │
    │  ┌─▼────────┐     ┌──────▼──────┐
    │  │ PAUZIRANO│     │  Spremi Lap │
    │  └─┬────────┘     └─────────────┘
    │    │
    └────┘
   [START]
```

---

## 📁 Struktura Projekta

```
stoperica-flowcode/
│
├── 📄 README.md              ← Ova datoteka
├── 📁 src/
│   └── 🔧 stoperica.fcfx    ← Glavni Flowcode projekat
│
├── 📁 screenshots/           ← Snimci ekrana (dodaj ručno)
│   └── ...
│
└── 📁 docs/
    └── 📄 projektna_dokumentacija.pdf   ← Dokumentacija (opcionalno)
```

---

## 👤 Autor

**[Tvoje Ime i Prezime]**

- 🏫 Škola: [Elektrotehnička škola Tuzla]
- 📚 Razred: [3T2/Tehničar računarstva]
- 📅 Školska godina: 2025/2026
- 👨‍🏫 Profesor: [Alen Nuhić]

---

## 📝 Licenca

Ovaj projekat je izrađen u obrazovne svrhe i slobodan je za korištenje i modifikovanje.

---

<div align="center">

Izrađeno sa ❤️ u **Flowcode-u** | Školski projekat 2025/2026

</div>
