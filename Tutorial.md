# 📘 Tutorial: Jak zbudować stronę "Przychodnia Medica" - HTML i CSS

## 🎯 Dla kogo jest ten tutorial?
Ten tutorial jest dla Ciebie! Pokażę Ci **krok po kroku**, jak zrobić stronę internetową. Nie śpiesz się. Czytaj spokojnie. 

---

## 📂 Krok 1: Przygotuj pliki

### Co musisz zrobić:
1. Stwórz **nowy folder** na pulpicie (nazwij go swoim numerem PESEL)
2. Wrzuć tam obrazki z archiwum:
   - `obraz1.jpg` (zdjęcie lekarza)
   - `obraz2.png` (czerwony krzyż - musi mieć rozmiar 32x32 piksele)
   - `obraz3.png` (zielony ptaszek)

3. W tym samym folderze utwórz **3 nowe pliki**:
   - `medica.php` (główna strona)
   - `styl.css` (style)
   - `opis.html` (dodatkowa strona)

---

## 📄 Krok 2: Plik HTML - Podstawy (medica.php)

### Zacznij od szkieletu strony:

```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Przychodnia Medica</title>
    <link rel="icon" href="obraz2.png" type="image/png">
    <link rel="stylesheet" href="styl.css">
</head>
<body>

</body>
</html>
```

### 🔍 Co tu się dzieje?
- `<!DOCTYPE html>` = To jest HTML5
- `lang="pl"` = Strona jest po polsku
- `charset="UTF-8"` = Polskie znaki będą działać
- `<title>` = Nazwa na karcie przeglądarki
- `rel="icon"` = Mała ikonka (favicon) na karcie
- `<link rel="stylesheet">` = Podłączamy style CSS

---

## 🏗️ Krok 3: Budujemy strukturę strony

### Nasza strona ma 4 części:
1. **NAGŁÓWEK** (góra)
2. **ARTYKUŁ** (informacje o pakietach)
3. **GŁÓWNA CZĘŚĆ** (3 kolorowe pudełka)
4. **STOPKA** (dół)

### Dodaj te części do `<body>`:

```html
<body>
    
    <!-- CZĘŚĆ 1: NAGŁÓWEK -->
    <header>
        <h1>Abonamenty w przychodni Medica</h1>
    </header>

    <!-- CZĘŚĆ 2: ARTYKUŁ -->
    <article>
        <h3>Pakiet Standard - cena 200 zł</h3>
        <p>Zdrowie jest dla Ciebie ważne...</p>
        
        <h3>Pakiet Premium - cena 500 zł</h3>
        <p>Szukasz najwygodniejszego rozwiązania...</p>
        
        <a href="opis.html">Dowiedz się więcej</a>
    </article>

    <!-- CZĘŚĆ 3: GŁÓWNA - 3 SEKCJE -->
    <main>
        
        <section>
            <h2>Standardowy</h2>
            <ul>
                <li>Lekarz POZ</li>
                <li>Endokrynolog</li>
                <li>Kardiolog</li>
                <li>Ginekolog</li>
                <li>Urolog</li>
                <li>Podstawowe badania laboratoryjne</li>
            </ul>
        </section>

        <section>
            <h2>Premium</h2>
            <ul>
                <li>Lekarz POZ</li>
                <li>Pediatra</li>
                <li>Geriatra</li>
                <li>Kardiolog</li>
                <li>Ortopeda</li>
                <li>Laryngolog</li>
                <li>Urolog</li>
                <li>Endokrynolog</li>
                <li>Ginekolog</li>
                <li>Wszystkie badania laboratoryjne</li>
                <li>Diabetolog</li>
            </ul>
        </section>

        <section>
            <h2>Dziecko</h2>
            <ul>
                <li>Pediatra</li>
                <li>Kardiolog</li>
                <li>Ortopeda</li>
                <li>Laryngolog</li>
                <li>Urolog</li>
            </ul>
        </section>

    </main>

    <!-- CZĘŚĆ 4: STOPKA -->
    <footer>
        <p>
            <img src="obraz2.png" alt="przychodnia">
            Stronę przygotował: TWÓJ_NUMER_PESEL
        </p>
    </footer>

</body>
```

### ⚠️ PAMIĘTAJ:
- Zamień `TWÓJ_NUMER_PESEL` na swój prawdziwy numer PESEL!

---

## 📄 Krok 4: Mała strona opis.html

Utwórz plik `opis.html` i wpisz:

