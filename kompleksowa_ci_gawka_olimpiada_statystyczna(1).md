# Kompleksowa Ściągawka: Szybka Statystyka na Kartce i Prosty Kalkulator (Olimpiada Statystyczna)

Niniejsza ściągawka opiera się na metodzie **uniwersalnych klocków obliczeniowych**. Zamiast zapamiętywać skomplikowane wzory ze średnimi arytmetycznymi, sprowadzamy wszystkie miary statystyczne do sum z jednej tabeli pomocniczej.

---

## 1. Fundament metody: Tabela i Dwa Klocki

Dla dowolnej pary cech $(X, Y)$ tworzymy tabelę o 5 kolumnach:
1. $X$
2. $Y$
3. $X^2$
4. $Y^2$
5. $XY$

Obliczamy sumy kolumn: $\sum x$, $\sum y$, $\sum x^2$, $\sum y^2$, $\sum xy$, gdzie $n$ to liczba obserwacji.

### Definicje klocków:
* **Klocek dwuzmienny (dla $X$ i $Y$):**
  $$K_{xy} = n \sum (xy) - (\sum x)(\sum y)$$

* **Klocek jednozmienny (dla zmiennej $X$):**
  $$K_{xx} = n \sum x^2 - (\sum x)^2$$
  *(Analogicznie dla zmiennej $Y$: $K_{yy} = n \sum y^2 - (\sum y)^2$)*

---

## 2. Główne miary wyrażone przez klocki

* **Współczynnik korelacji liniowej Pearsona ($r_{xy}$):**
  To **klocek dwuzmienny ($K_{xy}$)** podzielony przez **pierwiastek z iloczynu dwóch klocków jednozmiennych ($K_{xx}$ oraz $K_{yy}$)**:
  $$r_{xy} = \frac{K_{xy}}{\sqrt{K_{xx} \cdot K_{yy}}} = \frac{n \sum (xy) - (\sum x)(\sum y)}{\sqrt{[n \sum x^2 - (\sum x)^2][n \sum y^2 - (\sum y)^2]}}$$

* **Kowariancja z próby ($cov(x, y)$):**
  To **klocek dwuzmienny ($K_{xy}$)** podzielony przez mianownik próbkowy $n(n-1)$:
  $$cov(x, y) = \frac{K_{xy}}{n(n-1)} = \frac{n \sum (xy) - (\sum x)(\sum y)}{n(n-1)}$$

* **Wariancja z próby ($s_x^2$):**
  To **klocek jednozmienny ($K_{xx}$)** zmiennej $X$ podzielony przez mianownik próbkowy $n(n-1)$:
  $$s_x^2 = \frac{K_{xx}}{n(n-1)} = \frac{n \sum x^2 - (\sum x)^2}{n(n-1)}$$

* **Odchylenie standardowe ($s_x$):**
  To pierwiastek z wariancji próby (czyli pierwiastek z klocka jednoznacznego podzielonego przez mianownik):
  $$s_x = \sqrt{s_x^2} = \sqrt{\frac{K_{xx}}{n(n-1)}}$$

---

## 3. Prosta regresji liniowej ($y = ax + b$)

* **Współczynnik kierunkowy ($a$):**
  To **klocek dwuzmienny ($K_{xy}$)** podzielony przez **klocek jednozmienny ($K_{xx}$)** zmiennej $X$:
  $$a = \frac{K_{xy}}{K_{xx}} = \frac{n \sum (xy) - (\sum x)(\sum y)}{n \sum x^2 - (\sum x)^2}$$

* **Wyraz wolny ($b$):**
  $$b = \bar{y} - a\bar{x} = \frac{\sum y - a \sum x}{n}$$

---

## 4. Rachunek prawdopodobieństwa i zmienne losowe

* **Schemat Bernoulliego (prawdopodobieństwo $k$ sukcesów w $n$ próbach):**
  $$P(X = k) = \binom{n}{k} p^k q^{n-k}$$
  gdzie $\binom{n}{k} = \frac{n!}{k!(n-k)!}$, $p$ – sukces, $q = 1-p$ – porażka.

* **Wartość oczekiwana (nadzieja matematyczna) $E(X)$:**
  $$E(X) = \sum x_i \cdot P(X = x_i)$$

* **Wariancja zmiennej losowej $Var(X)$:**
  $$Var(X) = E(X^2) - [E(X)]^2$$
  gdzie $E(X^2) = \sum x_i^2 \cdot P(X = x_i)$.

---

## 5. Analiza dynamiki

* **Przyrost absolutny:** 
  $$\Delta_t = y_t - y_{t-1}$$ (łańcuchowy) lub $\Delta_t = y_t - y_0$ (jednopodstawowy).

* **Indeks łańcuchowy:** 
  $$i_t = \frac{y_t}{y_{t-1}} \cdot 100\%$$

* **Indeks jednopodstawowy:** 
  $$i_t = \frac{y_t}{y_0} \cdot 100\%$$

---

## 6. Statystyka gospodarcza i finansowa

* **Próg rentowności (BEP – *Break-Even Point* w sztukach):**
  $$BEP = \frac{K_S}{p - k_j}$$
  gdzie $K_S$ – koszty stałe, $p$ – cena sprzedaży jednostkowa, $k_j$ – koszt zmienny jednostkowy.

* **Wskaźnik płynności bieżącej (Current Ratio):**
  $$\text{Płynność bieżąca} = \frac{\text{Aktywa obrotowe}}{\text{Zobowiązania krótkoterminowe}}$$

* **Stopa bezrobocia BAEL:**
  $$\text{Stopa bezrobocia} = \frac{\text{Liczba bezrobotnych}}{\text{Ludność aktywna zawodowo}} \cdot 100\%$$