# Kompleksowa Ściągawka: Szybka Statystyka na Kartce i Kalkulatorze
*Przewodnik stworzony specjalnie pod kątem zadań z etapów okręgowych i centralnych Olimpiady Statystycznej.*

---

## 1. Metodologia Tabelaryczna i „Klocki” Obliczeniowe

Zamiast pamiętać skomplikowane wzory ze średnimi arytmetycznymi $\bar{x}$ i $\bar{y}$ (które prowadzą do błędów zaokrągleń na prostym kalkulatorze), sprowadzamy każde zadanie dwuzmienne do **jednej tabeli z 5 kolumnami**:

| $i$ | $X$ | $Y$ | $X^2$ | $Y^2$ | $XY$ |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | $x_1$ | $y_1$ | $x_1^2$ | $y_1^2$ | $x_1 y_1$ |
| 2 | $x_2$ | $y_2$ | $x_2^2$ | $y_2^2$ | $x_2 y_2$ |
| $\vdots$ | $\vdots$ | $\vdots$ | $\vdots$ | $\vdots$ | $\vdots$ |
| **Sumy** | $\sum x$ | $\sum y$ | $\sum x^2$ | $\sum y^2$ | $\sum xy$ |

### Dwa Uniwersalne Klocki Obliczeniowe
Wszystkie kluczowe miary opierają się na dwóch potężnych konstrukcjach algebraicznych:

1. **Klocek dwuzmienny (wspólny dla $X$ i $Y$):**
   $$K_{XY} = n \sum (xy) - (\sum x)(\sum y)$$

2. **Klocek jednozmienny (dla zmiennej $X$):**
   $$K_{X} = n \sum x^2 - (\sum x)^2$$
   *(Analogicznie dla zmiennej $Y$: $K_{Y} = n \sum y^2 - (\sum y)^2$)*

---

## 2. Wzory Pochodne z Klocków

### Współczynnik korelacji liniowej Pearsona ($r_{xy}$)
Dzięki sprytnemu uproszczeniu, $n$ oraz $(n-1)$ w mianowniku całkowicie się redukują:
$$r_{xy} = \frac{n \sum xy - (\sum x)(\sum y)}{\sqrt{[n \sum x^2 - (\sum x)^2][n \sum y^2 - (\sum y)^2]}} = \frac{K_{XY}}{\sqrt{K_X \cdot K_Y}}$$

### Kowariancja z próby ($Cov(X,Y)$)
$$Cov(X,Y) = \frac{K_{XY}}{n(n-1)}$$

### Wariancja z próby ($S_x^2$) – Korekta Bessela
$$S_x^2 = \frac{K_X}{n(n-1)}$$
*Odchylenie standardowe:* $S_x = \sqrt{S_x^2}$

---

## 3. Prosta Regresji Liniowej ($y = ax + b$)

Aby wyznaczyć równanie prostej regresji $y = ax + b$:

1. **Współczynnik kierunkowy ($a$):**
   $$a = \frac{n \sum xy - (\sum x)(\sum y)}{n \sum x^2 - (\sum x)^2} = \frac{K_{XY}}{K_X}$$

2. **Wyraz wolny ($b$):**
   $$b = \bar{y} - a\bar{x} = \frac{\sum y - a \sum x}{n}$$

---

## 4. Rachunek Prawdopodobieństwa i Zmienne Losowe

### Schemat Bernoulliego
Prawdopodobieństwo uzyskania dokładnie $k$ sukcesów w $n$ próbach:
$$P(X = k) = \binom{n}{k} p^k q^{n-k} = \frac{n!}{k!(n-k)!} p^k (1-p)^{n-k}$$
*(gdzie $p$ to sukces, $q = 1-p$ to porażka)*

### Wartość Oczekiwana i Wariancja Rozkładu Dyskretnego
* **Wartość oczekiwana (nadzieja matematyczna):**
  $$E(X) = \sum_{i} x_i P(X = x_i)$$
* **Wariancja zmiennej losowej:**
  $$Var(X) = E(X^2) - [E(X)]^2$$

---

## 5. Analiza Dynamiki

* **Przyrost absolutny:** 
  $$\Delta_t = y_t - y_{t-1} \quad \text{(łańcuchowy)} \quad \text{lub} \quad \Delta_t = y_t - y_0 \quad \text{(jednopodstawowy)}$$
* **Indeks łańcuchowy (dynamika rok do roku / okres do okresu):**
  $$i_t = \frac{y_t}{y_{t-1}} \cdot 100\%$$
* **Indeks jednopodstawowy (w odniesieniu do bazy stałej):**
  $$I_t = \frac{y_t}{y_0} \cdot 100\%$$

---

## 6. Statystyka Gospodarcza i Finansowa

* **Próg rentowności (BEP – *Break-Even Point* w sztukach):**
  $$BEP = \frac{K_S}{p - k_j}$$
  *gdzie:* $K_S$ – koszty stałe ogółem, $p$ – cena sprzedaży jednostkowa, $k_j$ – koszt zmienny jednostkowy.

* **Wskaźnik rentowności sprzedaży (ROS):**
  $$ROS = \frac{\text{Wynik finansowy}}{\text{Przychody ze sprzedaży}} \cdot 100\%$$

* **Wskaźnik płynności bieżącej (current ratio):**
  $$\text{Płynność bieżąca} = \frac{\text{Aktywa obrotowe}}{\text{Zobowiązania krótkoterminowe}}$$

* **Stopa bezrobocia BAEL:**
  $$\text{Stopa bezrobocia} = \frac{\text{Liczba bezrobotnych}}{\text{Ludność aktywna zawodowo}} \cdot 100\%$$

---
*Powodzenia na Olimpiadzie Statystycznej! Trzymamy kciuki za wynik w ścisłym finale!*