```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Opis</title>
</head>
<body>
    <p>Strona w trakcie budowy</p>
</body>
</html>
```

---

## 🎨 Krok 5: Style CSS (styl.css)

Teraz **upiększymy** naszą stronę!

### Otwórz plik `styl.css` i wpisz:

```css
/* Wszędzie czcionka Georgia */
* {
    font-family: Georgia;
}

/* NAGŁÓWEK I STOPKA - ciemnozielone */
header, footer {
    background-color: #1B5E20;
    color: white;
    text-align: center;
    padding: 5px;
}

/* ARTYKUŁ - tło ze zdjęciem */
article {
    background-image: url('obraz1.jpg');
    color: DimGray;
    font-size: 150%;
    height: 350px;
    overflow: auto;
}

/* GŁÓWNA CZĘŚĆ - 3 pudełka obok siebie */
main {
    display: flex;
    justify-content: space-around;
}

/* SEKCJE - zielone pudełka */
section {
    background-color: #00E676;
    color: #1B5E20;
    width: 28%;
    height: 560px;
    margin: 2%;
    border-radius: 10px;
    box-shadow: 8px 8px 6px DimGray;
}

/* Gdy najedziemy myszką na sekcję */
section:hover {
    background-color: #10EF84;
}

/* Gdy najedziemy na paragraf */
p:hover {
    color: black;
}

/* NAGŁÓWKI H2 i H3 */
h2, h3 {
    color: #1B5E20;
    text-align: center;
    letter-spacing: 3px;
    padding-top: 20px;
}

/* LISTA - zielone ptaszki */
ul {
    list-style-image: url('obraz3.png');
}
```

---

## ✅ Krok 6: Sprawdź czy działa!

1. **Zapisz wszystkie pliki** (Ctrl + S)
2. **Otwórz plik** `medica.php` w przeglądarce (kliknij 2 razy)
3. **Sprawdź czy widzisz**:
   - ✅ Ciemnozielony nagłówek
   - ✅ Zdjęcie lekarza w tle
   - ✅ 3 zielone pudełka obok siebie
   - ✅ Ciemnozieloną stopkę

---

## 🐛 Coś nie działa? Sprawdź!

### Problem: Nie widzę obrazków
- ✅ Czy obrazki są w **tym samym** folderze co strona?
- ✅ Czy nazwy plików są **dokładnie** takie: `obraz1.jpg`, `obraz2.png`, `obraz3.png`?

### Problem: Strona wygląda brzydko (bez kolorów)
- ✅ Czy plik `styl.css` jest w **tym samym** folderze?
- ✅ Czy w HTML masz linijkę: `<link rel="stylesheet" href="styl.css">`?

### Problem: Pudełka są pod sobą, nie obok siebie
- ✅ Sprawdź czy w CSS jest: `display: flex;` dla `main`

---

## 📋 Checklist - Lista kontrolna

Zaznacz ✅ gdy zrobisz:

- [ ] Utworzyłem folder z moim numerem PESEL
- [ ] Przeskalowałem obraz2.png do 32x32 piksele
- [ ] Utworzyłem plik medica.php
- [ ] Dodałem podstawowy szkielet HTML5
- [ ] Dodałem `<header>` z nagłówkiem H1
- [ ] Dodałem `<article>` z informacjami i linkiem
- [ ] Dodałem `<main>` z 3 sekcjami
- [ ] W każdej sekcji jest H2 i lista UL
- [ ] Dodałem `<footer>` ze zdjęciem i moim numerem PESEL
- [ ] Utworzyłem plik opis.html
- [ ] Utworzyłem plik styl.css
- [ ] Dodałem wszystkie style CSS
- [ ] Sprawdziłem stronę w przeglądarce
- [ ] Stworzyłem plik przeglądarka.txt z nazwą przeglądarki

---

## 💡 Wskazówki na koniec

1. **Pisz powoli** - Lepiej napisać wolno i dobrze, niż szybko i źle
2. **Sprawdzaj często** - Otwieraj stronę w przeglądarce co chwilę
3. **Używaj F5** - Gdy coś zmienisz, naciśnij F5 w przeglądarce aby odświeżyć
4. **Pytaj** - Jeśli coś niejasne, pytaj egzaminatora

---

## 🎓 Pamiętaj!

To zadanie **nie** wymaga od Ciebie PHP i baz danych. Wystarczy HTML i CSS. Skup się na tym co umiesz! 

**Powodzenia!** 🍀