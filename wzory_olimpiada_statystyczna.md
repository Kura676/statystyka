# Kluczowe Wzory na Olimpiadę Statystyczną

Ten dokument zawiera zestawienie podstawowych wzorów, które należy znać na pamięć na etapie szkolnym, okręgowym i centralnym Olimpiady Statystycznej.

---

## 1. Statystyka Opisowa

### Średnia arytmetyczna (prosta)
$$\bar{x} = \frac{\sum_{i=1}^{n} x_i}{n}$$

### Średnia arytmetyczna (ważona)
$$\bar{x} = \frac{\sum_{i=1}^{k} (x_i \cdot w_i)}{\sum_{i=1}^{k} w_i}$$

### Średnia geometryczna
$$\bar{x}_g = \sqrt[n]{x_1 \cdot x_2 \cdot \ldots \cdot x_n}$$

### Średnia harmoniczna
$$\bar{x}_h = \frac{n}{\sum_{i=1}^{n} \frac{1}{x_i}}$$

### Wariancja ($s^2$)
$$s^2 = \frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{n}$$

### Odchylenie standardowe ($s$)
$$s = \sqrt{s^2}$$

### Rozstęp ($R$)
$$R = x_{\max} - x_{\min}$$

### Rozstęp ćwiartkowy ($Q$)
$$Q = Q_3 - Q_1$$

### Odchylenie ćwiartkowe ($Q_d$)
$$Q_d = \frac{Q_3 - Q_1}{2}$$

### Klasyczny współczynnik zmienności ($V_s$)
$$V_s = \frac{s}{\bar{x}} \quad (\text{lub } V_s = \frac{s}{\bar{x}} \cdot 100\%)$$

---

## 2. Analiza Dynamiki i Indeksy

### Przyrost bezwzględny jednopodstawowy
$$\Delta x_{t/0} = x_t - x_0$$

### Przyrost bezwzględny łańcuchowy
$$\Delta x_{t/t-1} = x_t - x_{t-1}$$

### Indeks indywidualny jednopodstawowy ($i_{t/0}$)
$$i_{t/0} = \frac{x_t}{x_0}$$

### Indeks indywidualny łańcuchowy ($i_{t/t-1}$)
$$i_{t/t-1} = \frac{x_t}{x_{t-1}}$$

### Względne tempo zmian (w procentach)
$$\text{Tempo} = (i - 1) \cdot 100\%$$

---

## 3. Rachunek Prawdopodobieństwa i Kombinatoryka

### Permutacje
$$P_n = n!$$

### Kombinacje
$$C_n^k = \binom{n}{k} = \frac{n!}{k!(n-k)!}$$

### Wariacje bez powtórzeń
$$V_n^k = \frac{n!}{(n-k)!}$$

### Wariacje z powtórzeńiami
$$W_n^k = n^k$$

### Klasyczna definicja prawdopodobieństwa
$$P(A) = \frac{|A|}{|\Omega|}$$

### Prawdopodobieństwo warunkowe
$$P(A|B) = \frac{P(A \cap B)}{P(B)}, \quad \text{dla } P(B) > 0$$

### Schemat Bernoulliego ($k$ sukcesów w $n$ próbach)
$$P_n(k) = \binom{n}{k} p^k q^{n-k}, \quad \text{gdzie } q = 1 - p$$

### Wartość oczekiwana zmiennej losowej skokowej
$$E(X) = \sum x_i \cdot p_i$$

---

## 4. Wskaźniki Demograficzne i Gospodarcze

### Przyrost naturalny ($\text{PN}$)
$$\text{PN} = \text{Urodzenia żywe} - \text{Zgony}$$

### Saldo migracji ($\text{SM}$)
$$\text{SM} = \text{Imigracja} - \text{Emigracja}$$

### Przyrost rzeczywisty ($\text{PR}$)
$$\text{PR} = \text{PN} + \text{SM}$$

### Współczynnik feminizacji
$$\text{W}_{\text{feminizacji}} = \frac{\text{Liczba kobiet}}{\text{Liczba mężczyzn}} \cdot 100$$

### Stopa bezrobocia
$$\text{Stopa bezrobocia} = \frac{\text{Liczba bezrobotnych}}{\text{Aktywni zawodowo}} \cdot 100\%$$

### Współczynnik aktywności zawodowej ($\text{WAK}$)
$$\text{WAK} = \frac{\text{Aktywni zawodowo (pracujący + bezrobotni)}}{\text{Ludność w wieku 15+ (lub produkcyjnym)}} \cdot 100\%$$